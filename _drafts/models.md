---
title: Mapping True Open Source Business Models
description:
layout: post
---

Most open source business models aren't business models at all.  They assume a business model, and tell us open source will make it better.  Very often, the actual business model is "sell closed software", one way or another.  Open's just a way of selling more closed.

If you want to work in the open, you need an open source business model that stands on its own.  Fortunately, complete open source models exist, and many have long track records.  There is also plenty of new territory left to explore.  This post offers the first draft of a map for that territory.

# History

The history of open source software is a bid for acceptance from the software industry.  The software industry mostly sells closed software, as apps or services.  So key to courting industry was showing open could complement closed.  

Consider the business models summarized in Raymond's _Magic Cauldron_:

- _Loss-Leader/Market Positioner_, example Mozilla, from Netscape, a proprietary web server company hoping to stop Microsoft from dominating the web browser market

- _Widget Frosting_, example Darwin, from Apple, a hardware maker

- _Give Away the Recipe, Open A Restaurant_, examples Cygnus and RedHat, professional services firms

- _Accessorizing_, example O'Reilly Media, a technical bookseller and conference host

- _Free the Software, Sell the Brand_, example Star Office, now OpenOffice.org and LibreOffice, the crux of a certification business

- _Free the Software, Sell the Content_, for intangible media businesses

Each of these models assumed another functioning business model doing something other than creating open software.  Each of these models offered open source as a way to defended or feed those lines of business.  But one of Raymond's models was not quite like the others:

- _Free the Future, Sell the Present_, key example Ghostscript, from Aladdin Software, now Artifex, which offered its latest work on proprietary terms, but released older versions as open source

Like _Loss-Leader_, _Free the Future, Sell the Present_ presupposes a proprietary software business.  But there's a silver lining: that proprietary software _becomes_ open source in time.  In the end, the company's efforts flow into the open.

# Evolution

