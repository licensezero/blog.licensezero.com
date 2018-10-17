---
title: Exploring Complete Open Source Business Models
description: a framework for financial independence
layout: post
---

Most open source business models aren't business models at all.  They assume a business model, and tell us that open source will make it better.  Very often, the actual business model is "sell closed software", one way or another.  Open's just a way of selling closed.

If you want to work in the open, you need an open source business model that stands on its own.  Fortunately, complete open source models exist, and many have long track records.  There is also plenty of new territory left to explore.  This post offers the first draft of a map for that territory.

# History

The history of open source software is a bid for acceptance from the software industry.  The software industry mostly sells closed software, as apps or services, so key to courting industry was showing open could complement closed.  

Consider the business models summarized in Eric S. Raymond's _Magic Cauldron_:

- _Loss-Leader/Market Positioner_, example Mozilla, from Netscape, a proprietary web server company hoping to stop Microsoft from dominating the web browser market

- _Widget Frosting_, example Darwin, from Apple, a hardware maker

- _Give Away the Recipe, Open A Restaurant_, examples Cygnus and RedHat, professional services firms

- _Accessorizing_, example O'Reilly Media, a technical bookseller and conference host

- _Free the Software, Sell the Brand_, example Star Office, now OpenOffice.org and LibreOffice, the crux of a certification business

- _Free the Software, Sell the Content_, for intangible media businesses

Each of these models assumed another functioning business model doing something other than creating open source software.  Each of these models offered open source as a way to defend or feed those lines of business.  But one of Raymond's models was not quite like the others:

- _Free the Future, Sell the Present_, key example Ghostscript, from Aladdin Software, now Artifex, which offered its latest work on proprietary terms, but released older versions as open source

Like _Loss-Leader_, the _Free the Future, Sell the Present_ model presupposes a proprietary software business.  But there's a silver lining: that proprietary software _becomes_ open source in time, on a schedule.  In the end, the company's efforts flow into the open.

# Evolution

_Free the Future_, also known as _Delayed Release_, evolved.

The Business Source License, originally written for MariaDB, successor to MySQL, automates the process, using legal terms.  A company can publish its code under The Business Source License _before_ its scheduled release date, or even work publicly, online, by default.  Before the release date, the license gives permission for non-production use only.  On the scheduled release date, the license's terms automatically transform into those of a standard open source license, effectively releasing the code as open source without any further action by the company.

Whether a company releases its old code by publishing it on a schedule, or by publishing under proprietary terms and relicensing on schedule, the company steps onto a treadmill.  It has to keep developing, keep maintaining, keep offering new functionality worth licensing on its own, to earn license fees.  It can't rely on revenue from code written long ago, because that becomes open, allowing use without pay.  But if the company fails, automatic release ensures its code will remain available for the open community, which can use and develop it on open terms.

For incomplete software like libraries and frameworks, useful only when built into other programs, the treadmill proved unnecessary.  By choosing an open license that prohibits reuse in closed software---a _copyleft_ license like AGPL---companies create opportunity to sell licenses for closed use.  They can license not just their latest work, released as open source as soon as it's developed, but also old work.

This is _Dual Licensing_ as we know it today. Release software under a copyleft license, and sell alternative licenses for the same software to do what the copyleft license doesn't allow.

MySQL famously applied this model to the client libraries for their database.  Ghostcript eventually followed, releasing its latest and greatest under GPL terms in real time, while charging commercial developers for permission to build on and distribute Ghostscript as part of closed systems.  Printer manufacturers, who build Ghostscript into their printers' software, paid to ship the latest and greatest, without making the rest of their systems open to competitors.

# Completeness

Crucially, models based on selling permission for software, like _Dual Licensing_ and _Delayed Release_ before it, make money by selling the value of software, in the form of deals for permission to use for closed systems.  That makes permission-based models complete in themselves.  They don't have to create some other kind of value to charge for.  The value they sell is the value of the software, and the software is open.

A single, complete business model affords many benefits, from operational simplicity to lower overhead and clarity of business purpose.  There's no splitting time between open and closed software, or incentives to make features closed, as for _Loss-Leader_, now popular as _Open Core_.  There's no need to develop an orthogonal, capital-intensive hardware, media, or publishing business first, or to accept software development as a second-rate endeavor at the company, as under _Widget Frosting_, _Accessorizing_, and _Sell the Content_.  There's no pressure to divert time and attention to services, or to divide developers into coding developers and service developers, or to accept the relatively poor scaling dynamics of person-bounded service or support plays, as under _Give Away the Recipe_ and _Sell the Brand_.

