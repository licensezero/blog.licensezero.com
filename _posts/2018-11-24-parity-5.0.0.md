---
title: Parity 5.0.0
description: Listen to devs. Write a better license.
layout: post
---

Happy to announce the release of version 5.0.0 of the Parity Public License!

This new major version greatly improves clarity in use by companies, in addition to  individual developers.  Additional wording tweaks improve readability, reduce repetition, and increase consistency.

The [text of the license](#license-text) follows.  At less than three hundred words of plain English, every interested developer should read it.

After the text, I'll take the opportunity to [walk through the license, line-by-line](#line-by-line), with notes and comments.

# License Text

```text
The Parity Public License 5.0.0

Contributor: {Licensor Name}

Source Code: {https://example.com/project}

This license lets you use and share this software for free, as
long as you contribute software you make with it. Specifically:

If you follow the rules below, you may do everything with this
software that would otherwise infringe either the contributor's
copyright in it, any patent claim the contributor can license
that covers this software as of the contributor's latest
contribution, or both.

1. Contribute changes you make to this software.

2. If you run or combine this software with other software as
   part of any larger application, contribute that application.

3. Contribute software you develop, deploy, monitor, or run with
   this software.

4. Ensure everyone who gets a copy of this software from you, in
   source code or any other form, gets the text of this license
   and the contributor and source code lines above.

5. Do not make any legal claim against anyone for infringing any
   patent claim they would infringe by using this software alone,
   accusing this software, with or without changes, alone or as
   part of a larger application.

To contribute software, publish all its source code, in the
preferred form for making changes, through a freely accessible
distribution system widely used for similar source code, and
license contributions not already licensed to the public on terms
as permissive as this license accordingly.

You are excused for unknowingly breaking 1, 2, or 3 if you
contribute as required, or stop doing anything requiring this
license, within 30 days of learning you broke the rule.

**This software comes as is, without any warranty at all. As far
as the law allows, the contributor will not be liable for any
damages related to this software or this license, for any kind of
legal claim.**
```

# Line-by-Line

Parity 5.0.0 breaks down logically like so:

- [Header](#header)
  - [Title and Version](#title-and-version)
  - [Contributor Line](#contributor-line)
  - [Source Code Line](#source-code-line)
- [Summary](#summary)
- [License Grant](#license-grant)
  - [Rules Qualification](#rules-qualification)
  - [Permission](#permission)
  - [Copyright Scope](#copyright-scope)
  - [Patent Scope](#patent-scope)
- [Rules](#rules)
  - [Contribution Rules](#contribution-rules)
    - [Rule 1](#rule-1)
    - [Rule 2](#rule-2)
    - [Rule 3](#rule-3)
  - [Rule 4](#rule-4)
  - [Rule 5](#rule-5)
- [Contribution Instructions](#contribution-instructions)
- [Automatic Excuse](#automatic-excuse)
- [Limits on Liability](#limits-on-liability)
  - [Warranty Disclaimer](#warranty-disclaimer)
  - [Damages Exclusion](#damages-exclusion)

## Header

#### Title and Version

>  The Parity Public License 5.0.0

The Parity Public License descends from an earlier effort, The License Zero Reciprocal Public License.  Almost nobody seems to need explanation for the name change.  "The Parity Public License" is straightforward, evokes the overall purpose, non-redundant, and shortens neatly to "Parity".

I haven't followed any particular versioning scheme.  But generally speaking, I've bumped patch for small technical corrections, minor for additions or tweaks that merely improve on the prior version, and major for any change that I think warrants special attention.  I've been very wiling to bump major, bringing us to 5.0.0.

#### Contributor Line

>  Contributor: {Licensor Name}

##### Modern-Day Copyright Notice

This line serves much the same purpose as the copyright notice lines in MIT- and BSD-family licenses.  In years long past, copyright law required copyright notices specifically, in order to claim copyright in the work.  Under the [Berne Convention](https://en.wikipedia.org/wiki/Berne_Convention), as implemented in various countries, that's no longer necessary for copyright.

However, it's still legally and practically important to ensure developers' names stick to their software.  The names make clear who is giving the license, and who is protected by the [limits on liability](#limits-on-liability) that come later.  If the law ends up interpreting the license terms as a contract between contributor and user, rather than just a license, the name makes clear who that contributor is.  More practically, developers deserve credit for their work.  Names in licenses aren't a complete solution to open source credits, [that takes specific terms](https://github.com/berneout/posterity-public-license), but name lines are traditional.

##### No More First Person

Before 5.0.0, Parity spoke in the first person, from the developer giving the license.  For example, the license grant read, in part, "...you may do everything with this software that would otherwise infringe either my copyright in it...".

That made for a very clear, short license.  However, it also made awkward reading when the one giving the license was a corporation or other legal entity, rather than an individual.  English speakers aren't used to reading messages in the first-person singular from companies.

I used the first person singular anyway because the majority of open source contributors remain individuals, and I expect most developers using Parity for their work will also be individuals.  I still believe that's true.  But I no longer believe that Parity should optimize for individual licensors _over_ company licensors. 

Functionally, Parity wants to be a minimal, generic legal tool.  Politically, Parity wants to be useful to a coalition of different legal "user groups", not niched to any particular activist group or business use case.  Parity appeals to developers who want all software to be open, and need a stronger set of terms to close loopholes in existing strong-copyleft licenses.  Parity _also_ appeals to developers that want a strong-copyleft license for dual licensing, through licensezero.com or otherwise, and to prevent closed-software competitors from putting them out of business.

Legally, there's no telling whether users of the license will act as individuals, or through companies.  Even many independent developers act through companies, often limited liabilities companies, or LLCs, for tax and legal reasons.  Foundations are sprouting up like mushrooms, and even traditionally anarchic activists are getting better at setting up entities.

I believe that prior versions of Parity supported individual and entity licensors equally well, from a legal point of view.  But company licensors took a readability penalty.

Parity 5.0.0 equalizes readability.  Everyone who wants Parity's functionality should read it as a license that suits their needs.  Everyone who wants that functionality should feel welcome to pick the license.

##### Choice of the Term "Contributor"

Parity isn't the first public software license to use this kind of notice line for the developer's name.  Most recently, the [Fair Source License](https://fair.io/) did so with the legal term "licensor".

Parity 5.0.0 uses "contributor", for a couple reasons.  First, while "licensor" is legal jargon, "contributor" is commonly used among developers.  Developers readily recognize themselves as "contributors" without checking a dictionary.  Second, Parity uses the words "contribute" and "contribution" elsewhere, both in the text of the license granted to users, and in the rules that require users to share back.  Symmetry across licensor terms and licensee terms emphasizes the point of license: parity between them.  Parity requires users who make software to be contributors, too.

#### Source Code Line

> Source Code: {https://example.com/project}

In addition to a blank for the licensing developer's name, Parity has a blank for an address, like a URL, pointing users to source code.  [Rule 4](#rule-4) requires users to keep copies of _both_ the contributor and source code lines with copies of the software.

Source notice is especially important, since Parity doesn't follow the GPLs and similar copyleft licenses in requiring those who share copies of Parity software to also share source code.  As we'll see below, Parity instead requires those who build on Parity software to _publish_ source for their software where it's likely to be found.  That means users of compiled software built with Parity code won't necessarily receive source with their binaries, but _will_ receive notices that help them find source code for at least the original distribution of the Parity code.  Parity's [instructions for contribution](#contribution-instructions) work to ensure they will be able to find source code for any changes, too.

## Summary

> This license lets you use and share this software for free, as long as you contribute software you make with it.

Parity uses plain language, so coders can read it for themselves and get a working understanding of what it does.  Coder readability, along with short length, have been and will remain key goals of the license.

All the same, Parity starts with an additional, high-level summary of purpose.  That summary not only gives new readers a framework for Parity's rules to have in mind as they read, but also provides a fallback statement of legal intent.  When courts reach vagueness or ambiguity in legal terms, standing on their own or in application to specific cases, they can use expressions of intent within the "four corners" of the document they're trying to interpret to resolve.

No public software license is completely clear in all circumstances.  The English language isn't capable of that, and formal, constructed languages can't adequately describe all relevant circumstances.  But in comparison to other licenses with share-alike rules, like the GPLs, Parity does trade precision and detail for clarity and brevity.  That does _not_ make Parity an inferior license, taking its purpose and environment into account.  Within limits, readability increases what can be done without legal assistance, decreasing friction.  Brevity makes the license easier to understand, as well as to draft, reducing the amount of material to fit in the head at once, as well as the potential for unexpected interactions between those terms, under the legal rules for reading license language.

The open software community continues to favor short, academic-style licenses, despite their age and several known deficiencies, perhaps in part for these reasons.  We will see the same trade-offs again and again, throughout Parity's terms.

> Specifically:

"Specifically" helps to clarify that the summary is just an overview, to be overridden by the more specific language that follows.  The main operative terms of the license follow the colon.

## License Grant

> If you follow the rules below, you may do everything with this software that would otherwise infringe either the contributor's copyright in it, any patent claim the contributor can license that covers this software as of the contributor's latest contribution, or both.

This language does the main work of the license, granting permission to do what intellectual property rights, specifically copyright and patents, would prevent.

### Rules Qualification

> If you follow the rules below, ...

"Follow the rules" is plain English, not legal English.  "Rule" has no specific legal meaning in this context, leaving a court to read in its common meaning.

Placing this phrase _before_ the language giving permission alerts readers that they can't just read up to the part they like---permission for the software---and stop.  They have to pay attention to the rest of the terms, too.

In legal practice, rules that come with a license can take two legal forms:

1. _License conditions_ limit what someone is allowed to do under their license.  If the license is a copyright license, breaching a condition of that license leaves the user open to a copyright infringement lawsuit.
2. _Contract covenants_ are promises the other side can enforce under the law of contracts.  If the one giving the promise fails to keep it, the side receiving the promise can sue for breach of contract.

There is a long-running debate about whether public licenses for software are just licenses, just contracts, can be both, or must be both.  The Free Software Foundation has always included terms in its GPL licenses saying that the GPLs are just licenses, and not contracts.  Other software licenses, like Apache 2.0, MIT-family licenses, and BSD-family licenses, don't say anything about license-or-contract.  Public licenses for other media, like Creative Commons forms, make clear that courts _could_ read them as contracts, but don't try to force any specific conclusion.

Parity mostly ignores this debate, since it doesn't appear to matter much, in practice.  American courts considering these kinds of licenses tend to approach public software licenses both ways.  They use contract-law rules to interpret terms.  But they allow both contract and copyright-based legal claims for breaching those rules.  Parity's terms don't go out of their way to limit Parity developers to one legal theory or another, for enforcement.

### Permission

> ... you may do everything with this software that would otherwise infringe either ... or both.

Popular public licenses for software write their permissions, or license grants, in two major styles:

1. _Academic-style terms_ like MIT- and BSD-family forms use generic terms without any specific legal meaning, or a mishmash of legal terms from both patent and copyright.
2. _Enterprise-style terms_ like Apache 2.0 copy long lists of specific verbs from the laws that define copyright and patent infringement, with separate sections for the copyright license and patent license.

Academic-style terms pose interpretive problems.  It's often unclear whether they grant effective patent permission, or whether or how they cover all the things that count as copyright infringement.  This is why many guides to open source licensing recommend Apache 2.0 over MIT or BSD when patents are a concern.  But such enterprise-style terms also tend to run long in their permission language, scaring away non-lawyer readers and hiding the overall point of those provisions.

The overall point is that these licenses don't cherry-pick specific exclusive rights of copyright and patent holders.  They're meant to be _total licenses_, to keep users who follow the other rules from getting sued for infringement, whatever they do, as long as they follow the other license rules.

There is nothing to stop a public software license from saying this directly.  So that is what Parity does.

The approach does bury a bit of legal detail.  Permission is only to do things that would count as infringement.  That does _not_ include privileges that only owners of copyright and patent have, such as assigning ownership.

The word "either" begins a list, with two phrases, [one for copyright](#copyright-scope), and [one for patent](#patent-scope).

One action may infringe both copyright and patent.  For example, sending a customer a copy of software for pay might count as both distributing to the public under copyright law and selling under patent law.  The "either ... or both" construction make explicitly clear that "or" is not exclusive.

### Copyright Scope

> ... the contributor's copyright in it ...

Completing the previous phrase, "you may do everything with this software that would otherwise infringe [the contributor's copyright in it]" grants a total copyright license.  The contributor is the individual or legal entity identified [on the contributor line](#contributor-line).

It's relatively easy to identify _which_ copyright a public software license has to cover: copyright in the software.  As we'll see, it's not so easy for patent.

### Patent Scope

> ... any patent claim the contributor can license that covers this software as of the contributor's latest contribution ...

Popular "academic" licenses like MIT- and BSD-family forms create patent uncertainty in two primary ways: by failing to grant clear patent licenses to begin with, and if they do, by failing to specify what patents, if any, they cover.

Enterprise-style licenses put patent-permission language in its own section, use the word "patent", and describe what patents they cover at some length.  [Apache 2.0 section 3](https://www.apache.org/licenses/LICENSE-2.0#patent) exemplifies.

Parity follows academic style in granting all permission in a single sentence, but follows enterprise style in explicitly mentioning both "copyright" and "patent", and taking some time to address _which_ patents get covered.

Language setting the scope of a public patent license has to balance three major interests:

1. Users want to know which versions of the software are "safe" from patent suit by contributors, even if they don't know which patents might apply.
2. Contributors want control over which patents they license.
3. Both users and contributors want clarity, if they end up in a patent infringement lawsuit.

Parity follows Apache 2.0 in its general solution to this problem:  Contributors license all the patents that cover the work they contribute, as well as the work of others that was part of the project when they contributed.

Parity departs from Apache 2.0 in putting this rule as succinctly as possible, without explicitly defining what does and does not count as a "contribution".  Apache 2.0 spends many words defining both "Contribution" and "submitted", a term used in that definition.  But the terms of those definitions are themselves very broad, so as to avoid specializing the Apache license to any particular development methodology or toolkit.

My read of those definitions calls out three key effects:

1. Work must be submitted _intentionally_ to be covered.

   I'm not sure what this achieves.  Would work submitted accidentally count as being submitted intentionally?

   Parity uses "the contributor's latest contribution". I do _not_ believe "contribute" is commonly used to describe involuntary or inadvertent action.  That's buttressed by the fact that users will only receive reliable licenses on Parity terms for contributions if those licensing it manifest their choice to license, and document it.

2. Others can submit work that's covered on behalf of the copyright owner, with their permission.

   This is practically necessary, since companies often own the rights in work by their employees and contractors, and give those employees and contractors permission to contribute back.  Apache 2.0 could strengthen this by requiring written permission.  As for Parity, I believe the common meaning of "contribution" would cover work an entity directed to be contributed.

3. Submission happens by communication to the "Licensor".

   Apache 2.0 gets used by many organizations, and by many projects.  But it was written originally for projects hosted by the Apache Software Foundation, which collects all rights in its projects via contributor license agreements, and licenses the results to the public, rather than relying on all contributors to license their work independently.  Apache 2.0's language on patent scope makes most sense with a single "Licensor".  There's nothing to stop multiple contributors from granting independent Apache 2.0 licenses for their contributions to a single project.  But it gets much harder to the language in those cases.  Is it enough to "submit" a patent-leaden contribution to _any_ Licensor?

   As a practical matter, I think many projects that use licenses like Parity will come from specific companies.  But Parity doesn't _require_ that one individual or entity hold all the rights that need to be licensed.  As a result, it cannot assume that there is or always will be any particular person or entity to receive all contributions.  Parity projects may be abandoned by their original developers, or taken up by successors.

4. The magic words "Not a Contribution" keep work that would otherwise get covered from becoming a "Contribution" under the license.

   Magic words can achieve clarity.  As a practical matter, I don't know how many companies or developers aware that Apache 2.0 does this.  But when you need it, it's nice to have it.

   Again, since Parity doesn't address contribution back, but only speaks from one contributor to the public, there's less risk of accidental contribution.

Overall, Parity 5.0.0 uses "contributor", "contribution", and "contribute" to describe not just what the licensor is licensing, but also what licensees must share back, and how.  Parity therefore develops the idea of "contribution" implicitly, by usage, rather than formally, by definition.  When Parity's own usage of "contribute" doesn't suffice, courts will fall back to meaning in the industry, if there is one, and finally to plain meaning, in everyday English.  Parity might achieve more clarity with explicit definitions, but at a significant price in length and readability.

## Rules

The [rules qualification](#rules-qualification) to the license grant makes clear that users get licenses subject to the numbered rules that follow.

### Contribution Rules

The first three rules require users to contribute software they make with the licensed software in various ways.

Why use three rules to express a single, general rule that if licensees use the licensed software to make software, they have to contribute that software, too?  In experimental drafts, I've combined rules 1, 2, and 3 into a single rule.  While shorter overall, that approach creates an unavoidably long rule full of unavoidably broader terminology.  Developers who've seen those drafts have scratched their heads, especially if they have experience of existing copyleft licenses, like GPLs.  Three rules, two relatively specific, and one very broad, seem to strike the right balance of clarity, readability, and reader confidence.

Note that in contrast with prior copyleft licenses, none of Parity's three requires to contribute software gets tied to "distributing" or "conveying" a copy to anyone else, or offering to others as a network service.  For example, Rule 1, which covers changes to the software, in pseudocode:

```javascript
if (changed) contribute()
```

Rule 3 does _not_ say:

```javascript
if (changed && (distributed || service)) contribute()
```

Popular strong copyleft licenses before Parity, like [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html), almost always limited their contribution rules in this way.  That approach had the effect of giving users unlimited, and sometimes explicitly expanded rights to make and use what the Free Software Foundation calls "private changes".  The FSF has in fact rejected three licenses approved by the Open Source Initiative---Plan 9, Open Watcom, and the Reciprocal Public License---for requiring users to share back otherwise private changes that they make.

[I don't understand why the FSF requires permission to make and use private changes, especially within large organizations.](https://blog.licensezero.com/2018/09/14/free-to-take-freedom.html#extra-freedom)  The more I look into it, the more it seems a unilateral compromise, a kind of appeasement, rather than a hard stance on any articulated principle.  Moreover, it makes the task of writing an effective strong-copyleft license a great deal harder.

GPLs only require contributing source code when the licensee distributes copies of that new work to others.  That created the ASP loophole: developers writing network services, like web apps, don't send copies of their server code to end users.  As a consequence, they don't trigger GPL's requirement to share and license source code.

AGPL attempted to close that loophole by adding an additional way to trigger: providing a network service.  [The new trigger itself has loopholes.](https://writing.kemitchell.com/2018/11/04/Copyleft-Bust-Up.html#bounty)  New licenses, like MongoDB's SSPL [explicitly aim to closed them](https://www.mongodb.com/licensing/server-side-public-license/faq).  But if the goal is to prevent users making changes without contributing back, the surest way is not to add any additional trigger at all.  Require contribution of changes, full stop.

Parity follows licenses like the [Reciprocal Public License 1.5](https://opensource.org/licenses/RPL-1.5) in this approach.  From a license-politics point of view, that begs controversy.  OSI and FSF clearly disagree on private changes, and there's no sign they can or will reconcile.  But popular free/open license politics ignore [how many developers pick FSF copyleft licenses wrongly believing they actually require patches back](https://writing.kemitchell.com/2018/08/28/Unhappy-Coincidences.html#software-freedom-doesnt-mean-patches-back), or because a GPL is as close as they can get without controversy.  Linus has [given that very rationale for his choice of GPL for the kernel](https://youtu.be/1Mg5_gxNXTo?t=47m20s).

#### Rule 1

> Contribute changes you make to this software.

Rule 1 requires users who change the licensed software to contribute their changes.  [Instructions for contributing](#contribution-directions) come later.

Note that Parity doesn't introduce unnecessary distinctions about which kinds of changes users must contribute. There's no other technical distinction to clarify the boundary between covered and not covered, as under the [Eclipse Public License](https://www.eclipse.org/legal/epl-2.0/) or [Mozilla Public License](https://www.mozilla.org/en-US/MPL/2.0/).  Parity doesn't want any such line.  All changes must be contributed.

Seeing the ability to make "private changes", discussed above, as a loophole, rather than a feature, Rule 1 closes the private changes loophole.  The [Reciprocal Public License](https://opensource.org/licenses/RPL-1.5) took the same step, explicitly, almost twenty years ago.

#### Rule 2

> If you run or combine this software with other software as part of any larger application, contribute that application.

Rule 2 requires users who build Parity code into applications to contribute those programs.  Per the [instructions for contributing](#contribution-directions), that means contributing _all_ the source code for the application.

Licenses like the GPLs tend to express this idea in terms of a "larger program", rather than a "larger application".  Those approaches risk missing parts of broader systems comprised of many "programs", or arguably no "programs" at all.  Applications compromised of many interconnected services, deployed to containers or virtual machines, fall under Rule 2, but arguably not under existing, program-focused contribution rules.

Note again that Parity doesn't introduce unnecessary distinctions.  There's no library-linking exception, as under LGPL.  There's no static-dynamic linking distinction, as under some readings of GPL.  It doesn't matter _how_ users make Parity code a part of larger applications, only that they do.

If anything, Rule 2 may go broader.  I've considered replacing "larger application" with "larger piece of software", to avoid any argument that "application" excludes system software, or incomplete software components, like frameworks.  I've seen some rather specific definitions of "application" in distinction from other categories.  But so far, those distinctions seem largely the product of would-be taxonomists, without effect on common usage, which will affect how courts read the terms.

#### Rule 3

> Contribute software you develop, deploy, monitor, or run with this software.

As far as I'm aware, Rule 3 is entirely unique in public software licensing history.

The purpose of Rule 3 is to allow developers to offer "free for open source" terms for development tools.  By development tools, I mean software that that other developers use to develop software not by changing or building upon, but by running.  Compilers.  Linters.  Bundlers.  Minifiers.  Interpreters.  Debuggers.  Formatters.

No existing open source software licenses require sharing code built with open source back as open source.  That fact denies activists the ability to give other open advantageous access to their work, and denies business-minded developers the ability to use open source dual licensing business models with such tools.  My point of view, shared with developers who've faced that licensing gap in their work work and business, sees that gap as a loophole, a dev tools loophole.

Rule 3 has provoked by far the most controversy among open source licensing analysts.  I won't recap those debates, many of them long and tiring, here.  I have always conceded that this kind of rule is new in open source licensing.  I continue to maintain that it's consistent with the writing, purpose, and principles of both open source and free software, based on how those principles have been articulated.  Rule 3 is new.  Rule 3 is radical.  In many situations, Rule 3 is necessary.

For additional thoughts on Rule 3 under the Free Software Foundation's definition of free software, see my prior post, [_Free To Take Freedom_](https://blog.licensezero.com/2018/09/14/free-to-take-freedom.html).

For notes on how the Open Source Definition regulates---or more accurately, doesn't effectively regulate---the use of copyleft as in Rule 3, see [my analysis of the Definition's copyleft rules](https://writing.kemitchell.com/2018/11/05/OSD-Copyleft-Regulation.html).

Finally, note that Rule 3 acts as a fallback or catch-all contribution rule in some circumstances.  The verb "develop" is particularly broad.  If we rewrote all of Parity's contribution rules into a single contribution rule, "develop software" would be candidate for its most important term.  The [summary](#summary) comes close with "software you make with [the licensed software]".

### Rule 4

> Ensure everyone who gets a copy of this software from you, in source code or any other form, gets the text of this license and the contributor and source code lines above.

Rule 4 mirrors "attribution conditions" found in the overwhelming majority of open source licenses, permissive or copyleft.  See, for example, [the second paragraph of the MIT License](https://spdx.org/licenses/MIT.html), and [clauses 1 and 2 of the two-clause BSD license](https://spdx.org/licenses/BSD-2-Clause.html).  Copies of the software must come with copies of the license and its notices.

Rule 4 differs slightly from most existing open source licenses to preserve _two_ notices: the contributor line, analogous to copyright notices in prior licenses, and the source code line, peculiar to Parity.  Requiring that users pass along word on where to find source code---and potentially, where to contribute back---helps to prevent users from ending up with software they're told is open source, but with no way to find that source.

As a practical matter, I expect most Parity licensors to list a GitHub repository address or project homepage URL on their source code lines. 

### Rule 5

> Do not make any legal claim against anyone for infringing any patent claim they would infringe by using this software alone, accusing this software, with or without changes, alone or as part of a larger application.

Rule 5 implements a "defensive termination" or "patent termination" provision.  These provisions are common in recent open source licenses, especially licenses that address patents explicitly.  The overall gist: If someone sues _you_ for patents, they don't get to use your open license to stop you suing back.

Rule 5 largely follows the approach of [Apache 2.0 section 3](https://www.apache.org/licenses/LICENSE-2.0#patent), the current benchmark for enterprise-friendly, patent-aware open source terms.  Rule 5 triggers on a patent claim against anyone, not just the original developer or a named organization.  Once triggered, Rule 5 ends all permission granted for the software, not just patent permission.

Note the reuse of "legal claim", "patent claim", "infringe", "changes", and "larger application".  Rule 5 parallels terms in the [patent permission](#patent-scope) language above it and the [damages exclusion](#damages-exclusion) below it, developing their meanings by consistent usage.  That development can help in legal disputes, as evidence of what the terms meant in context.  It also helps coders and other non-legal readers understand a few of the unavoidably legal terms sprinkled throughout the otherwise plain-language text.

## Contribution Instructions

> To contribute software, publish all its source code, in the preferred form for making changes, through a freely accessible distribution system widely used for similar source code, and license contributions not already licensed to the public on terms as permissive as this license accordingly.

Parity's [contribution rules](#contribution-rules) say when and what users must contribute back.  These instructions say how.

### Definition of "Contribute"

> To contribute software, ...

The [three contribution rules](#contribution-rules) all require users to "contribute" various kinds of software.  This part connects to the rules by defining "contribute".

### Publication of All Source Code

> ... publish all its source code ...

Parity departs from most popular copyleft licenses to date in requiring that users share back not by giving source code to downstream users, but by requiring them to publish source code so that the public at large can find and access it.  As a practical matter, this is how cooperative users of copyleft code choose to make source code available, anyway.  Even uncooperative copyleft users _made_ to share source code by license enforcement often post source code online, rather than distribute copies of source code to each recipient of the software who didn't get a copy to begin with.

Note that as with [the contribution rules](#contribution-rules), Parity's instructions for contributing source code don't draw any unnecessary lines between source code that does and does not need to be contributed.  _All_ source code for the software covered by the rule must be contributed.  For example, under [Rule 2](#rule-2), all source code for the "larger application" that the licensed software is made "a part of" must be contributed.

### Preferred Form

> ... in the preferred form for making changes ...

Parity follows the language of existing copyleft licenses, like the [GPLs](https://www.gnu.org/licenses/gpl-3.0.en.html#section1), as well as [language in the Open Source Definition](https://opensource.org/osd#include-source-code), in requiring the preferred form of source code.  Contributing just minified, generated, or other intermediate source code content doesn't satisfy Parity's contribution rules.

### Distribution System

> ... through a freely accessible distribution system widely used for similar source code ...

This phrase ensures that new contributors publish their work such that others can find it and get copies of it.  The specific language attempts to abstract past and current preferred methods for open source collaboration, from shell accounts to FTP servers, web directories, package repositories, and collaboration platforms.

This language also honors diversity in development communities' preferences.  Parity puts the burden on the new contributor to determine which system is widely used for source code like the source code they must contribute, and to use that system.

Alternatively, Parity could put the whole burden of choosing the proper distribution system on the new contributor.  For example, Parity could require publication where users will expect it, where they'll be able to find it, and where they'll be able to get it free of charge.  That would go more directly to the goal of the license.  But I've avoided that approach to date, because readers seem to stumble on terms written that way, while they readily jump from the current language to a particular system in mind.

### Contribution Licensing

> ... and license contributions not already licensed to the public on terms as permissive as this license accordingly.

All effective copyleft licenses require _both_ sharing source code _and_ licensing it under acceptable terms.  Parity differs from prior copyleft licenses by substantially loosening its licensing requirements.

First, Parity only requires licensing code that isn't already licensed on qualifying terms.  If part of the source code to be contributed is already available under qualifying open terms, the developer needn't republish, relicense, or avoid that source code.

Second, Parity doesn't require contributors to use Parity terms for their work.  Any terms at least as permissive as Parity qualify.

Open source license specialists, and especially open source license specialists who aren't lawyers and don't regularly work with other kinds of software licenses, often use "permissive" in a specific way.  In particular, "permissive" contrasts with "copyleft" or "reciprocal", as a category.  On a scale from maximally permissive terms, like [0BSD](https://spdx.org/licenses/0BSD.html), to maximally strong copyleft, Parity falls at the extreme strong end of copyleft.  Seen this way, Parity might be the least permissive open software license ever written.  Any popular open software license is arguably "as permissive" as Parity, and moreso.

In the grand scheme of things, open source included, open software licenses are all incredibly permissive.  Without a license, copyright and patent law permit very little.  Everything which is not permitted is forbidden.  Open software licenses substantially reverse those defaults.  Everything which is not forbidden is permitted.

The phrase "as permissive" may be the most vague bit of language in Parity.  It's not precisely clear whether a court would look to the open-source-jargon meaning of "permissive", or its more general meaning.  It's not precisely clear how a court would analyze specific licenses, especially specific licenses with rules different in kind from Parity's.  For example, the the Artistic License 2.0 has rules about changing the name of a changed copy of the licensed program, to avoid conflicts with the name of the "Standard Version".  Artistic 2.0 therefore prohibits some actions that Parity permits, like changing the standard versions without yielding its name, while Parity prohibits some actions that Artistic 2.0 does not, like hoarding private changes.

Generalizing all the kinds of terms that qualify, or listing out specific qualifying licenses, would double or triple Parity's length.  Such an approach would amount to either a survey of open source licensing terms, or a near clone of an existing approved-license list.  It would also go out of date, inevitably, and require either ongoing maintenance or delegation to a decision making body.

None of that seems wise.  As written, Parity clearly permits many popular permissive licenses, especially popular academic permissive licenses like MIT- and BSD-family terms.  In parallel with Parity, I've drafted and released [Charity](http://licensezero.com/licenses/charity): a permissive license made from Parity, by removing Parity's contribution rules.  Sharing much of the same text, but with fewer rules, Charity is clearly more permissive than Parity.

I continue to experiment with terser ways to clarify Parity's rules for qualifying license terms.  For example, a future version of Parity might require terms that permit at least the actions that Parity does.  That would exclude licenses with peculiar conditions and requirements, like Artistic 2.0, but continue to qualify more licenses like MIT and BSD.  Please [share any ideas or feedback you may have](https://github.com/licensezero/parity-public-license/issues/new).

## Automatic Excuse

> You are excused for unknowingly breaking 1, 2, or 3 if you contribute as required, or stop doing anything requiring this license, within 30 days of learning you broke the rule.

Parity follows recent copyleft licenses, like MPL 2.0, AGPLv3, and GPLv3, in giving users who unintentionally break its [contribution rules](#contribution-rules) a way to avoid legal liability.  In essence, if you break one of those rules without knowing about it and find out later, you have thirty days to contribute the software you should have contributed to begin with, or to stop using the Parity-licensed code altogether.

It's very time consuming and difficult to prove, in a court of law, when a person or especially a company knew something specific.  However, developers using Parity have a direct way to establish knowledge: send the user breaking the rule a notice that they are violating the license.  Licensors can start the thirty-day countdown running.

## Limits on Liability

Parity follows nearly all prior open software licenses in doing as much as possible to limit the contributor's legal liability for the software they contribute.  Typically, these provisions include long, run-on lists of risks and claims and theories of liability, in `ALL CAPS`.

Parity differs by making these terms short and readable, set apart from other terms with asterisks.

### Warranty Disclaimer

> **This software comes as is, without any warranty at all.** 

By default, many countries' laws [imply promises about software, called warranties](https://oss.kemitchell.com/#warranties), unless terms say otherwise.  This sentence says otherwise, as clearly and succinctly as possible.

Under the Uniform Commercial Code, a standardized contract law adopted by the vast majority of the United States, "as is" are magic words for disclaiming warranties.

For in-depth comments on a more traditional warranty disclaimer, from the MIT License, see [my previous line-by-line on that license](https://writing.kemitchell.com/2016/09/21/MIT-License-Line-by-Line.html#warranty-disclaimer).

Finally, note that some jurisdictions, like England and Ireland, continue to make a dubious, technical distinction between "warranties" and "conditions".  [Courts remain bound by precedent, but do what they can to work around the pedantry.](https://ipdraughts.wordpress.com/2012/02/26/using-us-contract-templates-outside-the-us-it-can-be-a-bad-mistake/)  Parity's disclaimer mentions only "warranty", without catering to that anachronism.  Parity's damages exclusion has overlapping effect.

### Damages Exclusion

>  **As far as the law allows, the contributor will not be liable for any
> damages related to this software or this license, for any kind of legal claim.**

For in-depth comments on a more traditional damages exclusion, again from the MIT License, see [the corresponding section of my post](https://writing.kemitchell.com/2016/09/21/MIT-License-Line-by-Line.html#limitation-of-liability).  Those comments touch on my arguments for short exclusions like Parity's in public software licenses.

In brief, "As far as the law allows" avoids overtly misleading users in jurisdictions where some warranties can't be disclaimed.  The phrase "related to" accomplishes the desired scoping effect without the pointless legal doublet, "arising out of or related to".   The disjunction "this software or this license" follows [OSL](https://opensource.org/licenses/OSL-3.0) and [AFL](https://opensource.org/licenses/AFL-3.0).  The phrase "for any kind of legal claim" addresses some unfortunate American precedent holding the fact that terms describe a contract, rather than anything _in_ those terms, to limit damages only for contract claims, and not for tort claims.

# What's Next?

I will keep reading feedback!

Since rewriting The License Zero Reciprocal Public License, Parity's predecessor, in plain English, I've been overjoyed with the quantity and reliable _quality_ of feedback, especially from coders.  Signal-to-noise on this license, and the License Zero project more generally, has been incredible.  Parity 5.0.0 [came straight from user feedback](https://github.com/licensezero/parity-public-license/issues/25).  That is how open software licenses should develop.

Of course, I will also keep reviewing the license on a schedule, polishing and experimenting, setting it aside, and returning to it again as soon as it's fresh again.  There's no substitute for legal attention.  Parity has plenty.  I'm sure I'll give it plenty more.

As always, feel free to reach out.  [Issues are open in the license's GitHub repo](https://github.com/licensezero/parity-public-license/issues).  I check [the @licensezero Twitter account regularly](https://twitter.com/LicenseZero).  For a quick read, [e-mail](mailto:kyle@artlessdevices.com) is always best.