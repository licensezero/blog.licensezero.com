---
title: The Case for Selling Exceptions
description: a model for copyleft, in more ways than one
author: K.E. Mitchell
layout: post
---

There's a view of copyleft that says:

> Copyleft doesn't achieve anything unless it applies to everyone, including the original developer.  If only one company can build proprietary add-ons, or sells exceptions, that's abusing copyleft as a business ploy.

We see the same view reflected in terms, like section 7 of [copyleft-next](https://github.com/copyleft-next/copyleft-next) 0.3.1, a kind of research license looking forward to the next GPL:

> 7\. Nullification of Copyleft/Proprietary Dual Licensing
>
> If I offer to license, for a fee, a Covered Work under terms other than a license that is OSI-Approved or FSF-Free as of the release date of this License or a numbered version of copyleft-next released by the Copyleft-Next Project, then the license I grant You under section 1 is no longer subject to the [copyleft] conditions in sections 3 through 5.

We could glean more of the same from the Free Software Foundation's [policy against granting one-off exceptions to the GPL](https://www.gnu.org/philosophy/selling-exceptions.en.html) for its own projects.

But not so fast.  Dig around [FSF.org](https://fsf.org) long enough, and you'll find that RMS doesn't condemn selling exceptions to copyleft.  He accepts and encourages it.  [Quoting](https://www.gnu.org/philosophy/selling-exceptions.en.html):

> I've considered selling exceptions acceptable since the 1990s, and on occasion I've suggested it to companies.  Sometimes this approach has made it possible for important programs to become free software.

He goes on to give the example of Qt's transition from proprietary to reciprocal to GPL licensing, a phenomenon I recently [explored on my personal blog](https://writing.kemitchell.com/2019/04/06/Stairway-to-Heaven.html).  Then, later in the same piece:

> When I first heard of the practice of selling exceptions, I asked myself whether the practice is ethical.  If someone buys an exception to embed a program in a larger proprietary program, he's doing something wrong (namely, making proprietary software).  Does it follow that the developer that sold the exception is doing something wrong too?
>
> If that implication were valid, it would also apply to releasing the same program under a noncopyleft free software license, such as the X11 license.  That also permits such embedding.  So either we have to conclude that it's wrong to release anything under the X11 license---a conclusion I find unacceptably extreme---or reject the implication. Using a noncopyleft license is weak, and usually an inferior choice, but it's not wrong.

I don't think condemnation of licenses like X11, better known as MIT, unacceptably extreme.  If the point is one of principle, picking a permissive license when copyleft would do is a straightforward offense.  Perhaps a venal sin, rather than a mortal one, but a sin all the same.  RMS doesn't show any more work, offering a structure for cost-benefit analysis to show that letting willful permissivity slide nets out well for software freedom.  We have only the conclusion and a general outline.

As for me and my house, [License Zero](https://licensezero.com) and its [Parity Public License](https://paritylicense.com) strongly encourage selling exceptions.  [licensezero.com](https://licensezero.com) makes buying and selling exceptions easy.  Parity expects a single licensor in a unique position to sell those exceptions.

I'm happy to show the work behind the decision to educate and systematize that particular model, of all those I've explored.

## Copyleft is a network play.

Copyleft encourages release of software into the open by two key mechanisms:

{: #network-effect}

First, a wealth of existing copyleft software rewards the choice to build open software in the open with free access to a wealth of other software.  I've called this [copyleft's _network effect_](https://blog.licensezero.com/2018/05/13/commons-club.html#network).  The crux of the effect is the accumulated utility of software available, for free, under compatible copyleft terms.

{: #social-proof}

Second, lots of copyleft projects, from lots of different kinds of developers, make others confident in releasing their own work likewise.  Let's call this _social proof_.  Socialization depends not on the utility of the software released, but the number and diversity of developers who release under copyleft terms and succeed by it.

Note that I do _not_ mention license enforcement, political propaganda, blockbuster projects, or fear of ostracism by other developers.  Those are at best secondary factors.  In my experience, they're closer to negligible.  Unless things change radically, we shouldn't optimize for them.

## Releases strengthen the copyleft network.

How does selling exceptions contribute to copyleft's leverage on software development decision makers?

{: #builds-network-effect}

Every earnest release of copyleft source code strengthens copyleft's network effect.  From the point of view of other open developers, it doesn't matter if the developer sells exceptions, what price they charge, or on what terms.  That offer simply doesn't matter to those building more open, rather than closed, software.   Only the availability of source code under copyleft terms does.

This is even more true under terms like [Parity's](https://paritylicense.com), which avoid issues around compatibility _among_ open licenses by allowing release under more permissive terms.  If you use a Parity-licensed library to build an app, you can release the app under Apache or Blue Oak.  You can also license it under Parity.  What you _can't_ do is change the license for the Parity code from Parity to something else.

{: #builds-social-proof}

Selling exceptions also builds copyleft social proof.  Individual activists have strong intrinsic motivation to release software under copyleft terms.  That isn't broadly true of business firms.  Every company selling exceptions, and making money that way, builds the business case for copyleft.  Success creates case studies that pave the path to copyleft for other managers.  Fees for exceptions redistribute money from those who aren't willing to release their code to those who are.

It's been hard for License Zero to make this point in its early days.  As part of my commitment to License Zero developers, [I guarantee them total control of messaging and relationships with their contributors and users](https://licensezero.com/commitment#relationships).  That means no publicizing each new License Zero project as it launches.  But if License Zero's catalog of projects continues to grow apace, that won't be necessary.  Especially as the parallel network effect from customers being able to buy any number of licenses in a single transaction at once takes hold.

## The network matters more than any project.

So much for the benefits.  What about the costs, and how to weigh them?

If the point is more open, rather than closed, software, the cost of selling exceptions is the exceptions.  If a project is developed entirely by a single company, with permissive contributor license agreements from outsiders, the primary developer can create closed work based on their copyleft release.  If the developer sells exceptions to copyleft to others, those others can do the same.  That means closed software, which we're trying to avoid.

Costs obviously vary by project.  But in general, selling exceptions nets out positive because effects of the network---the wealth, availability, and variety of code under copyleft terms---outweigh the effects via any single project.  _Any_ single project.  Given the realities of permissive competition and public perception, no single work can ever compare to the attractive power of a broader catalog, no matter how much utility it offers, or how fundamental it seems.

Consider the original killer apps of free software: Linux and GCC.  Both have studiously maintained permissive safe zones for their most common use cases, Linux by [clarifying that using syscalls doesn't trigger copyleft](https://spdx.org/licenses/Linux-syscall-note.html), and GCC by [clarifying that bits of libgcc built into binaries don't trigger copyleft](https://spdx.org/licenses/GCC-exception-2.0.html).  Linux kernel developers don't uniformly share FSF's software-freedom goals.  But the reality of both projects remains that sufficiently strict copyleft would cripple them in competition against permissive rivals.  All things considered, Patrick McHardy is a competitive boon for BSDs, and the complexity of GPL plus libgcc exception is a boon for LLVM.

Folks are fond of quoting astronomical figures for the value of time contributed to Linux and GCC.  But competitors don't have to reenact those projects' long development histories.  They need only provide a substitute for their outputs.  And that without the burden of broad-based, collaborative governance among open contributors.

Even when companies do sell exceptions to large, high-value projects, structural factors suppress the broader impact.  Selling exceptions imposes transaction costs.  Buying a license can never be as quick, cheap, or easy as already having one.  If we see the benefits of copyleft release and the costs of exceptions in a contest for cost-benefit, exceptions bear a significant handicap.  One-to-many approaches, like selling an exception to a company that can resell in turn, mitigate, but only mitigate, that inherent disadvantage.

Moreover, there are apparent structural limits on how much utility a project driven by one developer or company can offer.  The banner "community" copyleft projects are all facilitated by apparnetly neutral foundations that don't sell exceptions.  The runaway success of those projects, in adoption and contribution, is itself exceptional.  We may never see software projects so broad-based again.  But even at that high end, all the rarefied success stories still face competition, or the credible threat of it.  The most useful projects we know of aren't immune.

In the end, a project, no matter how large, is simply easier to replace than a whole catalog of software and the perceptions that largesse conditions in developers, managers, and other decision makers over the years.  This is as much about people, availability heuristics, business confidence, and politics as technology.  Projects and practices installed in developers' minds simply can't be hot-swapped in a few weeks, like their projects' dependencies.

## Handle business failure correctly.

Competition afflicts firms, and not just software projects.  The harsh truth is that the only reasonable expectation of any new upstart business firm is failure.  Most attempts at selling exceptions will fail monetarily, on licensezero.com and elsewhere.  Most companies releasing copyleft software, with or without offering exceptions, or frankly any kind of software, will fail in the business sense.

From the copyleft point of view, the business model of selling exceptions fails in the right way.  It fails open.  When the company behind a copyleft project stops leveraging its exclusive rights to build proprietary add-ons, or stops selling exceptions to copyleft, the likeliest result, license-wise, is the same as magically replacing the company with a foundation that chooses not to do those things, or throwing all the contributor license agreements in a fire and locking the combined work into copyleft for all.

It's important not to overstate this case.  Selling exceptions has succeeded, and will succeed again.  It's a viable business plan, and a meaningful business opportunity.  But no opportunity is guaranteed, and the negative externalities, to use an economic term, ought to be minimized.  Fortunately, failed attempts at selling exceptions don't threaten the copyleft network.  The copyleft side of selling exceptions, and the way copyleft licenses work, prevent it.

## Fund bounties on new business models.

That isn't to say that the copyleft network is entirely neutral, as would-be exception sellers go.  In fact, the copyleft network itself can occasionally be a source of serious and unexpected competition.  Accepting that risk is part of the dual licensing deal.

Every developer considering selling exceptions faces a basic choice.  There are use cases for their software that they do not want to license.  To avoid handing their competitors leverage, these firms need terms that cover all use cases, except the ones that involve competing with them.

The most straightforward approach is writing a new restricted license, specific to the firm, that says, in short:

> Everybody can do whatever they want, except compete with us.

Or:

> Everybody can do whatever they want, except X.

Where X is whatever would compete with them.

Such licenses aren't broadly considered "open" or "free" or "commons".  They don't ingratiate companies to activists or others who identify with unrestricted terms.  To secure that kind of recognition, companies have to use strong copyleft.

Strong copyleft terms say:

>  Everybody can do whatever they want, but if that involves making software, that software has to be open, too.

That's never _exactly_ the same as "do what you want, but don't compete with us".  But when your competitors insist on keeping their work closed, the two often coincide.  A license that says "if you build software, release it", given that "if our competitors make software that competes with us, they won't release it", reads pretty close to "don't compete with us" in practice.  So firms can often say what they want to say about competition _through_ copyleft, or in copyleft terms.

Historically, the assumption that business competitors will insist on keeping code closed has largely held.  That has been the greatest failure of copyleft, in activist terms.  But occasionally, a new business model has broken through.

The copyleft network itself _incentivizes_ entrepreneurs to find new business models that abide releasing more software as free software.  In [other writing](https://writing.kemitchell.com/2018/11/04/Copyleft-Bust-Up.html#bounty), I've portrayed the network effect benefit of strong-copyleft software as funding a de facto bug bounty:  Find a loophole in a copyleft license, collect first-mover advantage building a closed solution with the benefit of code under that copyleft license.  But the same bounty awaits any firm that manages to accept the copyleft terms as intended.  Find a way to do business without caring that your code has to be open, and all the same software value unlocks for your firm, and with a great deal more goodwill, besides.

In that sense, every company contributing copyleft code and selling exceptions indirectly funds opposition research against the very assumption underlying their business model.  That is a risk that every exception selling firm must accept, in exchange for the benefits of being "free" or "open" while still charging for licenses.  The gambit is that the firm will establish itself on firmer footing, such that it no longer need rely on copyleft to keep competitors at bay, before the new business model gets identified and operationalized.

At the same time, copyleft social proof conditions the business environment to accept that innovation.  Copyleft terms empower those within organizations who want to open their work to do so.  More organizations releasing code validates the trade-off.  The availability of the free-and-open approach increases in the collective mindset.  New, free-software models seem less crazy all the time.

The clearest potential for the next breakaway business move is cloud computing.  We have endured a proprietary cloud computing revolution.  Now it's evolving to a service variant of Open Core.  Big cloud vendors sell wrapped versions of popular open source service components.

Open source database companies, including MongoDB, [which began life as an open source cloud, and pivoted to focus on its database layer](https://www.mongodb.com/press/10gen-announces-company-name-change-mongodb-inc), dare a challenger for AWS's throne to go fully open.  Open Core companies who withhold valuable add-ons as proprietary software or features exclusive to their services, like Elastic, do not.  Another reason for proponents of selling exceptions to reject open core, as RMS [condemned "proprietary extensions or proprietary versions of a free program"](https://www.fsf.org/blogs/rms/selling-exceptions).

## Selling exceptions is different.

There are many reasons to promote selling exceptions, dual licensing, [public-private licensing](https://indieopensource.com/public-private)---whatever we choose to call it.  The model offers advantages unmatched by any other approach, especially for small, bootstrapping firms and independent developers.

Add to that list that selling exceptions, like other copyleft-based models, creates more copyleft software, strengthens copyleft network effects, socializes business comfort with open terms, and incentivizes practical research in new copyleft-compatible business models.  The broader the perspective we can take on that network, and the less we fixate on particular projects and the narrow, intercompany spats that surround them, the more selling exceptions makes sense, strategically.  _By definition_, selling exceptions is a tactical concession.  Nonfree software will be built with free software.  But strategically, we're glad to accept small steps back for one project, in exchange for giant leaps forward, overall.

Selling exceptions is a model of the past, which powered many of the earliest open source business breakaways.  It's a model of the present, in active use across language and industry communities.  It can and should be a model of the future, if we think that copyleft, and its preference for openness over closed, should have a future, too.

I do.