Just make open software, make it as good as possible, and charge as much money as you can for the right to build closed applications and services with it.  Take money from people working closed, and use it to work open.

# Map

Fortunately, _Dual Licensing_ and _Delayed Release_ are just two members of a broader family of complete business models for open source development.  Even under the constraint that software developed must become open source, there is quite a bit of choice.  Some choices are well explored, and well proven.  Others remain untested.

We can map those choices by stepping away from the vendor point of view and into the user point of view.  What do users need to benefit from software?  A generalization:

- _Implementation_: Users can't run software that doesn't exist.
- _Distribution_:  Users can't run software someone else wrote, but didn't share.
- _Permission_:  Users can't safely run software without a license.

Each of these is necessary, but not alone sufficient.  Users need all three at any significant scale.

Developers can meet each of these needs _partially_ or _completely_, form a user's point of view.  They can implement all the software a customer needs or wants, or only part of it.  They can distribute code by publication on the Internet, or share it only with specific customers.  They can grant permission to do everything with their software, or only some things.

Developers can also meet users' needs at different times.  Some models incorporate time through deadlines or schedules.  That's true of _Delayed Release_: closed software gets released as open source on a schedule.  Other models incorporate time for conditionality, most crucially _before payment_ and _after payment_.  Under _Dual Licensing_, a developer grants incomplete permission before payment, and complete permission after payment.  A developer can also do half an implementation before payment, and half after.

Finally, developers can segment implementation, distribution, and especially permission. They can implement what one customer needs or wants, but not what another does.  They can distribute copies to some users, but not to others.  They can grant permission for the software to everyone, or only to specific customers.

# Constraints

Practical circumstances, the nature of software, and norms of open software limit developers' choices.  There are some invariant background rules and and practicalities that impose constraints, linking choices about user needs and affecting what choices developers can make over time.  Some choices simply aren't available.

For example, on the legal front, once software's distributed under a standard open source license, it's legally and practically difficult to _reduce_ the permission others receive for the same software.  On the other hand, it can be relatively straightforward to reduce permission for as yet unreleased code, by applying different license terms for working going forward, and to increase permission for code already released, by announcing a license change.  It's difficult to change the license terms for a prior published release from MIT to GPL, but it's often possible to apply GPL to new work on an old MIT project, or to change the terms for your old work from GPL to MIT. 

For a mix of legal and practical reasons, once code's distributed with open source permission, it's usually hard or impossible to control further distribution or permission.  You can grant an MIT license for particular software to a particular customer.  They may just keep the software to themselves, especially if it represents a competitive advantage.  But there's no stopping them publishing the same code online, resulting in free copies and licenses for everyone.  Conversely, granting permission under typical commercial terms gives developers fine-grained, configurable control over who else gets a copy and permission, and when.

# Nowhere

Every approach to meeting software users' needs over time is a software-production model, but not every software-production model is a business model.  If you implement, distribute, and give permission away, completely, without segmenting users, and before payment, full stop, you do not have a business model.

A business model means fulfilling at least one need, more completely than you have before, for more users than you have before, _after payment_, and not before.  Any model meeting that criterion is a complete business model.  Any business model meeting the additional criterion of creating only software that becomes open source is a complete open source business model.

You can have a business without a complete open source business model, but your model will need to be complete for some other business, like producing closed software.  If you're at a firm, perhaps you employ one of the models Raymond described.  If the only business you manage is your own, perhaps your open source works leads into a personal payoff, like educational value, reputation, or personal enjoyment.

To avoid self-deception, remember that giving software away, on its own, is the antithesis of a plan for getting paid, a business plan.  If you receive compensation for generously giving software away, either you weren't being entirely generous to begin with, your "customer" was the one being generous, or one of you is very mistaken.

# Exploration

With all of this in mind, we can begin to chart a few complete, pure open source business models, known-viable and innovative.

There are a few ways to group models.  Most obviously, we can categorize by the user needs leveraged: implementation, distribution, or permission.  Within our framework, the relevant question is:

> Which needs does the model fulfill for at least some users only after payment?

Purebred models leverage primarily one particular user need.  Hybrid models leverage more than one.  

We can also ask whether a model requires meaningful speculation on the part of the developer.  Within our framework, that means:

> Does the developer implement before payment?

