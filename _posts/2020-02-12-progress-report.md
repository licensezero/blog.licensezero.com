---
title: Progress Report
description: schemas and new CLI are stabilizing
---

Progress continues apace on the redesign and reimplementation of License Zero's structure and protocol.  The [schemas and API specification](https://github.com/licensezero/schemas.licensezero.com) have evolved considerably, largely as a consequence of working through [reimplementation of the CLI](https://github.com/licensezero/cli/tree/v2).  I believe the hard parts of that rewrite are now behind me.

The next step will be reimplementing the server side, with an eye toward both licensezero.com itself and self-hosting users selling licenses for just their own work.  licensezero.com is currently a single Node.js application combining API and web front end, but I'm strongly considering splitting API from web front end for the new iteration.  I'm also considering shifting the implementation language for the API to Go as well, to simplify development and deployment.  If at all possible, I'll keep the API writing to POSIX file system only, which make the deployment story pretty slick.

The key differences between licensezero.com and self-hosted versions will likely be multiple seller support and payment processor.  licensezero.com has to stick with Stripe for one-to-many payor-to-payees checkout transactions.  And I suppose there's nothing to stop self-hosters from choosing Stripe, too.  But I anticipate that most folks choosing to self-host will do so because Stripe doesn't support their country.  The obvious self-hoster choice then becomes PayPal, which supports many, many countries.
