---
title: But You Said I Could
description: a clear-eyed view of open software funding, impediments, and possibilities
layout: post
---

If you want money for open work, you have three good options:

1.  Pick an [open-only](https://paritylicense.com), [noncommercial](https://polyformproject.org/licenses/noncommercial/1.0.0/), or [restricted](https://polyformproject.org/licenses/) license and advertise [closed, commercial, or unrestricted terms for sale](https://indieopensource.com/public-private/indies).  That's [License Zero](https://licensezero.com).

2.  Pick a [permissive license](https://blueoakcouncil.org/list) and aggressively force your funding message on users who don't want to think about it.  That's [OpenCollective](https://opencollective.com), [Tidelift](https://tidelift.com), [hosting](https://indieopensource.com/hosting/indies), [support](https://indieopensource.com/open-core/indies), and [so on](https://indieopensource.com/paid-support/indies).

3.  Stop releasing so much software.  Put that time into networking, online presence, and telling everyone who will listen that you want paid open gigs.  You've [crossed break-even](https://writing.kemitchell.com/2019/06/25/Get-In-Get-Out.html).

Odds are, picking a permissive license and registering for a payment account, signing up for [a funding platform](https://blog.licensezero.com/2019/03/16/sustainability-as-a-service.html), or offering contracts in `README` just won't work.  Very few will look past the good news of your license to the bad news of your payment plea, and very few who do will actually pay you.  You will grow increasingly disappointed, embittered, and poor as time rolls on.

There is no viable option that involves just pumping out more permissively licensed software without forcing unwelcome messages and changes on entitled users.  There is no viable option 100% inside the open-coder comfort zone, with no risk of [drive-by condemnation](https://blog.licensezero.com/2019/08/24/Process-of-Elimination.html).  I've looked.

I have seen [exceptions](https://reference.kemitchell.com/top-donations-developers.html) to this rule.  But the exceptions are highly exceptional.  They are also over-publicized, like lotto winners, both as software projects and as funding outcomes.  Chance favors the prepared mind, but planning to get lucky is not a plan you can follow.

What is going on here?

## Miscommunication

The strongest arguments for paying open software developers boil down to fairness and enlightened self-interest.  Users should pay, and they should want to pay.  After all, an open license isn't a Get Out of Ethics Free card.  Honest work for honest pay still applies.  The Golden Rule still applies.  Basic fairness still applies.  But basic fairness is not what we see for a lot of contributors.  If word of pervasive unfairness gets around among contributors, users can expect less new and interesting software to come out on permissive terms.

The strongest counterargument boils down to "but you said I could".  Honest work for honest pay is and ought to be the rule.  But open developers slapping permissive licenses on their honest work explicitly waive the pay part of the equation.  Inviting free riding, then crying foul when riders don't pay, is also unfair.  If all permissive software developers started angrily demanding back pay, users would be a lot less willing to lap up permissively licensed work.

As usual, when communication fails, it fails on a few levels at once.

Licenses don't express the whole situation for many developers.  They're not designed to.  Many developers choose MIT or BSD or Apache for maximum adoption, having seen how far code under those terms can go.  They don't want to compromise the chance of success on that scale.  But standardized permissive licenses don't come with blanks to fill in about whether the developer needs a job, wants donations, or has to sell products or services to continue their work.  Users go ahead and assume none of the above, since that's what's best for them, and they'd rather just not think about it.

When developers express their needs elsewhere, as in `README`, on a project website, or in documentation, they rely on far less reliable channels for their messages.  Licensing is TCP.  Users need to know they have the right license terms.   So platforms, package managers, build tools, and the rest all work diligently to make sure license messages get through.  Anything else is UDP.  Some users can meet special needs through it.  But it's not essential to using the software.

To use code you found online, licensing information is both practically necessary and practically sufficient.  Ads for the developer's funding model are neither.

## Eyeballs

When it comes to getting a message across, distinguish messages developers force users to see, like advertisements, messages users are forced to seek out, like license terms, and messages users see of their own volition, or by chance, like notes in `README`.

[OpenCollective messages](https://www.npmjs.com/package/opencollective), [core-js' postinstall](https://github.com/zloirock/core-js/issues/548), and Feross' [`funding`](https://www.npmjs.com/package/funding) forced messages on users, as advertisements for donation portals, maintainer availability, or sponsors.  The common refrain against them demanded that the developers put their ads in `README` or other places where they could be easily overlooked.  In other words, to make them ineffective ads.

License Zero bootstraps off license terms.   Users have to verify license terms, and when they don't find the permissive terms they were hoping for, they're prompted to look deeper, and find out about available paid licenses.  The command-line interface automates the process of finding, fetching, and acting on that information.

Some months back, I PR'd a [new `sustainability` field for npm `package.json` files](https://github.com/npm/cli/pull/187) to encode a JSON endpoint with data on calls to funding action.  But the upshot of that kind of standard is pretty narrow.

Standardized funding metadata would make it marginally easier for developers at companies that decide to go fund developers to compile the relevant data.  It would do little if anything to bring funding needs to the attention of users overall, whether they've decided to fund or not.

I recently pushed commits to my PR starting to implement automatic reporting of funding calls to action on `npm install`.  Users would receive a report of all funding opportunities for their dependencies, along with their summary of packages installed and any known security vulnerabilities.  Rather than police what postinstall scripts print out, reserve a bit of attention at the end of the install lifecycle event, and regulate the form of its content.

## Fame

I'm hearing more and more about a new approach---as far as I can see, still largely theoretical---that bears mentioning.  In essence, it's an inversion:  Instead of worrying about how to put your plea, your wares, or your cause in front of eyeballs, get the eyeballs first, and work backwards to funding from there.  At this point, somebody mentions [twitch.tv](https://twitch.tv).

I find this angle interesting, largely, I think, because it is new, at least in software.  We've already seen an evolution of donation-based models toward sponsorship, with logo fields emblazoning `README` files and project websites, especially via OpenCollective and Patreon.  We may yet see developers wearing sponsor t-shirts, adding sponsor flair to their GitHub profiles, and distributing swag at events in more systematic ways.

That would amount to software imitating other fields, not a new software innovation.  Witness motorcycle racing.  Many amateur riders love to add stickers from well known parts manufacturers and other suppliers to their motorcycles.  In time, successful local racers get small-scale sponsorships, often with discounts and occasional free parts.  From there, the top of the racing crop attract full-time commercial relationships riding for factory teams and wearing lots of logos whenever cameras might see.  At the highest levels of racing, sponsors' businesses needn't have any direct connection to racing at all.  Repsol is an oil company.  Red Bull and Monster Energy make beverages.  All are name sponsors of 2020 motorcycle grand prix teams.

Assuming viability for software personalities, this approach suffers much the same drawback as other models that turn on making open software, but selling something else.  Attracting eyeballs and developing great software entail disparate skills, frequently divergent personalities, and inevitably competing time commitments.  Software production becomes merely a byproduct, or a catalyst, of a different main line of business.  The most popular game streamers are rarely the best gamers, to say nothing of game designers.

## Realism

In the end, the taking-off point has to be a clear-eyed assessment of the current state of play.  Independent developers earning well for making open software are not the norm.  Institutional policies, social norms, and conventions currently run against that outcome, not for it.

With odds that bad, beating the odds means changing the odds.  Independent developers experimenting with new ideas in developer-user relations can expect to take flak.  But they can press on knowing that their results---positive or negative---contribute not to just to a good personal outcome, but to the state of the art for all independent developers.
