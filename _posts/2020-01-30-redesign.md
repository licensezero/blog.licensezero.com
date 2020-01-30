---
title: Redesigning License Zero
description: notes on data records, protocol, building blocks, and motivation
---

I've been working hard for a number of weeks now on redesigning License Zero.  This post will share my latest thinking.

## Goals

I went into the redesign process with two goals:

1.  Make License Zero's systems and approach accessible to developers who can't or choose not to sell through licensezero.com.

2.  Streamline the design with the benefit of a couple years' hindsight.

Fundamentally, users come to License Zero one of two ways: to buy permission to use software or to sell permission to use software.

Buyers need to be able to run a single command in their projects, see a list of all the dependencies and other artifacts they need to pay for, and start a checkout process for everything they're missing.  Once they've finished that process, running the command again should show they're ready to go.  Buyers should also be able to buy specific licenses online, using their web browsers.

Sellers need to be able to create an account, offer to sell, and add metadata to their work that tells potential buyers and the `licensezero` command for everything they need to know.

Currently, licensezero.com and the `licensezero` command-line interface implement all of this core functionality and more.  The two are tightly coupled.  The CLI talks to licensezero.com and licensezero.com talks to the CLI.

## Motivation

licensezero.com handles payments via [Stripe](https://stripe.com).  Stripe has been excellent to work with, technically.  And it is still the only mainstream payment processor I'm aware of that supports a key feature: splitting a single payment transaction among an arbitrary number of payees.  For License Zero, that means the ability to offer buyers a single checkout page, take their credit cards details once, and to the right amounts to all the developers they're buying from, whether there's one or dozens.

Stripe's [support for developers based outside North America, western Europe, Australia, New Zealand, and Japan](https://stripe.com/global) remains very limited.  Stripe's stopgap solution, Stripe Atlas, reaches users outside supported countries by helping them to form companies within the United States.  But to be frank, tax and other complexities of that approach make it very hard to recommend.  Competitors like PayPal support hundreds of countries without a stopgap like Atlas, but don't offer the one-pays-many or "marketplace" functionality License Zero needs.

That being the case, where License Zero needs to go is plain:  Developers who want to sell through License Zero should be able to do so.  Everyone else should be able to host their own "vending machine" server that interoperates with the License Zero CLI.

In some cases, that will mean that buyers running `licensezero buy` will end up going through multiple checkout processes, one for each "vending machine" server selling the licenses they need.  That's obviously worse than a single checkout process on licensezero.com.  But also obviously better than simply not being able to buy licenses for projects they want in an automated way.

Best Case:  There's one, solid, integrated platform available to everyone, buyers and sellers.

Second Best:  One solid, integrated platform serves most, but a clear _protocol_ makes it possible for others to serve themselves.

## Records

To implement this kind of system, License Zero's protocol needs to represent a few different kinds of data.  The most interesting are:

_Artifact Metadata_ attaches to a software artifact, like a package, and describes the public license terms that make certain kinds of use free, as well as where and how to buy licenses for other kinds of uses.  In the analog retail world, artifact metadata correspond to bar codes on merchandise.

_Offers_ describe offers to sell licenses for software, with details about who is selling, pricing, and so on.  In retail, offers correspond to entries in a catalog or price sheet.

_Receipts_ testify to the fact that someone has bought a license.  Receipts need to identify the offer made, the _licensor_ who made the offer, the _licensee_ who bought a license, and the _vendor_ through which the sale was made.  Currently, Artless Devices, the LLC behind License Zero, is the only supported vendor.

## Building Blocks

To describe these data, the protocol that License Zero will implement, and that others can implement for themselves, I'll use a number of standards, formats, and tools.  I'll go over them briefly.

[JavaScript Object Notation (JSON)](https://www.json.org/json-en.html), a popular data-interchange format.  In exceptional situations, records may be better serialized in other formats, as in TOML for inclusion in `Cargo.toml` files for Rust crates.  But in their "native" form, and for exchange via APIs, License Zero will use JSON.

[JSON Schema](https://json-schema.org) defines a way to define schemas for JSON data.  Using JSON schema, we can describe whether data should take the form of objects, array, strings, or other JSON types.  For the complex types, like objects and arrays, we can define what elements they can and must have, such as the properties or an object or the number of array elements.  License Zero can use JSON Schemas to define the "shapes" of artifact, offer, receipt, and other data records.

[Swagger](https://swagger.io) builds on JSON Schema to specify HTTP APIs.  A Swagger specification defines endpoints, query parameters, request and response body schemas, error types, and the like.  License Zero can use Swagger to at least outline the API that servers vending licenses, like licensezero.com, must implement to interoperate with the `licensezero` command-line interface.

[Universally Unique Identifiers (UUIDs)](https://en.wikipedia.org/wiki/Universally_unique_identifier) define a way of generating and representing unique identifiers.  For example, `00202da8-a47c-4d45-86cb-fa45a05de817` is a valid version 4 (random) UUID.  A great benefit of UUID is that programs can generate them on the fly without any practical risk that other programs in the same system will generate an identical identifier.  License Zero can use UUIDs to identify offers, purchases, licensors, and so on.

[SPDX identifiers](https://spdx.org/licenses) map short strings like `MIT` to official texts of common public software licenses.  License Zero can use SPDX identifiers, possibly with custom extensions, to identify public license terms.

[ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) defines codes for world currencies.  For example, `RUB` denotes the Russian ruble.  The standard also specifies the "minor unit" of each currency.  So `USD` denotes United States dollar, whose minor unit is the United States cent.  When License Zero needs to express prices asked or paid, it can use ISO 4217 to denote the currency and integers to denote the amounts.

[ISO 3166-2](https://en.wikipedia.org/wiki/ISO_3166-2) defines codes for subdivisions of countries.  For example, `US-CA` denotes California, a subdivision (state) of the United States of America.  Since some countries impose taxes or other requirements on license sales, License Zero needs to record and provide data about buyers' and sellers' jurisdictions.

[ISO 8601](https://en.wikipedia.org/wiki/ISO_8601), overlapping with [RFC 3339 section 5.6](https://tools.ietf.org/html/rfc3339), which defines a way to represent dates and times as strings like `2020-01-30T08:01Z`.  Wherever the License Zero protocol needs to express points time, such as the date of a license, it can do so with ISO 8601 strings in Coordinated Universal Time (UTC).

[Ed25519](https://ed25519.cr.yp.to/), a modern, public-key, cryptographic signature system.  Receipts don't prove much of anything if anyone can type one up that says whatever they want.  Ed25519 signatures enable vendor servers to sign receipts so that others can verify their authenticity.

## Schemas

This is going to be something of data dump.  The action will continue to develop [in the GitHub repository for schemas.licensezero.com](https://github.com/licensezero/schemas.licensezero.com).  But to give a current sense of how these pieces are coming together:

### Artifact Metadata

```json
{
  "$id": "https://schemas.licensezero.com/1.0.0-pre/artifact.json",
  "type": "object",
  "required": [
    "schema",
    "offers"
  ],
  "additionalProperties": false,
  "properties": {
    "schema": {
      "const": "https://schemas.licensezero.com/1.0.0-pre/artifact.json"
    },
    "offers": {
      "type": "array",
      "items": {
        "type": "object",
        "required": [
          "offerID",
          "api"
        ],
        "additionalProperties": false,
        "properties": {
          "offerID": {
            "title": "UUIDv4 offer identifier",
            "type": "string",
            "format": "uuid"
          },
          "api": {
            "title": "licensing API",
            "type": "string",
            "format": "uri",
            "pattern": "^https://",
            "examples": [
              "https://api.licensezero.com"
            ]
          },
          "public": {
            "title": "public license identifier",
            "type": "string",
            "pattern": "^[A-Za-z0-9-.]+",
            "examples": [
              "Parity-7.0.0"
            ]
          }
        }
      }
    }
  }
}
```

### Receipt

```json
{
  "$id": "https://schemas.licensezero.com/1.0.0-pre/receipt.json",
  "title": "license receipt",
  "comment": "A receipt represents confirmation of the sale of a software license.",
  "type": "object",
  "required": [
    "schema",
    "key",
    "signature",
    "license"
  ],
  "additionalProperties": false,
  "properties": {
    "schema": {
      "const": "https://schemas.licensezero.com/1.0.0-pre/receipt.json"
    },
    "key": {
      "title": "public signing key of the license vendor",
      "$ref": "https://schemas.licensezero.com/1.0.0-pre/key.json"
    },
    "signature": {
      "title": "signature of the license vendor",
      "$ref": "https://schemas.licensezero.com/1.0.0-pre/signature.json"
    },
    "license": {
      "title": "license manifest",
      "type": "object",
      "required": [
        "values",
        "form"
      ],
      "properties": {
        "values": {
          "type": "object",
          "required": [
            "offerID",
            "orderID",
            "effective",
            "licensor",
            "licensee",
            "vendor"
          ],
          "additionalProperties": false,
          "properties": {
            "offerID": {
              "title": "offer identifier",
              "type": "string",
              "format": "uuid"
            },
            "orderID": {
              "title": "order identifier",
              "type": "string",
              "format": "uuid"
            },
            "effective": {
              "title": "effective date",
              "$ref": "https://schemas.licensezero.com/1.0.0-pre/time.json"
            },
            "price": {
              "title": "purchase price",
              "$ref": "https://schemas.licensezero.com/1.0.0-pre/price.json"
            },
            "expires": {
              "title": "expiration date of the license",
              "$ref": "https://schemas.licensezero.com/1.0.0-pre/time.json"
            },
            "licensee": {
              "title": "licensee",
              "comment": "The licensee is the one receiving the license.",
              "type": "object",
              "required": [
                "email",
                "jurisdiction",
                "name"
              ],
              "properties": {
                "email": {
                  "type": "string",
                  "format": "email"
                },
                "jurisdiction": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/jurisdiction.json"
                },
                "name": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/name.json",
                  "examples": [
                    "Joe Licensee"
                  ]
                }
              }
            },
            "licensor": {
              "title": "licensor",
              "comment": "The licensor is the one giving the license.",
              "type": "object",
              "required": [
                "email",
                "jurisdiction",
                "name",
                "licensorID"
              ],
              "properties": {
                "email": {
                  "type": "string",
                  "format": "email"
                },
                "jurisdiction": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/jurisdiction.json"
                },
                "name": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/name.json",
                  "examples": [
                    "Joe Licensor"
                  ]
                },
                "licensorID": {
                  "title": "licensor identifier",
                  "type": "string",
                  "format": "uuid"
                }
              }
            },
            "vendor": {
              "title": "licesne vendor",
              "comment": "information on the party that sold the license, such as an agent or reseller, if the licensor did not sell the license themself",
              "type": "object",
              "required": [
                "api",
                "email",
                "name",
                "jurisdiction",
                "website"
              ],
              "additionalProperties": false,
              "properties": {
                "api": {
                  "title": "license API",
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/url.json"
                },
                "email": {
                  "type": "string",
                  "format": "email"
                },
                "name": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/name.json",
                  "example": [
                    "Artless Devices LLC"
                  ]
                },
                "jurisdiction": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/jurisdiction.json"
                },
                "website": {
                  "$ref": "https://schemas.licensezero.com/1.0.0-pre/url.json"
                }
              }
            }
          }
        },
        "form": {
          "title": "license form",
          "type": "string",
          "minLength": 1
        }
      }
    }
  }
}
```

This schema unifies what are currently two separate concepts in License Zero: licenses, which are bought and sold, and waivers, which are given for free.

This schema also leaves open a method to implement term-limited and recurring licenses.  The `expires` date allows the `licensezero` client to detect when a receipt it has no longer applies.  As you'll see below, the `/orders/{orderID}` endpoint also leaves open the possibility that one purchase might lead to several licenses.  That way, a vendor can process a transaction to start a license subscription, and issue new receipts for the customer to download over time, as subsequent subscription payments clear.

## Vendor Server API

```yaml
openapi: 3.0.0
info:
  title: License Zero Vendor API
  version: 0.0.0
paths:

  /key:
    get:
      summary: Returns the public signing key of the server.
      responses:
        200:
          content:
            application/json:
              schema:
                $ref: https://schemas.licensezero.com/1.0.0/key.json

  /offers/{offerID}:
    get:
      summary: Returns information about a license offer.
      parameters:
        - name: offerID
          in: path
          required: true
          schema:
            type: string
            format: uuid
      responses:
        200:
          content:
            application/json:
              $ref: https://schemas.licensezero.com/1.0.0/offer.json
        400:
          description: The specified UUID is not a valid UUID.
        404:
          description: An offer with the specified UUID was not found.
        default:
          description: Unexpected Error

  /licensors/{licensorID}:
    get:
      summary: Returns information about a licensor.
      parameters:
        - name: licensorID
          in: path
          required: true
          schema:
            type: string
            format: uuid
      responses:
        200:
          content:
            application/json:
              schema:
                $ref: https://schemas.licensezero.com/1.0.0/licensor.json
        400:
          description: The specified UUID is not a valid UUID.
        404:
          description: An offer with the specified UUID was not found.
        default:
          description: Unexpected Error

  /order/:
    post:
      summary: Initiate an order for one or more paiod licenses.
      requestBody:
        required: true
        content:
          application/x-www-form-urlencoded:
            schema:
              $ref: https://schemas.licensezero.com/1.0.0/order.json
    responses:
      303:
        description: The order is ready to complete.
        headers:
          Location:
            description: The URL for the page to complete the order.
            schema:
              type: string
              format: uri
      5XX:
        description: Unexpected Error

  receipts/{receiptID}:
    get:
      summary: Returns a receipt.
      parameters:
        - name: receiptID
          in: path
          required: true
          schema:
            type: string
            format: uuid
      responses:
        200:
          content:
            application/json:
              schema:
                $ref: https://schemas.licensezero.com/receipt.json
        400:
          description: The specified id is not a valid UUID.
        404:
          description: An offer with the specified UUID was not found.
        default:
          description: Unexpected Error

  bundles/{bundleID}:
    get:
      summary: Returns a bundle of receipts.
      parameters:
        - name: bundleID
          in: path
          required: true
          schema:
            type: string
            format: uuid
      responses:
        200:
          content:
            application/json:
              schema:
                $ref: https://schemas.licensezero.com/bundle.json
        400:
          description: The specified id is not a valid UUID.
        404:
          description: An offer with the specified UUID was not found.
        default:
          description: Unexpected Error

  orders/{orderID}:
    get:
      summary: Returns the receipts for an order.
      parameters:
        - name: orderID
          in: path
          required: true
          schema:
            type: string
            format: uuid
      responses:
        200:
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: https://schemas.licensezero.com/receipt.json
        default:
          description: Unexpected Error

  orders/{orderID}/latest:
    get:
      summary: Returns the latest receipt for an order.
      parameters:
        - name: orderID
          in: path
          required: true
          schema:
            type: string
            format: uuid
      responses:
        302:
          headers:
            Location:
              description: The URL of the receipt.
              schema:
                type: string
                format: uri
        default:
          description: Unexpected Error
```
