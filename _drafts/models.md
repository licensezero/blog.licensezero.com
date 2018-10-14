---
title:
layout: post
---

Most open source business models aren't business models at all.  Rather, they _presuppose_ a business model, and proffer open source as a power-up.  Very often, the model is actually "sell closed software", one way or another.  Open's just a way of selling more of something closed.

If you want to work in the open, you need to find open source business models that are actual business models.  Fortunately, many of those models have long track records.  There is also plenty of new territory left to explore.

# History

The history of open source software is the history of a bid for software industry acceptance.  The software industry primarily sells closed software, to install or use as a service.  So key to courting industry was showing open could compliment closed.  Consider the business models summarized in Raymond's _Magic Cauldron_:

- _Loss-Leader/Market Positioner_, example Netscape's Mozilla, a proprietary software business

- _Widget Frosting_, example Darwin from Apple, a hardware business

- _Give Away the Recipe, Open A Restaurant_, examples Cygnus and RedHat, professional services firms

- _Accessorizing_, example O'Reilly Media, a bookseller

- _Free the Software, Sell the Brand_, example Star Office, now OpenOffice.org and LibreOffice, the crux of a certification business

- _Free the Software, Sell the Content_, for intangible media businesses

All of these models assumed a preexisting, functioning business model doing something other than creating open source software.  But one of Raymond's models was not like the others:

- _Free the Future, Sell the Present_, key example Ghostscript from Aladdin Software, now Artifex, a company that offered its latest work on proprietary terms, but released older versions as open source

Like _Loss-Leader_, _...Sell the Present_ presupposes a proprietary software business to lead into.  But there's a silver lining: proprietary software _becomes_ open source in time.

# Evolution

