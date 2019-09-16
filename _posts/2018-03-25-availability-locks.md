---
title: Availability Locks
description: freedom from choice might be what you want
layout: post
---

License Zero now supports locking availability and pricing of private licenses for specific projects.  Locking a project makes a public, verifiable commitment to keep selling private licenses for your work through [licensezero.com] at or below your current price.  You decide how long the lock will last.

```bash
l0 lock $PROJECT_ID 2020-01-01
```

Once a lock is in place, you can't remove it.  The [agency terms] make clear that the company behind [licensezero.com] won't undo locks under any circumstances.  That makes locks powerful tools.  Handle powerful tools carefully!

By default, contributors licensing through [licensezero.com] can change pricing for private licenses, or stop offering private licenses altogether, at any time.  Why would they ever choose to lock?

# Reassuring Users

Users of a package may be more willing to use a package, and pay for private licenses, with assurance that private licenses will be available and affordable.

Project pages on [licensezero.com] make these assurances public and verifiable:

![example locked pricing text from a licensezero.com project page](/images/locked-project-pricing.png)

Where a particularly large user of a project wants to assure availability, but doesn't want to pay the full price of [relicensing](https://guide.licensezero.com/#relicensing), I could see them paying a contributor agreeing to lock a project at a specific price, for a specific amount of time.

# Deals Between Contributors

Locks can help facilitate [stacked licensing](https://guide.licensezero.com/#stacked-licensing), where packages get distributed with metadata for multiple License Zero projects covering contributions from different developers.  Users need to buy private licenses for all the projects in the stack, but the [command-line interface]'s `quote` and `buy` commands handle that automatically.

Consider a hypothetical:
- Anna creates a package.  She licenses her work on the package via [licensezero.com].
- Bob forks Anna's project and makes lots of changes, vastly improving the package's performance.
- Bob licenses his work on the package via [licensezero.com], too, stacking metadata for Anna's work and his own work in `package.json`.

Anna would like to merge Bob's contributions into her own version of the package, and continue working on the combination of both her work and Bob's.   But If Anna builds on top of Bob's contribution, and Bob suddenly stops offering private licenses for his work, or massively increases the price, Anna may have to go back and either remove or redo Bob's work, to keep offering private licenses that users want to buy.

There are any number of ways Anna and Bob could address this risk.  For example, Anna could make a deal with Bob, where Bob licenses his work to Anna, Anna removes Bob's project metadata from the combined project, and Anna shares earnings from private license sales with Bob.  That would work, but License Zero's tools and systems don't offer much administrative help.

With locking, Anna and Bob can address the risk another way:  Anna can agree to merge and build on Bob's contribution if Bob locks pricing at a particular price for a time, perhaps the next two years.  If Bob agrees, he can lock the project with the [command-line interface].  Anna can confirm that Bob locked as agreed on the [licensezero.com] project page for Bob's work.

# Implementation

This change required additions to [licensezero.com] server software for the API and project pages, the [command-line interface], and the [agency terms] contributors agree to in order to sell private licenses through [licensezero.com].

As always, you can get the latest with `npm i -g licensezero`, or by running `npx licensezero`.

[licensezero.com]: https://licensezero.com

[command-line interface]: https://www.npmjs.com/package/licensezero

[agency terms]: https://licensezero.com/terms/agency
