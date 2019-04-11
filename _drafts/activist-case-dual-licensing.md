---
title: The Case for Selling Exceptions
description: a model for copyleft, in more ways than one
layout: post
---

There's a take on copyleft that says:

> Copyleft doesn't achieve anything unless it applies to everyone, including the original developer.  If only one company can build proprietary add-ons, or sells exceptions, that's just abusing copyleft as a business ploy.

We see the same view reflected in terms, like section 7 of [copyleft-next](https://github.com/copyleft-next/copyleft-next) 0.3.1, a kind of research license looking forward to the next GPL:

> 7\. Nullification of Copyleft/Proprietary Dual Licensing
>
> If I offer to license, for a fee, a Covered Work under terms other than a license that is OSI-Approved or FSF-Free as of the release date of this License or a numbered version of copyleft-next released by the Copyleft-Next Project, then the license I grant You under section 1 is no longer subject to the [copyleft] conditions in sections 3 through 5.

Much the same in the Free Software Foundation's [policy against making exceptions to the GPL](https://www.gnu.org/philosophy/selling-exceptions.en.html) for its own projects.

But not so fast.  Dig around [FSF.org](https://fsf.org) long enough, and you'll find that RMS doesn't condemn selling exceptions to copyleft.  He accepts and encourages it.  [Quoting](https://www.gnu.org/philosophy/selling-exceptions.en.html):

> I've considered selling exceptions acceptable since the 1990s, and on occasion I've suggested it to companies.  Sometimes this approach has made it possible for important programs to become free software.

RMS goes on to give the example of Qt's transition from proprietary to reciprocal to GPL licensing, a phenomenon I recently [explored on my personal blog](https://writing.kemitchell.com/2019/04/06/Stairway-to-Heaven.html).  Later in the same piece:

> When I first heard of the practice of selling exceptions, I asked myself whether the practice is ethical.  If someone buys an exception to embed a program in a larger proprietary program, he's doing something wrong (namely, making proprietary software).  Does it follow that the developer that sold the exception is doing something wrong too?
>
> If that implication were valid, it would also apply to releasing the same program under a noncopyleft free software license, such as the X11 license.  That also permits such embedding.  So either we have to conclude that it's wrong to release anything under the X11 license---a conclusion I find unacceptably extreme---or reject the implication. Using a noncopyleft license is weak, and usually an inferior choice, but it's not wrong.

I don't think condemnation of licenses like X11, better known as MIT, unacceptably extreme.  If the point is principle, picking a permissive license when copyleft would do is a straightforward offense.  Perhaps a venal sin, rather than a mortal one, but a sin nonetheless.  RMS doesn't show more work, offering any kind of structure or cost-benefit analysis to show that letting willful permissivity slide nets out positive for software freedom.

As for me and my house, License Zero and its [Parity Public License](https://paritylicense.com) strongly _encourage_ selling exceptions.  licensezero.com makes selling exceptions easy.  Parity expects a single licensor in a unique position to do so.  I'm happy to show the work behind the decision to throw weight behind that business model.

## Copyleft is a network play.

Copyleft encourages release of open software by two key mechanisms:

{: #network-effect}

First, a wealth of existing, compatible copyleft software rewards the choice to build open software in the open with free access to a wealth of other software.  I've called this [copyleft's _network effect_](https://blog.licensezero.com/2018/05/13/commons-club.html#network).  The crux of the effect is the accumulated utility of software available under copyleft terms.

{: #social-proof}

Second, lots of copyleft projects, from lots of different kinds of developers, make others confident releasing their own work likewise.  Let's call this _social proof_.  Socialization depends not on the utility of software released, but the number and diversity of developers who release under copyleft terms, and succeed by it.

Note that I do _not_ mention license enforcement, political propaganda, blockbuster projects, or fear of ostracism by other developers.  Those are at best secondary factors.  In my experience, they're closer to negligible.  Unless things change radically, we shouldn't optimize for them.

## Releases strengthen the copyleft network.

How does selling exceptions contribute to copyleft's leverage on software development decision makers?

{: #builds-network-effect}

All releases of copyleft source code strengthen copyleft's network effect.  From the point of view of other open developers, it doesn't matter if the developer sells exceptions, what price they charge, or on what terms.  That offer simply doesn't matter to those building more open, rather than closed, software.   Only the availability of source code under copyleft terms does.

This is even more true under terms like Parity's, which avoid issues around compatibility _among_ open licenses by allowing release under more permissive terms.  If you use a Parity-licensed library to build an app, you can release the app under Apache or Blue Oak.  You can also license it under Parity.  What you _can't_ do is change the license terms for the Parity code.

{: #builds-social-proof}

Selling exceptions also boosts copyleft social proof.  Individual activists have strong intrinsic motivation to release software under copyleft terms.  That isn't broadly true of business firms.  Every company selling exceptions, and succeeding that way, builds the business case for copyleft.  Success creates case studies that pave the path to copyleft for other managers to follow.  It also redistributes money from those who aren't willing to release their code to those who are.

It's been hard for License Zero to make this case in its early days.  As part of my commitment to License Zero developers, [I guarantee them total control of messaging and relationships with their contributors and users](https://licensezero.com/commitment#relationships).  That means no publicizing each new License Zero project as it launches.  But if License Zero's catalog of projects continues to grow apace, that won't be necessary.  Especially as the parallel network effect from customers being able to buy any number of licenses in a single transaction at once takes hold.

## The network matters more than any project.

So much for the benefits.  What about the costs, and how to weigh them?

On principle, the cost of selling exceptions is the exceptions.  If a project is developed entirely by a single company, or with permissive contributor license agreements for outside work, the primary developer can create closed work around their copyleft release.  If the developer sells exceptions to copyleft to others, those others can do the same.  That means closed software, which we're trying to avoid.

Costs obviously vary by project.  But in general, selling exceptions nets out positive because effects of the network---the wealth, availability, and variety of code available under copyleft terms---outweigh the effect of any single project.  _Any_ single project.  Given the realities of permissive competition and public perception, no single work can ever compare to the attractive power of the network, no matter how much utility it offers.

Consider the original killer apps of free software: Linux and GCC.  Both have studiously maintained permissive safe zones for their key use cases, Linux by [clarifying that using syscalls doesn't trigger copyleft](https://spdx.org/licenses/Linux-syscall-note.html), and GCC by [clarifying that bits of libgcc built into binaries don't trigger copyleft](https://spdx.org/licenses/GCC-exception-2.0.html).  Linux kernel developers don't uniformly share FSF's software-freedom goals.  But the reality of both projects remains that sufficiently strict copyleft would cripple them in competition against permissive rivals.

All things considered, Patrick McHardy was good for BSDs, and the complexity of GPL and the libgcc exception are good for LLVM.  Folks are fond of quoting astronomical figures for the value of time contributed to Linux and GCC.  But competitors don't have to achieve parity with those projects' development history.  They only have to provide a substitute for its output, without the burden of broad-based, collaborative governance among open contributors.

Even when companies do sell exceptions to large projects with high utility, structural factors suppress the broader effect.  Selling exceptions imposes transaction costs.  Buying a license can never be as quick, cheap, or easy as already having one.  If we see the benefits of copyleft release and the costs of exceptions in a contest for cost-benefit, exceptions bear a significant handicap.  One-to-many approaches, like selling an exception to a company that can resell in turn, mitigate, but only mitigate, that inherent disadvantage.

Moreover, there are apparent structural limits on how much utility a project driven by one developer or company can offer.  The banner copyleft projects, including Linux and GCC, are all facilitated by neutral, noncommercial organizations that don't sell exceptions.  The runaway success of those projects, in adoption and contribution, is itself exceptional.  We may never see software projects so broad-based again.  But even at that high end, all the rarefied success stories still face competition, or the credible threat of it.  The most useful projects we know of aren't immune.

In the end, a project, no matter how large, is simply easier to replace than a whole catalog of software, and the perceptions that largesse engenders over the years.  This is as much about people, availability heuristics, business confidence, and politics as technology.  Projects and practices installed in developers' minds are simply harder to replace than project dependencies.

## Handle business failure correctly.

Competition obviously afflicts firms, and not just software projects.  The harsh truth is that the reasonable expectation for any upstart business firm is failure.  Most attempts at selling exceptions will fail, on licensezero.com and elsewhere.  Most companies releasing copyleft software, with or without offering exceptions, or frankly any kind of software, will fail in the business sense.

Business models based on selling exceptions to copyleft software fail correctly.  They fail open.  When the company behind a copyleft project stops leveraging its exclusive rights to build the only available proprietary add-ons, or stops selling exceptions to copyleft, the result, license-wise, is the same as magically replacing the company with a foundation that chooses not to do those things.

It's important not to overstate this case.  Selling exceptions has succeeded, and will succeed again.  It's a viable business plan, and a meaningful business opportunity.  But no opportunity is guaranteed, and the negative externalities, to use an economic term, ought to be minimized.  Failed attempts at selling exceptions don't threaten the copyleft network.

## Fund bounties on new business models.

That isn't to say that the copyleft network is entirely neutral, as would-be exception sellers go.  In fact, the copyleft network itself can occasionally be a source of serious and unexpected competition.  Accepting that risk is part of the dual licensing deal.

Every developer considering selling exceptions faces a basic choice.  There are use cases for their software that they do _not_ want to license.  To avoid handing their competitors leverage, these firms need terms that cover all use cases, except the ones that might compete them to death.

The most straightforward path to these terms is writing a new restricted license that says, in short:

> Everybody can do whatever they want, except compete with us.

Such licenses aren't broadly considered "open" or "free" or "commons".  They don't ingratiate companies to activists or others who identify with unrestricted terms.  To secure that kind of recognition, companies have to settle for copyleft terms.

Strong copyleft terms say:

>  Everybody can do whatever they want, but if that involves making software, that software has to be open, too.

That's never _exactly_ the same as "do what you want, but don't compete with us".  But when your competitors insist on keeping their work closed, the two often overlap tightly.  A license that says "if you build software, release it", given that "if our competitors make software that competes with us, they won't release it", reads pretty close to "don't compete with us".  So firms can often say what they want to say about competition through copyleft.

Historically, the assumption that business competitors will insist on keeping code closed has largely held.  But occasionally, it hasn't.

The copyleft network itself _incentivizes_ business firms to find new business models that abide releasing more software as free software.  In [other writing](https://writing.kemitchell.com/2018/11/04/Copyleft-Bust-Up.html#bounty), I've portrayed the network effect benefit of strong-copyleft software as funding a de facto bug bounty:  Find a loophole in the license, collect first-mover advantage building a closed solution with the benefit of code under that license.  But the same bounty awaits any firm that manages to accept the terms as intended.  Find a way to do business without caring that your code has to be open, and all the same software value unlocks for your firm.

In that sense, every company contributing copyleft code, including those also selling exceptions, fund opposition research against their own business model, and for the expansion of the copyleft network as a whole.  That is a potential long-term cost that every exception selling firm must accept, in exchange for the short-term benefits of being "free" or "open" while still charging for licenses.  The clearest potential for this kind of breakaway gambit is cloud computing.  We have endured a proprietary cloud computing revolution, transitioning now to a kind of open core for services.  Open source database companies, including MongoDB, [which began life as an open source cloud, and pivoted to focus on its database layer](https://www.mongodb.com/press/10gen-announces-company-name-change-mongodb-inc), dare a would-be AWS challenger to go fully open.

Copyleft network effect ensures plenty of incentive to concoct a new, software-freedom-compatible business model.  But at the same time, copyleft social proof conditions the business environment to accept that innovation.  Copyleft terms empower those within organizations who want to open their work to do so.  More organizations releasing code validates the trade-off.  The availability of the free-and-open approach increases in the collective mindset.  New, free-software models seem less crazy all the time.

## Selling exceptions is different.

There are many reasons to promote selling exceptions, dual licensing, [public-private licensing](https://indieopensource.com/public-private)---whatever we choose to call it.  The model offers advantages unmatched by any other approach, especially for small, bootstrapping firms and independent developers.

Add to that long list that selling exceptions, like other copyleft-based models, creates more copyleft software, and strengthens the copyleft network.  The broader the perspective we can take on that network, the less we fixate on particular projects and the narrow, intercompany spats that surround them, the more selling exceptions makes sense.

It's a model of the past, powering many of the earliest meaningful open source business success stories.  It's a model of the present, still in active use across language and industry communities, albeit with much less self-conscious fanfare than "open core", which software freedom advocates have long opposed.  It can and should be a model of the future, if we think that copyleft, and its preference for openness over closed, should have a future, and not as historical curiosity.

I do.