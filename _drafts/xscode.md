---
title: Two (And More) Can Play at this Game
description: welcoming xs:code, a new open source dual licensing platform
---

A number of folks reached out to me at the end of last year about [xs:code](https://xscode.com/), a new startup that recently [tagged TechCrunch](https://techcrunch.com/2019/12/10/xscode-launches-subscription-platform-to-monetize-open-source-projects/) following its half-million-dollar seed round.

I could not be more excited to see another company trying to make dual licensing workable for small-scale open source developers.

It's early days, and every new company is subject to change.  The actual functionality xs:code automates appears to be recurring subscription payments for access to private GitHub repositories, along the lines of [gitstore](https://gitstore.app).  But from what I've been able to find poking through their website, xs:code aims to support a few different business models, include "dual licensing", which they list first.  The idea is to have one public GitHub repository for whatever's free, and another private repository, probably containing much of the same code, for everything that pays.

## One or Many

At the end of last year, I made a crucial decision for License Zero: [I'm actively rearchitecting the software tools to support selling private licenses through self-hosted checkout portals and other licensing agents](https://blog.licensezero.com/2019/11/30/License-Zero-2.0.html), not just through licensezero.com.  It's coming along nicely.

But why?  Wouldn't developers---and License Zero itself---benefit from building network effects in a single, standard system?  They would.  And wouldn't a single checkout experience for all dependencies of a project, through a single licensing agent with a single payment integration, make buying easier for customers?  It would.

There are some minor implementation problems, like lack of one-to-many payment processing availability in countries outside [Stripe's limited range](https://stripe.com/global).  But the major problems are autonomy and its converse, network effects.  What guarantees do developers have that License Zero won't become another GitHub?

One approach is to double down on establishing a single go-to service, network, or platform, but also structure that almighty singleton in a pliable, accountable, democratic way.  The spirit animal of that solution is [Stocksy United](https://www.stocksy.com), an agency for stock-photo and B-roll artists.  Much like License Zero, Stocksy provides standard license terms, a checkout flow, payment infrastructure, and a platform for licensing deals and takes a commission.  But unlike License Zero, Stocksy is a cooperative owned at least in part by the creators it represents, a so-called "platform coop".

The other approach is the model we see dominate the United States market in other creative fields like music, film, speaking, and so on: a broad and diverse pool of agents, labels, and other facilitators that cater to and compete for talent.  Where a member of a platform coop like Stocksy might vote or lobby to change the way their representation works through its ownership-governance structure, a creator with a broader pool of possible agents might simply their current relationship for another, or use their power to do so as leverage to renegotiate.

License Zero has leaned toward the lighter-weight approach from the get-go.  The legal terms for selling through License Zero don't require developers to sell only through License Zero.  In the jargon, License Zero is developers' _nonexclusive_ agent, not their _exclusive_ agent.  Unless developers choose to [guarantee availability through License Zero for a set period of time](https://guide.licensezero.com/#locks), they can also stop selling through License Zero at any time.  They can go elsewhere, or handle selling on their own.

But the ability to switch isn't meaningful without options.  Part of the solution to that problem is technical.  Next on my list after reachitecting is an open implementation of a licensing server for licenses from a single developer taking payment through PayPal, so that devs outside Stripe's range can host for themselves.  But part of the solution is cultivating more facilitators, like License Zero, that can do the job for those who prefer to outsource.

## Pointers

Along those lines, I'd like to provide xs:code a few thoughts.  Obviously, the company will need to make its own decisions, try and fail in its own way, and rely on its own legal counsel for legal advice.  But I'm deep in this game, and want to offer what I can.

### Dual Licensing

I suspect xs:code may have fallen victim to the old confusion about "dual licensing".  That phrase is used a number of different ways in free/open jargon.  As usual, overloading is trouble.

One meaning of "dual licensing" denotes a project available under a choice of open licenses.  For example, the Rust compiler is available under Apache 2.0 _or_ MIT, so that people worried about GPLv2 compatibility can "pick" MIT, and everyone else gets the benefits of Apache 2.0's more modern legal terms.

But "dual licensing" as a business model means something quite different.  It's not a choice of two open licenses, but a choice between an open license---usually a copyleft license---and a more traditional, proprietary license that applies only to the person or company paying the license fee.

Avoiding this confusion is one of the reasons I strongly prefer to call the business model ["public-private licensing"](https://indieopensource.com/public-private/indies).  The open license is the "public license".  It applies to everyone.  The paid license is the "private license".  It applies only to the one who pays.

Putting GPLv3 in a public repository and MIT in a paid, private repository with the same code mixes up the two meanings of "dual licensing".  The effect is likely that anyone who pays for access to the private repository gets the code under the MIT license.  The MIT license allows them to share the code with anyone else, or even publish it online---say, in their own public fork of the private repo---under the MIT license.  So the first customer who pays for access to your private repo could be your last.  Under MIT, they're fully within their rights to "release" your code without any obligation on anyone else to pay your price.

Some folks do advocate giving paying customers a permissive license along these lines.  But when I've spoken to them, I usually found one of two patterns.  Some count on a debatable reading of GPL to limit the broader permission to the one paying.  That's both tenuous for those who dig into the details, and unclear to everyone else.  Others aren't actually trying to make their work available under different sets of rules at all, but selling convenient and timely access to the latest and greatest code.  It's the Ghostscript model: selling printer manufacturers the latest and greatest version of their postscript processor, to include in thousands and thousands of units, but allowing that code to seep out to the community in time.

If xs:code would like to feed back and help improve the indieopensource.com guide to public-private licensing, I'd love to share leadership and responsibility for that resource with them.  [The org's on GitHub.](https://github.com/indieopensource)  I started it precisely to facilitate shared development of explanatory, business, and legal resources for independent developers trying to make money in open software.

### GPL

xs:code's documentation on the GPL gets it wrong.  But it's not their fault, and they're not the first to succumb to the oversimplification.

From [their dual licensing guide](https://xscodehelp.zendesk.com/hc/en-us/articles/360003926117-Dual-licensing-guide):

> However, most copyleft licenses, such as the GPL license---require the the user modifying the code, _will release the modified version as open source as well._  Often called a "viral" license, if you use GPL in your project, it "infects" any derivative code created using it, requiring your to release ALL derivative work with a GPL license to the public.

That's exactly what many hackers _think_ GPL says.  But that is not what GPLv2, GPLv3, or AGPLv3 actually say.

The GPLs are complex, strangely worded licenses.  If you have a specific question about GPL for a project that matters, you really need to do Q&A with an expert who can think through the exceptions and edge cases.  But in general, as an example:  If you license an image manipulation library under GPL and I patch the library and use it in the server software for a website, GPL doesn't require me to share my patch or my server code, even if a million people visit the site.  So long as I haven't shared a _copy_ of the library or my server code with anyone, GPL's requirements to share and license source code never kick in.  Even if all that work is a legal "derivative work" of your library.

This is just the best known loophole of the GPLs, the so-called "ASP loophole" or "network loophole".  There are other gaps in the GPLs' rules requiring sharing back.  For example, I can freely share copies of my patch and server code within my organization, even if it's a huge, and potentially also with contractors and service providers, without sharing alike.  They count as "private changes".  And even under AGPL, which aimed to close the network loophole, there are several ways to use code in network services without sharing back.  License changes from MongoDB and other database companies have brought those issues to the fore in the last year or so.

Reading GPL to mean "if you build with it, you must share alike" is tempting for developers who want to sell permission to build closed projects.  A lot of developers want that license.  But it isn't GPL.  It's [Parity](https://paritylicense.com), a license I wrote for License Zero and refined with the help of lots of License Zero developers, to fill the gap.  For software that isn't used to build other software, [Prosperity](https://prosperitylicense.com), a noncommercial license, fills a similar role.

If xs:code sees the need for licenses like Parity and Prosperity in supporting good business models for developers, I'd be ecstatic to have their feedback and support.  They were "License Zero Reciprocal" and "License Zero Noncommercial" to start.  I renamed them some time ago primarily to establish a neutral distance from License Zero itself.  Early on, that was most useful to developers and companies who wanted to use the licenses _without_ selling any right to use in closed projects.  But I hope it's just as welcoming to other facilitators, service providers, and licensing agents, including xs:code.

### Contributions

xs:code's [short guide to contributions to dual-licensed projects](https://xscodehelp.zendesk.com/hc/en-us/articles/360003926117-Dual-licensing-guide#h_d67888e7-6889-4b78-bbda-4bbd4fc86c49), gets the general outline right, but many important details confusingly wrong.  Compare the [guide I drafted on the same subject for indieopensource.com](https://indieopensource.com/public-private/contributors).

There is no requirement that contributors _assign_ their copyrights to the developer selling private licenses.  In the vast majority of cases, they can simply _license_ them, without transferring ownership, under terms that facilitate the business model.  Licensing developers rarely gain much of anything practical from taking assignments, rather than licenses.  Insisting on assignment often scares away developers who've developed an instinct to "keep their copyrights".  The laws of many countries, including the United States, also impose special signature or other procedures, called "formalities", to copyright assignments.

The form xs:code links to as a "contributor license agreement" is actually a copyright _assignment_ ambiguously titled "contributor agreement".  I'd strongly advise reading up a bit on how assignments differ from licenses, and glancing a few examples online.  Apache publishes contributor and individual contributor license agreements.  Several companies, including FANG, use house forms enforced by bots.

### Organizations

One detail that I went looking for, but couldn't find, concerns how xs:code handles organizations, clients, and other one-to-many developer affiliations.  If I work at Something, Inc. and pay for access to a private repo, does everyone at Something get access?  If I'm a contractor, can I share with my clients?

License Zero very explicit requires individual developers, not organizations, to buy licenses.  Those licenses apply to the developers who paid, not their teams or companies.  Very early on, License Zero supported buying "site licenses" that covered some or any number of employees and contractors of a company.  If the company paid, its developers were covered under the company's license.

License Zero focuses on licensing.  But this will be important for other benefits of private-repo access, as well.  Does each company or team pay for a single developer to have access to a private repo through xs:code, and then serve as liaison for their working group in private-repo issues and pull requests?  What happens if they leave the company, or take a new position?  If there's special documentation in the private repo that isn't available in the public repo, can the paying customer with access share all that doc with coworkers?  With contracting clients?

## Plaudits

To finish out, I'd like to offer xs:code a few nods, too.

As far as I can tell, xs:code doesn't support one-off payments, only subscriptions.  Recurring revenue is probably the most common business-side request for License Zero.  I'm still not convinced subscriptions are the right way to go for dual licensing in particular, both because they're hard to administer and because they tend to favor sellers over buyers.  But xs:code has bit the bullet and decided to embrace that complexity on behalf of developers, which is admirable.  Insofar as xs:code also supports "open core" proprietary add-ons and services like support or hosting, subscription billing makes a lot of sense.

I also see that xs:code sets a five dollar per month fee minimum for the cost of access to private repos.  That's great.  Most people with business experience see open developers dipping toes into business constantly underpricing themselves.  Five dollars is probably still too low, but any minimum at all sends the right kind of message.  Even if the motivation was really clearing processing fees or focusing attention on higher-value opportunities.

Finally, while I'm not privy to any details of the $500,000 seed round for xs:code that TechCrunch mentioned, I wouldn't be surprised to learn the investment took the form of a SAFE or "Series Seed" common stock purchase.  In other words, I hope and suspect that xs:code retained its independence, without sacrificing a board seat, managerial control, or any future right to take over, for the money.

Whether discussing License Zero specifically or some other "sustainability as a service" company, venture funding and the startup model have been a constant topic of concern.  I gather I'm both more ambivalent about venture financing and more concerned about fast-growth mentality than most devs I aim to serve.  I'd strongly encourage xs:code to make that a topic in its own conversations, and to choose its growth and development paths consciously.

Good luck, and God help us all!