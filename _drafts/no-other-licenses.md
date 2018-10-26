---
title: Why No Other Licenses?
description:
layout: post
---

License Zero supports just two public license choices: [Parity], a short maximalist copyleft license, and [Prosperity], a short noncommercial license.  Why not [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html), or even [GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html), probably the most common choices for dual licensing?  Why not [QPL](https://opensource.org/licenses/QPL-1.0) or [RPL], purpose-written for dual licensing and OSI-approved?

[Parity]: https://licensezero.com/licenses/parity
[Prosperity]: https://licensezero.com/licenses/prosperity

Users building closed, commercial software need a single [command](https://github.com/licensezero/cli) to run, to find all the private licenses they need:

```shell
licensezero quote
```

Building open commercial software?

```shell
licensezero quote --open
```

Building  closed noncommercial software?

```shell
licensezero quote --noncommercial
```

That's it.

License Zero needs new licenses to make legal and software components work together, simply and seamlessly, for users.  That's not possible with known-buggy, spaghetti-terms copyleft licenses of the past.  License Zero's integration of legal terms and software code is new.  It took [new code](https://github.com/licensezero) _and_ [new terms](https://licensezero.com/licenses/).

[RPL]: https://www.gnu.org/licenses/agpl-3.0.en.html

# Prior Artists

Of course, dual licensing itself isn't new.  Hardly.

Developers bootstrapping new projects have dual licensed open software at least since [Ghostscript](https://www.ghostscript.com/license.html) and [MySQL](https://www.mysql.com/about/legal/licensing/oem/), in the mid 1990s.  [Technical Pursuit](https://technicalpursuit.com/) has [dual licensed](https://technicalpursuit.com/license.xhtml) its [TIBET](https://technicalpursuit.com/tibet.xhtml) JavaScript web framework since the early 2000s.  [Metafizzy](https://metafizzy.co/) turned [dual licensing](https://isotope.metafizzy.co/license.html) of its [Isotope](https://isotope.metafizzy.co/) front-end JavaScript framework to a full-time business in the 2010s.  [Trolltech](https://www1.qt.io/licensing/).  [Digium](https://www.digium.com/products/asterisk/licensing).  [SQLite](https://www.sqlite.org/copyright.html).  [Particular Software](https://github.com/Particular/NServiceBus/blob/develop/LICENSE.md).

Dual licensors have tended either to pick the strongest available copyleft license the [Free Software Foundation](https://www.fsf.org/licensing/education) currently offers, or to write their own.  Ghostscript initially wrote its own, [Aladdin](https://en.wikipedia.org/wiki/Aladdin_Free_Public_License), but eventually moved to GPLv2.  MySQL used GPLv2.  BerkeleyDB wrote [Sleepycat](https://opensource.org/licenses/Sleepycat).  Technical Pursuit wrote [RPL].  Affero wrote AGPLv1.  Another company, Funambol, took AGPLv3 through OSI for approval.  Metafizzy gets away with GPLv3, because of the kind of library it is.  And there we have our first hint of the problem.

# Functional Specification

Before diving into the details, it's important to understand that the goal of a "free for open source" license is as old as copyleft itself, older in fact than "open source".  Here's Richard Stallman, founder of the Free Software Foundation, [in 2000](https://web.archive.org/web/20000303214900/https://www.gnu.org/philosophy/pragmatic.html), if not earlier:

> I make my code available for use in free software, and not for use in proprietary software, in order to encourage other people who write software to make it free as well.  I figure that since proprietary software developers use copyright to stop us from sharing, we cooperators can use copyright to give other cooperators an advantage of their own: they can use our code.

Next paragraph down, RMS acknowledges that his licenses can also be used for dual licensing.  Relating a conversation with a friend "many years ago":

> He was willing to share his work with a community that shares software, but saw no reason to give a handout to a business making products that would be off-limits to our community.  His goal was different from mine, but he decided that the GNU GPL was useful for his goal too.

Hackers have long thought of the strongest available copyleft license of the time as the "free for free software", now "free for open source", option.  That is largely how software companies have thought of them, too, to avoid getting into all the gritty details.  Companies making not-open software figure "free for open" isn't free for them.

When large proprietary software companies with megaton legal talent prohibit strong copyleft licenses by corporate policy, as Google famously [bans AGPL](https://opensource.google.com/docs/using/agpl-policy/) and [restricts OSL](https://opensource.google.com/docs/thirdparty/licenses/#restricted), that is "free for open" passing its most rigorous full-system integration test, not a bug.  An initiative to achieve massive corporate use of open software to build closed has always been part of the community.  So has an initiative to compete with closed development, to offer incentives to choose open over closed, and to protect upstart community allies against indifferent or antagonistic incumbents.

However, in time, licenses that once meant "free for open source" come to mean something less, and something more complicated.  Something that takes a lot more words to explain and understand.  Because the terms that developers and users have _thought_ meant "free for open source" have almost always actually said something else, something far more esoteric, something inherently weaker.

Eventually, when enough valuable software comes under a particular strong-copyleft license, or a company wants to appropriate a particular piece of work badly enough, lawyers are summoned, analyses are made, and loopholes appear.  Essentially, it's a bug bounty: first proprietary user to the software, past the license, wins a first-mover advantage.  Of course, once a loophole is known, it never stays a secret.  In the end, the barricade becomes a welcome mat.

# Hacks, Patches, and Holes

The reason for strong-copyleft's rough security record is twofold.

First, throughout copyleft history, the organizations willing to pay lawyers and technologists to draft, revise, and socialize new strong-copyleft licenses tended to self-impose limits on how strong their licenses could be.  Sometimes based on principle.  Sometimes at the limits of their own immediate needs and self-interests.

Self-limitation is most clear with the Free Software Foundation, the only coalition organization that has consistently published stronger copyleft licenses over time.  The FSF sees copyleft as a tool for promoting and achieving ["software freedom"](https://www.gnu.org/philosophy/free-sw.en.html), which the closed, proprietary, or "non-free" software produced by most companies denies.  Per the FSF, for software to be free software, it must come with source, and that source must be licensed under a free software license.  But in order to be an ethical "free software license" according to FSF, a license actually has to _allow_ certain kinds of use for development of non-free software.  That shows through in FSF's GPL, AGPL, and LGPL series licenses.  To give an example, FSF licenses studiously avoid requiring users to share "private changes" that they make.  That includes "private" changes used within enormous organizations, like proprietary patches to the Linux kernel deployed across non-free software companies with thousands of employees and contractors.  [I don't understand why.](https://blog.licensezero.com/2018/09/14/free-to-take-freedom.html#extra-freedom)  Arguably, their newest, strongest license skirts this rule.

Many developers and upstart projects, like Netscape starting Mozilla and Torvalds starting Linux, choose copyleft licenses explicitly to receive changes back from their users.  When unable to write their own licenses, like Mozilla, they often repurpose FSF licenses, like Linus.  In the early 2000s, the Open Source Initiative approved a few strong-copyleft licenses specifically drafted to bring patches back, without the FSF's self-imposed limits.  Some of these licenses required sharing back private changes.  Others shifted from requiring developers to share source with _users_, as under the FSF's licenses, which focus on end-user freedom, to sharing source with the original developer, or even publishing online, to ensure the _developer_ got the patches.  The FSF rejected these licenses as beyond its limits.

The second reason strong-copyleft licenses have fallen short of "free for open" will be familiar to every vocational programmer.  The idea of copyleft was a glorious, glorious hack, legally and coder-culturally.  Strong-copyleft implementers seem to have delighted in this hackishness, writing oddly low-level legal terms that proved just enough to get "free for free software" functionality at the time, in unnecessarily clever ways.  As new means of using and reusing software became common, these oddly specific terms and their tight coupling to their times proved predictably brittle, allowing ever more use of strong-copyleft software in closed projects.  The "free for free software" licenses became "mostly free for free software, unless you know the holes and fit through them".  Crack the hacker licenses.

The most infamous bug was and remains the "ASP Loophole", alias "SaaS Loophole" and "Google Problem".  The GPLs require sharing source for new work on the same terms only if the licensee distributed the changed software to others outside their organization.  But licensees don't distribute copies of software that they run for end-users to access over a network, like Web applications or peer-to-peer applications.  As a result, the GPLs don't require them to share source or give licenses for their work, which can remain closed and non-free.

Strong-copyleft drafters responded by writing the smallest license patches possible to close the vuln.  The relevant diff between GPLv2 and AGPLv1 is just one new numbered item in the rule on distribution.  The relevant diff between revised GPLv3 and AGPLv3, which many in the free software community wanted to merge into a single new GPLv3, but couldn't due to proprietary development pressure, is a single paragraph buried in section 13.  When Technical Pursuit found the network-copyleft licenses available to it wouldn't effectively reach all the code in apps using its web framework, it patched the definition of "Deploy" from [Sybase/Open Watcom](Sybase/Open Watcom), and tacked on a definition of "Required Components", all in an unsightly, 5,000-word, enterprise-EULA-style form.  Now that [MongoDB](https://www.mongodb.com/), a longtime, high-profiler AGPLv3 licensor, has found competitors exploiting loopholes in that license, it's proposing yet another patch to GPLv3 section 13 as the [Server Side Public License](https://www.mongodb.com/licensing/server-side-public-license).

Current strong copyleft licenses aren't cathedrals, and they aren't from any bazaar.  Even when rewritten entirely, they've developed by intellectual accretion, tied up in the past, demonstrably by committee, with the best of talent and intentions.

# Maintenance Hell

All of this hack-and-patch complexity makes it damn difficult for even plucky self-starters to answer two basic questions:

1. Which open source license do I pick to make my software "free for open source"?
2. Can I use this work I found under such-and-such "free for open source" license in my project?

Companies pay me hundreds, sometimes thousands of United States Dollars to answer these questions.  Which is ridiculous.  Especially when my answer is "no good option" or "no clear answer".  Especially when I have to interrogate at least one engineer, and cave dive into at least one codebase, before I can deliver the bad news.

There are some easy cases.  But you can't spot them confidently without spending a whole lot of time reading, analyzing, and talking about copyleft legacy systems first.  The best heuristic is general old-fashionedness.  The closer the software being licensed, and the software people will want to make with it, to the way things were done back in 1989, the better the chance of a solid, effective answer.

If I could write "Which license?" as a chat bot, I would.  That wouldn't do anything for the people who have to read:

```
No option for you.
Please rate my service today...
```

It might help some of the rest.  Unfortunately, I can't.  The decision tree is too wide and too deep.  Even when there is an answer, it always comes with an expiration date, waiting for new vulnerabilities.  Many prior copyleft implementations are electively coupled to legal definitions, which [change on us](https://en.wikipedia.org/wiki/Oracle_America,_Inc._v._Google,_Inc.).  In the end, "Which open source license do I pick to make my work free for free only?" is putt it the right way, but can't be answered in the same good terms in which it's asked.

If I could write "Can I use this?" as a program to run in continuous integration, I would, too.  I tried.  In the end, it involved far too much configuration, even within the relatively modern, consistent playpen of npm, under the conventions of that single ecosystem.  The [program](https://www.npmjs.com/package/licensee) I use personally and with clients requires a whitelist of licenses.  To avoid that format, I'd need a file full of flags corresponding essentially to the questions that I'd ask a client, as their lawyer, in order to map to licenses for a whitelist.  Whether I ask for licenses or legal assessments that point to licenses, if I'm asking developers, I'm asking for trouble.  That isn't solving the problem.  It's turning the easy parts into software, pushing the hard parts onto the user, and slapping `"AS IS", WITHOUT WARRANTY OF ANY KIND` on it.

A mess in the legal, and no software salvation in sight.  Where does that leave us?

Permissive licenses seem to get simpler.  Not necessarily better, but simpler.  Sometimes [dangerously so](https://opensource.org/licenses/FPL-1.0.0).

Meanwhile, copyleft gets more complex, and seems to get worse.

Copyleft is thrashing in the tar pit.  It can't get out of where it is now, and where it it, it's sinking.

# Refactor

So I trod off to fresh ground, and wrote a new license: The License Zero Noncommercial Public License.  I pasted the noncommercial bits of Creative Commons' CC-BY-NC into BSD, and went from there.  Lots of work modernizing the base terms.  Now it's [Prosperity].

Some of my friends and colleagues won't use a noncommercial license.  They insist on copyleft, but not on the FSF's compromises or self-limitations.  So I wrote another license: The License Zero Reciprocal Public License.  I pasted "free for open source" into BSD, and went from there.  Modernized the base terms.  Split it out into three rules, for clarity.  Required sharing alike, but not necessarily on the same terms, to avoid some compatibility headaches and facilitate some new collaborative licensing models.  After a few months through the tar pit, the escaped survivor became [Parity].  Lots and lots of good feedback from there.

The decision tree for developers into and out of License Zero is now pretty simple.

If the majority of people will use your software to make other software, consider [Parity].  Application?  Library?  Framework?  Toolkit?  Plugin?  Front-end?  Back-end?  Peer-to-peer?  Compiled?  Interpreted?  Distributed?  Interpreter?  Package manager?  Dev tool?  Doesn't matter.  [Parity] it is.

If the majority of people will use your software to do something else, consider [Prosperity].

The decision tree for users is much simplified, too.

Building closed software?  You need private licenses for [Parity] code.

Doing commercial work?  You need private licenses for [Prosperity] code.

Static or dynamic linking?  Distributed or networked application?  Modified or unmodified use?  Production or development dependency?  Doesn't matter.  See above.  And `licensezero quote --help`.

# Apologia

If you're running a dual licensing play with GPL or AGPL or OSL or RPL or, heck, even Sleepycat, I'd love to help you.  But License Zero and your project's license would not be good for each another.  License Zero can only complicate itself by [reverently binging itself to the mast of the past](https://blog.licensezero.com/2018/05/13/commons-club.html#past).  Standing where we are now, I can't place license history above either developers or users, or pretend that their needs pale in comparison to network benefits in emerging language communities.

As it turns out, radical copyleft and noncommercial licenses, while gnawing for those, like me, who have invested in the old terms and their vagaries, turn out to be simpler for eschewing compromise.  By taking the community's intentions and understandings and writing them into legal terms, License Zero avoids the complexity of dictating to practice from theory and history.  That, in turn, makes room in the complexity budget for the software and other conventions---metadata, private licenses, collaboration management---that close the loop for developers looking to stay independent while bootstrapping their projects.