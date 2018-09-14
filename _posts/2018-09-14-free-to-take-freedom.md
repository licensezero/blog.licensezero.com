---
title: Free to Take Freedom
description: Why can't "free for free software" be free software itself?
layout: post
---

I don't understand the Free Software Foundation's position on software used to make other software.  As far as I can tell, their definition of "free software" precludes licenses that make developer tools free for use for free software only, or "free for open source".

Free-only libraries?  Yes.  Free-only compilers, bundlers, static analysis tools, and deployment utilities?  Apparently no.  And not just strategically undesirable, but philosophically verboten.

I see good reason for specific strategic decisions of the past.  But as a general matter of strategy, this seems a terrible handicap to take.

# Practical Interference

Earlier this week, I ran into [libgcc](https://gcc.gnu.org/onlinedocs/gccint/Libgcc.html), the low-level runtime library for GCC, for the first time in a long time.  When compiling a program, GCC generates calls to libgcc, which the compiled program must link.  GCC links libgcc by default.  The actual content of libgcc depends on the target architecture.  In other words, GCC puts a bit of its own code into the programs it compiles.

What does that have to do with "free for open source"?

The GPL doesn't require you to share source code for programs that you compile with GPL-licensed software.  Broadly speaking, its requirements to share and license your own code apply only when you make changes to GPL code, or build it into your own code, and share the results with someone else.  GPL's requirements don't say anything about running the GPL software, or running it for a particular purpose, like making nonfree software.

If you assumed that a software license _can't_ legally require sharing alike based on how a program is used---I get the feeling FSF [doesn't think this is true](https://www.gnu.org/licenses/agpl-3.0.en.html#section13), but [wishes it were](https://www.gnu.org/philosophy/programs-must-not-limit-freedom-to-run.en.html), about which more later---then GPL's approach would do all that's possible to require sharing and licensing other software as free software.  But it couldn't do anything about compiling nonfree software with a free-software compiler.  If you _wanted_ to require sharing and licensing compiled software as free software, a runtime library like libgcc, which gets combined with code and distributed with it, gives you a _technical_ way around the limitation of the license.

In other words: If you want to require others to make as much software free software as possible, but you _can't_ or won't require them to share just because they compiled with your compiler, though you _can_ require them to share for building your code into theirs, then build a compiler that puts bits of your code into programs it compiles.  You've just worked around the limitation of your license.  Practically speaking, programs compiled with the compiler and shared with others have to be free software.

This is <a id="definition-of-practical-interference">_practical interference_</a>: some fact about software and how we use it gives us the practical power to write effective legal rules we otherwise couldn't.  We'll see practical interference a few more times, shortly.

# Legacy

The FSF stewards GCC, perhaps the most important developer tool in existence.  So does libgcc require developers using GCC to compile programs to make their programs free software?  No, [it does not](https://www.gnu.org/licenses/gcc-exception-3.1-faq.en.html):

> [I]f these libraries [(libgcc)] were simply distributed only under the terms of the GPL, all the object code that GCC produces would have to be distributed under the same terms.  However, the FSF decided long ago to allow developers to use GCC's libraries to compile any program, regardless of its license.

The FSF [created an exception to its most important license, for its most important software](https://www.gnu.org/licenses/gcc-exception.html), specifically to stop it from requiring more software to be free software.

Why?  GCC was the killer app of open software development.  The first.  It carried the flag both for the practice of open, collaborative software development, and for software freedom, as implemented in the first version of the GPL.  It rose to popularity, and proved its first point, in large part by permitting compilation of nonfree programs.  Taking GCC away from the bulk of its user base, due to a technical detail, [would have been jarring](https://www.gnu.org/licenses/gcc-exception-3.1-faq.en.html):

> Developing nonfree software is not good for society, and we have no obligation to make it easier.  We decided to permit this because forbidding it seemed likely to backfire, and because using small libraries to limit the use of GCC seemed like the tail wagging the dog.

There are two distinct rationales here: first that changing the effective license terms for GCC would blow back, in some strategic sense, and second that relatively minor code like libgcc shouldn't affect rules for GCC.

The second doesn't make any sense to me.  The free software movement is and always has been an insurgency.  It self-consciously lacks the financial, political, and other resources of the proprietary establishment.  As such, software freedom activism succeeds by leverage, in the tactical sense: methods to get a lot done for software freedom with relatively few resources.  libgcc is extraordinarily high-leverage.

I suspect the first rationale is the real story, and a near cousin to the FSF's prescriptions [for LGPL](https://www.gnu.org/licenses/why-not-lgpl.html) and [even Apache 2.0](https://www.gnu.org/licenses/license-recommendations.en.html).  It comes down to competition:

> Some libraries implement free standards that are competing against restricted standards, such as Ogg Vorbis (which competes against MP3 audio) and WebM (which competes against MPEG-4 video).  For these projects, widespread use of the code is vital for advancing the cause of free software, and does more good than a copyleft on the project's code would do.
>
> ...
>
> [W]here the library implements an ethically superior standard, here adoption for its own sake will not accomplish any special objective goal, so there's no reason to avoid copyleft entirely.  However, if you require developers who use your library to release their whole programs under copyleft, they'll simply use one of the alternatives available, and that won't advance our cause either.  The Lesser GPL was designed to fill the middle ground between these cases, allowing proprietary software developers to use the covered library, but providing a weak copyleft that gives users freedom regarding the library code itself.

[I've written about competition and the software-freedom network before.](https://blog.licensezero.com/2018/05/13/commons-club.html)  We should expect more of it.  Even for copyleft front-runners like [the kernel](https://en.wikipedia.org/wiki/Google_Fuchsia) and [GCC](https://llvm.org/).

# Prospects

This begins to take us away from the specific, peculiar historic case of GCC, and into the present day.  For today, FSF [recommends AGPL](https://www.gnu.org/licenses/license-recommendations.en.html#server) for anything likely to end up in a service.  That license carries the software freedom torch, requiring more software to be free software than GPL.  There's no software-freedom reason I can see to pick GPL over AGPL, other than that AGPL scares nonfree software companies.

But even AGPL does not make dev tools free for free software only.  If GCC were AGPL-licensed, it would still need technical interference, like GCC, to require compiled programs to be free software.  Why doesn't AGPL go further?

# Freedoms

The FSF's [definition of free software](https://www.gnu.org/philosophy/free-sw.en.html) casts their criteria for free-software licenses in terms of four end-user freedoms to be protected:

> - The freedom to run the program as you wish, for any purpose (freedom 0).
>
> - The freedom to study how the program works, and change it so it does your computing as you wish (freedom 1).
>
> - The freedom to redistribute copies so you can help others (freedom 2).
>
> - The freedom to distribute copies of your modified versions to others (freedom 3).

At the same time, the FSF itself publishes and recommends licenses that impinge on some of these freedoms.  Specifically, GPL's copyleft rules impinge on freedom 2 and freedom 3.  You can't redistribute copies of GPL-licensed code without source code or notice that the GPL applies.  You can't distribute copies of modified versions without applying GPL to your modifications and providing source for them.

The free software definition [explains](https://www.gnu.org/philosophy/free-sw.en.html):

> Certain kinds of rules about the manner of distributing free software are acceptable, when they don't conflict with the central freedoms.  For example, copyleft (very simply stated) is the rule that when redistributing the program, you cannot add restrictions to deny other people the central freedoms.  This rule does not conflict with the central freedoms; rather it protects them.

Copyleft rules, then, are valid rules about exercising freedom 2 (to redistribute) and freedom 3 (to distribute modified copies).  Under GPL, you can only exercise those freedoms if you also follow rules about source code and license terms.

# Crime

In this way, denying others software freedom, by giving them software without source code or a license protecting their freedoms, works a bit like a tort or a crime.  In the United States, we have freedom of speech.  But using our freedom of speech to keep someone confined, incommunicado, against their will, by threats of physical violence, gives them a legal claim against us, and the state a crime to charge.  Laws for those torts and crimes seek to prevent us using our freedom of speech to unjustly take freedom from others.

Other laws prevent us using other freedoms to similar effect.  Generally speaking---there are always exceptions---I cannot legally take your freedom of speech with my right to shoot firearms.  Or to move my body as I please.  Or to express my religious or political beliefs.  The point is the harm, not which legal concepts I exhibit while inflicting it.

That begs the question:  Why does the FSF's definition of copyleft set rules only about exercising freedom 2 (redistribute) and freedom 3 (distribute with changes), but not freedom 0 (run the program) or freedom 1 (change the program)?  In other words, why does the FSF prohibit denying others software freedom only if you happen to do so by distributing copies of software, and allow to do it by turning source code into binary, or making changes to code you keep to yourself?  It's as if FSF prohibits fraud, but only if you speak it, and not if you write it.

# Mandatory Freedom

The GPL, as written, freely allows developers to build GPL code into network services, and provide those services to users, without sharing or licensing their code.  [Section 13 of AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html#section13) adds to GPLv3 a requirement to "offer all users interacting with [modified AGPL software] remotely through a network" source code and an AGPL license.  But it's impossible to trigger section 13's requirement without running the software, and running it in a particular way: to offer a network service to others.  AGPL _has_ a rule about exercising freedom 0, your right to run the program as you wish, for any purpose.  Under AGPL, you may _not_ run the program to provide a modified, nonfree network service.

AGPL section 13 diligently avoids the words "use" and "run" and "execute".  I believe this reflects the view that I first heard from Bruce Perens, that AGPL's authors wanted to synthesize "a public performance right for software".

Copyright law gives copyright owners a list of exclusive rights: things they can sue others for doing without a license.  One of those is public performance.  If I compose a symphony, I can sue orchestras for performing it without a license.  But that exclusive right in the copyright law doesn't apply to software, to cover uses like running web applications for customers or the public at large.  That is what AGPL's authors wanted to regulate, in order to plug the loophole that allows developers to build GPL software into network applications, and avoid the requirement to make the applications free software, by never distributing them to others.

AGPL is a copyright license that sets rules for publicly performing software in this sense.  But copyright doesn't give licenses control over publicly performing software.  So how does AGPL work, legally?  The answer: [practical interference](#definition-of-practical-interference) once again.

In much the same way that the combination of GCC and libgcc managed to create "free for open source" rules, by leveraging a _practical_ fact about how we use software to bring use under the copyleft requirements of its GPL license, AGPL depends on the fact that to run software, we inevitably make copies of it.  Copyright law _does_ give licenses the power to set rules for reproduction---making copies of software---and preparation of derivative works---making changes and building into other software.  AGPL section 13 requires preparing a derivative work explicitly: you only trigger its requirements if you "modify the Program".  But in order to run that modified program for others to interact with over a network, you're going to have to make a copy at least once, and probably many times.  Copyright licenses can set rules about copying.

Long story short, legally, AGPL section 13 is, among other things, a rule about making copies.  In particular, it's a rule about making copies _for the purpose of running the program to provide a network service to others_, in exercise of freedom 0, the freedom to run the program.  "The freedom to publicly perform the program" isn't in the copyright law, and it isn't one of the four freedoms, either.  It's part of freedom 0, which includes the freedom to run the program for other people.

This particular exercise of freedom 0 can feel a bit like "distribution", but only in a far broader sense than freedom 2 (redistribution) and freedom 3 (distribute with changes) entail.  The _consequence_ of exercising freedom 0 to provide a modified AGPL network service is that you have to offer to exercise freedom 3 to distribute copies of your modified version.  One consequence of section 1(c) of [OSL 3.0](https://opensource.org/licenses/OSL-3.0), which doesn't require modification, and which FSF also [approves as a free software license](https://www.gnu.org/licenses/license-list.en.html#OSL), can be that you have to exercise freedom 2 to redistribute copies of even unmodified OSL software.  These rules don't regulate exercise of freedom 2 and 3.  They force you to exercise freedom 2 and 3 when you otherwise have not, and might not.

# Extra Freedom

There aren't actually four freedoms.  There are at least five.  The fifth, unenumerated freedom, also in [the definition](https://www.gnu.org/philosophy/free-sw.en.html), is _private changes_:

> You should also have the freedom to make modifications and use them privately in your own work or play, without even mentioning that they exist. If you do publish your changes, you should not be required to notify anyone in particular, or in any particular way.

In other words, software freedom _also_ means the freedom to exercise freedom 1 (make changes) and to choose _not_ to exercise freedom 3 (distribute changes).  The FSF's rejection of [RPL](https://www.gnu.org/licenses/license-list.en.html#RPL) corroborates:

> The Reciprocal Public License is a nonfree license because of three problems. ... 3. It requires publication of any modified version that an organization uses, even privately.

But we've just seen freedom 1 linked freedom 3 together, in two FSF-approved licenses.  When you modify an AGPL program (freedom 1) and run it to provide a network service, AGPL section 13 _requires_ you to distribute source code (freedom 3).  That is, AGPL specifically requires you to share changes you might like to keep private.  Its language takes pains to avoid the word "use", but the word "modify" is right in the text.

Legally, copyright law includes an exclusive right to prepare derivative works, such as by making changes or building into other software.  So AGPL didn't _need_ to require exercise of both freedom 0---running the program, implicating reproduction by practical interference---and freedom 1---making changes, implicating production of derivative works---to trigger the requirement to offer freedom.  In fact, AGPL could have accomplished its goal of closing the software-service loophole by triggering on modification, or preparation of derivative works, alone.

That is _exactly_ the approach of RPL, published for a JavaScript web application framework behind the service barrier, six years before AGPL.  The only implementation puzzle is who to offer source code to.  RPL required those making changes to send them back to the original developer, a very [popular](https://blog.licensezero.com/2018/01/25/imaginary-licenses.html) [reason](https://writing.kemitchell.com/2018/08/28/Unhappy-Coincidences.html#software-freedom-doesnt-mean-patches-back) to repurpose FSF licenses, and to which the FSF objected.  But we could sketch a variation that avoids that problem:

> If you prepare a derivative work of this software, offer complete source code and a license on these terms to every user of your work, free of charge, and provide them promptly, on request.

This rule shifts the focus from the user who made the change and ran the service to the end-user.  Under this rule, it doesn't matter how users become users.  Every user gets a path to software freedom.  Exactly in line with the free software definition.

Would the FSF approve a license with that rule as a free software license?  How about a license that requires proactive _publication_ of changes, rather than offer, request, and delivery on an individual-user basis?  Frankly, I have no idea.  We've explored some relationships between the freedoms with approved licenses.  But the rationales for the distinctions I've pointed out haven't been pronounced in any writing I have seen.

# Extra Law

If this seems complicated, if writing rules in copyright or software-freedom language seems too delicate, I'm with you.  If we want a license that says "free for free software" or "free for open source", can't we just write that, and explain what it means?

In my opinion, yes.  Practically, we can.

US copyright law has a few provisions peculiar to software.  But copyright is a general framework.  Software licenses run on the same basic legal "operating system" of copyright law as music licenses, film licenses, book licenses, and, yes, nonfree proprietary software licenses.  Inability to learn from one's peers, and especially one's competitors, is a terrible handicap, especially if they learn readily from you.

We can start a bit closer to home.  [Creative Commons](https://creativecommons.org) publishes professionally drafted public copyright licenses for creative works.  One of their licenses is CC-BY-NC, which allows use for noncommercial purposes only.  Here's the relevant text from the ["legal code"](https://creativecommons.org/licenses/by-nc/4.0/legalcode):

> a. License grant.
>
> 1. Subject to the terms and conditions of this Public License, the Licensor hereby grants You a ... license ... to:
>
> A. reproduce and Share the Licensed Material, in whole or in part, for NonCommercial purposes only; and
>
> B. produce, reproduce, and Share Adapted Material for NonCommercial purposes only.
>
> ...
>
> i. NonCommercial means not primarily intended for or directed towards commercial advantage or monetary compensation. ...
>
> j. Share means to provide material to the public by any means or process that requires permission under the Licensed Rights, such as reproduction, public display, public performance, distribution, ... and to make material available to the public including in ways that members of the public may access the material from a place and at a time individually chosen by them.

If you think that's straightforward, search online for "software trial license".  Proprietary software licenses frequently restrict use with mere clauses:

> ...for Licensee's internal business purposes only...
>
> ...for nonproduction, evaluation purposes only...

This is [practical interference](#definition-of-practical-interference) in action, as a tool of licensing, rather than a side effect to be avoided.  Which exclusive rights of copyright holders to these restrictions relate to?  Whichever one the copyright owner giving the license manages to show the user exercised, when enforcing their license terms.  Perhaps reproduction, or preparing a derivative work, or distributing to the public.  You can't practically work with software without exercising at least one of those exclusive rights.  Exercising any single one without permission is copyright infringement.

I'm reminded of a sign over my grandparents' garage, in rural Rising Star, Texas:

        THIS GARAGE
     GUARDED BY SHOTGUN
     FOUR DAYS PER WEEK

    YOU GUESS WHICH ONES

There's no legal rule that says the copyright holder has to spell out exactly how they'll enforce their terms.  The license can leave some of that uncertainty with the user.  Professionally drafted license terms do this all the time.

Of course, there is no perfect certainty in the law.  The difference between owning and licensing a copy under 17 U.S.C. § 117.  The difference between [granting a license on its own](https://lwn.net/Articles/61292/), or through a contract.  [Whether that's even a practical difference](https://en.wikipedia.org/wiki/Jacobsen_v._Katzer).  [Vernor v. Autodesk](https://en.wikipedia.org/wiki/Vernor_v._Autodesk,_Inc.) and the [MAI](https://en.wikipedia.org/wiki/MAI_Systems_Corp._v._Peak_Computer,_Inc.) trio.  Specialist opinions differ.  The leading copyright treatise sets impartiality aside, and includes a full brief on the matter, against the grain of recent court decisions.

Meanwhile, millions, maybe billions of dollars in software license fees course through the economy under terms leveraging practical interference.  Licensees aren't keen to finance the public good of legal clarity on underlying doctrinal issues, by fighting them out in the courts at great private expense.  Trend and policy favor copyright holders, and protection for their power to control use of their works.  The power to keep copies from reaching a user to begin with remains unquestioned, and that is a greater power than prohibiting specific kinds of use.  The path of clean-room reimplementation stands open to those who want a way around licensors with whom they can't or won't deal, as a kind of policy relief valve, dissipating pressure to reform copyright so as to avoid granting monopolies on ideas, rather than specific code.

All of those trends sound terrible if you think all software ought to be in the public domain.  But software in the copyright public domain can't use copyright to effect change in the other dimensions that matter for software freedom: source availability, attribution, patent encumbrance, and so on.  To function, copyleft needs copyright, and in many cases, software freedom needs copyleft.  The stronger copyright is, the stronger copyleft can be.  Copyleft is strong, and getting stronger, while software freedom flags.

# Compromise

Perhaps what I'm missing here is a more complete map of the relationships between freedoms, as the FSF sees them.  With freedoms, there are always exceptions, always balances to be struck.  Sometimes one freedom yields to another, as of a higher priority, in particular circumstances.  We can feel our way around that territory, based on what the FSF has written, and what it has approved.  I don't think the FSF has published a map.

But on the subject of how permissive copyleft licenses should be, the long thread I see running through the FSF's writing isn't principle, but pragmatism.  The watchword here is "strategy".  The FSF has compromised when it feared loss of popularity and attention, the only effective platform from which it can speak loudly through all the noise online.  So it publishes more permissive software than it might, and takes every change to talk free as in freedom over free as in beer.

# Coalition

Free software isn't a meaningful coalition without proprietary-software allies, and the allies software freedom believes it has in proprietary users of GPL programs and LGPL libraries seem far more concrete than the allies it might gain with "radical" dev tools copyleft licenses and projects suffused with uncompromising spirit.  This is loss aversion at work in free software politics, both symptom and partial cause of [a fatal tendency to look back, instead of forward](https://blog.licensezero.com/2018/05/13/commons-club.html#past).

It is not inevitable.  There is another theory of coalition in free software, also proved in its history.  Small businesses need license terms that demand something back from established, proprietary industry players, to force a bargain for financial life support.  In current parlance, this is a subproblem of ["sustainability"](https://blog.licensezero.com/2018/06/14/profit-sustainability.html).  Many companies have used GPL, and now AGPL, to [solve this problem with dual-licensing plays](https://blog.licensezero.com/2018/09/08/ramji-dual-licensing.html), not because their business plans supported software freedom, but because software-freedom licenses supported their business plans.  Copyleft network power, and its power to protect software freedom, grew all the same.

That is exactly why [Parity](https://licensezero.com/licenses/parity), the strong-copyleft, "free for open source" dev tools license for License Zero, [excites me so much](https://blog.licensezero.com/2017/09/15/hacker-public-license.html).  I believe in both movements: the movement for software freedom, as I understand it, and the movement to establish financially rational models of open source production for small businesses and independent developers.  In the culture, those lines have drifted apart.  On paper, that their licensing requirements should overlap seems mere coincidence, a fluke.  But we've seen that fluke over and over again.  When I look at the people and companies that would use radical copyleft licenses to turn open development into a gainful line of work, I see many hackers who, like myself, came up on copyleft software, and believed in software freedom, but lost touch as they came into the industry during an era of compromise and concession to popularity.

From one point of view, these lost comrades' business plans are heresy.  They pick licenses that protect software freedom, and sell the right to deny software freedom to others to big, proprietary software companies, for cash.  But the alternatives are giving proprietary software companies the right to deny freedom to others _without_ supporting free software advocates, or not making those tools free software.  Every piece of strong-copyleft code released advantages free software developers, and free software companies, willing to meet its conditions.  Redistributing coin from those who support free software only as an input to nonfree software, to those who would make only free software if they could, bodes well for software freedom.

I can write the license that drives that redistribution.  But I don't know how to write that license as a free software license the FSF would approve.  If you think you can, drop me a line.
