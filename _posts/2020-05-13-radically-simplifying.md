---
title: Radically Simplifying
description: major streamlining underway
---

Response to [the proposal to radically simplify License Zero](/2020/05/09/radical-simplification.html) has been overwhelming.  License Zero is on a diet!

The [command-line interface](https://github.com/licensezero/cli) is now for sellers only.  Customers could always buy their licenses through the website, [as on this page for, for fuzzyset.js](https://licensezero.com/offers/562c0ffe-df98-4348-87b7-e60e3c37c534).  Now that is the only way.  Several new developers selling through L0 have reached out with improvements to the layout and content of offer pages with this in mind, and more improvements are in the works.  Developers can already customize pages for specific offers to match project websites or preferred styles.

None of the work on scaling license buys to an arbitrary number of dependencies per project has been thrown away.  Rather, we're acknowledging that those tools of scalability take tolls in explanation, indirection, and potential confusion for potential customers.  That trade-off doesn't make sense yet.  When it does, we'll have plenty of prior art to look back to.  Now is _not_ the time to catch license-management Kubernetes.

I have also discontinued support for sponsored relicensing onto permissive terms through licensezero.com.  Developers are still welcome to offer those kinds of deals on their own, and [License Zero's documentation](https://licensezero.com/licenses#relicensing) for closing them remains available.  Doing those deals on the side, without License Zero in the middle, was my most common advice about them already.  Why pay a large transaction fees to Stripe, or L0's lesser commission, for that matter?  Do a bank transfer.

And of course I'm in the process of streamlining and updating [the guide](https://guide.licensezero.com), License Zero's primary documentation.  I'm particularly happy with how short and straightforward [a step-by-step guide to offering licenses for a project](https://guide.licensezero.com/#step-by-step) can now be.

With SPDX identifiers for Parity and Prosperity in hand, we can leverage the existing channel of license metadata to communicate licensing models to users.  We can also leverage funding-specific comms, like [npm funding metadata](https://blog.licensezero.com/2020/05/09/npm-metadata.html), to link users to offer pages.  Eschewing License Zero-specific metadata, like the old `licensezero.json` files, simplifies the process, and dispenses with a lot of custom tooling.
