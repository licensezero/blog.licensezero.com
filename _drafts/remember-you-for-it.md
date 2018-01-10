---
title: We Can Remember You For It Wholesale
description: maintainers, gone from my sight
layout: post
---

Part of a series, _Unsustainability at Scale_

Nadia Eghbal's [_Roads and Bridges: The Unseen Labor Behind Our Digital Infrastructure_](https://www.fordfoundation.org/library/reports-and-studies/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/) blazed a trail out of the stale metaphors and hackneyed theories that captivated minds for so long, freeing us to talk about open source's discontents in new ways.  Nadia's principal metaphor, "infrastructure", adroitly spans policy-speak and engineer-speak, at once enobling open source and intimating its problems.  Problems are hard to get solved when nobody sees them.

It isn't just that consumers and policy makers don't see the problems within software.  More and more, software can't see the problems within itself.

In the past few years, independent efforts around open source licensing, packaging, and compliance coalesced into a complete maintainer-to-user toolchain that lets consumers eat their fill of open source without ever so much as glancing the names of developers behind the work.  I contributed to closing that circle, especially in JavaScript, convincing thousands of open source maintainers to disappear themselves from the consciousness of their peers, their users, and others who might help sustain them.  Practical, automated license compliance remains an obvious win.  But that win accrues only to users, further widening consumer-producer disparity.

That realization, and a new ability to talk about it, led directly to License Zero.

# For Example

