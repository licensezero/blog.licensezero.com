---
title: We Can Remember You For It Wholesale
description: maintainer, be gone from my sight
layout: post
---

Part of a series, _Unsustainability at Scale_

Nadia Eghbal's [_Roads and Bridges: The Unseen Labor Behind Our Digital Infrastructure_](https://www.fordfoundation.org/library/reports-and-studies/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/) freed the community to talk about the open source sustainability problem in new, more productive ways, blazing a trail out of the stale metaphors and hackneyed theories that captivated minds for so long.  "Infrastructure" spans policy-speak and engineer-speak, at once enobling open source and intimating its problems.  Problems are hard to solve when you can't see them.

In the past few years, independent efforts around open source licensing, packaging, and compliance coalesced into a complete maintainer-to-user toolchain that helps open source consumers eat their fill without ever so much as glancing the names of developers behind the work.  I contributed to closing that loop, especially in JavaScript, convincing thousands of open source maintainers to disappear themselves from the consciousness of their peers and those that might sustain them.  Practical, automated license compliance remains an obvious win.  But that win accrues only to users, further widening the disparity between users and contributors.

# For Example

Jane creates a JavaScript library for parsing a data format for genetic information.  As part of setting up her project, she uses [the npm command-line interface](https://github.com/npm/npm)'s `init` subcommand to generate a `package.json` file.  In addition to details like package name and version number, the wizard prompts her for a license, offering [The ISC License](https://spdx.org/licenses/ISC) as default.  Jane prefers [the two-clause BSD License](https://spdx.org/licenses/BSD-2-Clause), and tries to enter that instead:

```
$ npm init
...
license: (ISC) BSD
Sorry, license should be  avalid SPDX license expression
(without "LicenseRef"), "UNLICENSED", or "SEE LICENSE IN
<filename>" and license is similar to the valid
expression "BSD-2-Clause"
license: (ISC) BSD-2-Clause
...
```

`npm init` has successfully coaxed Jane into setting her `package.json` file's `license` property to the exact string `"BSD-2-Clause"`.  That string is a valid expression for the two-clause BSD License standardized by [Software Package Data eXchange](https://spdx.org), a project of the [Linux Foundation](https://linuxfoundation.org).  npm incorporates that expression language into its guidelines for [license metadata in `package.json`](https://docs.npmjs.com/files/package.json#license).  The npm command-line interface validates and interprets SPDX license expressions with a [parser](https://www.npmjs.com/packages/spdx-expression-parse) and [correction algorithm](https://www.npmjs.com/packages/spdx-correct) implemented in JavaScript.

Sam uses Jane's library in a front-end web application he writes for work, by installing a format-conversion package that in turn depends on Jane's library.  Sam uses [`licensee`](https://www.npmjs.com/packages/licensee) to automatically recurse the npm dependencies for his software project, checking that each is licensed under an open source license on a list approved by his company.  He uses [browserify-licenses](https://www.npmjs.com/package/browserify-licenses) to generate a long list of license terms and notices from each package bundled for the browser, to meet attribution requirements.

Sam has no reason, incentive, or requirement to see Jane's name.  He will not see her name when he runs `npm install` to download the format-conversion package he needs.  He will not see her name when `licensee` validates the license metadata for her package, along with the data for a pile of other packages.  He will not see her name when compiling a notice file, since that's done by a program Sam runs, without Sam's assistance.

Sam _may_ run into Jane, or at least see her name, if he seeks support for her library, reports a bug, or submits a patch.  Perversely, Sam will be more likely to run into Jane if her software does not work as expected, in circumstances of frustration and disappointment.  Circumstances that may appear, on Jane's end, very needy, demanding, or both.  Perversely, Sam _would_ become aware of Jane's existence if she neglected to code her choice of the two-clause BSD License in a machine-readable way, so that Sam had to manually review her package's `LICENSE` file before including her work in his project.  Perversely, the better Jane is at writing and packaging her software, the more invisible she is to Sam and users like him.

Jane will not see Sam, because users of open source don't report their use of software to its contributors as a matter of course.  Sam won't see Jane, because metadata and tooling suppress Jane's existence as an unnecessary detail.  Until something goes wrong, and goes wrong specifically for Sam.  If Jane has a problem, say inability to make rent and keep landing patches, she's no reliable means of reaching her user base as a whole.

# Whodunnit

I didn't make the decision to use SPDX in `package.json`.  But I noticed it, proposed [a change to npm to validate data](https://github.com/npm/normalize-package-data/pull/61), [proposed a change to `npm init` to encourage compliant metadata](https://github.com/npm/init-package-json/pull/42), [rewrote the documentation](https://github.com/npm/npm/pull/8179), and wrote the initial parser and correction implementations.  Then I proposed a patch to [npmjs.com](https://www.npmjs.com) to show the [Open Source Initiative](https://opensource.org) logo for packages that correctly set metadata for an OSI-approved license.  I sent a few hundred pull requests, asking maintainers to correct the `license` values in their `package.json` files.  I launched a [website](https://npm1k.org)  naming and shaming popular packages that did not comply.  When I needed an avatar for the GitHub org page, I [put the npm wombat on a wanted poster](https://github.com/npm1k).  A hit list.  Not exactly subtle.

I knew and understood that developers, as a culture, appreciate standards, esteem technical correctness, and would respond to a `package.json` specification that determined a "correct" value for their projects.  I knew and understood that developers, as a culture, don't like receiving criticism on `stderr`, and would respond to feedback coaxing them toward valid metadata.  I knew and understood that developers, as a culture, suffer from completionism in cultivating online presence for their work, and would seek the [green doughnut](https://opensource.org/node/442), even if they'd never heard of the Open Source Initiative.  I knew and understood because developer culture is my culture, too.  By taking hold of that leverage, I put myself in the position not just of telling other developers what they should do, but pressuring them, psychologically, into doing it.

Auditing open source licenses for compliance at the time was a terrible chore.  In projects using npm dependencies, depending on literally hundreds of open source packages---libraries and tools you choose to use, plus all the libraries and tools _they_ choose to use, in turn, and so on---made deep wells of open source code to review and approve.  I only saw those wells getting deeper as the npm repository grew and JavaScript gained popularity.  Time bore that prediction out.

In my mind, machine-readable license metadata was all about minimizing time and effort wasted checking licenses.  Instead of seeing that burden grow, year by year, as project dependency graphs grew larger and larger, the community could make it scalable with data.  Computers can read literally hundreds of well structured `package.json` files in the time it takes to `cat` one `LICENSE` file.  With software doing license compliance checking, it wouldn't matter if you used five hundred open source npm packages or five thousand.  Especially if those five thousand packages stuck to five or so standard licenses.

I didn't think about the fact that, years later, I'd meet developers running automated license checks on each push of their npm-based projects, but who've never heard the names of friends of mine, whose code they rely on.  Friends who've resorted to fleeing the Bay Area and begging on Patreon to keep working on open source projects that are clearly the best uses of their time.

# Free as in Forget About It

There is a view of open source licensing, often associated with the modern BSDs, that defines developer freedom not just as maximum permission, but maximum convenience, as well.  That school naturally privileges permissive licenses over copyleft licenses, and short licenses over longer ones.

Its values max out in [public domain dedications](https://creativecommons.org/publicdomain/zero/1.0/) and [abrasive anti-licenses](https://www.wtfpl.net), fall back to the likes of [The Unlicense](https://www.unlicense.org) and [The Free Public License](https://opensource.org/licenses/FPL-1.0.0), and typically settle, in time, for the practicality of the old classics, [The MIT License](https://spdx.org/licenses/MIT), the [two-clause BSD License](https://spdx.org/licenses/BSD-2-Clause), and their [progeny](https://spdx.org/licenses/ISC).  From this point of view, even attribution---reproducing copyright notices and license terms---should be eschewed, if only legal circumstances uniformly permitted.

The licensing-compliance toolchain crosses most of the last mile from legal practicality to maximum convenience and minimum bother.  With the right tooling and the right data, the choice, use, and redistribution of open source software becomes an automated affair of little or no day-to-day burden on the programmer.  With the exception of an occasional veto for lack of metadata, or more exacting license terms, permissive licensing and the compliance toolchain allow programmers to use an ocean of existing software as if they wrote it themselves.

# Doubly-Linked List

Pull down an open source library in your language of choice for, say, hyphenation.  Best case, you can give the library text, and get hyphenated text in return.  You needn't concern yourself with the particular way this was accomplished, or how that method was programmed.  Or who came up with the method.  Or who did the programming.

That's abstraction.  And it's not just the method and implementation that got abstracted.  The people got abstracted, too.  They probably abstracted _themselves_, for your convenience.  With the right standards and tooling in place, it probably worked.

From electrical engineering to architecture, lawyering to entrepreneurship, most kinds of complex building look more and more like composition, not scratch cooking.  Sprawling supply chains afford the myriad, abstracted components, at qualities from artisanal to commodity, prices from dear to dirt-cheap.  Artful curators piece those parts together to tackle ever more demanding challenges.

Abstracting people along those lines needn't shock the conscience.  But we know how it so often does.  Working conditions.  Pay.  Tax relief.  It's impossible to tell, holding a finished, physical product, whether someone involved in the making lived out the consequences of a race to the bottom, under hands that passed down far less than a rightful share of what they received.  The system works well when, and only when, fair compensation goes down as the work comes up, at each stage of production and distribution.

In theory, we expect negotiation to achieve and maintain that calibration.  In practice, well functioning market competition often leads those on higher rungs precisely to where there's no functioning market below, no alternatives, and therefore no real negotiation.  The moral response is corporate social responsibility, sending not just quality controllers to police corner-cutting and substitution, but auditors to uphold labor standards.  Not to mention selective purchasing, as a consumer, and investment, as a financier, in favor of responsible companies.

Open source developers put themselves down toward the bottom of the software supply chain.  Tooling for the top increasingly abstracts people just as effectively as in hard-goods commerce, insofar as consumers don't really want to know.  But we don't pay people for the privilege of abstracting them in open source.  The race to the bottom on price can't go any lower than zero, at least until producers start paying for users as a loss-leader.

On the other hand, it's far easier to concretize open source contributors, reversing the process of abstraction.  Finding out who sewed my sneakers probably involves international travel and a lot of gumshoe research.  But I can usually find out who wrote my hyphenation library with a few shell commands, or at worst a request to an online repository that will tell me, immediately and for free.  A look at the Git repository, plus social media, probably gives me some hint about their work situation.

I need a reason why.  It's not that open source doesn't preserve links connecting users to contributors.  It's that those links are only visible to one side, users, and the only consistent motivations for traversing them are most directly user-serving, and entail more demands on contributor time.

# Backpressure

[License Zero](https://licensezero.com) uses public license terms to create a contributor-serving reason for users to connect with contributors: Depending on the license the maintainer picked, users need paid licenses to use either for commercial purposes or in closed-source work.  License Zero also automates that process, by extending package metadata to include not just data about license terms, but also data about how to pay maintainers.

License Zero links the means of supporting maintainers and the reason to connect with them individually.  We could imagine variations that don't, but they're inherently limited.

License Zero with new licenses, but no extended metadata would create massive licensing hassle for users.  You'd have to dive into `README` or other documentation for each project requiring a paid license.  Each process might be different.  Some licenses might not be available at all.  We see this now with bespoke or non-open source licenses on publicly available code.  And even under open source licenses like [AGPL](https://www.gnu.org/licenses/agpl-3.0.en.html) and [Reciprocal Public License 1.5](http://opensource.org/licenses/RPL-1.5).

License Zero with payment metadata but no new licenses would amount to little more than a recursive tip jar, a way send, say, $5 to every maintainer in your `node_modules` with a single command.  The company facilitating those payments would be a regulated money transmitter, since the payment isn't for goods or services.  Also, I expect the command probably wouldn't get run that often, or for meaningful amounts.

By combining motivation for support and method of support, License Zero sends fair compensation down for work coming up without sacrificing abstraction.  A License Zero checkout page will list the maintainers a user is about to pay for private licenses, and ensure that each gets paid the right amount.  But neither user or maintainer need correspond directly, or even acknowledge one another.  The process itself is standardized and entirely automated.  Users have to decide whether the price of the licenses on offer is something they can pay, but they needn't care whether that price goes to two maintainers or two hundred, whether they're in Cleveland or Copenhagen.

# Paradise (Population: 0)

We can follow this line out further, to a walled garden, a kind of [library of software babel](https://en.wikipedia.org/wiki/The_Library_of_Babel) as a platform or a network.  As a condition of entry, all code gets licensed under maximally permissive terms, on the way in.  Nothing else passes through.  Not metadata.  Not authorship information.   Not versions.  Not project names.  The one, global license requires no attribution, and there's no information with which to do so, anyway.  There are no "owners" of code or projects, no "maintainers" or "core contributors" or committees.  Each users chooses for himself the names they'll apply to available work.  They see for themself how others have developed prior code, its popularity among users as a whole.

Within that walled garden, there's no need for license tooling or standards.  There is only one license to give, and only one license to take.  Neither are there any responsible parties to abuse.  Every user is as privileged as any other to advance the state of any particular work of art.

There is no gratitude, either.  No reputation.  No means of telling who to support, if supporting any particular kind of development is what you want or need.  Only the platform itself, which charges each by their usage, based only its costs.
