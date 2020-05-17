---
title: Private License 8
description: clarifying and improving
---

I'm nearing a new version 8.0.0 of License Zero's standard private license, the terms customers get when they buy licenses through licensezero.com.

A few goals advanced in this version:

- Use the more intuitive terms "Developer" and "User" throughout.  The current license form uses "Licensor" and "Licensee", which while legally rigorous, mostly seem offputting and confusing to people who practice software instead of law.

- Spell out clearly that the developer's agent, Artless Devices, signed on their behalf.

- Record the price paid, and also make it possible for developers to issue $0 licenses.  This will allow us to merge the concept of private license and waiver.  The easiest explanation for "waiver" was always "free private license".  Now we can make that actually true.

- Clarify what's going on in terms of contributions.  There is a "Project".  The Developer has made "Contributions" to that Project.  The Contributions covered by the license are those tagged with a specific offer identifier.

- Clarify the rules on sublicensing, and spell out the [purpose](#purpose) for the most important ones about [added value](#added-value) and [maintenance](#maintenance).

- Add a basic warranty, or guarantee, that the developer has the right to license the work.  This is unusual in open licenses, and many developers would arguably do without.  But conceptually, customers ought to get some legal assurance that they're actually getting the rights they're paying for.

As always, this remains a [flipped form](https://flippedform.com).  Everyone involved in software should be able to read it.  If parts don't make sense, or feel awkward, please [let me know](mailto:kyle@artlessdevices.com).  We should fix them!

> # License Zero Private License
>
> Version 8.0.0 Draft
>
> ## Summary
>
> This is a private license for software, granted by a software developer through their agent to a specific user.
>
> ## Details
>
> - The **Developer** is `$developerName`, `$developerJurisdiction` (ISO 3166-2), `$developerEMail`.
>
> - The **Agent** is `$agentName`, `$agentJurisdiction` (ISO 3166-2), `$agentWebsite`.
>
> - The **User** is `$userName`, `$userJurisdiction` (ISO 3166-2), `$userEMail`.
>
> - The **Project** is `$projectRepository`, `$projectDescription`.
>
> - The **Price** is `$price` (USD).
>
> - The **Term** begins on `$date` (ISO 8601) and continues `$term`.
>
> - The **Offer Identifier** is `$offerIdentifier`.
>
> - The **Licensed Contributions** are the contributions the _Developer_ has made to the _Project_ with the _Offer Identifier_ in metadata, as well as any contributions the _Developer_ makes to the _Project_ in the future without changing the _Offer Identifier_ or adding a new one.  _Licensed Contributions_ do not include any contributions the _Developer_ makes to the project int he future with a different or additional identifier.
>
> ## Payment
>
> All the licenses granted under these terms are conditional on payment of the _Price_.  If there is no _Price_, the _Developer_ nonetheless expects the _User_ to rely on this license nonetheless, and will not revoke it unless the _User_ breaks one of its rules.
>
> ## Copyright
>
> The _Developer_ licenses the _User_ for the _Term_ to do everything with the _Licensed Contributions_ that would otherwise infringe the _Developer_'s copyright in them.
>
> ## Patent
>
> The _Developer_ licenses the _User_ for the _Term_ to do everything with the _Project_ that would otherwise infringe patent claims the _Developer_ can license or becomes able to license.
>
> ## Sublicensing
>
> If the _User_ combines some or all of the _Licensed Contributions_ with other software in a larger application, the _User_ may sublicense those _Licensed Contributions_ as part of their larger application, and allow further sublicensing in turn, under the following rules:
>
> ### Added Value
>
> The larger application must have significant additional content or functionality beyond that of the _Project_, and end users must license the larger application primarily for that added content or functionality.
>
> ### Maintenance
>
> The _User_ may sublicense others to maintain the larger application, but not to use the _Licensed Contributions_ in new or different ways in that application, or to develop larger applications of their own.
>
> ### Purpose
>
> The purpose of [Added Value](#added-value) and [Maintenance](#maintenance) is to prevent the _User_ from sublicensing others who should buy their own private licenses.
>
> ### Passthrough
>
> [Sublicensing](#sublicensing) and [Notices](#notices), as well as warranty disclaimers and damages exclusions at least as broad as [Disclaimer](#disclaimer) and [Exclusion](#exclusion), must apply to each sublicense.
>
> ### Unlimited Applications
>
> The _User_ may build, and sublicense for, as many larger applications as they like.
>
> ## Notices
>
> In order to make sure that everyone who gets a copy of the _Licensed Contributions_ knows about the license terms for their use, the _Developer_ agrees to give everyone who gets a copy of some or all of the _Licensed Contributions_ from them, with or without changes, the text of this license and any public license for them.
>
> ## Agency
>
> The _Developer_ has authorized the _Agent_ to sign this license on the _Developer_'s behalf.  The _Agent_ is not a party to this license.
>
> ## Rights
>
> The _Developer_ states that they either own or have the rights to license copyrights in the _Licensed Contributions_.
>
> ## Disclaimer
>
> **With the sole exception of [Rights](#rights), as far as the law allows, the _Project_ comes as is, without any warranty or condition.**
>
> ## Exclusion
>
> **With the sole exception of [Rights](#rights), as far as the law allows, the _Developer_ will not be liable to anyone for any damages related to the _Project_ or this license, under any kind of legal claim.**
