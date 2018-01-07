---
title: We Can Remember You For It Wholesale
description: maintainer, be gone from my sight
layout: post
---

Part of a series, _Unsustainability at Scale_

Nadia Eghbal's [Roads and Bridges: The Unseen Labor Behind Our Digital Infrastructure](https://www.fordfoundation.org/library/reports-and-studies/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/) called new attention to the open source sustainability problem, usurping the dominant, stale vocabulary of images and theory used to talk about it.  As always, Nadia chose her words, including her title, very capably.  "Infrastructure" is a noble and pleasingly utilitarian way to see open source software and its policy problems.  Policy problems are hard to solve when you can't see them.

In the past few years, independent efforts around open source licensing, packaging, and compliance coalesced into a complete maintainer-to-user toolchain that lets open source consumers eat their fill without ever so much as glancing the names of the developers behind the work, or even the work, for that matter.  I've contributed a small bit to that system, convincing thousands of open source maintainers to disappear themselves from the consciousness of their programming peers.

In that way, I have been a very helpful part of the problem.

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

Sam uses Jane's library in a front-end web application he writes for a client, by installing a format-conversion package that in turn depends on Jane's library.  Sam uses [`licensee`](https://www.npmjs.com/packages/licensee) to automatically recurse the npm dependencies for his software project, checking that each is licensed under an open source on a list approved by his client.  He uses [browserify-licenses](https://www.npmjs.com/package/browserify-licenses) to generate a long list of license terms and notices from each package bundled for the browser, to meet attribution requirements.

Sam has no reason, incentive, or requirement to see Jane's name.  He will not see her name when he runs `npm install` to download the format-conversion package he needs.  He will not see her name when `licensee` validates the license metadata for her package, along with the data for a pile of other packages.  He will not see her name when compiling the license terms and notice files, since that's done by a program Sam runs, and not by Sam.

Sam _may_ run into Jane, or at least see her name, if he seeks support for her library, reports a bug, or submits a patch.  Perversely, Sam will be more likely to run into Jane if her software does not work correctly, in circumstances of frustration and disappointment that may appear, on Jane's end, like entitlement.  Perversely, Sam _would_ become aware of Jane's existence if she neglected to code her choice of the two-clause BSD License in a machine-readable way, so that Sam had to manually review her package's `LICENSE` file before including her work in his project.  Perversely, the better Jane is at writing and packaging her software, the more invisible she is to Sam and users like him.

Jane will not see Sam, because users of open source, as a general rule, aren't reported back to contributors.  Sam won't see Jane, because metadata and tooling suppress Jane's existence as an unnecessary detail.  Except if something goes wrong.  Specifically, if something goes wrong for Sam.

# Whodunnit

I didn't make the decision to use SPDX in `package.json`.  But I noticed it, proposed [a change to npm to validate data](https://github.com/npm/normalize-package-data/pull/61), [proposed a change to `npm init` to encourage compliant metadata](https://github.com/npm/init-package-json/pull/42), [rewrote the documentation](https://github.com/npm/npm/pull/8179), and wrote the initial parser and correction implementations.  Then I proposed a patch to [npmjs.com](https://www.npmjs.com) to show the green-doughnut [Open Source Initiative](https://opensource.org) logo for packages that correctly set metadata for an OSI-approved license.  I sent a few hundred pull requests, asking maintainers to correct the `license` values in their `package.json` files.  I launched a [website](https://npm1k.org)  naming and shaming popular packages that did not comply.  When I needed an avatar for the GitHub org page, I [put the npm wombat on a wanted poster](https://github.com/npm1k).

I knew and understood that developers, as a culture, appreciate standards, like technical correctness, and would respond to a `package.json` specification that determined the "correct" value for their projects.  I knew and understood that developers, as a culture, don't like receiving criticism on `stderr`, and would respond to feedback coaxing them toward valid metadata.  I knew and understood that developers, as a culture, suffer from completionism in cultivating online presence for their work, and would seek the green doughnut, even if they'd never heard of the Open Source Initiative.  I knew and understood because developer culture is my culture, too.  By taking hold of that leverage, I put myself in the position of telling other developers what they should do, and pressuring them, psychologically, into doing it.

Auditing open source licenses for compliance at the time was a terrible chore.  In projects using npm dependencies, depending on literally hundreds of open source packages---libraries and tools you choose to use, plus all the libraries and tools _they_ choose to use, in turn, and so on---made deep wells of open source code to be reviewed and approved.  I only saw those wells getting deeper as the npm repository grew and JavaScript gained popularity.  Experience bore those predictions out.

In my mind, machine-readable license metadata was all about insuring minimum wasted time and effort spent checking licenses.  Instead of seeing that burden grow, year by year, as projects grew larger and larger, the community could tackle it with software.  Programs can read literally hundreds of `package.json` files in the blink of an eye.  With software doing license compliance checking, it wouldn't matter if you used five hundred open source npm packages or five thousand.  Especially if those five thousand packages stuck to five or so standardized open source licenses.

I didn't think about the fact that, years later, I'd meet developers running automated license checks on each push of their npm-based projects, sure, but who've never heard the names of friends of mine, whose code they rely on.  Friends who've resorted to fleeing the Bay Area and beginning on Patreon to keep working.

# Free as in Convenient

There is a view of open source licensing, often associated with the modern BSD Unix distributions, that defines developer freedom not just as maximum permission, but maximum convenience, as well.  That school naturally privileges permissive licenses over copyleft licenses, and short licenses over longer ones.  It maxes out with [public domain dedications](https://creativecommons.org/publicdomain/zero/1.0/) and [abrasive anti-licenses](https://www.wtfpl.net), then compromises to the likes of [The Unlicense](https://www.unlicense.org) and [The Free Public License](https://opensource.org/licenses/FPL-1.0.0), and retreats finally to the practicality of the old classics, [The MIT License](https://spdx.org/licenses/MIT), the [two-clause BSD License](https://spdx.org/licenses/BSD-2-Clause), and their [progeny](https://spdx.org/licenses/ISC).  From this point of view, even attribution---reproducing copyright notices and license terms with copies---should be eschewed, if only legal circumstances uniformly permitted.

The licensing-compliance toolchain crosses most of the last mile from legal practicality to maximum convenience and minimum bother.  With the right tooling and the right data, the choice, use, and redistribution of open source software becomes an automated affair of little or no day-to-day burden on the programmer.  With the exception of an occasional veto for lack of metadata or more exacting license terms, permissive license and the compliance toolchain allow programmers to use an ocean of existing software as if they wrote it
