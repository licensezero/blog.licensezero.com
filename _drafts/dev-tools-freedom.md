---
title: Free to Take Freedom
description: Why can't "free for free software" be free software itself?
layout: post
---

I don't understand the Free Software Foundation's position on software used to make other software.  As far as I can tell, their definition of "free software" precludes licenses that make developer tools free for use for free software only, or "free for open source".

Free-only libraries?  Yes.  Free-only compilers, bundlers, static analysis tools, and deployment utilities?  Apparently no.  And not just strategically undesirable, but philosophically impermissible.

I see good reason for specific strategic decisions of the past, in context.  But as a general matter of strategy, this seems a terrible handicap to take.

# Practical Interference

Earlier this week, I ran into [libgcc](https://gcc.gnu.org/onlinedocs/gccint/Libgcc.html), the low-level runtime library for GCC, for the first time in a long time.  When compiling a program, GCC generates calls to libgcc symbols, which the compiled program must link.  GCC links libgcc by default.  The actual content of libgcc depends on the target architecture.  But in general: GCC puts a bit of its own code into the programs it compiles.

What does that have to do with licensing?

The GPL doesn't require you to share source code for programs that you compile with GPL-licensed software.  Broadly speaking, its requirements to share and license your own code apply only when you make changes to GPL code, or build it into your own code, and share the results with someone else.  GPL's requirements don't say anything about running the GPL software, or running it for a particular purpose, like making nonfree software.

If you assumed that a software license _can't_ legally require sharing alike based on how a program is used---I get the feeling FSF [doesn't think this is true](https://www.gnu.org/licenses/agpl-3.0.en.html#section13), but [wishes it were](https://www.gnu.org/philosophy/programs-must-not-limit-freedom-to-run.en.html), about which more later---then GPL's approach would do all that's possible to require sharing and licensing other software as free software.  But it couldn't do anything about compiling nonfree software with a free-software compiler.  If you _wanted_ to require sharing and licensing compiled software as free software, a runtime library like libcc, which gets combined with compiled and distributed with it, gives you a _technical_ way around the limitation of the license.

In other words: If you want to require others to make as much software free software as possible, but you _can't_ require them to share just because they compiled with your compiler, though you _can_ require them to share for building your code into theirs, then build a compiler that puts bits of your code into programs it compiles.  You've just worked around the limitation of your license.  Practically speaking, programs compiled with the compiler and shared with others have to be free software.

Let's call this phenomenon <a id="definition-of-practical-interference">_practical interference_</a>: when some fact about software and how we use it gives us the practical power to write effective legal rules for it.  We'll see it again shortly.

# Legacy

The FSF stewards GCC, perhaps the most important developer tool in existence.  So does libgcc require developers using GCC to compile programs to make their programs free software?  No, [it does not](https://www.gnu.org/licenses/gcc-exception-3.1-faq.en.html):

> [I]f these libraries [(libgcc)] were simply distributed only under the terms of the GPL, all the object code that GCC produces would have to be distributed under the same terms.  However, the FSF decided long ago to allow developers to use GCC's libraries to compile any program, regardless of its license.

The FSF [created an exception to its most important license, for its most important software](https://www.gnu.org/licenses/gcc-exception.html), specifically to stop it from requiring more software to be free software.

Why?  GCC was the killer app of open software development.  The first.  It carried the flag both for the practice of open, collaborative software development, and for software freedom, as implemented in the first version of the GPL.  It rose to popularity, and proved its first point, in large part by permitting compilation of nonfree programs.  Taking GCC away from the bulk of its user base, due to a technical detail, [would have been jarring](https://www.gnu.org/licenses/gcc-exception-3.1-faq.en.html):

> Developing nonfree software is not good for society, and we have no obligation to make it easier.  We decided to permit this because forbidding it seemed likely to backfire, and because using small libraries to limit the use of GCC seemed like the tail wagging the dog.

There are two distinct rationales here: first that changing the effective license terms for GCC would backfire, in some strategic sense, and second that relatively minor code like libgcc shouldn't affect the terms for GCC.

The second doesn't make any sense to me.  The free software movement is and always has been an insurgency.  It self-consciously lacks the financial, political, and other resources of the proprietary establishment.  It needs leverage, in the tactical sense: methods to get a lot done for software freedom with relatively few resources.  libgcc is extraordinarily high-leverage.

I suspect the first rationale is the real story, and a near cousin to its arguments [for LGPL](https://www.gnu.org/licenses/why-not-lgpl.html) and [even for Apache 2.0](https://www.gnu.org/licenses/license-recommendations.en.html).  It comes down to competition:

> Some libraries implement free standards that are competing against restricted standards, such as Ogg Vorbis (which competes against MP3 audio) and WebM (which competes against MPEG-4 video).  For these projects, widespread use of the code is vital for advancing the cause of free software, and does more good than a copyleft on the project's code would do.
>
> ...
>
> [W]here the library implements an ethically superior standard, here adoption for its own sake will not accomplish any special objective goal, so there's no reason to avoid copyleft entirely.  However, if you require developers who use your library to release their whole programs under copyleft, they'll simply use one of the alternatives available, and that won't advance our cause either.  The Lesser GPL was designed to fill the middle ground between these cases, allowing proprietary software developers to use the covered library, but providing a weak copyleft that gives users freedom regarding the library code itself.

[I've written about competition and the software-freedom network before.](https://blog.licensezero.com/2018/05/13/commons-club.html)

# Prospects

This begins to take us away from the specific, peculiar historic case of GCC, and into the present day.  For today, FSF [recommends AGPL](https://www.gnu.org/licenses/license-recommendations.en.html#server) for anything likely to end up in a service.  That license carries the software freedom torch, requiring more software to be free software than GPL.  There's no software-freedom reason I can see to pick GPL over AGPL, other than that AGPL scares nonfree software companies.  Like the FSF generally.

But even AGPL does not make dev tools free for free software only.  If GCC were AGPL-licensed, it would still need technical interference, like GCC, to require compiled programs to be free software.  Why doesn't AGPL go further?

# Freedoms

The FSF's [definition of free software](https://www.gnu.org/philosophy/free-sw.en.html) defines their criteria for free-software licenses in terms of four end-user freedoms to be protected:

> - The freedom to run the program as you wish, for any purpose (freedom 0).
>
> - The freedom to study how the program works, and change it so it does your computing as you wish (freedom 1).
>
> - The freedom to redistribute copies so you can help others (freedom 2).
>
> - The freedom to distribute copies of your modified versions to others (freedom 3).

At the same time, the FSF itself publishes and recommends licenses that impinge on some of these freedoms.  Specifically, GPL's sharing rules impinge on freedom 2 and freedom 3.  You can't redistribute copies of GPL-licensed code without source code or notice that the GPL applies.  You can't distribute copies of modified versions without applying GPL to your modifications and providing source for them.

The free software definition [explains](https://www.gnu.org/philosophy/free-sw.en.html):

> Certain kinds of rules about the manner of distributing free software are acceptable, when they don't conflict with the central freedoms. For example, copyleft (very simply stated) is the rule that when redistributing the program, you cannot add restrictions to deny other people the central freedoms. This rule does not conflict with the central freedoms; rather it protects them.

Copyleft rules, then, are valid rules about exercising freedom 2 (to redistribute) and freedom 3 (to distribute modified copies).  Under GPL, you can only exercise those freedoms if you also follow rules about source code and license terms.

# Crime

In this way, denying others software freedom works a bit like a tort or a crime.  In the United States, we have the freedom to speak.  But using our freedom of speech to keep someone confined, incommunicado, against their will, by threats of physical violence, gives them a legal claim against us, and the state a crime to charge.  Laws for those torts and crimes seek to prevent us using our freedom of speech to unjustly take freedom from others.

Various laws prevent us using different freedoms to deny freedom of speech others, too.  Generally speaking---there are always exceptions---I cannot legally take your freedom of speech with my right to shoot firearms.  Or to move my body as I please.  Or to express my religious or political beliefs.  The purpose, or policy, is to protect your freedom of speech.  No matter which freedom of mine I exercise to do so, the harm to you is the same.

That begs the question:  Why doesn't the FSF's definition of copyleft set rules about exercising freedom 0 (run the program) and freedom 1 (change the program), but only about freedom 2 (redistribute) and freedom 3 (distribute with changes)?  Why does FSF prohibit denying others software freedom only if you happen to do so by distributing copies of software, and take pains to allow it if you do so by compiling a program, or making changes to code you keep to yourself?  It's as if FSF prohibited fraud, but only if you speak it, and not if you write it.

# Mandatory Freedom

[Section 13 of AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html#section13) adds to GPLv3 a requirement to "offer all users interacting with [modified AGPL software] remotely through a network" source code and an AGPL license.  But it's impossible to trigger section 13's requirement without running the software, and running it in a particular way: to offer a network service to others.  AGPL _has_ a rule about exercising freedom 0, your right to run the program as you wish, for any purpose.  Under AGPL, you may _not_ run the program to provide a modified, nonfree network service.

AGPL section 13 diligently avoids the words "use" or "run" or "execute".  I believe this reflects the view that I first heard from Bruce Perens, that AGPL's authors wanted to synthesize "a public performance right for software".

Copyright law gives copyright owners a list of exclusive rights: things they can sue others for doing without a license.  One of those is public performance.  If I compose a symphony, I can sue orchestras for performing it without a license.  But that exclusive right in the copyright law doesn't apply to software, to cover uses like running a web application for customers or the public at large.  That is what AGPL's authors wanted to regulate, in order to plug the loophole that allows developers to build GPL software into network applications, and avoid the requirement to make the applications free software, by never distributing them to others.

AGPL is a copyright license that sets rules for publicly performing software in this sense.  But copyright doesn't give licenses control over publicly performing software.  So how does AGPL work, legally?  The answer: [practical interference](#definition-of-practical-interference) again.

In much the same way that the combination of GCC and libgcc managed to create a "free for open source" license, by leveraging a _practical_ feature of how we use software, AGPL leverages the fact that to run software, we inevitably make copies of it.  Copyright law _does_ give licenses the power to set rules for reproduction---making copies of software---and preparation of derivative works---making changes and building into other software.  AGPL section 13 requires preparing a derivative work explicitly: you only trigger its requirements if you "modify the Program".  But in order to run that modified program for others to interact with over a network, you're going to have to make a copy at least once, and probably many times.  Copyright licenses can set rules about making copies.

Long story short, legally, AGPL section 13 is, among other things, a rule about making copies.  In particular, it's a rule about making copies _for the purpose of running the program to provide a network service to others_, in exercise of freedom 0, to run the program.  "The freedom to publicly perform the program" isn't in the copyright law, and it isn't one of the four freedoms, either.  It's part of freedom 0: the freedom to run the program for other people.

This particular exercise of freedom 0 only feels like "distribution" in a far broader sense than freedom 2 (redistribution) and freedom 3 (distribute with changes) entail.  The _consequence_ of exercising freedom 0 to provide a modified AGPL network service is that you have to offer to exercise freedom 3 to distribute copies of your modified version.  One consequence of section 1(c) of [OSL 3.0](https://opensource.org/licenses/OSL-3.0), which doesn't require modification, and which FSF also [approves as a free software license](https://www.gnu.org/licenses/license-list.en.html#OSL), can be that you have to exercise freedom 2 to redistribute copies of even unmodified OSL software.  These rules don't regulate exercise of freedom 2 and 3.  They force you to exercise freedom 2 and 3 when you otherwise have not and might not.

# Extra Freedom

There aren't actually four freedoms.  There are at least five.  The fifth, unenumerated freedom, also in [the definition](https://www.gnu.org/philosophy/free-sw.en.html), is _private changes_:

> You should also have the freedom to make modifications and use them privately in your own work or play, without even mentioning that they exist. If you do publish your changes, you should not be required to notify anyone in particular, or in any particular way.

In other words, software freedom _also_ means the freedom to exercise freedom 1 (make changes) and _not_ exercise freedom 3 (distribute changes).  The FSF's rejection of [RPL](https://www.gnu.org/licenses/license-list.en.html#RPL) corroborates:

> The Reciprocal Public License is a nonfree license because of three problems. ... 3. It requires publication of any modified version that an organization uses, even privately.

But we've just seen freedom 1 and freedom 3 together, in a different context.  When you modify an AGPL program (freedom 1) and run it to provide a network service, AGPL section 13 _requires_ you to distribute source code (freedom 3).  AGPL specifically requires you to share changes you might like to keep private.  It doesn't take pains to avoid the word "modify".

Legally, copyright law includes an exclusive right to prepare derivative works, such as by making changes or building into other software.  So AGPL didn't _need_ to require exercise of both freedom 0---running the program, implicating reproduction by practical interference---and freedom 1---making changes, implicating production of derivative works---to trigger the requirement to offer code.  In fact, AGPL could have accomplished its goal of closing the software-service loophole by triggering on modification, or preparation of derivative works, alone.

That is _exactly_ the approach of RPL, which was purpose-drafted for a JavaScript web application framework behind the service barrier, six years before AGPL.  The only implementation puzzle is who to offer source code to.  RPL required those making changes to send them back to the original developer, to which FSF objected.  But we could sketch a variation that avoids that problem:

> If you prepare a derivative work of this software, offer complete source code and a license on these terms to every user of your work, free of charge, and provide them promptly, on request.

Under this rule, it doesn't matter how users become users.  Every user gets a path to software freedom.

Would a license with that rule be free software license?  Frankly, I have no idea if or why.  We've explored some relationships between the freedoms with licenses.  But so far what's been found there hasn't been distilled in any writing I have found.

# Extra Law

If this seems complicated, if writing rules in copyright or software-freedom language seems overly delicate, I agree.  If we want a license that says "free for free software" or "free for open source", can't we just write that?

In my opinion, yes.  Practically, indeed we can.

US copyright law has a few provisions peculiar to software.  But copyright is a general framework.  Software licenses run on the same basic legal "operating system" of copyright law as music licenses, film licenses, book licenses, and, yes, nonfree proprietary software licenses.  Inability to learn from one's opponents is a terrible handicap, especially if they learn readily from you.

We can start a bit closer to home.  [Creative Commons](https://creativecommons.org) publishes professionally drafted public copyright licenses for creative works.  One of their licenses is CC-BY-NC, which allows use for noncommercial purposes.  Here's the relevant text from the ["legal code"](https://creativecommons.org/licenses/by-nc/4.0/legalcode):

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

This is [practical interference](#definition-of-practical-interference) in action.  Which exclusive rights of copyright holders to these restrictions relate to?  Whichever one the copyright owner giving the license manages to show the user exercised.  For software, perhaps reproduction, or preparing a derivative work, or distributing to the public.  If they're working with the software, it's highly likely they're exercising at least one of those rights.  Exercising any without permission is copyright infringement.

I'm reminded of a sign over my grandparents' garage, in rural Rising Star, Texas:

        THIS GARAGE
     GUARDED BY SHOTGUN
     FOUR DAYS PER WEEK

    YOU GUESS WHICH ONES

It's not up to the copyright holder giving the license to spell out exactly how they'll enforce their way.  The license can leave some of that uncertainty with the user.  Happens all the time, in professionally drafted terms.

Of course, there is uncertainty in the law.  The difference between owning and licensing a copy under 17 U.S.C. § 117.  The difference between [granting a license on its own](https://lwn.net/Articles/61292/), or through a contract.  [Whether that's even a practical difference](https://en.wikipedia.org/wiki/Jacobsen_v._Katzer).  [Vernor v. Autodesk](https://en.wikipedia.org/wiki/Vernor_v._Autodesk,_Inc.) and the [MAI](https://en.wikipedia.org/wiki/MAI_Systems_Corp._v._Peak_Computer,_Inc.) trio.

Specialist opinions differ.  The leading copyright treatise sets impartiality aside, and includes a full brief on the matter.  But those relying on licenses usually aren't keen to finance the public good of legal clarity on these issues, by fighting them out in the courts at great private expense.  Trend and policy favor copyright holders, and protecting their power to control use of their works.  The power to keep copies from reaching a user to begin with remains unquestioned, and that is a greater power than prohibiting specific kinds of use.  Copyright does not grant monopolies on ideas alone, but the path of clean-room reimplementation is a long, tedious, and costly one.

All of that sounds terrible if you think all software ought to be in the public domain.  But software in the public domain can't do anything in the other dimensions that matter: source availability, credit, and so on.  To function, copyleft needs copyright.  The strong copyright is, the stronger copyleft can be.

# Compromise

Perhaps what I'm missing is a more complete map of the relationships between freedoms, as the FSF sees them.  With freedoms, there are always exceptions, always balances to be struck.  Sometimes one freedom yields to another, as of a higher priority.

But on the subject of where to draw the line between copyleft and permissive, the long, common thread isn't principle so much as strategy.  The FSF has compromised when it feared loss of popularity, and attention, which are its only real platform from which to speak online.  The hook is ever practicality: talking free as in freedom over free as in beer.
