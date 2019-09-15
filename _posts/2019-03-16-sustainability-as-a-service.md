---
title: Sustainability as a Service
description: open questions in communication and approach
author: K.E. Mitchell
layout: post
---

License Zero is one of a growing category of companies promoting and systematizing ways to get open software developers paid.  Behold:

<a class="noglyph" href="/images/open-questions.svg"><img alt="graph" src="/images/open-questions.svg"></a>

I could not be more happy to see that graph grow.  Granted, I have very strong opinions about the trade-offs of different approaches represented.  I also have my own set of constraints: personal, business-wise, and self-imposed.  License Zero's particular design reflects those constraints as much as my views.

The one prescription I push not just for myself, but also for others, is diversity.  Perhaps we theorize our way to what works, but in the end, it isn't up to the service providers to prove it out.  If and when we end up with a stable "menu" of well understood options for developers, we're going to be able to look back and find precursors that tried and failed, ahead of their time.

All that said, it's worth working backwards from what a company or foundation offers to why they think it will work and why that way is preferable.  Partly because the trade-offs matter.  Partly because supporting those offerings also supports their priorities and values. Partly because it's the only reliable way to separate a company's design from its constraints.

# Should developers hold stuff back to trade for money?

I've written that [if open source means giving people everything they want for free, then open source developers end up with nothing left to trade for support](https://blog.licensezero.com/2018/03/05/withholding.html).  But the first question isn't what developers should withhold, but whether they should withhold at all.

## Donations

