---
title: Selling Exceptions
description:
layout: post
---

There's a take on copyleft that says:

> Copyleft doesn't achieve anything unless it applies to everyone, including the original developer.  If just one company can build proprietary add-ons, or sells exceptions, that's abusing copyleft as a business ploy.

We see the same view reflected in terms, like section 7 of [copyleft-next](https://github.com/copyleft-next/copyleft-next) 0.3.1, a kind of research license looking forward to the next GPL:

> 7\. Nullification of Copyleft/Proprietary Dual Licensing
>
> If I offer to license, for a fee, a Covered Work under terms other than a license that is OSI-Approved or FSF-Free as of the release date of this License or a numbered version of copyleft-next released by the Copyleft-Next Project, then the license I grant You under section 1 is no longer subject to the [copyleft] conditions in sections 3 through 5.

Much the same in the Free Software Foundation's [policy against making exceptions to the GPL](https://www.gnu.org/philosophy/selling-exceptions.en.html) for its own projects.

But not so fast.  Dig around FSF.org long enough, and you'll find that RMS doesn't condemn selling exceptions to copyleft.  He accepts and encourages it.  [Quoting](https://www.gnu.org/philosophy/selling-exceptions.en.html):

> I've considered selling exceptions acceptable since the 1990s, and on occasion I've suggested it to companies.  Sometimes this approach has made it possible for important programs to become free software.

RMS goes on to give the example of Qt's transition from proprietary to reciprocal to GPL licensing, a phenomenon I recently [explored on my personal blog](https://writing.kemitchell.com/2019/04/06/Stairway-to-Heaven.html).  Later in the same piece:

> When I first heard of the practice of selling exceptions, I asked myself whether the practice is ethical.  If someone buys an exception to embed a program in a larger proprietary program, he's doing something wrong (namely, making proprietary software).  Does it follow that the developer that sold the exception is doing something wrong too?
>
> If that implication were valid, it would also apply to releasing the same program under a noncopyleft free software license, such as the X11 license.  That also permits such embedding.  So either we have to conclude that it's wrong to release anything under the X11 license---a conclusion I find unacceptably extreme---or reject the implication. Using a noncopyleft license is weak, and usually an inferior choice, but it's not wrong.

I don't think condemnation of licenses like X11, better known as MIT, unacceptably extreme.  If the point is principle, picking a permissive license when copyleft would do is a clear offense.  Perhaps a venal sin, rather than a mortal one.  But a sin nonetheless.  RMS doesn't show more work, offering any kind of structure or cost-benefit that shows how letting willful permissivity slide nets out positive for software freedom.

License Zero and its [Parity Public License](https://paritylicense.com) strongly _encourage_ selling exceptions.  licensezero.com makes selling exceptions easy.  Parity expects a single licensor in a unique position to do so.

If I don't accept Stallman's justification for selling exceptions, what's my line?

## Copyleft is a network play.

Copyleft encourages release of open software by two key mechanisms:

{: #network-effect}

First, a wealth of existing, compatible copyleft software rewards the choice to release software in the open with free access to a wealth of other software.  I've called this [copyleft's _network effect_](https://blog.licensezero.com/2018/05/13/commons-club.html#network).  The crux of the network effect is the accumulated utility of software available under copyleft terms.

{: #social-proof}

Second, lots of copyleft projects, from lots of different kinds of developers, released in the near and distant past, make others comfortable releasing their own work.  Let's call this _social proof_.  Socialization depends not on the utility of software released, but the number and diversity of developers who release under copyleft terms, and succeed by it.

Note that I do _not_ mention license enforcement, political propaganda, blockbuster projects, or fear of ostracism among developers.  Those are at best secondary factors.  In my experience, they're closer to negligible.

## Releases strengthen the copyleft network.

How does selling exceptions map onto copyleft's key mechanisms?

{: #builds-network-effect}

All releases of copyleft source code strengthen copyleft's network effect.  From the point of view of other open developers, it doesn't matter if the developer sells exceptions, what price they charge, or on what terms.  That deal structure simply doesn't apply to those building more open, rather than closed, software.   Only the availability of source code under copyleft terms matters.

This is even more true under terms like Parity, which avoid issues around compatibility _among_ open licenses by allowing release under more permissive terms.  If you use a Parity-licensed library to build an app, you can release the app under Apache or Blue Oak.  You can also license it under Parity, but that's not your only choice.

{: #builds-social-proof}

Selling exceptions also boosts copyleft social proof.  Individual activists have strong intrinsic motivation to release software under copyleft terms.  That isn't broadly true of business firms.  Every business firm selling exceptions to copyleft, and succeeding that way, builds the missing business case for copyleft.  Success creates case studies that pave the path to copyleft for more managers to follow.  Success means money flowing to those who are willing to release their code, from those who aren't.

It's been hard for License Zero to make this case in its early days.  As part of my commitment to License Zero developers, [I guarantee them total control of messaging and relationships with their contributors and users](https://licensezero.com/commitment#relationships).  That means no publicizing each new License Zero project as it launches all over social media.  But if License Zero's catalog of projects continues to grow apace, that won't be necessary.  Especially as the parallel network effect from customers being able to buy any number of licenses in a single transaction at once takes hold.

## The network matters more than any project.

So much for the benefits.  What about the costs, and how to weigh them?

On principle, the cost of selling exceptions is the exceptions.  If a project is developed entirely by a single company, or with permissive contributor license agreements for outside work, the primary developer can create closed work around their copyleft work.  If the developer sells exceptions to copyleft to others, those others can do the same.  That means closed software, which we're trying to avoid.

Costs obviously vary by project.  But in general, selling exceptions nets out positive because network effects outweigh the effect of any single project.  Any single project.  Given the reality of permissive competition, no single project can ever compare to the attractive power of the network, no matter how much utility it offers.

Consider the original killer apps of free software: Linux and GCC.  Both have veered more permissive, Linux by [clarifying that using syscalls doesn't trigger copyleft](https://spdx.org/licenses/Linux-syscall-note.html), and GCC by [clarifying that bits of libgcc built into binaries don't trigger copyleft](https://spdx.org/licenses/GCC-exception-2.0.html).  Linux kernel developers don't uniformly share FSF's software-freedom goals.  But the reality of both projects remains that sufficiently strict copyleft would cripple them in competition against permissive rivals.  All things considered, Patrick McHardy was good for BSDs, and the complexity of GPL and the libgcc exception are good for LLVM.  Folks are fond of quoting astronomical figures for the value of time contributed to Linux and GCC.  But competitors don't have to achieve parity with those projects' development history.  They only have to provide a substitute for its output.

Even when companies do sell exceptions to large projects with high utility, structural factors suppress the broader effect of that offer.  Selling exceptions imposes transaction costs.  The "Zero" in "License Zero" stands for the goal of reducing those transaction costs to zero.  But actually reaching zero is impossible.  Buying a license can never be as quick, cheap, or easy as already having one.  If we see the benefits of copyleft release and the costs of exceptions in a contest for cost-benefit, exceptions shoulder a significant handicap.

Moreover, there are apparent structural limits on how much utility a project driven by one developer or company can offer.  The cornerstone copyleft projects, including Linux and GCC, are all facilitated by neutral, noncommercial organizations that don't sell exceptions.  The runaway success of those projects, in adoption and contribution, is itself exceptional.  We may never see software projects so broad-based again.  But even at the high end, those rarefied success stories face competition.  In the end, projects are simply easier to replace than networks and the perceptions they engender.

## Handle venture failure correctly.

Speaking of competition, that obviously afflicts firms, and not just software projects.  The harsh truth is that the rational expectation of any upstart business firm is failure.  Most attempts at dual licensing will fail.  Most companies releasing copyleft software, with or without offering exceptions, will fail.

Business models based on selling exceptions to copyleft software fail correctly.  They fail open.  When the company behind a copyleft project stops leveraging its exclusive rights to build the only available proprietary add-ons, or stops selling exceptions to copyleft, the net result, license-wise, is the same as replacing the company with a foundation that refuses to do those things, or converting the project to one with multiple contributors and no CLAs.

## Research bounty for finding out how to do the business open.

...