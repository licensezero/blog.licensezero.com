---
title: Fulcrums
description: what leverage do indie devs have to gain support?
layout: post
---

If you're a developer unhappy with the open source status quo, you need leverage to improve it.  You need leverage just to start the conversation about improving it.

Right now, open source consumers have it good.  It's not in their immediately apparent, short-term interest to entertain change, other than change that asks more of open source producers.  Without leverage, or willingness to use it, conversations about "sustainability" start out acknowledging that specific open source developers can't keep doing what they already do with so little support, but end with [lists of more things independent open source developers ought to do](https://medium.com/libraries-io/what-does-a-sustainable-open-source-project-look-like-bf9b8cf824f8).  Security.  Documentation.  Release notes.  Making yourself fungible.

Open source consumers have headcount, well-understood organizational structures, money, and clout.  What do open source developers have that they can sell or wield, to escape the downward spiral toward burnout and replacement?

In three words: [Convenience](#convenience), [Power](#power), and [Freedom](#freedom).

# Convenience

Platforms used to make and distribute open source software give developers power to take action online in centralized, discoverable places that are easiest for consumers to find and use.  By taking on those burdens, and leveraging the network effects around names, open source developers make a lot of convenience for consumers.

## Collaboration Platform Permissions

As an open source developer, Open source developers have accounts on revision control, bug tracking, and patch submission systems.  Their accounts have permissions that allow them to do what consumers of their software cannot, and to decide what consumers can do in the relevant parts of those platforms.

Consumers can fork projects and exercise these permissions for their forks.  But there are significant network-effect detriments to any fork, even a fork whose sole purpose is floating a patch.  It's just more convenient to go to one place for code, questions, development, history, builds, and so on.

Developers can leverage this potential for convenience into support by prioritizing support requests and patches from those who support them, or replacing open channels for support with paid, private channels.

License Zero leaves entirely open how indie open source developers handle the actual process of development.  Developers are free to combine License Zero's approach with leveraging development platform permissions.

## Distribution System Permissions

Open source developers have powerful accounts on artifact distribution systems like [npm](https://www.npmjs.com).  Those accounts have permissions to publish new versions under well known names that are easy to consume with package managers and other prebuilt tools and services.

Consumers can also sign up for distribution-system accounts and publish copies of open source work.  But for discoverability and search purposes, it's far more convenient to have a single name that always points to the latest and greatest.

Developers can leverage this potential for convenience into support by selling binaries and other build products.  The work they publish as open source may even include all configuration necessary to make those builds.  But many consumers will find it more convenient to pay a price than reproduce a build environment and invoke a build chain.

Apart from requiring developers to distribute their work with particular metadata, License Zero leaves entirely open how indie open source developers handle distribution of their work.  Developers are free to combine License Zero's approach with distribution-based support approaches.

# Power

Community rules and dynamics afford open source maintainers will significant power, which they can use to compel support.

## Intellectual Property Law

Intellectual property laws give independent developers enforceable rights over the use of their code and distinctive names, like project names.  When others use that code, or those names, without permission, the developer can potentially sue.  The ability to sue for money gives the rights holder leverage to get paid up front, for licenses, rather than after the fact, for infringement.

In some aspects, as with copyright in source code, open source consumers may have alternatives.  They might clean room reimplement an open source library, for example.  In other aspects, as with marketing use of a trademarked name or use of a patented algorithm, there's no such workaround.  If the open source maintainer has the rights and an open source consumer needs the rights, the consumer needs the maintainer's permission, which may come at a price.

Developers can leverage intellectual property power into support by choosing licenses that don't suffice for some users, requiring them to buy alternative terms.  This has long been done with GPL and especially AGPL.

License Zero uses intellectual property as its primarily lever.  License Zero's public licenses give many users permission to use for free, but require users [for commercial purposes](https://licensezero.com/licenses/noncommercial) or [in proprietary, closed software](https://licensezero.com/licenses/reciprocal) to buy permission, which licensezero.com makes very easy.

## Influence

The social side of writing software can vest open source developers with peculiar notoriety and influence over the attention and preferences of other developers.  That attention can translate into more open source contribution along particular lines of development, increased use of tools, libraries, and other projects, and signals to those producing educational, reference, and other resources.  In a word: development has fashion, and open source devs are often trendy.

Open source notoriety competes with other interests and resources in setting current fashion.  Company hiring policies.  Outreach programs.  But open source maintainer influence is also a factor, and a factor with an often markedly different social and cultural character.

Open source developers can leverage their influence into support by accepting donations to use particular development tools and services, even paid tools and services, in visible ways.  They can sell public recognition, as in lists of supporters in a `README` file.  They can appear at company events, or throw their weight behind company social media.

License Zero neither uses nor precludes selling influence as a means of support.  Personally, I've written that [I'm uncomfortable with undisclosed commercial relationships in open source, and advocate for their disclosure](https://blog.licensezero.com/2017/10/16/mercenary-rapport.html#promo).

# Freedom

The fact that a developer made a particular piece of useful open source yesterday does not mean that they have to make improvements to it today, or other open source their consumers would also like tomorrow.  Independent open source developer control their time, and their contributions.  They control what they do and make, and whether that's free, paid, or open source.

## What to Do Next

Developers can sell their freedom to decide what work to do next to companies in the form of service contracts that give the companies influence on how they spend their time.  Those service contracts may produce more open source software, they may produce proprietary software, or they may produce no software at all, but only advice, consulting, training, and so on.

Companies can usually hire other developers to do these things, as well.  But an open source developer can often get them done more efficiently, especially if they relate to their prior open source work.  The reputation and notoriety of the open source developer may make them the obvious, stand-out choice, or the only choice the client knows about.

[Switchmode](https://github.com/switchmode/switchmode) is a free, open form contract for developers doing a mix of open and closed work.  Its terms are compatible with open source work, in both the proprietary and paid-open-source contexts, unlike any standard consulting contracts.  It's designed to take away the legal friction of doing deals between companies and open source leaning developers.

## Withheld Knowledge

The ideal open source project is entirely open and transparent.  Some may know it better than others, but everything necessary to read up---user documentation, developer documentation, overviews of key implementation decisions, hosting guides, deployment configurations---comes with the project.  It is up to the developer of the open source project how much of this knowledge actually gets written out in the open, and how much of it they retain privately.  For parts of this knowledge that are hard to relate to others in writing---tacit knowledge, like the philosophy behind a project or tool set---it's up to the developer how much time they spend developing ways to make that knowledge explicit, instead.

Open source developers can leverage withheld knowledge into support by selling training, consulting, and other services, or by selling copies of, or access to, proprietary materials like books, documentation, and training guides.

License Zero doesn't try to leverage withheld knowledge in any specific way.  Quite the opposite: License Zero's focus on intellectual property power largely came from the belief that open source developers ought to create as much valuable work as possible---code and otherwise---and receive support commensurate with the value of that work.  That being said, with the exception of the obligation to update licensing information for projects that developers are paid to relicense on permissive terms, License Zero imposes no obligations on any developer to write more code, or do other work.  It's therefore possible to leverage both intellectual property, through License Zero, and withheld knowledge, in tandem.