Jane creates a JavaScript library for parsing a data format for genetic information.  As part of setting up her project, she uses [the npm command-line interface](https://github.com/npm/npm)'s `init` subcommand to generate a `package.json` file.  In addition to details like package name and version number, the wizard prompts her for license metadata, offering [The ISC License](https://spdx.org/licenses/ISC) as default.  Jane prefers [the two-clause BSD License](https://spdx.org/licenses/BSD-2-Clause), and tries to enter that instead:

```
$ npm init
...
license: (ISC) BSD
Sorry, license should be a valid SPDX license expression
(without "LicenseRef"), "UNLICENSED", or "SEE LICENSE IN
<filename>" and license is similar to the valid
expression "BSD-2-Clause"
license: (ISC) BSD-2-Clause
...
```

`npm init` has successfully coaxed Jane into setting her `package.json` file's `license` property to the exact string `"BSD-2-Clause"`.  That string is a valid expression for the two-clause BSD License standardized by [Software Package Data eXchange](https://spdx.org), a project of the [Linux Foundation](https://linuxfoundation.org).  npm incorporates that expression language into its guidelines for [license metadata in `package.json`](https://docs.npmjs.com/files/package.json#license).  The npm command-line interface validates and interprets SPDX license expressions with a [parser](https://www.npmjs.com/packages/spdx-expression-parse) and [correction algorithm](https://www.npmjs.com/packages/spdx-correct).

Sam uses Jane's library in a front-end web application he writes for work, by installing a format-conversion package that in turn depends on Jane's library.  Sam uses [`licensee`](https://www.npmjs.com/packages/licensee) to automatically recurse the npm dependencies for his software project, checking that each is licensed under an open source license on a list from his legal department.  He uses [browserify-licenses](https://www.npmjs.com/package/browserify-licenses) to generate a long list of license terms and notices from each package bundled for the browser, to meet attribution requirements.

Sam has no reason, incentive, or requirement to see Jane's name.  He will not see her name when he runs `npm install` to download the format-conversion package he needs.  He will not see her name when `licensee` validates the license metadata for her package, along with the data for a pile of other packages.  He will not see her name when compiling a notice file, since that's done by a program Sam runs, without Sam's assistance.

Sam may run into Jane, or at least see her name, if he seeks support for her library, reports a bug, or submits a patch.  Perversely, Sam will be more likely to run into Jane if her software does not work as expected, in circumstances of frustration and disappointment.  Perversely, Sam _would_ become aware of Jane's existence if she neglected to code her choice of the two-clause BSD License in a machine-readable way, so that Sam had to manually review her package's `LICENSE` file before including her work in his project.  The better Jane is at writing and packaging her software, the more invisible she is to Sam and users like him.

Jane will not see Sam, because users of open source don't report their use of software to its contributors as a matter of course.  If Jane has a problem, say inability to make rent, she's no reliable means of reaching her user base as a whole.  She's only aware of those who've come back to her for one reason or another, and often only aware of the individuals who did so, [not the broader interests they represented](https://blog.licensezero.com/2017/10/16/mercenary-rapport.html).

# Whodunnit

I didn't make the decision to use SPDX in `package.json`.  But I noticed it, proposed [a change to npm to validate data](https://github.com/npm/normalize-package-data/pull/61), [proposed a change to `npm init` to encourage compliance](https://github.com/npm/init-package-json/pull/42), [rewrote the documentation](https://github.com/npm/npm/pull/8179), and contributed the initial parser and correction implementations.  Then I proposed a patch to [npmjs.com](https://www.npmjs.com) to show the [Open Source Initiative](https://opensource.org) logo for packages that correctly set metadata for an OSI-approved license.  I sent a few hundred pull requests, asking maintainers to correct the `license` values in their `package.json` files.  I launched a [website](https://npm1k.org)  naming and shaming popular packages that did not comply.  When I needed an avatar for the GitHub org page, I [put the npm wombat on a wanted poster](https://github.com/npm1k).  Not exactly subtle.

I knew and understood that developers, as a culture, appreciate standards, esteem technical correctness, and would respond to a specification that determined a "correct" value for their projects.  I knew and understood that developers, as a culture, don't like receiving criticism on `stderr`, and would respond to feedback coaxing them toward valid metadata.  I knew and understood that developers, as a culture, suffer from completionism in cultivating online presence for their work, and would seek the [green doughnut](https://opensource.org/node/442), even if they'd never heard of OSI.  I knew and understood because developer culture is my culture, too.  By taking hold of those levers, I put myself in the position not just of educating fellow developers about what they should do, but pressuring them, psychologically, into doing it.

Auditing open source licenses for compliance at the time was a terrible chore.  In projects using npm dependencies, depending on literally hundreds of open source packages---libraries and tools you choose to use, plus all the libraries and tools they choose to use, in turn, and so on---made deep wells of open source code to plumb and approve.  I only saw those wells getting deeper as the npm repository grew and JavaScript gained popularity, especially among enterprise users.

I didn't see that, years later, I'd meet developers running automated license checks on each push to their npm-based projects who've never heard the names of friends of mine, whose code they rely upon in fundamental ways.  Friends who've resorted to fleeing Bay Area cost of living and begging on Patreon to keep up work that's clearly the best use of their time.

# Free as in Forget About It

There is a view of open source licensing, often associated with the modern BSDs, that defines developer freedom not just as maximum permission, but maximum convenience, as well.  That school naturally privileges permissive licenses like MIT over copyleft licenses like GPL, and short licenses like ISC over longer ones like Apache.

Its values max out in [public domain dedications](https://creativecommons.org/publicdomain/zero/1.0/) and [abrasive anti-licenses](https://www.wtfpl.net), fall back to the likes of [The Unlicense](https://www.unlicense.org) and [The Free Public License](https://opensource.org/licenses/FPL-1.0.0), and typically settle, in time, for the old classics, [The MIT License](https://spdx.org/licenses/MIT) and [two-clause BSD License](https://spdx.org/licenses/BSD-2-Clause).  From this point of view, even attribution---reproducing copyright notices and license terms---should be eschewed, if only legal rules uniformly permitted.

The licensing-compliance toolchain crosses most of the last mile from legal practicality to zero hassle.  It makes up the difference between what licenses can do under the law, and the ideal of giving not one thought to licensing.  With the right tooling and the right data, the choice, use, and redistribution of open source software becomes an automated affair of little or no day-to-day burden on the programmer.  With the exception of an occasional veto for lack of metadata, pervasive permissive licensing and the compliance toolchain allow programmers to use a wealth of existing software as if they wrote it themselves.

# Singly-Linked

Pull down an open source library in your language of choice for, say, hyphenation.  Best case, you can give the library text, and get hyphenated text in return.  You needn't concern yourself with the particular way this was accomplished, or how that method was programmed.  Or who came up with the method.  Or who did the programming.

That's abstraction.  Not just of method and implementation, but of people.  The people probably abstracted _themselves_, for your convenience.  With the right standards and tooling in place, it probably worked.

From electrical engineering to architecture, lawyering to entrepreneurship, most kinds of complex building look more and more like assembly, not scratch cooking.  Sprawling supply chains afford the myriad, abstracted components, at qualities from artisanal to commodity, prices from dear to dirt-cheap.  Capable curators recombine those pieces to meet ever more challenging demands.

Abstracting people along those lines needn't shock the conscience.  But we know how it so often does.  Working conditions.  Compensation.  Community concessions.  It's impossible to tell, holding a finished, physical product, whether someone involved in its making lived out the consequences of a race to the bottom, under hands that passed down far less than a rightful share of what they received.  The system works well when, and only when, fair compensation goes down as the work comes up, at each stage of production and distribution.

In theory, we expect negotiation to achieve and maintain that calibration.  In practice, well functioning market competition often leads those on higher rungs precisely to where there's no functioning market below, no alternatives, and therefore no bargain.  The moral response is corporate social responsibility, sending not just quality controllers to police corner-cutting and substitution, but auditors to uphold labor standards and safety codes, all the way down the supply chain.  Not to mention selective purchasing, as a consumer, and selective investment, as a financier, in favor of responsible companies.

Open source developers of piece-parts put themselves at the bottom of the software supply chain.  Tooling for the top increasingly abstracts people just as effectively as in hard-goods commerce.  But we don't pay anything for the privilege of abstracting people in open source.  The race is on to higher and salaries for top-level talent, to hear business needs and translate them into assemblies of closed and open code.  The race to the bottom on piece price can't go any lower than zero, at least until producers start paying for users as a loss-leader.

On the other hand, it's far easier to concretize open source contributors, reversing the process of abstraction, when we choose to.  Finding out who sewed my sneakers probably entails international travel and a lot of gumshoe research.  But I can usually find out who wrote my hyphenation library with a few shell commands, or at worst a request to an online repository.  Git and social media probably give a pretty good idea of their working situations.

It's not that open source breaks links connecting users to contributors.   It's that those links are only visible up the chain, to users, and that the only consistent motivations for traversing them are directly user-serving.

# Recursive Descent

[License Zero](https://licensezero.com) uses public license terms to create a contributor-serving reason for users to connect with contributors.  Depending on the license the maintainer picked, users need paid licenses to use either for commercial purposes or in closed-source work.  License Zero also automates that process, by extending package metadata to include not just data about license terms, but also data about how to pay maintainers.

Why does License Zero link means of financially supporting maintainers and motivation to do so?  Shouldn't we prefer to separate those concerns?  Indeed, we could imagine variations that do just one or the other.  But they're inherently flawed.

License Zero with new licenses, but no extended metadata, would create massive licensing hassle for proprietary users.  As a proprietary user, you'd have to dive into `README` or other documentation for each project for which you need a paid license.  Each purchasing process might be different, and some licenses might not be available at all.  We see this now with bespoke and non-open source licenses, and under open source licenses like [AGPL 3.0](https://www.gnu.org/licenses/agpl-3.0.en.html) and [Reciprocal Public License 1.5](http://opensource.org/licenses/RPL-1.5).

License Zero with payment metadata, but no new license terms, would amount to little more than a tip pool, a way to send, say, $5 to maintainers for every package in your `node_modules` with a single command.  The company facilitating those payments would be a regulated money transmitter, since the payment isn't for goods or services.  And I don't expect the command would get run that often, or for meaningful amounts, in aggregate.  Rather, I'd expect highly visible celebration of the exceptional, generous few, contributing to a misleading overall picture.

By combining motivation for support and method of support, License Zero sends fair compensation down for work coming up, without sacrificing abstraction.  A License Zero checkout page lists the maintainers a user is about to pay for private licenses, and ensures that each gets paid the right amount.  But user and maintainer needn't correspond directly, or even acknowledge one another.  The support process is standardized and entirely automated.  Maintainers have to decide what to charge.  Users have to decide whether to pay it.  It's a single-variable negotiation about support for those abstracted.  That's all.

# Paradise Without People

License Zero is both an extension of prior work and a departure.  There are other directions to take, with different trade-offs.  But I like less where they seem to lead.

In my mind, the natural extension of the antilicense philosophy, absent highly improbable, worldwide legal reform, coalesces as a walled garden, a kind of private [library of software babel](https://en.wikipedia.org/wiki/The_Library_of_Babel) as platform or network, implementing a voluntary, quasi-public domain for its members.  As a condition of entry, all code submitted gets licensed under maximally permissive terms, waiving all exclusive rights.  Only code comes in.  Not metadata.  Not version tags.  Not project names.  Not a single byte about authorship.  Just code and comment, anonymous by default.

The global license requires nothing, not even attribution.  There's no information with which to attribute anyone, anyway.  Or to hold them liable.  There are no owners of code or projects, no maintainers, core contributors, or committees.  Each user chooses for themself the names they'll apply to available work.  Each sees for themself how others have developed prior code, and the popularity of different lines of development, among the community as a whole.

Within this intentional community, this intellectual property demilitarized zone, there's no need for license tooling or standards.  There is only one license to give, given by all, and only one license to accept, accepted by all.  Neither are there any permissions or structural preferences to wield or request.  Every user is as privileged as any other to advance the state of any particular work of art.  Only interest binds them to any project.  When they tire, grow bored, have children, or move on, they simply leave the work where it fell, for others to pick up, if so inclined.  No structures, gamifications, or social incentives induce guilt.

This is not the ideal of the academy.  Far from it.  There is no reputation, no prestige.  No means of determining who to blame, esteem, or support for any particular work.  No human heuristics for quality, no trust.  Only the platform itself, a heap of code for the taking.  A commons, but not a community.

If each participant came to open source as emissary of some other fully fledged community---a company, a university, a nonprofit, a government---that provided all the belonging, esteem, sustenance, and inspiration they needed, there'd be little reason to preserve open source as a community unto itself.  From time to time, I hear advice reflecting this potential.  It's said those without a lucrative work situation shouldn't be churning out open source code.  I see increasing truth in that, but don't welcome it.

As it stands, many of us do practice open source relations for companies and other concerns.  But on a personal level, we often identify more strongly with open source, as source of identity, than with the interests we represent, as sources of pay.  The opportunity, and resulting independence, that open source software gives us breeds a loyalty, and a taste for individual agency.  It socializes us in its own peculiar way, for better and worse, and gives us a history.  Some of us "go native" in open source, but more and more of us are born there.  For companies and clients, we're local fixers, not diplomats on foreign assignment.

I've tried to structure License Zero specifically to support, and encourage, independent open source careers, independent open source products and services.  That's the best evolution of open source in my mind, not as a lauded adjunct to proprietary, closed-source development, but as an increasingly viable alternative organizing principle, for people and for code.

If abstracting oneself away is part of software craft, or part of useful work in general, let the value of that selflessness, that structural humility, be acknowledged and rewarded.  Code can be granted, and taken for granted.  But people ought not to be.  A community based on martyrdom never lasts long.
