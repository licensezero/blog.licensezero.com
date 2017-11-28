---
title: Open Source Accession via License Zero?
description: a paved path to permissivity
layout: post
---

I've written that License Zero ought to be a simple machine, an [artless device](https://artlessdevices.com)---plain, transparent, and self-consciously scrutable.  But the simplest machine does nothing at all.  I'm wondering whether License Zero shouldn't add one more service to its competency: administering offer and closing of deals to buy out License Zero projects to Open Source.

I have a lot of material and prior thinking on this, but it's not enough.  If these deals are of interest, as part of or entirely separate from License Zero, I'd greatly appreciate your help figuring out how to do this right.  Even if doing it right means not doing it through License Zero at all, and having good reasons why.

# Double Stairway to Heaven

The License Zero toolkit already paves a road to Open Source.  Condition 3 of [the public license](https://licensezero.com/licenses/public), which contains all the new legal terms, falls away if private licenses stop being available:

> The conditions of this paragraph [Condition 3] are waived if licenses on other terms cease to be available via the following agent, or a successor named in a subsequent release, for 90 consecutive calendar days: [Agent Name, Website, and Product ID follow.]

In essence, [License Zero is a patch to two-clause BSD](https://licensezero.com/licenses/public/diff).  Waiving---giving up the legal benefit of---Condition 3 undoes the patch, leaving you with two-clause BSD again.

The difference between turning License Zero into Open Source software by `l0-retract`-ing private licenses from sale and turning License Zero into Open Source software for a price boils down mostly, but not entirely, to payment, `LICENSE`, and metadata updates.  The company's published a form contract for these kinds of deals, the [License Zero Open Accession Agreement](https://github.com/licensezero/open-accession-agreement).  The form is short, and its essence is very simple: Developer has code under relatively restrictive public terms, or no public terms at all.  Sponsor pays Developer.  Developer relicenses under a pre-agreed Open Source license, and publishes into a pre-agreed distribution system.  There are no ongoing service commitments, other than keeping the project code on distribution for a year, as long as that's free.  There's no obligation to make future contributions Open Source, or to make them at all.  That's [Switchmode](http://github.com/kemitchell/switchmode) territory.

The Accession Agreement is already public, and publicly licensed.  It's perfectly possible to use the form as a starting point on deals for existing License Zero or proprietary software, right now.  Get lawyer help.  Go get paid.

Linguistic Relativity

In conversation with maintainer friends, we often land on the term "ransom" to describe these kinds of exchanges.  For many, that single word does more, and more quickly, to explain what the Open Accession agreement is about than anything else.  I understand why.  I also have deep misgivings about that why.  Hence a new term, "accession", in my writing and throughout the License Zero toolkit.

Intuitively, Open Source is the high point on a scale of practical liberation for code.  It's where, ideally, we want code to be.  Extending the analogy, License Zero holds software captive, takes it out of its natural state of freedom.  Perhaps for some valid purpose, sure, but takes it captive all the same.  "Ransom" is paid to bring it home.

One side wants freedom.  The other side wants cash.  Pirates are fun.  Culturally, [we're into pirates](https://www.npmjs.com/package/optimist).  But Good Guys don't tend to practice ransom as a business model.  You're The Baddies.

Unfortunately, that view embarks from a point of view that fundamentally depersonalizes software, often as "information", which compares unfavorably to "work product", to say nothing of "craft".  Were everyone well cared for as a matter of course, and software written only for aesthetic, intellectual, addiction-service, or other inherent motivation, everything would be Open Source.  Or rather, the law would make total freedom in software the norm, rendering Open Source as we know it---an escape hatch out of laws that lock up software---legally and practically unnecessary.

Open Source is very, very necessary.  The law is not as our ideals would like to dictate.  And neither is software impersonal, in conception or in maintenance, though it's easy to see it that way, especially when it works reliably and well.  If there's a price to be paid ferrying indie software between the distant shores of reality and paradise, it's not clear to me that developers should always pay the whole toll.  They get stuck with all kinds of bills---and risks---as it is.

So more to reject a damaging framing effect than to add any new coinage under my name, License Zero calls deals to bring software across "accessions", not ransoms.

In my mind, "accession" carries strongest association to libraries: each new volume added to a library or collection is an "accession", receives an "accession number", and adds to the available store made open to all, for any purpose, free-of-charge.  There's no resentment of the fact that books take paper, glue, ink, printing, editing, distributing, storing, and repairing to make and bring in.  "Accession" holds no disdain for just compensation en route to the commons behind its teeth.  That's not what software and software makers deserve, even if they happen to be invisible.

Implementation

As I see it, License Zero could simplify the process of acceding software to Open Source in a fairly straightforward way:

- In addition to flat prices for private licenses, developers could optionally specify a standing-offer accession price.  So in addition to, say, $10 for solo, $20 for team, $30 for company, and $50 for enterprise, I might also specify that I'll accede the project, under the two-clause BSD License, for $1,000.

- I'm fairly sure that I'd lock the accession license to two-clause BSD.  First because no choice is the simplest kind of choice to make.  Second because I expect many License Zero maintainers will accept outside contributions under those terms.  Third because it's an established, if somewhat dated and fuzzy, permissive license, the immediate progenitor of the License Zero Public License, and essentially the terms that non-commercial users enjoy under License Zero before accession.

- The site's agency terms would make clear that the agent can sign the License Zero Open Accession Agreement on the developer's behalf if they set an accession price.

- On payment, licensezero.com would notify the developer, and provide instructions, right out of the contract, for what to do next.  It would also stop selling private licenses, and report to users generating quotes that the software is now Open Source.

- licensezero.com may or may not connect the sponsor and developer by e-mail.  I'm not sure.  My natural preference is to avoid sending e-mail unless I know it's very worthwhile, most of the time.

There are a few potential problems with this approach that I can see:

- Accession prices will tend to exceed private license prices, and fees---payment processing, perhaps a commission to the agent---will add up quickly on any percentage basis, like Stripe's.  It could be worthwhile, fairly often, for sponsors and developers to close accession deals "on the side", using a check or wire transfer for payment.  For what it's worth, I will seriously consider zeroing out agent commission on accessions, or setting a flat fee close to cost of service, once I can measure it.  Not for any good business reason, but because it's my damn company, and I think that sends a clearer message about values and relationship to Open Source than any blog post could.

- Again, accession prices will tend to be larger than private license prices, and that may trip financial control and budgetary limits on credit-card transactions.  Folks may have to use payment methods that License Zero doesn't want to support.  Credit cards are bad enough.

- Purchasers of private licenses who find a project acceded the next day may feel cheated or tricked.  That's primarily a feelings and perceptions issue---customers take or don't take the deals they see at the time---but potentially a messy one.

Can you think of any more?

# Lawyerball

Apart from structuring the process, this calls for continued, thorough analysis of the form agreement.  Or rather, what developers and sponsors will think of the form agreement.

Unlike private licenses, where there's ample prior art and established practice on terms, accession looks newfangled.  In terms of prior art, it's probably closest to my own work on [Switchmode](https://github.com/switchmode/switchmode), which is seeing use, but still very young.  Issues and pull requests on both stand open, and I'd love input on what would work, especially from the company-sponsor point of view.
