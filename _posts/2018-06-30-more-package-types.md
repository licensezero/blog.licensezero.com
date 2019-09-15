---
title: npm, Ruby, Python, Maven, and More
description: first-class support for more package ecosystems
author: K.E. Mitchell
layout: post
---

Version 4.0.0 of the [`licensezero` command](https://github.com/licensezero/cli), out today, supports npm packages, RubyGems, Maven packages, Python packages, and any kind of package that shows up within the directory of depending user's working tree.

The major change is `licensezero.json` files.  Rather than write License Zero metadata into a package system's native manifest file, like `package.json`, `setup.py`, `.gemspec`, or `pom.xml`, the `licensezero` command now writes to its own metadata file, `licensezero.json`.  Wherever a `licensezero.json` file appears within a working directory, `licensezero quote` quotes the projects within it.  When it can, `licensezero quote` reads package-specific metadata files in the same directory for name, scope, and version, and reports those findings in its output.

For some dependencies, like RubyGems, creating a full inventory of dependencies means looking _outside_ the working directory, to packages installed at the user or system level.  `licensezero quote` achieves that by querying [Bundler](https://bundler.io/) for Ruby projects.  For other languages and packaging approaches, like [Go](https://golang.org), `licensezero` [needs more code](https://github.com/licensezero/cli/issues/10), to determine where to look for `licensezero.json` files.

If you're interested in bringing first-class support to your ecosystem, [share what you know about how to find dependencies in your community](https://github.com/licensezero/cli/issues/new).  Even if you can't contribute Go code to the `licensezero` command, guidance on what conventions matter, and how to support them, will be an enormous help.  Writing the code isn't the hard part.  Knowing what that code should do is.

In the end, nothing about License Zero's approach to licensing limits it to a specific programming language or packaging standard.  Wherever License Zero _can_ go to support independent developers, it will go.
