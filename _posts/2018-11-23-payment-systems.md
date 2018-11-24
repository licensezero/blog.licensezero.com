---
title: Payment Systems Research
description:
layout: post
---

Every time a user buys licenses through licensezero.com, the system needs to:

1.  Take payment-card details.

2.  Route payments to all the developers the user needs to buy licenses from.

3.  Route commission to License Zero.

4.  Send license files and receipts to users.

Currently, licensezero.com achieves this through [Stripe Connect](https://stripe.com/connect).  Connect allows licensezero.com to "connect" to developers' own Stripe accounts.  Once connected, licensezero.com can create API tokens for developer accounts.  Using those tokens, licensezero.com can initiate multiple payment transactions with the same set of payment-card details.

Crucially:

1.  Stripe Connect allows licensezero.com to initiate payment transactions for as many developers as needed.
2. Payment transactions happen almost exactly as though the developers wrote Stripe applications and processed payment themselves.
3. License Zero needn't receive money that ultimately belongs to developers.  Money goes _directly_ to the developers.

Stripe is well known for good API design, documentation, and programming language support.  Connect is no exception.

Unfortunately, Stripe [currently supports twenty three countries](https://stripe.com/global), with Brazil, India, and Mexico to come.  Stripe's coverage pales in comparison to [PayPal's jurisdiction support](https://www.paypal.com/us/webapps/mpp/country-worldwide).

My personal experiences with PayPal have been terrible, developer-wise and customer-wise.  But if PayPal supported the kinds of payment-splitting features that licensezero.com needs, I'd use it anyway, to make licensezero.com available to more people.

Technically, PayPal is playing catch-up.  They bought Braintree, a company offering marketplace-focused payment features, especially for e-commerce, about five years ago.  Unfortunately, the acquisition has not brought [Braintree's country support](https://www.braintreepayments.com/country-selection) in line with PayPal's.

At first glance, Braintree's global reach compares favorably to Stripe's.