By far the most common answer from services on offer is "no".  Instead of holding back and trading,  rely on gift transactions: donations, grants, and other forms of gratuity.  [Patreon](https://patreon.com), [LiberaPay](https://liberapay.org), and [OpenCollective](https://opencollective.com) for recurring donations.  Now [CommunityBridge](https://communitybridge.org) for grants.

This approach is easy to adopt, because it carries near-zero social risk of frustrating widely held open source consumer expectations.  The idea that [money and open source don't mix](https://dhh.dk/2013/the-perils-of-mixing-open-source-and-money.html) is out there, but no longer in vogue, and not in line with "open source won" expansion via widespread software industry adoption.  Recognition of the maintainer's plight is on the rise.

Unfortunately, low risk usually means low reward.  Much is made of [happy outliers](https://www.patreon.com/evanyou), to the same effect as putting lottery winners on billboards.  The image of the successful, donation-funded developer looms large in the collective consciousness, but very small in daily experience.  Add the fact that many successful donations-based developers are actually withholding substantial value as perks, like [security information](https://www.patreon.com/eranhammer), and perception skews still further.

What the success cases really seem to want is exchange results under the guise of unilateral, voluntary support.  We want to withhold without anyone noticing we're withholding.  That could be the best of both approaches, but also inherently deceptive, not least self-deceptive.

In my view, the underlying problem with "donation", as with "community", and "sustainability"---as opposed to "fee", "company", and "profit"---is that they [give permission to exempt open developers](https://blog.licensezero.com/2018/06/14/profit-sustainability.html) from [baseline business norms of respect and fair reward](https://writing.kemitchell.com/2017/10/16/Mercenary-Rapport.html#hired-guns), which [apply plenty well to open developers' closed counterparts](https://blog.licensezero.com/2018/01/22/largesse-oblige.html).  We're desensitized to the voraciousness of businesspeople and the monomania of megacorps, but also to the [starvation of artists](https://twitter.com/forexposure_txt) and the [destitution of dogooders](https://www.nbcbayarea.com/news/local/Oakland-Teachers-to-Walk-Off-the-Job-Thursday--506133701.html).  Taking the donation tack opts you out of norms that accept your winnings, and into norms that accept your losses.  A radically different baseline for the same work, often better.

Self-interest is in abundant supply.  Enlightened self-interest is as rare as it sounds.  Foregoing the former, and depending on the latter, puts a lower ceiling over expectable and attainable financial outcomes.  I think it locks "sustainability" into a boom-bust cycle driven by [crisis](https://heartbleed.com).  Big organizations spend _too_ much in response to crises, because they're functionally incapable of proportionate, high-resolution payments.  But [sudden largesse](https://www.coreinfrastructure.org/) gets gobbled up quickly by pent-up need, [necessitating a drumbeat of new crises](https://twitter.com/i/web/status/1105164477626900480) to smooth out the jarring, feast-famine curve.  A kind of attention-economy [Fourier transform](https://en.wikipedia.org/wiki/Fourier_transform) for stability.

## Unexpected Exchanges

Within the narrative of "no withholding", but not within "no exchange", we see firms helping developers enter lines of business orthogonal to software development.

For example, [CodeFund](https://codefund.io/) helps developers sell ads on project sites, `README`s, and other materials.  Sponsored projects through [OpenCollective](https://opencollective.com) often add sponsors' names and logos to those materials, too.  Some developers on [Patreon](https://patreon.com) offer the same, as perks for high-dollar patrons.

In a general sense, developers using these services aren't holding anything that users expect back.  Instead, they're introducing something that users don't expect---advertising---for a fee.  These projects [run a risk of disappointing expectations](https://medium.com/@nayafia/the-kite-debacle-is-democracy-at-work-6a04bc043c50) if they go "too far".  But they rely on developers to know their own communities and ride the line without pissing users off.

Nobody, developer or not, likes ads.  But we are, again, largely desensitized to the matter.  Ads on a project website fit the broader Web experience.  If their unexpected appearance causes chagrin, users don't expect any meaningful forum to express it or redress it.

# What should developers hold back?

Among those services that do provide services for holding back and trading, practices and supporting theories vary widely.

Some services, like License Zero, [itch.io](https://itch.io/), and various bounty-program services, advocate for essentially one particular form of withholding.  For License Zero, it's license permission.  For itch.io, distribution. Through bug bounty programs, maintenance and further development.

Other services mix up a cocktail offering for paying customers.  [Tidelift](https://tidelift.com) is the principal proponent of this approach, tying [scope of offering](https://tidelift.com/docs/lifting/tasks-overview) to [results of open source consumer surveys](https://blog.tidelift.com/).  We also see it on the company side, where offerings typically [cross the broad spectrum of legal assurances, proprietary features, support, and other benefits, comprehensively](https://www.mongodb.com/products/mongodb-enterprise-advanced).

For those looking to mix their own, many of these services are actually compatible for concurrent use on a single project.  You could sell access to GitHub issues through [GitStore](https://gitstore.app/), dual license with License Zero, claim bounties through [BountySource](https://bountysource.com), and offer Tidelift's package of additional work, all at the same time.  Sounds like a messaging mess.  But it's possible.

Ask many developers why they're using this-or-that approach, and their answer will likely be that they tried it and it worked.  But from a higher perspective, one with concern for the effects of those approaches on the production and phenomenon of open software more generally, it's worth asking which kinds of withholding we ought to prefer and encourage, and why.

There's no agreement, or even any vocabulary, for how to go about that assessment.  License Zero does [uniline permission withholding](https://guide.licensezero.com/#read-this-first), for tightly coupling value delivered to value earned.  Tidelift is [against license withholding, for introducing friction](https://blog.tidelift.com/2018s-new-open-source-licenses-will-they-work-should-they-work).  Bounty proponents arguably take a composite of those positions.

So how do we go about deciding whether withholding some aspect or another of software value works or won't work, improves the state of open software more generally, or harms it?  How do we weight the costs and benefits, private and more general?  In my own terms:  Which [fulcrums should developers leverage for support](https://blog.licensezero.com/2018/03/04/fulcrums.html), and why?

This is largely unexplored---and unarticulated---territory, beyond expounding any particular theory.  But I'll take a first stab.

## Meet consumer expectations.

We might choose our leverage to minimize disappointment---and resentment---on the basis of open source consumer expectations.

At an extreme, that means no withholding at all, but rather donations, ads, or another business, like ads, that doesn't overlap with software development or bear its expectations.  The [donation](#donations) and [ad](#unexpected-exchanges) platforms covered earlier fall here.

In more moderate form, this view manifests as an aversion to [friction](https://www.youtube.com/watch?v=qvB_PZHJlAE)---roughly definable as things consumers dislike---but not exchange, coupled with a push to package and monetize new parts of the overall software picture before GitHub turns gobble them up as yet more things users expect for free.  Again, [Tidelift](https://tidelift.com) leads here.

## Correct consumer expectations.

We might instead conclude that expanding consumer expectations of open source  are precisely to blame for crushing open source contributors and maintainers, and assault them head-on.

License Zero takes this position, in substance and style.  Services like [GitStore](https://gitstore.app/), which helps sell access to GitHub repos, do so in substance, with a more neutral or even conciliatory tone.

## Deregulate.

Another slice through available fulcrums follows the greater open licensing theme of [reversing default rules that impose transaction and compliance costs](https://oss.kemitchell.com/#in-brief) on the use of software.  If the law, or other important rules, [regulate the production, sharing, and support of software](https://writing.kemitchell.com/2019/03/04/Back-to-IP.html), we should duck those rules and return to a pristine [state of software nature](https://en.wikipedia.org/wiki/State_of_nature), where norms and boundaries arise socially and become intuitive, rather than formal.

This view cuts strongly against leveraging license terms and open defaults, like open GitHub repos.  It favors paid-development approaches, like bounties and maintenance contracts, as well as sideline services, like hosting, training, and support.

Some variants of this view lean heavily on notions of the Internet's inherent rules, as distinct from the default social order before or without the network.  Faith in network values enables [sweeping prognostications about the fate of software production](http://shop.oreilly.com/product/0636920033325.do) more generally, but also attracts [biting empirical criticism](https://www.publicaffairsbooks.com/titles/evgeny-morozov/the-net-delusion/9781610391061/).

## Promote software freedom.

For free software activists, question about software are almost always questions about software freedom.  But it's often difficult to tell where that leads.

RMS has expressed [approval for dual licensing](https://www.gnu.org/philosophy/selling-exceptions.en.html), especially in preference over "open core", and also [respect for those who work for free on free software, but expect pay when they do not](https://www.gnu.org/philosophy/pragmatic.en.html).  The use of copyleft licenses for dual licensing increases the amount of copyleft software, and therefore [the network effects of honoring software freedom](https://blog.licensezero.com/2018/05/13/commons-club.html), at least [to the imperfect extent to which copyleft licenses express what that means](https://blog.licensezero.com/2018/10/26/no-other-terms.html).  Accommodating users building non-free software does not.

## Maximize earning potential.

We might accept above all else that making money as an independent anything is hard, software not excepted, and that developers should withhold and trade as much and whatever they can to make ends meet.

This view manifests often in very pragmatic terms.  Try everything.  The more that work, the more you can make.  Or do one thing, and put your whole effort into maximizing it.

More commonly still, this approach dovetails with delegation to experiment and competition---the market---rather than formulating and proving any particular thesis.  Trust the process, be as flexible and agnostic as possible, and let things shake out.

## Maximize unbounded upside.

Another approach stresses, and protects, the awesome value-delivery potential of unencumbered software.  Withhold nothing that benefits all comers.  We can't possible measure the good it will do them, to weight against any cost.  Focus instead on delivering value that's inherently specific to known, singular beneficiaries, who become customers.

Sell customization work, but don't make the software hard to customize.  Sell training, but don't skimp on public docs.  Host or configure as a service, but check your tooling into the public repo, so others can, too.  Depend on virtue to avoid these temptations.  You will need it, because incentives are strong.

# Where do we go from here?

Unlike some of my other writing, which offers a holistic framework for thought on a given point, this post is admittedly incomplete.  I am riffing on---and projecting---various heuristics to cut the _Should I withhold?_ and _What to withhold?_ problems down.  I can offer no preworked solution, only the particular thought narrative informing and justifying my own approaches.

More than anything, I'd like to hear from others about how they weigh the big-picture ramifications of various "sustainability" services, available and hypothetical.  And I'd like to see more such services own the implications of their choices, and show more or their work.

It's a fairly safe bet that _none_ of the current crop of sustainability as a service companies or foundation programs will survive ten years.  That's the nature of business, and the nature of experiment.

If you can succeed, by all means succeed!  I will be glad for workable solutions, even at the expense of my own.   But as we rush to profess our concern for the plight of open software developers, and not just our personal interests in redressing it, we should both show and tell that we see broader our work and its implications in broader context.  It's fun to say that License Zero [is just a vending machine](http://licensezero.com/vending-machine.svg), but not really true.

Those we seek to serve often care more for the whole than their part in it.  That goes a long way, explaining how they're into this mess.  But it's not a fault we can criticize them for.  I think it's a fault we'd better share.
