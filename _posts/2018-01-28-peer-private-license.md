---
title: A Peer Private License
description: draft of developer-to-developer commercial and closed-source license
layout: post
---

_[Largesse Oblige](https://blog.licensezero.com/2018/01/22/largesse-oblige.html)_ asked whether License Zero should restructure from licensing companies toward licensing developers.  _[Developer Licensing](https://blog.licensezero.com/2018/01/26/developer-licensing.html)_ sketched how that might work, in more detail.  I've drafted a form private license along those lines.

Let's have a look:

> # License Zero Private License
>
> Version {Version}
>
> <https://licensezero.com>

The license header identifies the license by title and version, and provides a link to the project homepage.  This should help orient those unfamiliar with the License Zero system.

> Date: {Date}
>
> Licensor: {Name} {Jurisdiction} (ISO 3166-2)
>
> acting through their agent: {Name} {Jurisdiction} (ISO 3166-2) {Website}
>
> Licensee: {Name} {Jurisdiction} (ISO 3166-2) {E-Mail}
>
> Project: {Project ID} {Description} {Repository}

This header identifies who is giving the license, for which project, to whom, and when.  [licensezero.com](https://licensezero.com)'s API will populate the fields appropriately, and cryptographically sign the populated form license, as a whole.

> ## Background
>
> I have made contributions to the project, and licensed my contributions on the terms of either the License Zero Noncommercial Public License (L0‑NC) or the License Zero Reciprocal Public License (L0‑R).  Broadly speaking, L0‑NC's conditions limit use for commercial purposes, and L0‑R's conditions require you to release changes to, software built on, and software build using the project as open source software.
>
> This is a separate private license for my contributions to the project, with different conditions.
>
> This private license lets you to use my contributions to the project for commercial purposes, and to create software that is not released as open source.  However, this private license applies only to you, and in a more limited way to those you're allowed to sublicense.

This section introduces some basic terms and concepts, notably the licensor's "contributions" to the project, and explains the purpose of the license.  In even simpler terms:  The project is available under a public license, either [L0‑NC](https://licensezero.com/licenses/noncommercial) or [L0‑R](https://licensezero.com/licenses/reciprocal).  This private license gives permission to use the project in ways those public licenses don't, but only for the developer buying the private license.

[L0‑NC]: https://licensezero.com/licenses/noncommercial

[L0‑R]: https://licensezero.com/licenses/reciprocal

> ## No Liability
>
> ***My contributions to the project come as is, without any warranty at all.  As far as the law allows, I will not be liable for any damages related to the project or this license, for any kind of legal claim.***

This language is nearly the same as in [L0‑NC] and [L0‑R], which does the same job as the long, ALL CAPS texts in licenses like BSD and MIT, but much shorter.

> ## Copyright License
>
> Subject to the other terms this license, I grant you a perpetual, worldwide, non-exclusive, royalty-free, irrevocable copyright license to reproduce, prepare derivative works of, publicly display, publicly perform, and distribute my contributions to the project, in source code or any other form.
>
> ## Patent License
>
> Subject to the other terms of this license, I grant you a perpetual, worldwide, non-exclusive, royalty-free, irrevocable patent license to make, have made, use, offer to sell, import, and otherwise transfer the project.  That license applies only to patent claims I can license that are necessarily infringed by my contributions alone, or by combination of my contributions with the project as it was when I submitted my contributions.

Like [L0‑NC] and [L0‑R], this private license gives explicit copyright and patent licenses, rather than using broad, vague terms like BSD and MIT.  However, where [L0‑NC] and [L0‑R] take a shortcut for clarity and readability, giving permission to "do everything ... that would otherwise infringe my copyright ... or any covered patent claim", this private license uses more traditional legal language for its licenses.  The list beginning "reproduce, prepared derivative works of..." comes right from the copyright law describing what counts as copyright infringement.  The list beginning "make, have made..." comes right from the patent law describing what counts as patent infringement.  Copying out those lists is orthodox legal style for enterprisey license agreements, which we also see in [Apache 2.0].

[Apache 2.0]: https://www.apache.org/licenses/LICENSE-2.0

Why use one style in License Zero's public licenses, and another in its private licenses?  The most important thing the public licenses can achieve is ease of reading, so developers understand and apply the terms with minimum legal help.  Even though this private license is meant for use between developers, the most important thing it can achieve is demonstrate to company lawyers that developers using License Zero code under private license have met their legal obligations.  As a matter of course, developers sign contracts, often titled "confidentiality and invention assignment agreement".  Under those contracts, developers guarantee that they have the rights they need to license their company or client to use the work they provide.

> ## Defensive Termination
>
> If you may any legal claim against anyone for infringing any patent claim they would infringe by using the project alone, accusing the project, with or without changes, alone or combined into a larger program, then your patent license automatically terminates.

Like [L0‑NC], [L0‑R], and [Apache 2.0], this private license includes a broad defensive termination provision.

> ## Sublicensing
>
> If you combine the project with other software into a larger program, you may sublicense my contributions to the project as part of that larger program, and allow further sublicensing in turn, on the conditions below:

It's all well and good to give _developers_ permission to use License Zero projects for company and client projects.  But where do companies and clients get their permission?  The answer:  They get it from developers who've purchased private licenses, via sublicense.

How about when the developer builds software for a company or client?  Where do end-user customers get their permission?  The answer: They get it from the company or client, again via sublicense. 

> <ol start="1"><li>The larger program must have significant additional content or functionality beyond that of the project, and end users must license the larger program primarily for that additional content or functionality.</li></ol>

The Sublicensing section partially tracks condition four of [L0‑R], which requires release as open source if licensees "combine this software with other software into a larger program", to put a limit on sublicensing very familiar from proprietary value-added-reseller (VAR), independent software vendor (ISV), and system integrator (SI) contracts.

In essence, the developer buying the private license can't turn around and give anyone they like permission to use the project without following the conditions of its public license.  That would create a loophole through which a single developer could purchase a private license and promptly sublicense everyone who doesn't like [L0‑NC] or [L0‑R].

Rather, the developer can only sublicense others to use programs they write that build on the License Zero code in a substantial way.  They can't simply offer the License Zero project as it came, but under private license terms.  It isn't enough to service-ize the project, or to wrap it in a thin user interface.

> <ol start="2"><li>Sublicenses must not permit anything that would violate the public license for my contributions to the public, other than as combined in your larger program.</li></ol>

Privately licensed developers can pass on permission to use software they build using License Zero code, but others who want to develop on the License Zero project need to buy their own private licenses.  By purchasing a private license for the project, developers receive the right to make exceptions to the noncommercial and reciprocity conditions of the public license, but only for use of the work they build on top.

In the case of an [L0‑NC]-licensed project, the developer buying the license can only give their companies, clients, and end-users the right to use the work they've built on top of the License Zero code for commercial purposes.  They can't give them the right to use the same License Zero code in other programs for commercial purposes.

In the case of an [L0‑R]-licensed project, the developer buying the license can only give their companies, clients, and end-users the right to use the proprietary or closed-source work they've built on top of the License Zero code without releasing as open source.  They can't give them the right to make changes to the project, build on it, or build other software with it, without releasing that other work as open source.

> <ol start="3"><li>Sublicenses may permit copying and adaptation necessary for utilization of the program, archiving, maintenance, or repair, as described in United State Code title 17, section 117.</li></ol>

[17 USC 117](https://www.gpo.gov/fdsys/pkg/USCODE-2016-title17/html/USCODE-2016-title17-chap1-sec117.htm) puts limits on copyright, to allow owners of copies of computer programs to archive copies and keep their software and systems working.  You'll often see clarifications that "the software is licensed, not sold" in proprietary license agreements, to avoid those limits.

The limits are usually a good thing.  A company or end-user that pays for a proprietary license of software that incorporates a License Zero library ought to be able to patch that software, ten years down the line, without violating their sublicense by using for a commercial purpose, or failing to release the fixed program as open source.

> <ol start="4"><li>No Liability, Defensive Termination, Sublicensing, and Redistribution must apply to everyone sublicensed.</li></ol>

Not just the permissions granted, but also the conditions on those permissions, must be passed down to sublicensees.  They can't hold the developer liable under a warranty, sue for patent infringement while keeping their own patent license, or give others more permission than they received.

> ## Redistribution
>
> You must ensure that everyone who gets a copy of the project from you, in source code or any other form, also gets the complete text of the public license applied to my contributions to the project, including copyright and source notices.

The developer and sublicensees must continue to keep the project's public license terms and information with it, wherever it goes.  They can choose to include a copy of the private license, as well.  This language tracks the first conditions of [L0‑NC] and [L0‑R].
