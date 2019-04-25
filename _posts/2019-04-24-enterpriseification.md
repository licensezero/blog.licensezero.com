---
title: Enterpriseification
description: Open software changed big business.  Should big business change it back?
layout: post
---

At first glance, it's obvious:

- Open software developers make software and need money.

- Big companies need software and make money.

- Big companies should pay open software developers.

Unfortunately, many open software developers are terrible at getting paid, especially by big companies.  So:

> Let's make a thing the big companies can pay, that turns around and pays the open software developers.

In technical terms, it's the [adapter pattern](https://en.wikipedia.org/wiki/Adapter_pattern).  Build a middleman, as a brokerage or a platform, that big companies can interface with on one side, and open software developers can interface with on the other.  Then money can flow from one to the other, as water flows through a culvert, without changing how company pays or developer builds.  Hire a sales team and expect lots of redlines.  Don't change the governance or the tools or the license.

This was License Zero once.  But License Zero changed.

## Unfortunately

Side-effect-free enterprise adapters are fantasy.  Interfacing with big companies changes how developers work, how they think, how they relate, how their projects develop.  Interfacing with big companies changes the experience of users and contributors who aren't clients or customers, too.  That's part of why so many open developers who need money nonetheless refuse to go work for big companies.

They know that a corporate [adapter](https://en.wikipedia.org/wiki/Adapter) is really a corporate [coupling](https://en.wikipedia.org/wiki/Coupling), and the company drives.  You're not simply plugging into the enterprise money grid, you're becoming part of the enterprise system, the [supply](https://www.openchainproject.org/) [chain](https://youtu.be/h0A8IhJQz0E?t=721).  Where big-company money goes, big-company practice follows.  Even when the big company pays to do open source full time, dealing with company policy can itself be a full-time job.

Call it <dfn>enterpriseification</dfn>.

Enterpriseification is related to, but distinct from, the issue known as "money in open source".  Bringing money into any open project works changes, too.  But those changes differ, depending on who brings the money, how much, and with what expectations.

Bringing big-company expectations into an open project, whether via cash, contribution, governance, or other influence, tends to effect an overlapping, but different, set of differences.  Some of those can be more stark and project-changing than full-time maintainer pay provided otherwise.

## Progress

Most troubling, enterpriseification reverses the course of open software progress.

Open approaches did not achieve widespread acceptance, in the main, by conforming to big company expectations.  There was lots of that, for sure.  I always think first of the [Apache License](https://www.apache.org/licenses/LICENSE-2.0), the "enterprise license", which reads the way corporate lawyers write.  But even Apache is miles from what big companies would have accepted twenty years ago.

Where's the warranty?  Where's the patent indemnity?  What about support?  Where's the vendor?  Whose bottom line stands behind this?

As it turns out, none of those things are strictly necessary, most of the time.  In many cases, social proof, widespread adoption, and reputation achieve the same ends better than old-school commercial assurances did.  It took years for enough crazy companies to build on open and get away with it, in plain public view, before the more conservative, lumbering giants of industry dipped their toes.

## Scope

I recently published an [Enterprise Ready Open Software Supplement](https://writing.kemitchell.com/2019/04/11/enterprise-supplement.html) under the [indieopensource.com](https://indieopensource.com) umbrella.  Basically, it's a legal form for selling the difference between big company license expectations and open license expectations.

What does that mean?

| "Enterprise Ready" | Open Normal |
| - | - |
| Demonstrate a basic understanding of common intellectual property traps for open software projects. | No understanding demonstrated. Widespread confusion abounds.  Most look past the question of whether contributors had the right to license. |
| Guarantee you have the intellectual property rights needed to license the project. | No such guarantee given. |
| Keep good records showing other contributors license their work appropriately. | Rely on non-legal community expectations of inbound=outbound licensing, reputation, and "too adopted to fail". |
| Give basic assurance that the project isn't covered by a known patent. | See no patents.  Hear no patents.  Speak no patents. |
| Promise to keep malicious code, like malware, out of the software. | `THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED...` |
| Give an explicit patent license. | MIT, BSD, ISC, and similar do not. |
| Forgive inadvertent breaches of the project's license. | Most licenses immediately terminate for even inadvertent breach of basic conditions, like attribution. |
| Stand behind your guarantees financially. | `IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY...` |

We can use this "diff" as a baseline, to look at different initiatives to change how open software is done, and how they relate to the kind of business bringing these expectations.

### Blue Oak

Drop a few requirements from the table above and layer on top of existing open source licenses, and you end up with the [Blue Oak Model License](https://blueoakcouncil.org/license/1.0.0).  Blue Oak better addresses patents, contributor licensing, and forgiveness for breaches, not in private terms for paying customers, but in the public license terms for all.

As a consequence, if you use Blue Oak and want to sell additional assurances under something like the Enterprise Ready Supplement, you have less to offer, because given more away.  Not that that's necessarily a bad thing.

### Apache

Drop a few different requirements from the table above and layer on top of the Apache License, and you end up with [The Apache Way](https://www.apache.org/foundation/how-it-works.html).  Apache addresses contributor licensing issues head on, with processes and [standardized CLAs](https://www.apache.org/licenses/#contributor-license-agreements).  Their standard license gives explicit patent permission, but doesn't offer forgiveness for inadvertent breaches.  They don't offer corporate warranties, but anticipate that [other companies building on their code will](https://www.apache.org/licenses/LICENSE-2.0#additional).

Overall, Apache has earned its reputation for welcoming companies, and company programmers, into open source.  And also for serving as ideal neutral ground to receive projects born in one corporate environment, but seeking adoption in others.

### Tidelift

Add a few ongoing maintenance obligations to the table above and layer on top of existing open source licenses, and you get the [Tidelift](https://tidelift.com/) package.  From [their summary](https://tidelift.com/docs/lifting/tasks-overview):

> ## Goals: what we ask you to do
> - Make sure that the package gets to, and stays at, a level of maturity that enterprise subscribers expect.
> ...

Issues like right to license and forgiveness for breaches get covered in [the "Lifting Agreement"](https://writing.kemitchell.com/2018/09/18/Lifting-Agreement.html) developers agree to in order to take pay through the platform.

Tidelift recently took this a step further, by rolling out software tooling [flagging software dependencies as "unmaintained"](https://blog.tidelift.com/up-to-20-percent-of-your-application-dependencies-may-be-unmaintained).  Quibbles about heuristics and sales-driver-FUD-factor aside, the more basic question is whether that distinction---essentially the absence of the kind of enterprise-friendly maintenance that Tidelift brokers---is meaningful, or ought to be encouraged.

Lots of money has been made running dependencies that Tidelieft flags as unmaintained.  In other words, firms got away with without maintenance.  Should open developers appease, and therefore reinforce, enterprise expectations that those dependencies ought to stay the same, and someone ought to maintain them?  Or should open be teaching closed to embrace permissionless forks, small-module substitution, and [package succession](https://github.com/yargs/yargs), instead?  Should funding mechanisms be teaching in-house developers to delegate work to the open "community" by default, or to join that community, and do it themselves?

### License Zero

Finally, compare the [License Zero form private license](https://licensezero.com/licenses/private), the thing that License Zero sells on behalf of developers.  It's just a grant of permission, without any one-time or ongoing service obligation.

License Zero adds nothing to the public license for the project being licensed, other than what is missing from the public terms, [noncommercial](https://licensezero.com/licenses/prosperity) or [copyleft](https://licensezero.com/licenses/parity).  This is [in line with dual-licensing wisdom distilled from long experience](https://monty-says.blogspot.com/2009/08/thoughts-about-dual-licensing-open.html).

That design reflects a fundamental difference in approach.  [Artless Devices](https://artlessdevices.com), the company behind License Zero, doesn't negotiate with big-company procurement departments for deals with the customer.  Rather, it serves as developers' agent for [selling licenses to their developer peers](https://blog.licensezero.com/2018/01/26/developer-licensing.html) directly, more [vending machine](https://licensezero.com/vending-machine.svg) than matchmaker.  License Zero does everything it can to _avoid_ coupling open software developers to the expectations and norms of corporate production and procurement.

Like other approaches analyzed here, License Zero is consistent, from its own point of view.  But it seems to answer key questions about the relationship of open developer to the enterprise differently.

## Upstream

By insisting that open licensing norms are enough, License Zero is rowing upstream of the corporate river, as open source licensing itself once did.  But open victory was never total.  Open style licensing, publicly or privately, now charts a course up a tributary of the way software is bought and sold, not the main course.

There are no standardized, open-source-style terms for services, free or paid.  (Yes, I'm working on it.)  If you do a deal with a service provider---for infrastructure, a platform, or an application---you do a deal in the way big companies understand and expect, either self-serve on take-it-or-leave-it terms, or negotiated through sales and procurement.  In other words, there's no standard corporate _policy_ that says employees can use such-and-such kind of online service for free.  Only machinery to get one-off deals for those services closed.

Turning a software program into a service offering is more and more the predominant way that commercial software makers couple themselves to customers today.  Many programs, from general purpose databases to project management suites, can be transmuted, as if by magic, from software that corporate customers prefer to download and expect to use for free, under open source policies, into software that corporate customers expect to pay for.  All of the slicing and dicing of features and permission, for which companies doing open core or innovating in licensing [stand accused of today](https://opensource.com/article/19/4/fauxpen-source-bad-business), is far more rife, and accepted, in software-as-a-service.  Between one set of expectations that drives price to free, and another set of expectations that anticipates payment, why on earth would a business choose the former?

In myriad ways, the infrastructure of open software---from licenses to architecture---fossilizes the state of software play in the 1990s, before the current thin-client, service-oriented, consumer-Internet-enabled revival.  It hasn't adapted to respond to proprietary service licensing, the "[cloud computing](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf)" economy, the way it once responded to proprietary software distribution.  Failing to adapt its challenge, open software has in many respects simply been subsumed, made subservient.  Even so-called "strong copyleft" software is often built into closed services without so much as a whimper.

## Self-Preservation

For those wedded philosophically to open values and ways of working, one response is simply: "no enterprise".  Don't court their attention.  Don't cater to their needs.  Don't seek them as customers.  They'll change you.

I suspect this isn't nearly so rare as it seems.  I am certainly not the first to expound it.  [Quoth the 37 Signals](https://m.signalvnoise.com/why-we-never-sold-basecamp-by-the-seat/):

> The problem with per-seat pricing is that it by definition makes your biggest customers your best customers.  With money comes influence, if not outright power.  And from that flows decisions about what and who to spend time on.  There's no way to be immune from such pressure once the money is flowing. The only fix is to cap the spigot.
>
> ...
>
> Has this outlook cost us money?  I'm sure it has.  Over the years, we've gotten countless knocks on the door from large corporations and organizations begging us for an enterprise sales track.  And while flattering, we said thanks, but no thanks.

All of the Basecamp team's concerns about big company-to-company deals would have applied equally well to sales through License Zero in its first incarnation, as a vendor of both solo-developer licenses and site licenses.  All the trade-offs, including big-payoff corporate leads, apply to its current, evolved approach, which focuses on developers, however and wherever they happen to work.

Perhaps the drive for "sustainability", with its [predictable consequences](https://blog.licensezero.com/2019/04/18/diglossia.html), and [sustainability as a service](https://blog.licensezero.com/2019/03/16/sustainability-as-a-service.html), with its drive to entrench them, will simply complete on the level of open developer compensation what the industry has already wrought in the practice of open software consumption.  Perhaps any approach to developer pay---what I consciously term "gainful open development"---will inevitably become niche, as the niche of open software practice not yet remade in the enterprise image shrinks.  Perhaps.

I have hope.  But to make a difference, I have to explain the difference.  If I've expressed a difference that resonates with you, reach out.  I'm on all the [usual](mailto:kyle@artlessdevices.com) [channels](https://twitter.com/licensezero).