_Sell the Present, Free the Future_ has evolved.  [The Business Source License](https://mariadb.com/bsl11), originally written for MariaDB, open successor to MySQL, automates the process, using legal terms.  The company can publish its code under The Business Source License immediately, or even work in the open to begin with.  Once the code reaches a certain age, the license transforms into a standard open license, effectively releasing the code.

Whether a company releases its old code by publishing it, or by publishing it with a time-delayed license, the general approach puts them on a kind of treadmill.  The company has to keep developing, keep maintaining, keep offering new functionality worth buying, to earn license fees.  It can't rely on revenue for code written long ago, which has become open, to earn money.  On the upside, automatic release ensures that if the company side of the project does fail, its code will remain available for the community, which can use and develop it on open terms.

For incomplete software like libraries and frameworks, useful only when built into other programs, the treadmill proved unnecessary.  By choosing an open license that prohibits reuse in closed software---a _copyleft_ license like AGPL---companies create opportunity to sell licenses for closed use.  They can license not just their latest work, released as open source as soon as it's developed, but also old work.  This is _Dual Licensing_ as we know it today: releasing software under a copyleft license, and selling alternative licenses for the same software to do what copyleft doesn't allow.

MySQL famously pioneered this approach to the client libraries for their database.  Ghostcript eventually followed, releasing its latest and greatest under GPL terms in real time, while charging commercial developers for permission to build on and distribute Ghostscript as part of closed systems, especially software for printers.

# Completeness

Crucially, models based on selling permission for software, like dual licensing and _...Sell the Present_ before it, make money by selling the value of software, in the form of deals for permission to reuse in closed systems.  That makes permission-based models complete in themselves.  They don't have to presuppose any other business model to bring money into the picture.

A single, integral business model affords many benefits, from operational simplicity to lower overhead and clear purpose.  There's no splitting time between open and closed software, or incentives to make features closed, as for _Loss-Leader_, often called _Open Core_.  There's no need to develop an orthogonal, capital-intensive hardware, media, or publishing business first, or to accept software development as a second-rate endeavor at the company, as under _Widget Frosting_, _Accessorizing_, or _...Sell the Content_.  There's no pressure to divert time and attention to services, to specialize developers to development or service, or to accept the relatively poor scaling dynamics of person-bounded service or support plays, as under _Give Away the Recipe..._ or _...Sell the Brand_.

Just make open software, make it as good as possible, and charge as much money as you can for the right to build closed applications and services with it.  Take the money from people working closed, and pay it to people making open.

# Map

Fortunately, _Dual Licensing_ is just one member of a broad family of "pure" open source business models.  Even under the constraint that if a company makes software, that software must be or become open, there is quite a bit of choice.  Some choices are well explored.  Others remain uncharted.

We can map those choices by stepping away from the vendor point of view, into the customer point of view, to remember what users need to benefit from software.  One generalization:

- _Implementation_: Users can't run software that doesn't exist.
- _Distribution_:  Users can't run software somebody else wrote, but didn't share.
- _Permission_:  Users can't safely run software without a license.

Each of these is _necessary_, but not alone _sufficient_.  Users need all three at any significant scale.

Developers can meet each of these needs _completely_ or _partially_.  They can implement all the software a customer needs or wants, or only part of it.  They can  distribute code by publication on the Internet, or share it only with customers.  They can grant permission to do everything with their software, or only some things.  They can grant permission for the software to everyone, or only to customers.

Developers can also meet users' needs at different times.  They can implement software before payment or after payment.  They can do half an implementation before payment, and half after.  They can give limited permission before they get paid, or none at all, and limited or complete permission after.

But in meeting user needs with open software over time, developers don't have total freedom.  There are some invariant, background rules and and practicalities that create relationships between user needs, and act as practical constraints on an open developer's approach.

For example, once someone implements software, they usually don't have to implement it again.  Assignments of intellectual property rights, exclusive licenses, data loss, and lack of maintenance for compatibility, among other factors, can take previous implementations away.  But generally, implemented now means implemented later.

On the legal front, once software's distributed under a common open license, it can be legally and practically difficult to _reduce_ the permission others receive for the same software.  On the other hand, it can be relatively straightforward to reduce permission for as yet unreleased code, and to increase permission for code already released.  It's difficult to change the license terms for a prior published release from MIT to GPL, but it's often possible to apply GPL to new work on an old MIT project, or to change the terms for your old work from GPL to MIT. 

For a mix of legal and practical reasons, once code's distributed with open source permission, it's usually hard or impossible to control further distribution or permission.  You can grant an MIT license for particular software to a particular customer.  They may just keep the software to themselves, especially if it represents a competitive advantage.  But there's no stopping them publishing the same code online, resulting in free copies and licenses for everyone.  Conversely, granting permission under typical commercial terms gives developers find-grained, configurable control over who else gets a copy and permission.

# Nowhere

Not every approach to meeting user needs is a business plan.  If you implement, distribute, and give permission away, completely and before payment, full stop, you do not have a business model.  You need to fulfill at least one need, for at least some users, _after payment_, and not before.

You can absolutely have a business without meeting that criterion, but you will need to find a model elsewhere: perhaps one of the plans Raymond described, perhaps a plan for more personal benefit, like social enjoyment, educational value, or reputation.  But giving work away, on its own, is the antithesis of a plan for getting paid.  If you receive compensation for generosity, either you weren't actually being generous, your "customer" was, or one of you made a terrible mistake.

Archetypical permission-based business plans like dual licensing typically don't hold back on implementation or distribution.  They implement all the code needed to make their projects complete, and distribute all of that code.  Even in terms of permission, permission-based business models still give quite a lot of away.  Their business model is selling whatever permission is "missing" form their choice of public license, from their customers' points of view.  But even common public license choices come riddled with known loopholes, especially for internal and software-as-a-service use.

But of course permission isn't the only dimension in which an open source business model can hold back.  Implementation-based business models are in fact even more broadly practiced than permission-based models.  So much so, in fact, that we often neglect to mention them in business-model conversations at all.

Selling implementation of software that you will distribute with broad permission is paid open source development.  Rather than writing a bunch of code, distributing it, and then figuring out how to charge for it, you charge first, then develop and deliver.

It's very possible, and indeed common, to combine implementation- and permission-based models.  Sign a contract for paid open source development.  Make sure you retain ownership of intellectual property in your work, especially copyright, and commit to release on the terms of an open-only license, like AGPL.  Charge a premium for the development work, since for most end-users, you won't have another opportunity to get paid for the same work.  But mention in your license notice that you'll entertain offers to dual license existing work on more permissive terms.

If there's work still to do, you can also mention that you'll happily do paid contract work to develop the project further, on the same kind of terms you used before.  If you'd already implemented that software, and sold it as proprietary software, you'd be running the _Open Core_ model, with the proprietary add-ons as the "Closed Shell".  Instead you're sticking to a pure open source model, by moving implementation after payment.  

Alternatively, implement software for which you think there will be demand, without a business deal in place.  This entails a bit of speculation on your part, both in what you think is worth making, and also in the time you take to make it.  Distribute this software under open-only terms.  But also offer to relicense some or all of your work on more permissive terms, like MIT or Apache 2.  Signing that deal is essentially a dual licensing transaction, except the alternative license, which would usually apply only to the customer in traditional dual licensing, applies to everyone, just like the public license.  Instead of giving each customer complete permission, one by one, after payment, you give everyone complete permission after payment.