The higher the cost of implementation---the more labor-intensive, the more expensive inputs like outside help, data, and development tools, the more the business chooses to implement up-front---the greater the speculative bet.  Large enough bets require enlisting other speculators, be they investors, financial lenders, or contributors willing to work for uncertain compensation.  The need to recruit other speculators limits the number of businesses that can employ the model.

We can also ask whether the model segments the market for any particular user need.  In our terms:

> Does the developer fulfill any user need for less than all users at a time?

Segmenting implementation, distribution, or permission carries an administrative or transactional cost.  Treating everyone the same, by writing the same code, publishing to the net, and licensing under one set of terms apply to everyone is relatively simple, thanks to the Web.  But as we'll see, segmentation also creates business model choice.

Let's map and group and some models we've already discussed, then move on to some we haven't.  From there, we can extrapolate from familiar purebred models to less familiar hybrid models.

## The Coordinate System

As a brief review:

Software users have three needs: _implementation_, _distribution_, _permission_.

Software user needs are fulfilled with more or less _completeness_, at some point in _time_.

A model _leverages_ a user need if it completes that need only after payment.

A model is _segmented_ if it completes a user need for less than all users at a time.

A model is _speculative_ if it implements at any time before payment.

## Purebred Models Overview

- Leverages Permission
  - Speculative
    - Segmented: [Dual Licensing](#dual-licensing)
    - Unsegmented: [Paid Relicensing](#paid-relicensing)
  - Non-Speculative:
    - Segmented: [Paid Development to Dual Licensing](#hybrids)
    - Unsegmented: [Paid Development to Paid Relicensing](#hybrids)
- Leverages Distribution
  - Speculative
    - Segmented: [Paid Distribution](#paid-distribution)
    - Unsegmented: [Paid Release](#paid-release)
  - Non-Speculative: [Paid Development](#paid-development) (segmented or unsegmented)
- Leverages Implementation
  - Speculative: None (Models leveraging implementation are non-speculative by definition.)
  - Non-Speculative: [Paid Development](#paid-development) (segmented or unsegmented)

## Dual Licensing

- In Brief: Release software under an open-only license, and charge customers for permission to use for closed software.

- Implementation: complete before payment (speculative)
- Distribution: complete before payment
- Permission:
  - use in open software before payment
  - use in closed software after payment, for the paying customer only (segmented)

The key question for dual licensing is whether a suitably acceptable open-source license allows the developer to release without giving complete permission to all users.  That's usually true when the software is a library or framework that must be built into applications and distributed to end-users, or into web applications provided to end-users, to be useful.  Licenses like RPL, OSL, AGPL, and GPL require developers to provide complete source code and an open-source license to end-users in those cases, which closed-software developers refuse to do.

Developer tools like bundlers, compilers, static analyzers, debuggers, and editors aren't typically built into and distributed with applications.  License Zero's [Parity license](https://licensezero.com/licenses/parity) makes dual licensing viable for developer tools, by eliminating any license distinction based on _how_ applications are built with open software.  Licensed use of Parity-licensed software to create other software requires release of the other software.

[License Zero](https://licensezero.com) automates the back-end dual licensing process of selling permission to use for closed software.  Automation drags the administrative and transaction costs inherent in segmentation down toward zero.

## Paid Relicensing

- In Brief: Release software under an open-only license, like AGPL, and offer to relicense the software onto permissive terms that permit use in closed programs, like MIT, for a fee.

- Implementation: complete before payment (speculative)
- Distribution: complete before payment
- Permission:
  - use in open software before payment
  - use in closed software, after payment, for all users (not segmented)

Note that as with _Dual Licensing_, developers can only employ _Paid Relicensing_ to projects for which open-source license terms allow them to grant partial permission.

_Paid Relicensing_ differs form _Dual Licensing_ only in segmentation.  _Dual Licensing_ segments by customer.  Each customer buys their own license to use in closed software.  _Paid Relicensing_ doesn't segment.  Once _anyone_ pays for permission to use in closed source, _everyone_ gets that permission.

As a consequence, the cost of paid relicensing should greatly exceed the cost of buying closed-software permission for a single customer.  The developer is forfeiting not just the ability to sell permission to the customer again, but also the ability to sell all other potential customers.  As we'll see, the same pricing considerations apply to paid development.

Paid relicensing at such higher prices can and does make sense, financially, for both developer and paying customer. Often, the relicensing customer intends to build and distribute a product that its own customers will in turn use to build closed software.  On the developer side, a willingness to relicense for a single price reflects the administrative burden or doing and processing licensing deals with all possible customers.  If the sale value of a license is low, there are many potential customers, and the cost or hassle of selling each of them is high, taking a single lump-sum, essentially the present value of that potential business, makes more sense.

License Zero automates the process of selling paid licenses, even to many potential customers, reducing the cost of segmentation.  That helps increase the number of developers who can implement _Dual Licensing_, and increases the price at which developers can offer to relicense projects.  License Zero also [allows developers to offer and close deals to relicense](https://guide.licensezero.com/#relicensing).  But because the administrative and transaction costs of relicensing deals are relatively low---there's just one customer to deal with---and the price for relicensing is relatively high---much higher than for a private license that applies to just the paying customer---License Zero also provides [forms for closing relicense deals without using the License Zero platform](https://licensezero.com/licenses#quotes).  That way, developers can avoid fees for payment processing and brokerage through License Zero.

## Delayed Release

- In Brief: Develop and license closed software, but release it under open-source terms on a schedule.
- Implementation: complete before payment (speculative)
- Distribution:
  - Old Code: complete before payment
  - New Code:
    - Under the Business Source License:
      - complete before payment
    - Manually Releasing on Schedule:
      - none before payment
      - complete after payment, to the paying customer only
- Permission:
  - Old Code:
    - none before scheduled release
    - complete after scheduled release
  - New Code:
    - Under The Business Source License:
      - partial (non-production use) before payment
      - complete after payment, to the paying customer only (segmented)
    - Manually Releasing on Schedule:
      - none before payment
      - complete after payment, to the paying customer only

Note that a delayed-release model releasing new code manually can employ any kind of open license---a permissive license that permits reuse in closed software, or a copyleft license that doesn't---because leveraging distribution makes licensing permission irrelevant.  This points to the key way in which _Delayed Release_ remains relevant for business modelers.

Though delayed-release models have generally evolved toward _Dual Licensing_, delayed release remains useful in working around _Dual Licensing_'s limitations.  If the software itself is an application, usable on its own, the menu of standard open-source licenses doesn't offer an effective partial-permission choice.  Effectively, releasing that application under any standard open-source license gives complete permission away, to all users.  That means developers can't give partial permission before payment, and complete permission only after.  Delaying release of the latest and greatest version gives a business the ability to distribute partially before payment, and distribute completely after payment.

License Zero doesn't implement the delayed release model.  Instead, its [Prosperity license](https://licensezero.com/licenses/prosperity) gives developers a permission choice that allows only noncommercial use.  That makes Prosperity similar to the non-production-use permission granted by the Business Source License for new code that hasn't yet reached its scheduled open-source release date.

Very few people consider noncommercial or use-limited licenses to be "open source".  But such licenses give developers options with which to offer partial permission before payment, facilitating _Dual Licensing_.  For developers of applications that aren't software development tools, _Dual Licensing_ with a use-limited license allows selling the whole value of the software they've created, including the value of old code.  Under _Delayed Release_, they could only sell the value of the latest and greatest code that they haven't yet released as open source.

## Paid Open Development

- In Brief: Contract to develop and release open software for pay.

- Implementation:
  - none or incomplete before payment (non-speculative)
  - complete after payment
- Distribution:
  - none before payment
  - complete after payment
- Permission:
  - none before payment
  - complete or partial after payment

Note that paid development can entail release of code under any open source license.  That license is usually agreed ahead of time, in the contract for development services.

Commentators often forget paid open development among business models.  At scale, it suffers many of the same drawbacks as professional service models, including paid support.  But when priced rationally and practiced efficiently, it can do well.

The key to pricing rationally is recognizing the business model reality.  When paid development complements another business model not just on the client side, but on the developer side, clients can often drive a hard bargain.  We see this with relatively novice programmers, new freelancers, and experienced programmers without long track records of public open source work.  They often take discounts on their standard working rates to create open source, rather than closed software.

Conversely, when development and release don't create meaningful secondary business benefits for the developer, as in the case of an established developer, or a developer with a long open source record, focus shifts to the fact that open-source release eliminates future opportunity to sell similar work to other clients.  Service providers often succeed precisely by specialization, doing many projects in the same category over time.  Open-source release potentially turns would-be clients into free users, instead.  Some may even show up in bug trackers hoping for free maintenance and support from the developer.

License Zero doesn't address paid development.  [Switchmode](https://github.com/switchmode/switchmode), an open form contract for developers doing a mix of open and closed work, makes terms for open development widely available, for free.

## Paid Distribution

- In Brief: Release software and charge for distributing copies.

- Implementation: before payment (speculative)
- Distribution:
  - none before payment
  - complete after payment, to the paying customer only
- Permission: complete before payment

The FSF once made money this way.  Cheap, Web-based distribution and the freedom to redistribute under open licenses have made it nearly extinct where reliable Internet access is widespread.

## Hybrids

- In Brief: Contract to develop and release open software under a copyleft license for pay, then employ a permission-based model.  For example, with dual licensing:

- Implementation:
  - none or partial before payment (non-speculative)
  - complete after payment
- Distribution:
  - none before payment
  - complete after payment
- Permission:
  - use in open software before payment
  - use in closed software, after payment, for all users

We could also hybridize with paid relicensing and delayed release.

Who can dual license the newly implemented software depends on who owns the intellectual property rights in it, especially copyright.  If the developer transfers rights to the client, as work made for hire or by assignment, the company has the legal power to grant more complete permission, not the developer.  This is very common in standard contractor agreements, which typically aim to transfer all intellectual property to the company, in part just to avoid the effort and delay needed to decide whether the company needs the rights or not.

Conversely, if the developer retains its intellectual property rights, the developer can grant more complete permission.  Client and developer could also agree to share rights, by joint ownership or cross-licensing, perhaps with rules about sharing dual licensing revenue.  Regardless, whenever the developer retains rights, the contract for implementation typically includes a complete license to the client.

License Zero doesn't support hybrid models directly.  Instead, it's consciously designed, legally and in software, to make as few necessary assumptions about other models in practice as possible.  License Zero tries to be small, in that way, to preserve compatibility with other models.

[Switchmode](https://github.com/switchmode/switchmode), the author's open form contract for mixed open-closed development, preserves opportunity for hybrid models.  Developers and clients using Switchmode designate projects as open or closed.  For closed projects, developers assign intellectual property to their clients.  But for open projects, developers keep their intellectual property rights, and licenses the client on the same open-source license terms under which they promise to release their work.

License Zero can also play nice with other _Paid Development_ approaches.  It's a bit early to tell how, exactly, [Tidelift](https://tidelift.com) will structure participating developers' obligations.  But early marketing materials for the firm indicate that it could be combined with permission-based models like _Dual Licensing_, and from what I've seen so far, I agree.

# Wider World

I've tried to offer structure for thought about open source business models, generalizing open source history from early on.  But any attempt always represents the moment it was thought up, more than any other.

The open source community is in the throes of a broad debate about the scope of the community and the role that licensing norms play in it.  Having achieved acceptance at the pinnacles of the software industry, many in the open source movement are keen to capitalize and consolidate the approaches that serve that coalition best, notably patent-conscious, permissive license terms and broad commitments to detente and the use of exclusive soft power in copyleft communities.  Meanwhile, independent developers and small firms attempting to survive and thrive in an increasingly top-heavy industry are returning to reciprocal licensing as a bulwark against incumbent advantage.  They're suffering for the compromises written into the supposedly strong-copyleft community licenses they adopted, written for very different purposes, and riddled with compromises not in their interest.

BSD-school community members and enterprises have ensured emblems of acceptance for ever more permissive licenses, even legally precarious ones like FPL/0BSD and Unlicense.  Strong reciprocal licenses enjoy a similarly diverse constituency: free and open advocates tired of ruinous compromise, on the one hand, and independent and small businesses who need simple, complete business models, on the other.   But the radical copyleft constituency is not nearly so organized, not yet so self-consciously a coalition.  That is beginning to change, as more activists see their work slip through loopholes in old community licenses, and more entrepreneurial developers realize there's no blessed license with which which to drive any effective "free for open source" bargain, on strangely arbitrary grounds.

That asymmetry plays out in the large.  Open source now functions far more readily to exacerbate disparity, by allowing winners already flush with chips to double down when they stack the cards in their favor, and by establishing corporate charity as the entry fee for the online developer peer community, than to help upstarts challenge incumbents, as it once did.  That imbalance calls, in part, for more standardization in source-available, use-limited licensing, the ["third way"](https://blog.licensezero.com/2018/09/16/two-party.html) advocated here before.  But it also calls for a renewed project to reinvigorate maintenance of strong copyleft, both in license terms and within the community.  That's good not just for currently underserved open source contributors.  A broad contributor base is, and essential, for the movement as a whole.

---

Special thanks to [Dave Zvenyach](https://esq.io/blog/) for inspiration to get this written and early feedback.