_Free the Future_, also known as _Delayed Release_, evolved.  [The Business Source License](https://mariadb.com/bsl11), originally written for MariaDB, open successor to MySQL, automates the process, using legal terms.  The company can publish its code under The Business Source License immediately, or even work in the open from the get-go.  Once the code reaches a certain age, set by the license, its terms transform into those of a standard open license, effectively releasing the code as open source without any further action by the company.

Whether a company releases its old code by publishing it on a schedule, or by publishing under proprietary terms and relicensing open on a schedule, the company steps onto a treadmill.  It has to keep developing, keep maintaining, keep offering new functionality worth licensing on its own, to earn license fees.  It can't rely on revenue for code written long ago, because that becomes open, allowing use without pay.  But if the company fails, automatic release ensures its code will remain available for the open community, which can use and develop it on open terms.

For incomplete software like libraries and frameworks, useful only when built into other programs, the treadmill proved unnecessary.  By choosing an open license that prohibits reuse in closed software---a _copyleft_ license like AGPL---companies create opportunity to sell licenses for closed use.  They can license not just their latest work, released as open source as soon as it's developed, but also old work.

This is _Dual Licensing_ as we know it today. Release software under a copyleft license, and sell alternative licenses for the same software to do what the copyleft license doesn't allow.

MySQL famously applied this model to the client libraries for their database.  Ghostcript eventually followed, releasing its latest and greatest under GPL terms in real time, while charging commercial developers for permission to build on and distribute Ghostscript as part of closed systems.  Printer manufacturers, who build Ghostscript into their printers' software, paid to ship the latest and greatest.

# Completeness

Crucially, models based on selling permission for software, like _Dual Licensing_ and _Delayed Release_ before it, make money by selling the value of software, in the form of deals for permission to use for closed systems.  That makes permission-based models complete in themselves.  They don't have to create some other kind of value to charge for.  The value they sell is the value of the software, and the software is open.

A single, complete business model affords many benefits, from operational simplicity to lower overhead and clarity of business purpose.  There's no splitting time between open and closed software, or incentives to make features closed, as for _Loss-Leader_, now popular as _Open Core_.  There's no need to develop an orthogonal, capital-intensive hardware, media, or publishing business first, or to accept software development as a second-rate endeavor at the company, as under _Widget Frosting_, _Accessorizing_, and _Sell the Content_.  There's no pressure to divert time and attention to services, or to divide developers into coding developers and service developers, or to accept the relatively poor scaling dynamics of person-bounded service or support plays, as under _Give Away the Recipe_ and _Sell the Brand_.

Just make open software, make it as good as possible, and charge as much money as you can for the right to build closed applications and services with it.  Take money from people working closed, and use it to work open.

# Map

Fortunately, _Dual Licensing_ and _Delayed Release_ are just two members of a broader family of complete business models for open source development.  Even under the constraint that software developed must become open source, there is quite a bit of choice.  Some choices are well explored, and well proven.  Others have yet to be tested.

We can map those choices by stepping away from the vendor point of view, into the customer point of view.  What do customers need to benefit from software?  A generalization:

- _Implementation_: Users can't run software that doesn't exist.
- _Distribution_:  Users can't run software someone else wrote, but didn't share.
- _Permission_:  Users can't safely run software without a license.

Each of these is necessary, but not alone sufficient.  Users need all three at any significant scale.

Developers can meet each of these needs _partially_ or _completely_, form a user's point of view.  They can implement all the software a customer needs or wants, or only part of it.  They can distribute code by publication on the Internet, or share it only with specific customers.  They can grant permission to do everything with their software, or only some things.

Developers can also meet users' needs at different times.  Some models incorporate time through deadlines or schedules.  That's true of _Delayed Release_: closed software gets released as open on a schedule.  Other models incorporate time for conditionality, most crucially _before payment_ and _after payment_.  Under _Dual Licensing_, a developer grants incomplete permission before payment, and complete permission after payment.  A developer can also do half an implementation before payment, and half after.

Finally, developers can segment implementation, distribution, and especially permission. They can implement what one customer needs or wants, but not what another does.  They can distribute copies to some users, but not to others.  They can grant permission for the software to everyone, or only to customers.

# Constraints

Practical circumstances, the nature of software, and norms of open software limit developers' choices.  There are some invariant, background rules and and practicalities that serve as constraints, linking choices about user needs and affecting what choices developers can make over time.  Some choices and series of choices simply aren't available.

For example, on the legal front, once software's distributed under a common open license, it can be legally and practically difficult to _reduce_ the permission others receive for the same software.  On the other hand, it can be relatively straightforward to reduce permission for as yet unreleased code, and to increase permission for code already released.  It's difficult to change the license terms for a prior published release from MIT to GPL, but it's often possible to apply GPL to new work on an old MIT project, or to change the terms for your old work from GPL to MIT. 

For a mix of legal and practical reasons, once code's distributed with open source permission, it's usually hard or impossible to control further distribution or permission.  You can grant an MIT license for particular software to a particular customer.  They may just keep the software to themselves, especially if it represents a competitive advantage.  But there's no stopping them publishing the same code online, resulting in free copies and licenses for everyone.  Conversely, granting permission under typical commercial terms gives developers fine-grained, configurable control over who else gets a copy and permission, and when.

# Nowhere

Every approach to meeting software users' needs over time is a software-production model, but not every software-production model is a business model.  If you implement, distribute, and give permission away, completely, without segmenting users, and before payment, full stop, you do not have a business model.

A business model means fulfilling at least one need, more completely than you have before, for more users than you have before, _after payment_, and not before.  Any model meeting that criterion is a complete business model.  Any business model meeting the additional criterion of creating only software that becomes open source is a complete open source business model.

You can have a business without a complete open source business model, but your model will need to be complete for some other business, like producing closed software.  If you're at a firm, perhaps you employ one of the models Raymond described.  If the only business you manage is your own, perhaps your open source works leads into a personal payoff, like educational value, reputation, or personal enjoyment.

To avoid self-deception, it's key to remember that giving software away, on its own, is the antithesis of a plan for getting paid, a business plan.  If you receive compensation for such generosity, either you weren't being entirely generous to begin with, your "customer" was the one being generous, or one of you has made a mistake.

# Exploration

With all of this in mind, we can begin to chart a few complete, pure open source business models, known-viable and innovative.

There are a few ways to group models.  Most obviously, we can categorize by the user needs leveraged: implementation, distribution, or permission.  Hybrid models leverage more than one.  Within our framework, the relevant question is:

> Which needs does the model fulfill for at least some users only after payment?

We can also ask whether a model requires meaningful speculation on the part of the developer.  Within our framework, that means:

> Does the developer implement before payment?

The higher the cost of implementation---the more labor-intensive, the more expensive inputs like outside help, data, and development tools, the more the business chooses to implement up-front---the greater the speculative bet.  Large enough bets require enlisting other speculators, be they investors, lenders, or contributors willing to work for uncertain compensation.  The need to recruit other speculators limits the number of businesses that can employ the model.

We can also ask whether the model segments the market for any particular user need.  In our terms:

> Does the developer fulfill any user need for less than all users at a time?

Segmenting implementation, distribution, or permission carries an administrative or transactional cost.  Treating everyone the same, by writing the same code, publishing to the net, and licensing under one set of terms that apply the same to everyone, is relatively simple, thanks to the Web.  But as we'll see, segmentation also creates business model choice.

Let's map and group and some models we've already discussed, then move on to some we haven't.  From there, we can chart a course from purebred models to less familiar hybrid models.

## The Coordinate System

Software users have three needs: _implementation_, _distribution_, _permission_.

Software user needs are fulfilled with more or less _completeness_, at some point in _time_.

A model _leverages_ a user need if it completes that need in time only after payment.

A model is _segmented_ if it completes a user need for less than all users at a time.

A model is _speculative_ if it implements, partially or completely, at any time before payment.

## Purebred Models Outline

- Leverages Permission
  - Speculative
    - Segmented: [Dual Licensing](#dual-licensing)
    - Unsegmented: [Paid Relicensing](#paid-relicensing)
  - Non-Speculative:
    - Segmented: ???
    - Unsegmented: ???
- Leverages Distribution
  - Speculative
    - Segmented: [Paid Distribution](#paid-distribution)
    - Unsegmented: [Paid Release](#paid-release)
  - Non-Speculative: None (Developers cannot distribute as yet unimplemented software.)
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

The key question for dual licensing is whether a suitably acceptable open-source license allows the developer to release without giving complete permission to all users.  That's usually true when the software is a library or framework that must be built into applications distributed to end-users, or into web applications provided to end-users, to be useful.  Licenses like RPL, OSL, AGPL, and GPL require developers to provide complete source code and an open-source license to end-users in those cases, which closed-software developers refuse to do.

Developer tools like bundlers, compilers, static analyzers, debuggers, and editors aren't typically built into and distributed with applications.  License Zero's [Parity license](https://licensezero.com/licenses/parity) makes dual licensing viable for developer tools, by eliminating any license distinction based on _how_ applications are built with open software.  Licensed use of Parity-licensed software to create other software requires release of the other software. 

[License Zero](https://licensezero.com) automates the back-end dual licensing process of selling permission to use for closed software.  

## Paid Relicensing

- In Brief: Change the license terms for software under an open-only license, like AGPL, to permissive terms that permit use in closed programs, like MIT, for a fee.

- Implementation: complete before payment (speculative)
- Distribution: complete before payment
- Permission:
  - use in open software before payment
  - use in closed software, after payment, for all users (not segmented)

As with _Dual Licensing_, developers can only employ _Paid Relicensing_ to projects for which open-source license terms allow them to grant partial permission.

_Paid Relicensing_ differs form _Dual Licensing_ only in segmentation.  _Dual Licensing_ segments by customer.  Each customer buys their own license to use in closed software.  _Paid Relicensing_ doesn't segment.  Once _anyone_ pays for permission to use in closed source, _everyone_ gets that permission.

As a consequence, the cost of paid relicensing should greatly exceed the cost of buying closed-software permission for a single customer.  The developer is forfeiting not just the ability to sell permission to the customer again, but also the ability to sell all other potential customers.

Paid relicensing at such higher prices can and does make sense, financially, for both developer and paying customer. Often, the relicensing customer intends to build and distribute a product that its own customers will in turn use to build closed software.  On the developer side, a willingness to relicense for a single price reflects the administrative burden or doing and processing licensing deals with all possible customers.  If the sale value of a license is low, there are many potential customers, and the cost or hassle of selling each of them is high, taking a single lump-sum, essentially the present value of that potential business, makes more sense.

License Zero automates the process of selling paid licenses, even to many potential customers.  That helps increase the price at which developers will relicense projects.  But License Zero also [allows developers to offer and close deals to relicense](https://guide.licensezero.com/#relicensing).

## Delayed Release

- In Brief: Develop and license closed software, but release it under open terms on a schedule.
- Implementation: complete before payment (speculative)
- Distribution:
  - Old Code: complete before payment
  - New Code:
    - none before payment
    - complete after payment, to the paying customer only
- Permission:
  - Old Code:
    - none before scheduled release
    - complete after scheduled release
  - New Code:
    - none before payment
    - complete after payment, to the paying customer only

A delayed-release model can employ any kind of open license: a permissive license that permits reuse in closed software, or a copyleft license that doesn't.

Though delayed-release models have generally evolved toward dual licensing, delayed release remains useful in working around dual licensing's limitations.  If the software itself is an application, usable on its own, open source licensing doesn't offer an effective partial-permission option.  Effectively, releasing that application under any open source license gives all permission away, to all users.  That means developers can't give partial permission before payment, and complete permission only after.  But delaying release of the latest and greatest version gives a business the ability to distribute partially before payment, and distribute completely after payment.

License Zero doesn't implement the delayed release model.  Instead, License Zero's [Prosperity license](https://licensezero.com/licenses/prosperity) gives developers a license that allows only noncommercial use.  Very few people consider noncommercially licensed projects to be "open source".  But such a license gives developers a license option with which to offer partial permission before payment, facilitating the dual licensing model.  For developers of applications that aren't software development tools, noncommercial dual licensing also allows developers to license the whole value of the software they've created, rather than just the difference between the old code they've already released, and the latest and greatest they haven't, under a delayed release model.

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

Commentators often forget paid open development among business models.  It suffers many of the same drawbacks as professional service models, including paid support.  But when priced rationally, it can do well.

Note that paid development can entail release of code under any open source license.  That license is usually agreed ahead of time.

## Paid Development Hybrids

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

## Paid Distribution

- In Brief: Release software and charge for distributing copies.

- Implementation: before payment (speculative)
- Distribution:
  - none before payment
  - complete after payment, to the paying customer only
- Permission: complete before payment

The FSF once made money this way.  Cheap, Web-based distribution and the freedom to redistribute under open licenses have made it nearly extinct where reliable Internet access is widespread.