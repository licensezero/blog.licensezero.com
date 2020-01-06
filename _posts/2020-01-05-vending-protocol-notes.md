---
title: Notes on the Vending Protocol
description: more ways to buy and sell
---

Work on a new paid licensing protocol continues apace.  As I go, I find myself revisiting many of the decisions that went into License Zero's design.  I still believe License Zero represents the right overall direction, with the best trade-offs, to build the kind of world developers deserve to work in.  But in opening up automated public-private licensing to developers who can't use License Zero, or want to use other licensing agents, it occurs to me the protocol can and should support more than just License Zero clones.

Other sellers can and should experiment with how paid licenses are bought, sold, and written.

For example, License Zero only sells individual licenses.  It doesn't sell "site licenses" that cover everyone at a company.  But others might choose to sell site licenses, and so far, I don't see any reason the new protocol can't support that.

License Zero only takes payment in United States dollars.  Others may prefer to use their local currency, especially for sales to customers in the same country.  Why exchange local currency to dollars, only to exchange it back to pay out in local currency?  The protocol itself needn't handle payment.  That can be left to the developers, agents, and APIs that handle the money and vend the licenses.

When someone buys a license through License Zero, they get permission to use the current version of the software forever.  Others might choose to sell licenses that expire.  Still others might choose to sell subscriptions, under which customers essentially get a new license each month or each year, so long as they continue to pay.  The protocol could support that, as well.

License Zero only sells licenses automatically, self-service.  But others might prefer to negotiate their deals, or to approve them manually.  The protocol can certainly support that, too, without sacrificing the other conveniences of automated license audit and quoting.

At a high level, the protocol is very simple.  Users need to be able to answer a few questions:

1. Which dependencies of my project have free licenses that I can't rely on?
2. Which of my dependencies do I need paid licenses for, who is offering them, on what terms, and at what cost?
3. Which of those paid licenses do I already have, and which do I need to buy?
4. Where do I go to buy them?

In an ideal development world, all dependencies would come with standardized package metadata manifests, and those manifests would spell out their public licenses in a uniform, machine-readable way.  Ecosystems like npm, RubyGems, and Cargo come pretty close.  But for other language ecosystems, the protocol needs to provide a standard where it doesn't already exist.

Standard package metadata manifests frequently describe the _public_ license that applies to the package, but rarely provide any machine-readable way to express that _private_ licenses are for sale.  In some cases, the manifest standards allow for arbitrary additional metadata.  That's the case for `package.json` and `Cargo.toml`.  The protocol can use that support to describe paid licensing.

Taking an inventory of which dependencies need paid licenses and comparing that to the licenses the user already have is the primary job of the command-line client that users will run on their projects.  `licensezero quote` does this for License Zero today.

The CLI must also handle directing users to the checkout pages for the licenses they need to buy.  `licensezero buy` does this today, by directing users to webpages where they can enter credit-card details.  The main gist of the redesign is to support situations where `licensezero buy` returns _multiple_ addresses in cases where the license the users needs aren't all available from licensezero.com.  It must also ensure that `licensezero quote`, the command to import data files about the licenses that the user has bought, works with different APIs.

I'm close to having some preliminary specs for all the necessary elements:

- schema for dependency public and private licensing metadata
- API specification for online licensing web stores
- data schema for receipts for paid licenses
- client application command-line interface

JSON Schema and Swagger have been essential for sketching out data schemas and the API schema.  Within those schemas, a number of standards come into play: Ed25519 for public-key signatures, ISO 3166-2 for identifying countries and states, ISO 4217 for currency codes, UUID for random identifiers, ISO 8601 for dates and times, and various RFCs for URLs and e-mail addresses.  And of course POSIX utility argument syntax for the CLI.

With the exception of multiple currency support, these are the stuff License Zero is already made of.  But settings things out from the protocol point of view has already pointed out some unrealized opportunities for improvement of License Zero itself.  For example, License Zero currently treats paid licenses and (mostly) free waivers as different kinds of objects. They can easily be abstracted.