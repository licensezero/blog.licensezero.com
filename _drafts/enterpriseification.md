---
title: Enterpriseification
description:
layout: post
---

At first glance, it's obvious:

1. Open software developers make value, and need money.
2. Big companies reap the value open developers sow, and have money.
3. Big companies ought to pay open software developers the money.
4. Unfortunately, open software developers are really bad at getting paid.
5. Let's make a thing the big companies can pay that pays open software developers in turn.

In technical terms, it's one big [adapter pattern](https://en.wikipedia.org/wiki/Adapter_pattern).  Build a middleman, as a brokerage or a platform, that big companies can interface with on one side, and open software developers can interface with on the other.  Then money can flow from one to the other, without changing how big company pays or open developer builds.  Don't change the governance or the tools or the license.

That's fantasy.  Interfacing with big companies changes how developers work, how they think, how they relate.  That's why so many open developers don't want to work for big companies.

Every adapter is really a [coupling](https://en.wikipedia.org/wiki/Coupling), and the big company drives.  Where big-company money goes, big-company practice follows.  Even when the big company pays to do open source full time.

Let's call it <dfn>enterpriseification</dfn>.

Enterpriseification reverses the course of open software progress.  Open approaches did not succeed, in the main, by conforming to big company expectations.  There is some of that, as in the [Apache License](https://www.apache.org/licenses/LICENSE-2.0), which reads the way corporate lawyers write.  But even Apache is miles from what big companies would have accepted twenty years ago.  Where's the warranty?  Where's the patent indemnity?  What about support?  Where's the vendor?

As it turns out, none of those things were strictly necessary.  In many cases, social proof, widespread adoption, and reputation achieve the same ends better than old-school, commercial assurances did.  It took years for enough crazy companies to run on open software and get away with it, in public view, before the more conservative, lumbering giants dipped toes, and eventually took the plunge.

I recently published an [Enterprise Ready Open Software Supplement](https://writing.kemitchell.com/2019/04/11/enterprise-supplement.html).  Basically, it's a legal form for selling the difference between big company license expectations and open license expectations.  What does that mean?

| "Enterprise Ready"                                           | Open Norm                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Demonstrate a basic understanding of common intellectual property traps for open software projects. | No assurance given. No widespread education on the matter.   |
| Guarantee you have the intellectual property rights needed to license the project. | No such guarantee.                                           |
| Keep good records showing other contributors license their work the same way. | Rely on non-legal community expectations of inbound=outbound licensing. |
| Provide basic assurance that the project isn't covered by a known patent. | No such assurance.                                           |
| Keep malicious code, like malware, out of the software.      | THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED... |
| Give an explicit patent license.                             | MIT, BSD, ISC, and similar do not.                           |
| Forgive inadvertent breaches of the project's license.       | Most licenses immediately terminate rights for even inadvertent breach of basic conditions, like attribution. |
| Stand behind your guarantees financially.                    | IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY |

Add a few maintenance obligations, and you have Tidelift.  From their summary:

> Make sure that the package gets to, and stays at, a level of maturity that enterprise subscribers expect.

Compare the [License Zero form private license](https://licensezero.com/licenses/private), which is just a grant of permission.

We are already headed in that direction.  There are no open-source-style terms for services.  If you do a deal with a service provider, for infrastructure, a platform, or a service, you do a deal in the way big companies understand and expect.