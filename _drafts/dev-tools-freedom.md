---
title: Free to Nonfree
layout: post
---

I don't understand the Free Software Foundation's position on software used to make other software.  As far as I can tell, their definition of "free software" licenses precludes terms that make developer tools free for use for free software only, or "free for open source".  Free-only libraries?  Yes.  Free-only compilers, bundlers, static analysis tools, and deployment utilities?  Apparently no.  And not just strategically undesirable, but philosophically impermissible.

Earlier this week, I ran into [libgcc](https://gcc.gnu.org/onlinedocs/gccint/Libgcc.html), the low-level runtime library for GCC, for the first time in a long time.  When compiling a program, GCC generates calls to libgcc symbols, which the compiled program must link.  GCC links libgcc by default.  The actual content of libgcc depends on the target architecture.  But in general: GCC puts a bit of its own code into the programs it compiles.

What does that have to do with licensing?

The GPL doesn't require you to share source code for programs that you compile with GPL-licensed software.  Broadly speaking, its requirements to share and license your own code apply only when you make changes to GPL code, or build it into your own code, and share the results with someone else.  GPL's requirements don't say anything about running the GPL software, or running it for a particular purpose, like making nonfree software.

If you assumed that a software license _can't_ legally require sharing alike based on how a program is used---I get the feeling FSF [doesn't think this is true](https://www.gnu.org/licenses/agpl-3.0.en.html#section13), but [wishes it were](https://www.gnu.org/philosophy/programs-must-not-limit-freedom-to-run.en.html)---then GPL's approach would do all that's possible to require sharing and licensing other software as free software.  But it couldn't do anything about compiling nonfree software with a free-software compiler.  If you _wanted_ to require sharing and licensing compiled software as free software, a runtime library like libcc, which gets combined with compiled and distributed with it, gives you a _technical_ way around the limitation of the license.

In other words: If you want to require others to make as much software free software as possible, but you _can't_ require them to share just because they compiled with your compiler, though you _can_ require them to share for building your code into theirs, then build a compiler that puts bits of your code into programs it compiles.  You've just worked around the limitation of your license.  Practically speaking, programs compiled with the compiler and shared with others have to be free software.

The FSF stewards GCC, perhaps the most important developer tool in existence.  So does libgcc require developers using GCC to compile programs to make their programs free software?  No, [it does not](https://www.gnu.org/licenses/gcc-exception-3.1-faq.en.html):

> [I]f these libraries [(libgcc)] were simply distributed only under the terms of the GPL, all the object code that GCC produces would have to be distributed under the same terms.  However, the FSF decided long ago to allow developers to use GCC's libraries to compile any program, regardless of its license.

The FSF [created an exception to its own license](https://www.gnu.org/licenses/gcc-exception.html) specifically to stop its most important program from requiring more software to be free software.

Why?  GCC was the killer app of open software development.  The first.  It carried the flag both for the practice of open, collaborative software development, and for software freedom, as implemented in the first version of the GPL.  It rose to popularity, and proved its first point, in large part by permitting compilation of nonfree programs.  Taking GCC away from the bulk of its user base, due to a technical detail, [would have been jarring](https://www.gnu.org/licenses/gcc-exception-3.1-faq.en.html):

> Developing nonfree software is not good for society, and we have no obligation to make it easier.  We decided to permit this because forbidding it seemed likely to backfire, and because using small libraries to limit the use of GCC seemed like the tail wagging the dog.

There are two distinct rationales here: first that changing the effective license terms for GCC would backfire, in some strategic sense, and second that relatively minor code like libgcc shouldn't affect the terms for GCC.

The second doesn't make any sense to me.  The free software movement is and always has been a minority.  It self-consciously lacks the financial and other resources of proprietary developers.  It needs leverage, in the tactical sense: methods to get a lot done for software freedom with relatively little software.  libgcc would be extraordinarily high-leverage.

I suspect the first is really a subspecies of [FSF's argument for LGPL](https://www.gnu.org/licenses/why-not-lgpl.html) and even [FSF's arguments for using Apache 2.0](https://www.gnu.org/licenses/license-recommendations.en.html).  It comes down to competition:

> Some libraries implement free standards that are competing against restricted standards, such as Ogg Vorbis (which competes against MP3 audio) and WebM (which competes against MPEG-4 video).  For these projects, widespread use of the code is vital for advancing the cause of free software, and does more good than a copyleft on the project's code would do.
>
> ...
>
> [W]here the library implements an ethically superior standard, here adoption for its own sake will not accomplish any special objective goal, so there's no reason to avoid copyleft entirely.  However, if you require developers who use your library to release their whole programs under copyleft, they'll simply use one of the alternatives available, and that won't advance our cause either.  The Lesser GPL was designed to fill the middle ground between these cases, allowing proprietary software developers to use the covered library, but providing a weak copyleft that gives users freedom regarding the library code itself.

This begins to take us away from the specific, peculiar historic case of GCC, and into the present day.  For the present day, FSF [recommends AGPL](https://www.gnu.org/licenses/license-recommendations.en.html#server) for anything likely to end up in a service.  That license carries the software freedom torch, requiring more software to be free software than GPL.

Even AGPL does not cover dev tools.  If GCC were AGPL-licensed, it would still need a technical "hook", like libgcc, to require compiled programs to be free software.  Why doesn't AGPL go further?

The FSF's [definition of free software](https://www.gnu.org/philosophy/free-sw.en.html) defines their criteria for free-software licenses in terms of four end-user freedoms to be protected:

> - The freedom to run the program as you wish, for any purpose (freedom 0).
>
> - The freedom to study how the program works, and change it so it does your computing as you wish (freedom 1).
>
> - The freedom to redistribute copies so you can help others (freedom 2).
>
> - The freedom to distribute copies of your modified versions to others (freedom 3).

At the same time, the FSF itself publishes and recommends licenses that impinge on some of these freedoms.  Specifically, GPL's sharing rules impinge on freedom 2 and freedom 3.  You can't redistribute copies of GPL-licensed code without source code or notice that the GPL applies.  You can't distribute copies of modified versions without applying GPL to your modifications, and providing source for them.

The free software definition [explains (search for the "Copyleft" heading)](https://www.gnu.org/philosophy/free-sw.en.html):

> Certain kinds of rules about the manner of distributing free software are acceptable, when they don't conflict with the central freedoms. For example, copyleft (very simply stated) is the rule that when redistributing the program, you cannot add restrictions to deny other people the central freedoms. This rule does not conflict with the central freedoms; rather it protects them.

Copyleft rules, as FSF sees them, are valid rules about exercising freedom 2 (to redistribute) and freedom 3 (to distribute modified copies).  Under GPL, you can only exercise those freedoms if you also follow rules about source code and license terms.

In this way, denying others software freedom works a bit like a tort or a crime.  In the United States, we have the freedom to speak.  But using our freedom of speech to keep someone confined, incommunicado, against their will, by threats of physical violence, gives them a legal claim against us, and the state a crime to charge.  Laws for those torts and crimes seek to prevent us using our freedom of speech to unjustly take that freedom from others.

Various laws prevent us using other freedoms to deny others' freedom of speech.  I cannot take your freedom of speech with my right to shoot firearms.  Or to move my body as I please.  Or to express my religious or political beliefs.  The purpose, or policy, is to protect your freedom of speech.  No matter which freedom of mine I exercise to do so, the harm to you is the same.

That begs the question:  Why doesn't the FSF's definition of copyleft set rules about exercising freedom 0 (run the program) and freedom 1 (change the program), as well as freedom 2 (redistribute) and freedom 3 (distribute with changes)?  Why does FSF prohibit denying others software freedom only if you happen to do so by distributing, and take pains to allow it if you happen to do so by compiling a program, or making changes to code you keep to yourself?  It's as if FSF prohibited fraud, but only by speaking, and not by writing.

I'm most confused by the situation with respect to freedom 0, the right to run software.  [Section 13 of AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html#section13), which adds to GPLv3 a requirement to "offer all users interacting with [modified AGPL software] remotely through a network" source code and an AGPL license.  But it's impossible to trigger Section 13's requirement to make your software free software without running the software, and running it in a particular way: to offer a network service to others.  AGPL _has_ a rule about exercising freedom 0, your right to run the program as you wish, for any purpose.  Under AGPL, you may _not_ the program to provide a nonfree network service.

AGPL section 13 diligently avoids the words "use" or "run" or "execute".  I believe this reflects the view that I first heard from Bruce Perens, that AGPL 13's authors wanted to synthesize "a public performance right for software".  Copyright law gives copyright owners a list of exclusive rights: things they can sue others for doing without a license.  One of those is public performance.  If I compose a symphony, I sue orchestras for performing it without a license.  But there's no such performance right in the copyright law for software, to cover uses like running a web application for customers or the public at large.  Which is what AGPL's authors wanted to regulate, in order to plug the loophole that allows developers to build GPL software into network applications, and avoid the requirement to make the applications free software, by never distributing them to others.

AGPL is a copyright license that sets rules for publicly performing software in this sense.  But copyright doesn't give licenses control over publicly performing software.  So how does AGPL work, legally?

The answer: In much the same way that the combination of GCC and libgcc managed to create a "free for open source" license, by leveraging a _practical_ feature of how we use software.  Copyright law _does_ give licenses the power to set rules for reproduction---making copies of software---and preparation of derivative works---making changes and building into other software.  AGPL section 13 requires preparing a derivative work explicitly: you only trigger its requirements if you "modify the Program".  ([OSL](https://opensource.org/licenses/OSL-3.0), another license in AGPL's category, doesn't.)  But in order to run that modified program for others to interact with over a network, you're going to have to make a copy at least once, and probably many times.  Copyright licenses can set rules about making copies.

Long story short, legally, AGPL section 13 is, among other things, a rule about making copies.  In particular, it's a rule about making copies _for the purpose of running the program to provide a network service to others_, in exercise of freedom 0, to run the program.  "The freedom to publicly perform the program" isn't one of the four freedoms.  It's just a part of freedom 0: the freedom to run the program for other people.  It only feels like "distribution" in a far broader sense than freedom 2 (redistribution) and freedom 3 (distribute with changes), which involve copies.  The _consequence_ of exercising freedom 0 to provide a modified network service is that you have to offer to exercise freedom 3 to distribute copies of your modified version.  One consequence of section 1(c) of [OSL 3.0](https://opensource.org/licenses/OSL-3.0), which FSF also [approves as a free software license](https://www.gnu.org/licenses/license-list.en.html#OSL), can be that you have to exercise freedom 2 to redistribute copies of even unmodified software.  If these rules don't regulate exercise of freedom 2 and 3.  They force you to exercise those freedoms when you otherwise might not.
