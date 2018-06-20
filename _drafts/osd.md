---
title: The Case for L0-R under the Open Source Definition
layout: post
---

> # The Open Source Definition
> ## Introduction
> Open source doesn't just mean access to the source code. The distribution terms of open-source software must comply with the following criteria:

To conform to the Definition, a license has to meet all ten criteria.

> ## 1. Free Redistribution
> The license shall not restrict any party from selling or giving away the software as a component of an aggregate software distribution containing programs from several different sources. The license shall not require a royalty or other fee for such sale.

L0-R gives everyone permission to sell or give away copies of the software.  There's no restriction on putting L0-R software in the same archive, on the same FTP server, or on the same physical media as other software.

L0-R does not require any royalties or other payments.

> ## 2. Source Code
> The program must include source code, and must allow distribution in source code as well as compiled form. Where some form of a product is not distributed with source code, there must be a well-publicized means of obtaining the source code for no more than a reasonable reproduction cost, preferably downloading via the Internet without charge. The source code must be the preferred form in which a programmer would modify the program. Deliberately obfuscated source code is not allowed. Intermediate forms such as the output of a preprocessor or translator are not allowed.

Most of this language is holdover from Debian's Free Software Guidelines.  Debian won't distribute a program as part of Debian if it can only find a binary, without source, under a GPL license.  Including source code or having a well-publicized means of obtaining it in preferred form is important, but those aren't things that licenses accomplish.

L0-R's broad permission grant meets the one license requirement of #2: it allows distribution of the software.

> ## 3. Derived Works
> The license must allow modifications and derived works, and must allow them to be distributed under the same terms as the license of the original software.

L0-R allows changes and derived works.  L0-R's conditions require release of changes and derived works.  Release requires licensing under a specified category of licenses that includes L0-R itself.

> ## 4. Integrity of The Author's Source Code
> The license may restrict source-code from being distributed in modified form only if the license allows the distribution of "patch files" with the source code for the purpose of modifying the program at build time. The license must explicitly permit distribution of software built from modified source code. The license may require derived works to carry a different name or version number from the original software.

L0-R allows derived works and their distribution.  It has attribution conditions similar to those of MIT, BSD, and other licenses.  It does _not_ have conditions requiring name or version changes, as under [Artistic-2.0](https://spdx.org/licenses/Artistic-2.0.html).

> ## 5. No Discrimination Against Persons or Groups
> The license must not discriminate against any person or group of persons.

L0-R mentions only licensors and licensees.

> ## 6. No Discrimination Against Fields of Endeavor
> The license must not restrict anyone from making use of the program in a specific field of endeavor. For example, it may not restrict the program from being used in a business, or from being used for genetic research.

L0-R places conditions on use, particularly use to create closed, proprietary software.

    5. If you run this software to analyze, change, or generate
       software, you must release source code for that software that
       has not yet been released.

But closed, proprietary development is a means, not a "field of endeavor" under #6.  If we forced a reading of field of endeavor to include closed, proprietary development, approved open source licenses would not meet the #6:

1. [AGPL](https://spdx.org/licenses/AGPL-3.0.html) requires modified versions of the program to offer source to "users interacting with it remotely through a computer network".  The trigger for this requirement is twofold: making changes and use.

2.  [OSL](https://spdx.org/licenses/OSL-3.0.html) triggers copyleft on external deployment.  External deployment is defined to include "use ... of the Original Work or Derivative Works in any way such that the Original Work or Derivative Works may be used by anyone other than You".

3.  [RPL](https://spdx.org/licenses/RPL-1.5.html) triggers copyleft on deployment.  Licensees "Deploy" when they "use ... Licensed Software other than for [their] internal Research and/or Personal Use, and includes ... any and all internal use ... of Licensed Software within Your business or organization...."

All of these licenses close the "ASP loophole", where users under traditional copyleft licenses like GPLv2 avoided to requirement to share and license their modifications.  Instead of distributing copies of their modifications to others, they ran the modified software, and had users connect remotely, without their own copies.  The licenses only required sharing code on "distribution".

The United States' Copyright Act doesn't give copyright owners the right to control "use" of software explicitly.  It gives them rights to control reproduction (copying), distribution (sharing), and preparing derivative works (changing and building on) their work.  But it's practically impossible to use a program without reproducing, distributing, or preparing derivative works from its code.

All the licenses above use this fact to close the ASP loophole.  Their requirements to share and license source code apply when the software is "used" in particular ways.  The software can't be "used" without copying, sharing, changing, or building on it.

> # 7. Distribution of License
> The rights attached to the program must apply to all to whom the program is redistributed without the need for execution of an additional license by those parties.

L0-R grants permission to everyone, on its own, without any action on their part.

> ## 8. License Must Not Be Specific to a Product
> The rights attached to the program must not depend on the program's being part of a particular software distribution. If the program is extracted from that distribution and used or distributed within the terms of the program's license, all parties to whom the program is redistributed should have the same rights as those that are granted in conjunction with the original software distribution.

L0-R doesn't so much as mention software distributions.

> ## 9. License Must Not Restrict Other Software
> The license must not place restrictions on other software that is distributed along with the licensed software. For example, the license must not insist that all other programs distributed on the same medium must be open-source software.

L0-R affects only the code its applied to.  L0-R code can be placed on in the same archives, on the same servers, and on the same physical storage media as permissively licensed open source or copyleft open source.

> ## 10. License Must Be Technology-Neutral
> No provision of the license may be predicated on any individual technology or style of interface.

L0-R does not mention any individual technology or style of interface.
