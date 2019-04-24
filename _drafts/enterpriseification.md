---
title: Enterpriseification
description: coupling to big companies changes open development
layout: post
---

At first glance, it's obvious:

1. Open software developers make value and need money.

2. Big companies reap the value open developers sow, and have money.

3. Big companies ought to pay open software developers the money.

4. Open software developers are really bad at getting paid. So:

5. Let's make a thing the big companies can pay that pays open software developers in turn.

In technical terms, it's one big [adapter pattern](https://en.wikipedia.org/wiki/Adapter_pattern).  Build a middleman, as a brokerage or a platform, that big companies can interface with on one side, and open software developers can interface with on the other.  Then money can flow from one to the other, without changing how company pays or developer builds.  Don't change the governance or the tools or the license.

That's fantasy.  Interfacing with big companies changes how developers work, how they think, how they relate.  It changes the experience of users and contributors who aren't clients or customers.  That's part of why so many open developers who need money nonetheless refuse to go to work for big companies.

They know that every corporate adapter is really a corporate [coupling](https://en.wikipedia.org/wiki/Coupling), and the company drives.  Where big-company money goes, big-company practice follows.  Even when the big company pays to do open source full time.  Dealing with company policy to do open source can itself be a full-time job.

This is related to, but distinct from, the issue known as "money in open source".  Bringing money into any open situation works changes.  But those changes differ, depending on who brings the money, how much, and what expectations coincide.

Bringing big-company money, or just manpower and influence, without cash, into an open project works different changes.  Often more impactful changes than even full-time pay provided otherwise.  Call it <dfn>enterpriseification</dfn>.

## Progress

Enterpriseification reverses the course of open software progress.  Open approaches did not succeed, in the main, by conforming to big company expectations.  There is some of that, as in the [Apache License](https://www.apache.org/licenses/LICENSE-2.0), which reads the way corporate lawyers write.  But even Apache is miles from what big companies would have accepted twenty years ago.  Where's the warranty?  Where's the patent indemnity?  What about support?  Where's the vendor?

As it turns out, none of those things were strictly necessary.  In many cases, social proof, widespread adoption, and reputation achieve the same ends better than old-school, commercial assurances did.  It took years for enough crazy companies to run on open software and get away with it, in public view, before the more conservative, lumbering giants dipped toes, and eventually took the plunge.

## Scope

I recently published an [Enterprise Ready Open Software Supplement](https://writing.kemitchell.com/2019/04/11/enterprise-supplement.html) under the [indieopensource.com](https://indieopensource.com) umbrella.  Basically, it's a legal form for selling the difference between big company license expectations and open license expectations.  What does that mean?

| "Enterprise Ready"                                           | Open Norm                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Demonstrate a basic understanding of common intellectual property traps for open software projects. | No understanding demonstrated. Widespread confusion abounds. |
| Guarantee you have the intellectual property rights needed to license the project. | No such guarantee given.                                     |
| Keep good records showing other contributors license their work the same way. | Rely on non-legal community expectations of inbound=outbound licensing, reputation, and "too adopted to fail". |
| Give basic assurance that the project isn't covered by a known patent. | No such assurance given.                                     |
| Promise to keep malicious code, like malware, out of the software. | THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED... |
| Give an explicit patent license.                             | MIT, BSD, ISC, and similar do not.                           |
| Forgive inadvertent breaches of the project's license.       | Most licenses immediately terminate rights for even inadvertent breach of basic conditions, like attribution. |
| Stand behind your guarantees financially.                    | IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY |

Drop a few requirements from the table above, and you end up with the [Blue Oak Model License](https://blueoakcouncil.org/license/1.0.0).  Blue Oak better addresses patents, contributor licensing, and forgiveness for breaches, not in private terms for paying customers, but in the public license terms for all.  If you use Blue Oak, and want to sell additional assurances under something like the Enterprise Ready Supplement, you have less to offer, because given more away.  Not that that's necessarily a bad thing.

_Add_ a few ongoing maintenance obligations to the table above, and you have the [Tidelift](https://tidelift.com/) package.  From [their summary](https://tidelift.com/docs/lifting/tasks-overview):

> ## Goals: what we ask you to do
> - Make sure that the package gets to, and stays at, a level of maturity that enterprise subscribers expect.
> ...

Issues like right to license and forgiveness for breaches get covered in [the "Lifting Agreement"](https://writing.kemitchell.com/2018/09/18/Lifting-Agreement.html) developers agree to in order to take pay through the platform.

Finally, compare the [License Zero form private license](https://licensezero.com/licenses/private), which is just a grant of permission.  It adds nothing to the public license for the project being licensed, other than what is missing from the public terms.

That reflects a fundamental difference in approach.  Artless Devices, the company behind License Zero, doesn't negotiate with big-company procurement departments for deals with the customer.  Rather, Artless Devices serves as developers' agent for [selling licenses to their developer peers](https://blog.licensezero.com/2018/01/26/developer-licensing.html) directly.  License Zero does everything it can to _avoid_ coupling open software developers to the expectations and norms of corporate production and procurement.

## Upstream

By insisting that open licensing norms are enough, License Zero is rowing upstream of the corporate river, as open source licensing itself once did.  But open victory was never total.  Open style licensing, publicly or privately, still rows upstream of the way software is bought and sold.

There are no standardized, open-source-style terms for services, free or paid.  (Yes, I'm working on it.)  If you do a deal with a service provider---for infrastructure, a platform, or an application---you do a deal in the way big companies understand and expect, either self-serve on take-it-or-leave-it terms, or negotiated through sales and procurement.

Turning a software program into a service offering is the predominant way that commercial software makers couple their wares to big companies today.  Many programs, from general purpose databases to project management suites, can be  transmuted, as if by magic, from software that corporate customers prefer to download and use for free, under open source policies, into software that corporate customers expect to pay for.
