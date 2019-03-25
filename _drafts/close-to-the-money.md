---
title: Close to the Money
description: dissing distinction without difference in distribution
layout: post
---

There's nothing magical about software as a service.  The value chain begins where the software begins.  Code isn't worthless until somebody makes SaaS with it.

Sure, some kinds of customers prefer to buy some kinds of software on a service basis.  I'm a [FastMail](https://fastmail.com/)-[Pinboard](https://pinboard.in/)-[IRCCloud](https://www.irccloud.com/)-[Feedbin](https://feedbin.me/) man, myself.  And a great many vendors prefer to sell it that way, and manage to bring customers along, more or less.  [Creative Suite](https://www.adobe.com/creativecloud/plans.html) always comes to mind.  But the same customers prefer other kinds software to download and install.  So SaaS is king, but so, apparently, are app stores and marketplaces.  For games.  For mobile apps.  For add-ons to the pricey programs people use to practice professions.

In the end, customers get the value of software, and pay for it.  But between producer and consumer, software gets distributed any which way.  When the customer makes software themself, tellingly, download-and-install is by far the predominant model.  That's also changing to some extent.  But all else equal, we'd rather run [devise](https://github.com/plataformatec/devise) than rely on [Auth0](https://auth0.com/).  We'd rather load [VS Code](https://code.visualstudio.com/) than log into a web-based IDE.  And not just 'cause open costs nil.  Not Invented Here cohabitates with Host Everything we Run Ourselves.

When large software sellers justify [how their financial expectations differ from those they think open developers are justified in having](https://blog.licensezero.com/2018/06/14/profit-sustainability.html), they often invoke nebulous, unattainable, and purportedly inherent commercial virtues of whatever distribution model they happen to use, and you don't.  It's commercial predestination.  You are not among the Chosen Vendors, and cannot see The Light.  Rented services are the wave of the future, licensed software is not.  App store review ensures trust, openness does not.  All tenuous, often ridiculous.  And usually self-serving, which is the way of the gun.

There _is_ a fundamental difference, but it's much simpler.  The incumbent owns the customer relationship, and you do not.  Maybe they host a service, package an application, steward an app store, or do all three, willy-nilly.  But they are close to the money---other people's money---and you are at best close to them, or so it seems.  That makes them irreplaceable, and you---and your work---inevitable commodity, doomed to shrinking margins and eventual usurpation by the first lumbering behemoth with cash-on-hand willing to do what you do as a loss-leader.  Never mind the shortage of talent to do so, with the caliber of output they'd otherwise deign to depend upon.

AWS offers services, through an app store of sorts.  No particular kind of application or device locks customers into that store, but literal and figurative network effects---low latency within AWS datacenters, a few clicks from one indistinguishable service logo to another---encourage one-stop-shopping.  The interface is infamously bad.  Of late, individual services look more and more like 20% approximations of open source solutions, which nonetheless address 80% of need.  They make a lot of money.

Apple sells apps through its App Stores.  Apple computers, including smartphones, are actually or practically constrained to those App Stores for first-tier applications from vendors other than Apple.  Interface design is famously good, but curation is both painful and erratic for developers, and inconsistent for customers.  In-app purchases were banned, until Apple intermediate those, too.  Competition with native Apple apps and widgets remains verboten.  Apple takes its cut.

Red Hat sells subscriptions for software distribution, advice, and support.  Subscriptions come with a certain baseline guarantee of quality and accountability, within the boundaries of their branded distribution.  Overall, the experience meets corporate expectations.  It can be damn hard to compete in support, even for your own work.  Big companies know who Red Hat is, but they don't know you.

Each of these is a great gravity well in the fabric of the commercial universe.  They combine structural binds on customers they have, like network effects, with strong brands, high mental availability, and one-stop-shopping.  Geeks know AWS.  Many of their employers have standing contractual relationships with them.  As a consequence, they pull suppliers of lesser market power mass into their constricting folds.  Under pressure, they combust, which keeps the profit engine turning.

In a far-off universe, License Zero runs this risk, too, for the sake of the one-stop-shop.  Buying one license from a project page is fine, but buying a dozen licenses from all the projects you need at once is better.

The structural constraint is payment processing.  There's no good reason License Zero ought to handle payment card details, and each payment processor has their own way of turning numbers into safe-to-handle tokens.  There's no good reason open software developers ought to settle for Bitcoin or another crypto-coin.  The point is expressing the value of software delivered.  In dollars or other home currency, like everybody else.

All of this is bringing a bunch of disparate details to bear, but I think, in the end, the upshots are fairly straightforward.

First:  The relationship between open software developer and open software user should be established as the sole relationship of concern.  Any downstream vendor-customer relationship is no benchmark against which to mark open developers down.

Second:  As frictionless as commerce should be, any system facilitating vendor-customer relationships between open software developers and others should maximize opportunity for communication.  It should do what it can to facilitate other opportunities, and richer relationships, that the system does not mediate.

License Zero does less on this second point than it could.  I'm in the process of considering a number of optional features, mostly around license-purchase flow, to put developers and customers together in channels that invite communication about the broader context of the license and the project.  As large companies cultivate mental availability and a myriad of "hooks" to make their relationships long-lasting, fruitful, and sticky, so should open software developers.  If a license can turn into a service relationship, or a sponsorship-advertising arrangement, or Hell, even employment, License Zero should build that potential by default.

Of course, many tactics along these lines will have nothing to do with License Zero at all, though many will be quite compatible with it.  To give a concrete example, consider [these issue and pull request snippets for GitHub](<https://github.com/licensezero/transparent-github-templates>), which ask outside contributors directly whether their requests are related to paid work, and whether their employer or client might have resources to fund the work they're asking for.

I look forward to seeing more hacks along these lines in the near future.