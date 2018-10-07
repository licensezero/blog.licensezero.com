---
title: The Parity Public License 3.0.0, Line by Line
layout: post
---

License Zero offers two choices of public licenses: [The Parity Public License](https://licensezero.com/licenses/parity), a strong-reciprocal or radical copyleft license, and [The Posterity Public License](https://licensezero.com/licenses/prosperity), a noncommercial license.

As of this writing, Parity stands at version 3.0.0.  The [complete text of less than 300 very readable words](#text) appears below.  You should read that second.  A [line-by-line commentary](#commentary) follows, which you should read third.

But first, you _must_ read understand two points:

1.  ***If you need to understand what legal effect Parity may have, as a user or potential contributor of Parity-licensed software, speak to a lawyer.  This commentary is no substitute for professionally accountable legal advice.***

2.  ***The commentary that follows is my view, as the principal drafter of the license terms.  But in the end, a court's reading will determine rights and responsibilities under these terms, not my reading.***

# <a id="text"></a>The Complete Text

> The Parity Public License 3.0.0
>
> Copyright Notice: \{\{\{name}}}
>
> Source Notice: \{\{\{source}}}
>
> This license lets you use and share this software for free, as long as you contribute software you make with it. Specifically:
>
> If you follow the rules below, you may do everything with this software that would otherwise infringe either my copyright in it, any patent claim I can license that covers this software as of my latest contribution, or both.
>
> 1. Contribute source code for changes you make to this software.
>
> 2. If you run or combine this software with other software in any larger program, contribute all source code for that program.
>
> 3. Contribute all source code for software you develop, deploy, monitor, or run with this software.
>
> 4. Ensure everyone who gets a copy of this software from you, in source code or any other form, gets the text of this license and the copyright and source notices above.
>
> 5. Do not make any legal claim against anyone for infringing any patent claim they would infringe by using this software alone, accusing this software, with or without changes, alone or as part of a larger program.
>
> To contribute source code, publish the preferred form for making changes through a freely accessible distribution system widely used for similar source code, and license contributions not already licensed to the public on terms as permissive as this license accordingly.
>
> You are excused for unknowingly breaking 1, 2, or 3 if you contribute source code, or stop doing anything requiring this license, within 30 days of learning you broke the rule.
>
> **This software comes as is, without any warranty at all. As far as the law allows, I will not be liable for any damages related to this software or this license, for any kind of legal claim.**

# <a id="commentary"></a>Line-by-Line Commentary

## <a id="title"></a><a id="version"></a>Title and Version

> The Parity Public License 3.0.0

Parity derives from a prior license I called "The License Zero Reciprocal Public License".  I chose a new title for a few reasons:

1.  Further emphasize that Parity can be used without License Zero, or without dual-licensing at all.

2.  Cut down on the awkward repetition of "license" in "_License_ Zero Reciprocal Public _License_".

3.  Shorten the title, and create an obvious short name, "Parity", instead of begging an awkward acronym like "LZRPL".

4.  Emphasize the main theme of the license, sharing alike, without reusing a prior term like "share-alike", "reciprocal", or "copyleft".

I chose "Parity" because it's short, catchy, and on-point, but not too common in everyday conversation.  It begs some loose technical analogies.

All public licenses should have versions, and everyone involved should expect and encourage new versions with improvements.  Parity has benefited by incredibly insightful and constructive feedback, from lawyers and coders.  Version 3.0.0 will by no means be the last.  But 3.0.0 feels more settled, more stable, than at any previous point.

## Copyright Notice

> Copyright Notice: \{\{\{name}}}

Parity follows the "academic" or "template" style of providing a blank for copyright notice in the license itself, like MIT- and BSD-family forms.  Other forms, like the GPLs and Apache 2.0, work as fixed file texts to be copied into projects without change, expecting copyright and licensing notices in other source files.

I chose a template-style because I expect most of Parity's audience will be independent developers familiar with template-style terms, to better fit the trend of including all license information for a package in a single `LICENSE` file, and to make it clearer what [notice has to be retained with copies](#notices).  Template-style terms do tend to get inadvertently changed and reformatted more than fixed-form terms, but that risk is largely offset by rigorous versioning and the publication of official texts.

> Source Notice: \{\{\{source}}}

Parity uses the notice-you-must-preserve mechanism not just to preserve credit for developers, but also to help downstream users find source and the canonical distribution of Parity projects they receive indirectly, from intermediaries.  [Rule 4](#rule-4) requires preserving not just the copyright notice, but also this notice, which should usually contain the URL of a project homepage, project repository page, or source repository.

Source notice is especially important, since Parity doesn't follow the GPLs and similar copyleft licenses in requiring those who share copies of Parity software to also share source code.  As we'll see below, Parity instead requires those who build on Parity software to _publish_ source for their software where it's likely to be found.  That means users of compiled software built with Parity code won't necessarily receive source with their binaries, but _will_ receive notices that help them find source code for at least the original distribution of the Parity code.

## Summary

> This license lets you use and share this software for free, as long as you contribute software you make with it.

Parity uses plain language, so coders can read it for themselves and get a working understanding of its effect.  Coder readability, along with short length, have been and will remain key goals of the license.

All the same, Parity starts with an additional, high-level summary of purpose.  That summary not only introduces new readers to the general gist of Parity's rules, but also provides a fallback statement of intent.  When courts reach vagueness or ambiguity in legal terms, on their own or in application to specific cases, they can use expressions of intent within the "four corners" of the document they're trying to interpret to resolve.

No public software license is completely clear in all circumstances.  The English language isn't capable of that, and formal, constructed languages can't adequately describe all relevant circumstances.  But in comparison to other licenses with share-alike rules, like the GPLs, Parity does trade precision and detail for clarity and brevity.  That does _not_ make Parity an inferior license, taking its purpose and environment into account.  Within limits, readability increases what can be done without legal assistance, decreasing friction.  Brevity makes the license easier to understand, as well as to draft, reducing the amount of material to fit in the head at once, as well as the potential for unexpected interactions between those terms, under the legal rules for reading license language.

The open software community continues to favor short, academic-style licenses, despite their age and several known deficiencies, perhaps in part for these reasons.  We will see the same trade-offs again and again, throughout Parity's terms.

> Specifically:

"Specifically" helps to clarify that the summary is just an overview, to be overridden by the more specific language that follows.  The "operative" terms of the license follow the colon.

## Aside: First and Second Person

You've noticed that Parity uses second-person "you" for the one receiving the license, and first-person "I" for the one giving the license.  Parity might be the first general-purpose public license for software to do so.

Using "I" and "you" or "we" is common in plain-language legal drafting.  I wish plain-language drafting were itself more common.  The choice works especially well for "consumer" terms where at least one side is likely to be an individual without access to legal counsel.

First and second person make legal terms easier to read.  Non-lawyers aren't used to reading about themselves in the third person, especially in abstract legal terms like "Licensor" and "Licensee".  Using "you" and "I" makes it easy for both sides to remember who they are in the terms.

As always, there's a trade-off.  In English, "I" doesn't read naturally for companies.  If "Super Software, Inc." is the one giving a license on Parity terms, "Super Software" is the "I" in those terms.  "We" would be more acceptable, though still a bit off.  The same problems apply when the one _receiving_ a license on Parity terms is a company.

For Parity, I believe the benefits of "you" and "I" outweigh the costs:

1.  By count, open software projects licensed by individuals increasingly outnumber projects licensed by companies.

2.  When companies do contribute, they often do so through employees and contractors who erroneously contribute in their own names. The company often owns the intellectual property to license under "work made for hire" rules.

3.  When company officers give employees and contractors permission to contribute, that often gets documented as permission for the individual to contribute.

4.  In reader testing, "you" and "I" massively improve readability and comprehension.

There is one more wrinkle:  projects with multiple contributors, more than one of whom license on Parity terms.  Singular "I" in that context mismatches the plural number of contributors giving licenses.

We see similar problems with MIT- and BSD-family terms, which were originally written for releases from academic institutions, not teams of independent contributors.  Modern projects under those licenses often have `LICENSE` files with a copy of the terms and a single copyright notice, for the first contributor.  Later contributors may or may not add their own copyright notices, to `LICENSE` or in the files where they contribute.

I suspect diligent projects using Parity will clarify similarly.  For example, by adding a note in `README` to the effect that "all contributors to this project license their work on the terms of The Parity Public License 3.0.0", or by adding a copyright notice for each contributor to `LICENSE`.

## Permission

### Follow the Rules

> If you follow the rules below, ...

"Follow the rules" is plain English, not legal English.  "Rule" has no specific legal meaning in this context, leaving a court to read in its common meaning.

Placing this phrase _before_ the language giving permission alerts readers that they can't just read up to the part they like---permission for the software---and stop.  They have to pay attention to the rest of the terms, too.

In legal practice, rules that come with a license can take two legal forms:

1.  _License conditions_ limit what someone is allowed to do under their license.  If the license is a copyright license, breaching a condition of that license leaves the user open to a copyright infringement lawsuit.

2.  _Contract covenants_ are promises the other side can enforce under the law of contracts.  If the one giving the promise fails to keep it, the side receiving the promise can sue for breach of contract.

There is a long-running debate about whether public licenses for software are just licenses, just contracts, can be both, or must be both.  The Free Software Foundation has always included terms in its GPL licenses saying that the GPLs are just licenses, and not contracts.  Other software licenses, like Apache 2.0, MIT-family licenses, and BSD-family licenses, don't say anything about license-or-contract.  Public licenses for other media, like Creative Commons forms, make clear that courts _could_ read them as contracts, but don't try to force any specific conclusion.

Parity mostly ignores this debate, since it doesn't appear to matter much, in practice.  American courts considering these kinds of licenses tend to approach public software licenses both ways.  They use contract-law rules to interpret terms.  But they allow both contract and copyright-based legal claims for breaching those rules.  Parity's terms don't go out of their way to limit Parity developers to one legal theory or another, for enforcement.

### You May Do

> ...you may do everything with this software that would otherwise infringe either...

Popular public licenses for software write their permissions, or license grants, in two major styles:

1.  Academic-style terms like MIT- and BSD-family forms use generic terms without any specific legal meaning, or a mishmash of legal terms from both patent and copyright.

2.  Enterprise-style terms, like Apache 2.0, copy long lists of specific verbs from the laws that define copyright and patent infringement, with separate sections for the copyright license and patent license.

Academic-style terms pose interpretive problems.  It's often unclear whether they grant effective patent permission, or whether or how they cover all the things that count as copyright infringement.  This is why many guides to open source licensing recommend Apache 2.0 over MIT or BSD when patents are a concern.  But such enterprise-style terms also tend to run long in their permission language, scaring away non-lawyer readers and hiding the overall point of those provisions.

The overall point is that these licenses don't cherry-pick specific exclusive rights of copyright and patent holders.  They're meant to be _total licenses_, to keep users who follow the other rules from getting sued for infringement, whatever they do, as long as they follow the other license rules.

There is nothing to stop a public software license from saying this directly.  So that is what Parity does.

The approach does bury a bit of legal detail.  Permission is only to do things that would count as infringement.  That does _not_ include privileges that only owners of copyright and patent have, such as assigning ownership.

The word "either" begins a list, with two phrases, [one for copyright](#copyright), and [one for patent](#patent).

### <a id="copyright"></a>Copyright

> my copyright in it,

Completing the previous phrase, "you may do everything with this software that would otherwise infringe [my copyright in it]" grants a total copyright license.

It's relatively easy to identify _which_ copyright a public software license has to cover: copyright in the software.  As we'll see, it's not so easy for patent.

### <a id="patent"></a>Patent

> ...any patent claim I can license that covers this software as of my latest contribution,...

Popular "academic" licenses like MIT- and BSD-family forms create patent uncertainty in two primary ways: whether they grant patent licenses to begin with, and if they do, what patents, if any, they cover.

Enterprise-style licenses put patent-permission language in its own section, use the word "patent", and describe what patents they cover at some length.  [Apache 2.0 section 3](https://www.apache.org/licenses/LICENSE-2.0#patent) exemplifies.

Parity follows academic style in granting all permission in a single sentence, but follows enterprise style in explicitly mentioning both "copyright" and "patent", and taking some time to address _which_ patents get covered.

Language setting the scope of a public patent license has to balance three major interests:

1.  Users want to know which versions of the software are "safe" from patent suit by contributors, even if they don't know which patents might apply.

2.  Contributors want control over which patents they license.

3.  Both users and contributors want clarity, if they end up in a patent infringement lawsuit.

Parity follows Apache 2.0 in its general solution to this problem:  Contributors license all the patents that cover the work they contribute, as well as the work of others that was part of the project when they contributed.

Parity departs from Apache 2.0 in putting this rule as succinctly as possible, without describing what does and does not count as a "contribution".  Apache 2.0 spends many words defining both "Contribution" and "submitted", a term used in that definition.  But the terms of those definitions are themselves very broad, so as to avoid specializing the Apache license to any particular development methodology or toolkit.

My read of those definitions calls out three key effects:

1.  Work must be submitted _intentionally_ to be covered.

    I'm not sure what this achieves.  Would work submitted accidentally count as being submitted intentionally?

    Parity uses "my latest contribution".  Contribution is not defined in the license, and as far as I'm aware, it has no specialized legal meaning.  Courts will therefore look to its plain, common meaning.  I do _not_ believe "contribute" is commonly used to describe involuntary or inadvertent action.  That's buttressed by the fact that users will only receive reliable licenses on Parity terms for contributions if those licensing it manifest their choice to license, and document it.

2.  Others can submit work that's covered on behalf of the copyright owner, with their permission.

    This is practically necessary, since companies often own the rights in work by their employees and contractors, and give those employees and contractors permission to contribute back.  Apache could strengthen this by requiring written permission.  As for Parity, I believe the common meaning of "contribution" would cover work an entity directed to be contributed.

3.  Submission happens by communication to the "Licensor".

    The Apache 2.0 license gets used by many organizations, and by many projects.  But it was written originally for projects hosted by the Apache Foundation, which collects all rights in its projects via contributor license agreements, and licenses the results to the public, rather than relying on all contributors to license their work independently.  The Apache language on patent scope makes most sense with a single "Licensor".  There's nothing to stop multiple contributors from granting independent Apache licenses for their contributions to a single project.  But it gets much harder to the language in those cases.  Is it enough to "submit" a patent-leaden contribution to _any_ Licensor?

    As a practical matter, I think many projects that use licenses like Parity will come from specific companies.  But Parity doesn't _require_ that one individual or entity hold all the rights that need to be licensed.  As a result, it cannot assume that there is or always will be any particular person or entity to receive all contributions.  Parity projects may be abandoned by their original developers, or taken up by successors.

4.  The magic words "Not a Contribution" keep work that would otherwise get covered from becoming a "Contribution" under the license.

    Magic words can achieve clarity.  As a practical matter, I don't know how many companies or developers aware that Apache 2.0 does this.  But when you need it, it's great to have it there.

    Again, since Parity doesn't address contribution back, but only speaks from one contributor to the public, there's less risk of accidental contribution.

### Or Both

> or both.

One action may infringe both copyright and patent.  For example, sending a customer a copy of software for pay might count as both distributing to the public under copyright law and selling under patent law.  The "either ... or both" construction clarifies that "or" is not exclusive.

## Rule 1: Changes

> 1\. Contribute source code for changes you make to this software.

The first copyleft-like rule, comparable in scope to the Lesser GPL and file-based copyleft licenses like the Mozilla Public License.  There are two major differences:

1.  Parity's [instructions for contribution](#contribution) require licensing and _publication_ of source, not licensing and providing source specifically to users.  The requirement of which license terms to use also differs, which we'll get to in comments to the instructions.

2.  Parity's requirement to contribute changes triggers _when you make the change_, without any further requirement to make or distribute a copy to others.

The latter impinges on what the Free Software Foundation calls the right to "private changes".  I've [written about that "fifth freedom", and problems I see with it.](https://blog.licensezero.com/2018/09/14/free-to-take-freedom.html#extra-freedom)  It apparently extends not just to changes for personal use, but changes made and disseminated throughout an organization, such as a company.

Private changes are an obvious difference of principle between the Open Source Initiative and the Free Software Foundation.  OSI has approved several licenses that require sharing of private changes.  The FSF rejects those licenses as "nonfree".  I've brought this up recently to OSI, and received no indication that OSI and FSF are set to reconcile on it.

All that aside, Parity crosses the line for several reasons:

1.  By all the evidence I'm aware of, it's legally possible, and the purpose of Parity is to require contribution back of as much software as possible.

2.  It's never been cheaper or easier to comply.

3.  Requiring contribution of changes without any further requirement to trigger, like providing the changed software as a service over a network, reliably closes the ASP loophole, also known as the SaaS loophole, for changed versions.  There's no need to define or describe any additional concept for that trigger, like "Remote Network Interaction" under AGPLv3 or "External Deployment" under OSL 3.0.

    Furthermore, if the original contributor publishes their source code, there is no loophole to close for unchanged versions of the project, to begin with.  That source is already available, and available to all on demand.

## Rule 2: Incorporating Software

> 2\. If you run or combine this software with other software in any larger program, contribute all source code for that program.

The second copyleft-like rule, paralleling stronger copyleft licenses like the GPLs.  Prior strong-copyleft licenses also speak in terms of "larger programs".

Again, Parity doesn't add any additional requirement of "conveying" or distributing to others.  And very arguably, it doesn't need to, legally.  Ten- and twenty-year-old assumptions about the limits of what counts as a "derivative work" under copyright are foundering on decisions like Oracle v. Google.  The legal and policy trend is clearly toward a _broader_ definition of derivative work, and therefore more power to control works that build on existing material.

## Rule 3: Developed Software

> 3\. Contribute all source code for software you develop, deploy, monitor, or run with this software.

## <a id="rule-4"></a>Rule 4: Notices

> 4\. Ensure everyone who gets a copy of this software from you, in source code or any other form, gets the text of this license and the copyright and source notices above.

A classic attribution requirement.  Akin to what we see in MIT-family terms, or in points 1 and 2 of BSD-family terms.

## Rule 5: Defensive Termination

> 5\. Do not make any legal claim against anyone for infringing any patent claim they would infringe by using this software alone, accusing this software, with or without changes, alone or as part of a larger program.

## <a id="contribution"></a>Contribution Requirements

> To contribute source code, publish the preferred form for making changes through a freely accessible distribution system widely used for similar source code, and license contributions not already licensed to the public on terms as permissive as this license accordingly.

## Excuse

> You are excused for unknowingly breaking 1, 2, or 3 if you
> contribute source code, or stop doing anything requiring this
> license, within 30 days of learning you broke the rule.

## Disclaimer

> **This software comes as is, without any warranty at all. As far
> as the law allows, I will not be liable for any damages related
> to this software or this license, for any kind of legal claim.**

# General Notes

## (A)GPLv(n) Compatibility

