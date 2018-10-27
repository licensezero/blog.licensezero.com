---
title: No Other Terms Before Me
description: the minimalist case for radical terms
layout: post
---

License Zero supports just two public license choices: [Parity], a radical copyleft license, and [Prosperity], a simple noncommercial license.  Why not [AGPLv3], or even [GPLv3], the most common choices for dual licensing?  Why not [QPL] or [RPL], purpose-written for dual licensing?

[GPLv3]: https://www.gnu.org/licenses/gpl-3.0.en.html
[AGPLv3]: https://www.gnu.org/licenses/agpl-3.0.en.html
[Parity]: https://licensezero.com/licenses/parity
[Prosperity]: https://licensezero.com/licenses/prosperity
[RPL]: https://opensource.org/licenses/RPL-1.5
[OSL]: https://opensource.org/licenses/OSL-3.0
[QPL]: https://opensource.org/licenses/QPL-1.0

Because they're way too complicated, and License Zero needs to make legal and software components work together, simply and seamlessly, especially for users:

```shell
# Building closed commercial software:
licensezero buy

# Building open commercial software:
licensezero buy --open

# Building closed noncommercial software:
licensezero buy --noncommercial
```

Reliable, usable integration of code and terms isn't possible with the exception-ridden, spaghetti-terms copyleft licenses of the past.  We'd need a `--static-linking` flag.  A `--within-organization` flag. A `--using-gplv2` flag.  A `--just-separate-modules` option.  We'd need `--network-service` and `--without-changes`.  And several more.  The manpage would be a law treatise on copyleft licensing.

License Zero needs simpler licenses.  And as it turns out, simpler licenses, without the compromises of the past, seem radical by comparison.

# Prior Artists

Of course, dual licensing itself isn't new.  Hardly.

Developers bootstrapping new projects have dual licensed open software at least since [Ghostscript](https://www.ghostscript.com/license.html) and [MySQL](https://www.mysql.com/about/legal/licensing/oem/), in the mid 1990s.  [Technical Pursuit](https://technicalpursuit.com/) has [dual licensed](https://technicalpursuit.com/license.xhtml) its [TIBET](https://technicalpursuit.com/tibet.xhtml) JavaScript web framework since the early 2000s.  [Metafizzy](https://metafizzy.co/) turned [dual licensing](https://isotope.metafizzy.co/license.html) of the [Isotope](https://isotope.metafizzy.co/) front-end JavaScript library into a full-time business in the 2010s.  [Trolltech](https://www1.qt.io/licensing/).  [Digium](https://www.digium.com/products/asterisk/licensing).  [SQLite](https://www.sqlite.org/copyright.html).  [Particular Software](https://github.com/Particular/NServiceBus/blob/develop/LICENSE.md).  Developers have dual licensed since selling tape copies was a viable business model.

Along the way, dual licensors have tended either to pick the strongest available copyleft license from the [Free Software Foundation](https://www.fsf.org/licensing/education), or to write their own.  Ghostscript initially wrote its own, [Aladdin](https://en.wikipedia.org/wiki/Aladdin_Free_Public_License), and eventually moved to [GPLv2].  MySQL used GPLv2, as well.  BerkeleyDB birthed [Sleepycat], and eventually moved to [AGPLv3].  Technical Pursuit wrote [RPL].  Affero wrote [AGPLv1].  Another company, Funambol, took [AGPLv3] through OSI for approval.  Metafizzy gets away with [GPLv3], because of the kind of library it is.

[GPLv2]: https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html
[AGPLv1]: http://www.affero.org/oagpl.html
[Sleepycat]: https://opensource.org/licenses/Sleepycat

And there we have our first hint of the problem.

# Functional Specification

Before diving into the details, it's important to understand that the goal of a "free for open source" license is as old as copyleft itself, older in fact than "open source".

Here's Richard Stallman, founder of the Free Software Foundation, [at least as early as 2000](https://web.archive.org/web/20000303214900/https://www.gnu.org/philosophy/pragmatic.html):

> I make my code available for use in free software, and not for use in proprietary software, in order to encourage other people who write software to make it free as well.  I figure that since proprietary software developers use copyright to stop us from sharing, we cooperators can use copyright to give other cooperators an advantage of their own: they can use our code.

Next paragraph down, RMS acknowledges that his licenses can also be used for dual licensing.  Relating a conversation with a friend "many years" before:

> He was willing to share his work with a community that shares software, but saw no reason to give a handout to a business making products that would be off-limits to our community.  His goal was different from mine, but he decided that the GNU GPL was useful for his goal too.

Hackers have long thought of the strongest available copyleft license of the time as the "free for free software", now "free for open source", option.  That is largely how software companies have thought of them, too, to avoid getting into all the gritty details.

When large proprietary software companies with megaton legal talent prohibit strong copyleft licenses by corporate policy, as Google famously [bans AGPL](https://opensource.google.com/docs/using/agpl-policy/) and [restricts OSL](https://opensource.google.com/docs/thirdparty/licenses/#restricted), that is "free for open" passing its most rigorous integration test.  Not a bug.  An initiative to achieve massive corporate use of open software to build closed has always been part of the movement.  So have initiatives to compete with closed software, to offer incentives to choose working open over working closed, and to protect upstarts working open against incumbents.

However, in time, licenses that meant "free for open source" to start come to mean something less, something more complicated.  They come to mean what they actually say.  Something far more esoteric.  Something inherently weaker.

Eventually, when enough valuable software comes under a particular strong-copyleft license, or a company wants to appropriate a particular piece of work badly enough, lawyers are summoned, limits are tested, words are stretched, lines are smudged, and loopholes open.  Essentially, every strong copyleft license is its own kind of bug bounty program: first proprietary user to the software, past the license, wins a first-mover advantage.  The more valuable the software, the greater the advantage---the greater the bounty.  Of course, once a loophole is known, it never stays a secret.

# Hacks, Patches, and Holes

The reason for strong-copyleft's security record is twofold.

First, throughout copyleft history, the organizations willing to pay lawyers and technologists to implement, socialize, and maintain new strong-copyleft licenses tended to self-impose limits on how strong their licenses could be.  Sometimes they self-imposed limits on principle.  Sometimes they simply met their own immediate, present-tense needs, and stopped there, at their own self-interest.

Self-limitation is most evident in the Free Software Foundation, the only organization that has consistently published stronger copyleft licenses.  The FSF sees copyleft as a tool for promoting and achieving ["software freedom"](https://www.gnu.org/philosophy/free-sw.en.html), which the closed, proprietary, or "non-free" software produced by most companies denies.  Per the FSF, for software to be free software, it must come with source, and that source must be licensed under a free software license.  But in order to be an ethical "free software license", terms must _allow_ use for development of non-free software, at least in certain ways.  For example, FSF-drafted licenses avoid requiring users to share "private changes" that they make.  That includes "private" changes used within enormous organizations, like proprietary patches to the Linux kernel deployed across non-free software companies with thousands of employees and contractors.  [I don't understand why.](https://blog.licensezero.com/2018/09/14/free-to-take-freedom.html#extra-freedom)  Arguably, their newest, strongest license skirts this rule.

Many developers and upstart projects, like Netscape starting Mozilla and Torvalds starting Linux, choose copyleft licenses explicitly to receive changes back from their users.  When unable to write their own licenses, [as Mozilla did](https://www.mozilla.org/en-US/MPL/), they often repurpose FSF licenses, [as Linus did](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/COPYING).  In the early 2000s, the Open Source Initiative approved a few strong-copyleft licenses specifically drafted to bring patches back, without the FSF's self-imposed limits.  Some of these licenses required sharing private changes.  Some shifted from requiring developers to share source with users, as under the FSF's end-user-focused licenses, to sharing source with the original developer, or even publishing online.  The FSF rejected those licenses as beyond its self-imposed limits.

The second reason strong-copyleft licenses have fallen short of "free for open" will be familiar to every vocational programmer.  The idea of copyleft was a glorious, glorious hack, legally and coder-culturally.  Strong-copyleft implementers seem to have delighted in this hackishness, writing oddly low-level legal terms that proved just enough to get "free for free software" functionality at the time.  As new means of using and reusing software became common, narrow terms tightly coupled to their times proved predictably brittle, allowing ever more use of strong-copyleft software in closed projects.  The "free for free software" licenses became "mostly free for free software, in some ways, unless you know the holes and fit through them".  The hacker licenses got cracked.

The most infamous bug was and remains the "ASP Loophole", alias "SaaS Loophole" or "Google Problem".  The GPLs and all the licenses that followed their approach require sharing source for new work on the same terms only if the licensee distributed the changed software to others outside their organization.  But licensees don't distribute copies of software that they run for end-users to access over a network, like Web applications or peer-to-peer applications.  As a result, GPL-style copyleft doesn't require them to share source or give licenses for their work, which can remain closed and non-free.  So "free for free software" code ends up in nonfree services.

Strong-copyleft drafters responded by writing the smallest license patches possible to fix the vuln.  The relevant diff between GPLv2 and AGPLv1 is just one new numbered item in the rule on distribution.  The relevant diff between revised GPLv3 and AGPLv3, which many in the free software community wanted to merge into a single new GPLv3, but couldn't due to proprietary development pressure, is a single paragraph buried in section 13.  When Technical Pursuit found the network-copyleft licenses available to it wouldn't effectively reach all the code in apps using its web framework, it patched the definition of "Deploy" from [Sybase/Open Watcom](Sybase/Open Watcom), and tacked on a definition of "Required Components".  Now that [MongoDB](https://www.mongodb.com/), a longtime, high-profile AGPLv3 licensor, has found competitors exploiting loopholes in that license, it's proposing yet another patch to GPLv3 section 13, as the [Server Side Public License](https://www.mongodb.com/licensing/server-side-public-license).

Current strong copyleft licenses aren't cathedrals, devised as wholes by one mind at one time, and they don't come from any bazaar.  Even when rewritten from scratch, as was GPLv3, they've developed by intellectual accretion, hewed to past approaches, and developed largely by committee.  That has had the usual dampening, conservative effect on the talent and good intentions brought to bear.

# Maintenance Hell

All of this hack-and-patch complexity makes it damn difficult for even plucky self-starters to answer two basic questions about open source copyleft:

1. Which open source license do I pick to make my software "free for open source"?
2. Can I use this work I found under such-and-such "free for open source" license in my project?

Companies pay me hundreds, sometimes thousands of genuine United States Dollars to answer these questions.  Which is ridiculous.  Especially when my answer has to be "no good option" or "no clear answer".  Especially when I have to interrogate at least one engineer, and cave dive into at least one codebase, before I can deliver the bad news.

There are some easy cases.  But you can't spot them confidently without spending a whole lot of time reading, analyzing, and talking about copyleft legacy systems.  The best heuristic is general old-fashionedness.  The closer the software being licensed, and the software people will want to make with it, to the way things were done back in 1989, the better the chance of a solid, effective answer.

If I could write "Which license?" as a chat bot, I would.  That wouldn't do anything for the people who have to read:

```
LicenseBot: Thank you for answering my questions.
LicenseBot: Unfortunately, there is no good option
            for your software project.
LicenseBot: Please rate my service today: ...
```

But it might help some of the rest.

Unfortunately, it's not possible without precarious quality compromises.  The decision tree is too wide, too deep, too probabilistic.  Even when there is an answer, it always comes with a caveat about vulnerabilities.  Moreover, many copyleft implementations electively couple key rules to terms defined and evolved by law, like "derivative work", which are always [changing on us](https://en.wikipedia.org/wiki/Oracle_America,_Inc._v._Google,_Inc.).  In the end, "Which open source license do I pick to make my work free for free only?" is putting the question the right way.  But that question can't be answered in the same good terms.

If I could write "Can I use this?" as a program to run in continuous integration, I would, too.  I tried.  In the end, it involved far too much configuration, even within the relatively modern, consistent playpen of npm, under the conventions of that single ecosystem.

The [program](https://www.npmjs.com/package/licensee) I use personally and with clients requires a whitelist of licenses, essentially a legal prescription.  To avoid that, I'd need a file full of flags corresponding to the questions that I'd ask a client, as their lawyer, in order to map to licenses for a whitelist.  Whether I ask for licenses or legal assessments that point to licenses, if I'm asking developers, I'm asking for trouble.  That isn't solving the problem.  It's turning the easy parts into software, pushing the hard parts onto the user, and slapping `"AS IS", WITHOUT WARRANTY OF ANY KIND` on it.

A mess in the legal, and no software salvation in sight.  Where does that leave us?

Permissive licenses seem to get simpler.  Not necessarily better, but simpler.  Sometimes [dangerously so](https://opensource.org/licenses/FPL-1.0.0).

Meanwhile, copyleft gets more complex, and seems to work worse.  Its politics compound, rather than cancel out, over time.

Copyleft is thrashing in the tar pit.  It can't get out of where it is now, and where it stands, it's sinking.

# Refactor

So I trod off to fresh ground, and wrote a new license: The License Zero Noncommercial Public License.  I pasted the noncommercial bits of Creative Commons' [CC-BY-NC](https://creativecommons.org/licenses/by-nc/4.0/legalcode) into [BSD](https://spdx.org/licenses/BSD-2-Clause.html) terms, and went from there.  Lots of work modernizing the base terms.  Now it's [Prosperity].

Some of my friends and colleagues won't use a noncommercial license.  They insist on copyleft, but not on the FSF's compromises or self-limitations.  So I wrote another license: The License Zero Reciprocal Public License.  I pasted "free for open source" into BSD, and went from there.  Modernized the base terms.  Split it out into three rules, for clarity.  Required sharing alike, but not necessarily on the same terms, to avoid some headaches and facilitate some new collaborative licensing models.  That license became [Parity].  In large part thanks to great input from developers, who helped to keep it readable.

Thanks to [Parity] and [Prosperity], the decision tree for developers into and out of License Zero is pretty simple.

If the majority of people will use your software to make other software, consider [Parity].  Application?  Library?  Framework?  Toolkit?  Plugin?  Front-end?  Back-end?  Peer-to-peer?  Compiled?  Interpreted?  Linked?  Distributed?  Interpreter?  Package manager?  Dev tool?  Doesn't matter.  [Parity] it is.

If the majority of people will use your software to do something else, consider [Prosperity].

The decision tree for users is much simplified, too.

Building closed software?  You need private licenses for [Parity] code.

Doing commercial work?  You need private licenses for [Prosperity] code.

Doing both?  You need private licenses for both [Parity] and [Prosperity] code.

Static or dynamic linking?  Distributed or networked application?  Unmodified?  Separate modules?  File-level changes?  Production or development dependency?  Doesn't matter.  See above.  And `licensezero quote --help`.

# Apologia

If you're running a dual licensing play with [GPL][GPLv3] or [AGPL][AGPLv3] or [OSL] or [RPL] or [QPL] or, heck, even [Sleepycat], I'd love to help you.  But License Zero and your project's license would not be good for each another.  It'll be a bit more work, but you can sell private licenses just fine without [licensezero.com](https://licensezero.com).

Complicating the system isn't good for your, any individual user, or the system overall.  And License Zero can only complicate itself by [reverently tying itself to the mast of the past](https://blog.licensezero.com/2018/05/13/commons-club.html#past).  Standing where we are now, I can't place tradition above either developers or users.  That's wrong.  I can't pretend that new needs pale in comparison to network benefits of old copyleft licenses in young, predominantly permissive communities.  They don't.  I can't play Pied Piper for software freedom, assuming that everyone will come around to fsf.org as received wisdom.  They won't.

As it turns out, radical copyleft and simply drafted noncommercial licenses, while jarring for those who've invested in the peculiarities and esoteric debates of old terms, as I have, turn out to be far simpler, far more explainable, and far more automation-ready for eschewing twenty years of tactical and ideological compromise.  By taking the community's intentions and understandings and writing them into legal terms in the most direct ways possible, License Zero avoids telling developers on either side that they can't say what they want, as developers, or understand what was meant, as users.  That makes room in the complexity budget for the software and other conventions---metadata, private licenses, collaboration management---that create a complete system for developers looking to support and be supported in open work.