---
title: The Two-Party System
description:
layout: post
---

# Overture

Before GitHub, open source, and free software, before even hacks and hackers and hacking as we know them, there has always been a movement of enthusiasts demanding something back from the computer industry.  Hackers and hobbyists wanted community.  Academics wanted collaboration.  Craftsmen wanted reputation.  Free software wanted purpose.  Open source, having inherited community, collaboration, reputation, and purpose from prior efforts, wanted to keep those things, but also acceptance back into industry.  And got it.

Having met its own definition of success, open source can no longer call itself a counterculture.  Self-styled opposites---closed, proprietary software on the one hand, open, permissive software on the other---now thrive in self-declared symbiosis, at least for those already in positions of strength.

If that includes you, these are heady days, with fulfillment aplenty,and money to boot.  If that doesn't include you, you may have good reason, like those before you, to demand something back from the industry, open source now included.  Perhaps accountability for corporate misconduct.  Perhaps respect for users.  Perhaps patches back, or a fair wage.

But do you have the means to get it?

# Conflict

React, Redis, Lerna.  Three license tiffs in less than one year.  Each reaffirming a troubling trend in open source politics: eroding respect for developers' rights to choose their own terms.  Eroding respect for the very lever the law gives creative individuals to demand something back from larger interests.  The very leverage that [made a free software movement possible.  The leverage by which "open source" was defined.

Taking license power out of developers' hands sets the community police on a conflict course with those solving pressing community problems.  Problems that include financial inequity and the decay of copyleft.  Solutions that include License Zero.

I'll be frank.  Facebook's `PATENTS` file, Commons Clause, and Lerna-style blacklists don't matter that much, in the grand scheme of things.  They're niche tools, and few others will need to use them.  But you wouldn't know that from the reaction.

The purported existential threat to open source from these experiments can have little to do with their meager popularity and narrow utility.  It has everything to do with the power to experiment, and the power with which they experimented.  For some, the very prospect of license innovation threatens open source as they know it.  That being the case, it isn't enough to defend a definition, proclaim whether new approaches meet it, and avoid those that don't.  If new terms falls outside, and especially if they fall _just_ outside, approved practice, a preemptive sortie must be launched to rebuke, rout, and if at all possible eliminate it from the field of available developer choice.  Even if that means telling an open project to "just go proprietary" and close its source.

As I've followed responses to React, the Redis modules, and Lerna, I've been most disturbed by the use of legal fear, uncertainty, and doubt against developers experimenting with their rights.  As a lawyer, that kind of leverage offends me, morally.  I have to call it out, and I'm not done writing about it.  But in the end, appeal to fear of law is just a tactic, incidental to a broader program.

The broader program leads to a disciplined, two-party system in software.  A system that constrains practical developer choice to market-optimized "proprietary", at one extreme, or community-policed "open", at the other.  Within that system, third parties, especially third parties near to one or the other major party, threaten to split attention, loyalty, and credit off the incumbents.  At a higher level, alternatives threaten the ability of the bipartite system to claim effective representation of the whole community, despite failing to address pervasive needs.  Needs like "sustainability", if you're not yet a huge corporation, and don't want to hand them your software for nothing.

Projects that make source available, but effectively hold back some permission, as for commercial, closed-source, or unethical use, prove that you don't have to adopt the whole permissive-open creed, or all at once, to share and build code online.  Publishing code alone brings many of the benefits currently imputed exclusively to open source under licenses like MIT and BSD.  Moreover, live experiments reinforce that developers needn't rely on any outside institution's help or approval to prepare or approve terms for their work.

The political-system analogy fails here:  Developers don't need anyone, or any organization, to represent them.  Licensing gives contributors individual power, and how they use it is their individual choice.  The community can develop, identify, compare, and assimilate new licensing approaches, just as it nurtures and elevates new software.  You don't need a foundation or a large, corporate sponsor to create code, and you don't need a foundation or a large, corporate sponsor to license it.

In the end, license experiments _are_ a threat, but not a threat to open source as defined.  They're a threat to what open source sought, as a movement: recognition and collaboration with large companies producing proprietary software.  Patches to existing licenses and license ideas don't change how effective unpatched terms remain for other work.  Rather, innovation threatens the symbiosis of open source orthodoxy and enterprise-procurement-bound proprietary consumption.  Holding permission back reduces what the shepherds of open source can lead back to large company-consumers.  Offering a compelling middle way that better balances concerns for smaller players reduces the number of projects that end up under pushover licenses, for lack of better-fitting options, ready for selective assimilation by big-company incumbents that prefer to outlast and out-compete, rather than sustain or compensate.

Suppressing license choices suppresses those best served by such choices.  We should examine, and reject, any politics that limits large swathes of our community to choices that work better for others than for themselves.

# Spectrum

Enforcing diametric software choice is rarely an intentional personal or institutional goal.  It doesn't have to be.  The way free and open source software advocates learn to talk about free and open source software---mostly among themselves---bakes that limiting dichotomy into the common view of the software world, just as polarized left-right vocabulary limits our political views.  Third ways defy that vocabulary, and threaten that mindset.  To have a better conversation, we need a better vocabulary, and a way to get there from how we think and talk now.

Open source often speaks in terms of _open_ or _closed_, as if all software lay along one straight line:

```
closed                                           open
├───────────────────────────────────────────────────┤
proprietary                             free and open
software                              source software
```

In the early days, before open source and industry bent this line into a horseshoe, bringing very-closed and very-open together, parallels to the left-right political spectrum were often explicit:

```
right                                            left
closed                                           open
├───────────────────────────────────────────────────┤
businesspeople &                         communists &
proprietary                             free and open
software                              source software
```

It didn't matter that this was wildly misleading, or that those involved both in "free software" and "open source" held diverse political views and working affiliations.  Those nuances didn't fit on the line.

Meanwhile, within the movement at least, we're eager to split free and open source into _permissive software_ under terms like MIT, BSD, and Apache, and _copyleft software_ under terms like GPL, MPL, and EPL.  Where to plot what depends on your politics.

Software freedom advocates describe copyleft software as not only open, but locked open, unable to be closed.  In their view, the additional rules preventing proprietary closure make copyleft the more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                    permissive    copyleft
software                         software    software
```

Conversely, permissive-license advocates, the BSD school, see the share-alike rules of copyleft licenses as restrictions on what can be done with software.  Permissive software comes with fewer rules.  That makes permissive the more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                      copyleft  permissive
software                         software    software
```

These competing one-dimensional views of open source correctly render the classic debate _within_ free and open source software.  But like a cartoon, this one-dimensional view oversimplifies to exaggerate small differences.

We start to show what this view hides by asking where to put _source-available software_: software for which source code is available, but under different license terms, neither permissive nor copyleft.  Here's the model:

```
closed                                           open
├────────────────────────┼──────────────────────────┤
proprietary            source             open source
software              available              software
```

How does source-available software end up in the middle?  In terms of whether we can find source code, open source software and source-available software are of a kind:  We can.  In terms of the permission we have to work with the software, proprietary software and source-available software are of a kind:  There's no permissive or copyleft license.  That puts source-available software somewhere between proprietary and open source, but for two very different reasons.

# Compass

To render source-available software's relationship to permissive, copyleft, and proprietary software faithfully, a line from _open_ to _closed_ isn't enough.  We need a dimension for each dimension of difference:

1.  _availability_ of source code, from completely open to completely closed

2.  _permission_ to work with source code, from all-rights-reserved to public-domain

As perpendicular axes:

```
                    │source
                    │open
                    │
         source     │     open
      available     │     source
       software     │     software
                    │
                    │              public
                    │              domain
────────────────────┼────────────────────
all rights          │
reserved            │
                    │
         closed     │     mostly
    proprietary     │     terra
       software     │     incognita
                    │
              source│
              closed│
```

Because both availability and permission determine ability to work with software, they run like warp and weft through the whole history of the software industry.

Consider RMS' parable of the malfunctioning printer.  RMS could have fixed the printer's software.  But he never got the chance.  First because he couldn't get the source code.  The manufacturer wouldn't make it available to him.  Second because even if he had got the source somehow, the manufacturer wouldn't have given him permission to fix it, or to share his fix with others.  To fix the printer's software, RMS needed both source and permission to work with it.  Source code without permission wouldn't do, and neither would permission without source code.

We see the same two dimensions in the Debian Free Software Guidelines, and later in the Open Source Definition.  The Definition begins:

> Open source doesn't just mean access to the source code. The distribution terms of open-source software must comply with the following criteria: ...

It isn't enough to use distribution terms, otherwise known as a license, to meet the criteria.  The license has to apply to available source code.

Of course, proprietary software works both dimensions, as well.  A typical software company collects all rights in its products and services, through intellectual property agreements with employees and contractors.  Those terms also require personnel to keep technology, including source code, secret.  Software travels from vendor to customer under specific, limited licenses, and often in compiled or obfuscated form.  The combination ensures minimum source code availability and maximum rights reserved, preserving maximum opportunity to sell.  Control of source and permission makes the vendor the only efficient source not just of licenses and copies, but maintenance, integration, improvements, and support, as well.

# Third Parties

Commons Clause and the Lerna exclusion, as well as [Parity](https://licensezero.com/licenses/parity) and [Prosperity](https://licensezero.com/licenses/prosperity), the public licenses for License Zero, demonstrate that developers can mix and match availability and permission for their software.  There's no rule that if you make your source available, you have to give everybody every permission to work with it.  You can withhold some permission to work with your code, like permission to use commercially, in proprietary software, or in derogation of user freedom, even if you publish your code online for all to see.  If others take your published code and use it against your terms, you can sue for copyright infringement.

As specific examples, these new approaches challenge the one-dimensional view of software, like the source-available category more generally.  That challenge can feel very present and real, since each of these new licensing approaches was designed to apply to fully available source code, published and shared on the same platforms, and with the same tools, as permissive open source.  For those who understand software through the one-dimensional model, the challenge is both theoretical and practical.  This stuff exists, and it's on GitHub.

Commons Clause, Prosperity, and earlier experiments like [Fair Source](https://fair.io) depart from open source orthodoxy by restricting certain kinds of commercial use.  In that, they serve the same roles as the noncommercial licenses long offered by [Creative Commons](https://creativecommons.org), which publishes a full spectrum of public license choices for other kinds of creative work, including permissive- and copyleft-style options.  There are many, many creative works online under noncommercial Creative Commons licenses.  But that practice hasn't penetrated as deeply into open software.

The same is true of exclusionary license terms, like the Lerna exclusion.  Free and open source licenses have often imposed conditions that discriminate in practice, against proprietary software developers.  But the community as a whole has not accepted terms that deny permission to specific people, companies, governments, or organizations, or categories of them.  Intellectual property laws, like copyright laws and patent laws, give developers the legal power to do so.  But popular public licenses for software, as a rule, haven't exercised that power.

The Parity Public License differs from Commons Clause, the Lerna exclusion, and Prosperity by reviving a well established and broadly accepted kind of open source licensing term: copyleft conditions, which require developers who change or build with open software to share their own work, too.  Parity was written specifically to fall within open source principles, but to go further than any open source license had gone before, by demanding that developers contribute code back in as many situations as possible.  From the permissive or BSD point of view, that would make Parity the least open open-source-style license ever written.  From the software freedom or GPL point of view, Parity could be even more open than AGPL, by locking code open against more kinds of proprietary closure.

# Constituencies

As it happens, some free software advocates reject Parity, but not for its intent.  Parity requires contributing code back even if that code was written for private use, and not distributed to others, to avoid gameable rules about what is or isn't private.  Paradoxically, the Open Source Initiative has approved licenses that require contributing back private changes, but the Free Software Foundation rejects them.

From the FSF point of view, forcing contribution of private changes disqualifies a license categorically, like explicit commercial use limits or discrimination against particular users.  Best I can tell, that means the FSF excludes any license that would effectively implement "free for open source" for developer tools that one _runs_ to build new software, rather than _includes_ in new software like libraries and frameworks.  If I could write a license that closed the developer-tools loophole _and_ met FSF's criteria, I would.  If you think you can, please get in touch.

[Prosperity](https://licensezero.com/licenses/prosperity), License Zero's noncommercial public license, bridges a similar gap.  Like Parity, Prosperity addresses complete, standalone applications or plug-ins, rather than libraries, frameworks, or other build-in components.  But "free for open source" doesn't ask anything back when that standalone application is a word processor or chat program that doesn't help make software.  If the developer wants a license to drive demand for paid licenses to support their work, the most direct approach is withholding permission to use for profit without pay.  Prosperity allows developers to make this deal, while continuing to offer free use to non-commercial users, as do many traditional software companies, via free or low-cost educational and non-profit programs.

Commons Clause also fills a somewhat narrower niche, with a slightly different twist.  Rather than withhold permission to use commercially, Commons Clause withholds permission to _sell_ commercially.  But everyone can still use for commercial purposes in house, within their own organizations, for internal needs.  That distinction allows customers to download, install, and demo the software for themselves, while simultaneously withholding the right to sell the benefit of use to others, through full applications, software-as-a-service, or professional services.  If the program is, say, a video compression program, users can download and use it internally for free, but need to buy another license from the developer to use in the video hosting service they offer online, or to offer video encoding as an API to other software businesses, or to offer video-encoding consulting.  Crucially, Commons Clause stymies cloud service providers who might offer databases and similar programs as services.

The Lerna license patch excluding companies working with ICE stands in a category of its own.  But it does not stand alone there.  The JSON License adds text to MIT requiring use for good, rather than evil.  HESSLA prohibits uses in violation of human rights or personal privacy.  Licenses prohibiting military use, or use by countries or organizations implicated in specific atrocities, were known long before "open source" was coined.  These licenses sometimes speak to specific concerns developers have about the nefarious potential of particular work, like software that would obviously be useful in weapons.  But as often, developers choose these licenses out of overarching personal belief.  They tend adopt such a license for much or all of their work, rather than for specific projects.  Uses of specific software may vary, but the developer, as well as their desires to make a statement and build a network, remain constant.

# Party Discipline

Commons Clause and Lerna each varied from orthodox open source in ways that took them outside old definitions of free and open source software.  But recent history also teaches that the instinct to bite a novel license comes first, and justifying indictments come later.  Facebook attempted nothing particularly new or objectionable with React, but went about it in a somewhat novel way.  The whiff of nonconformity was enough for pitchforks and torches.  Pitchforks and torches did not improve React's licensing situation.

The part of Facebook's `PATENTS` file that rankled some implemented _defensive termination_, a common open source license term that takes away your free permission for the software if you sue others under patents.  Defensive termination terms in open source licenses vary, both in how much license they take away, and in when they're triggered.  Some disliked that Facebook's defensive termination provision triggered on any legal claim trying to invalidate a Facebook patent, and applied even if Facebook sued you under patents first.  But that is not the provision that caused the major drama.  In a rare show of responsiveness by a large corporation to comments from the Internet, Facebook actually updated their `PATENTS` file to address and clarify their original trigger.  They took community feedback into their new terms.

There are good reasons for specific companies to dislike even the revised terms, but not good reasons to condemn them as "not open source".  Terms to much the same effect have long been approved both by Open Source Initiative and by the Free Software Foundation, as in IBM's Common Public License.  Furor came all the same.  In the interim, OSI approved a variant of the BSD license, the base copyright license Facebook used for React, with Apache-style patent language bolted on, offering Facebook a chance to kiss the OSI ring.  Community commentators, for their part, preferred MIT, a dusty, old, but exceedingly popular form that never even says the word "patent".  And they got it.  Uniformity prevailed over substance, twice.

To make this out as a victory, you have to take a pretty narrow, shallow view.  Lots of projects are MIT.  Now React is MIT, too.  But MIT alone is a far inferior patent license to BSD with `PATENTS` 2.0, and patents were the problem to begin with.  By taking all this time to fret on its patent terms, Facebook have all but proclaimed they hold at least one patent that reads on React.  And perhaps on React's clones, often MIT licensed and from folks unlikely to own any patents, but newly popular in the wake of fear, uncertainty, and doubt about React.

This is the Law of Jante in action within open source.  The only improvement here is that React licensing now _looks_ standard.  React's importance and patent situation are anything but.

# Spoilers

When a project attempts to take a position _between_ proprietary and open source as practiced today, it hears either that it should close its source code, or that it should revert to a standard open source license.  Thus by vote of applause and rotten tomatoes, the wisdom of unsolicited opinion on social media I reviewed held that Redis Labs should continue development of its Redis modules in private, or take down its repositories entirely, and that React and Lerna should revert to unadorned permissive terms.

I've done my best to understand the dynamic at play.  As I've read, reread, and debated others, I've heard reasons that sound in two recurring themes: _confusion_ and _efficiency_.

On the infrastructure side, confusion manifests as worry that users who come to open source will have their expectations frustrated, or fall prey to a kind of bait-and-switch.  Among the properly open source code users find through a system distribution, repository, source code host, or search platform, they may unwittingly find software they don't have permission to use in their particular way, for their particular business, or for their particular purpose.  Infrastructure-based efficiency concerns lament that even users who become aware of these traps will have to spend time minding where they step.

On license terms, beyond invocation of the Open Source Definition or the Free Software Definition, confusion concerns sound much as they would from a marketer tending a well known brand.  Fledgling interlopers shouldn't be permitted to skim value off the good name of open source.  Experiments shouldn't raise doubts about where the borders of open source or free software fall.  All for the benefit of consumers.  As for efficiency, no consumer wants another license to read.  Even if it says something new, or might enable more developers to make more software available, over the short or long term.

# Plurality

A kind of licensing demilitarized zone around open source licensing practice vintage 2007 might fortify and preserve the iteration of open source that achieved peace with the Fortune 500.  But as one part of the community enforces conservatism afield, the home front of open source loosens up.  Laissez faire has done and will do more to turn community members away from open source originalism than license experiments ever could.  But also more to promote efficiency.

A preponderance of vital and popular open source infrastructure services of the day, from GitHub to npm to Travis CI, require "open" in only one dimension: source code availability.  If you're willing to publish your code, these services welcome your project, free of charge.  If you want to use the same services and tooling to work privately, even on publicly licensed code, you pay for that privilege.

As for what license terms apply to the work you share, modern infrastructure takes the licenses it needs for itself, via terms of service, not rules about `LICENSE`.  It doesn't rely on users to pick an open source or other license that gives permission required to fulfill its function.  Neither does it police what additional permission, if any, users offer to other users.  Infrastructure providers are more than happy to count even totally unlicensed projects, and users who publish only unlicensed projects, toward their stratospheric numbers, all the while flying the open source flag higher than anyone else.

Thus, with the partial exception of Stack Overflow, which poses unique problems, the most popular providers of open source infrastructure today don't make any expansive guarantees about licensing to users.  It's up to users to search, filter, and audit the source they find.  Service providers do provide functionality related to licensing, but only functionality to make licensing information more visible and uniform, ready to be crunched by software tools that understand standardized metadata.  As such, current-generation open source infrastructure encourages diversity, rather than enforcing uniformity.  Both because diversity is good for business, and because enforcing uniformity would mean diving into the mire of definitional politics, throwing a lot of structural power to one side or the other, driving off everybody else, and languishing in pious obscurity.  Like GNU Savannah.

On the license side, we also see accommodation, rather than control.  Standards like SPDX embrace not just FSF- or OSI-approved licenses, but public licenses of all kinds, including noncommercial and proprietary licenses.  Packaging standards tackle the problem of multiple- and composite-licensed projects, which incorporate code under a variety of terms, head on.  Many provide escape valves for specifying completely singular terms, by reference to files or Web pages.  Meanwhile, data consuming audit tools almost universally support whitelisting specific third-party artifacts for any reason, and not just identification of a miscoded, institutionally approved license.  After all, the overwhelming majority of consumers taking open source consumption seriously at scale are working for large corporations making proprietary software.  Such firms have long grappled with one-off and privately-licensed components.  Diversity is their norm.  These enterprises often fear particular open source licenses---the "viral" ones---more than unfamiliar proprietary terms.

Overall, these developments explain why the greatest source of confusion for new open source community members is often a revelation that a licensed-obsessed definition stewarded by a foundation they've never heard of is supposed to define the movement.  And why open source advocates have spent the last twenty years, and will spend many more, attempting to convince programmers that having source that is open does not make software open source.  All the go-to license choices are older than the new programmers are.  Definitions promise uniformity and predictability, but you're either consuming indiscriminately, spending a lot of time picking through options for one that says "MIT" or "BSD", or using a tool that does it for you.

# Swing Voters

Short-term, standardized radical-copyleft and noncommercial licenses could attract projects that might otherwise pick more permissive terms, for lack of available, better-fitting options.  But long-term, third-way licenses might very well increase both the amount of software in the open, and the amount of permissively licensed software, overall.

It's no longer any kind of secret that choosing maximally permissive terms hobbles a project financially.  Achieving popularity, in part by giving a permissive license, does not guarantee that _any_ of the value produced by the project will flow back.  Rather, lived experience of independent developers shows that popularity almost always means more demand on time and energy.  A few projects attract broad and diverse contributor teams, but most just don't, leaving a very small group to do the overwhelming majority of the work, much of which has more to do with community than code.

As a general rule, permissively licensed projects are either subsidized by large corporations for business reasons, or subsidized by individuals, with unpaid time.  Open source is only justifiable as a loss leader if the loss actually leads to win.  That means products or services that _aren't_ open source development, and compete with it for time and energy.  Running both an open source development program and a winning business offering means either balancing the two very carefully, as an individual, or spinning up a firm to field a team to distribute responsibilities.  If you can't or don't want to walk the tightrope alone, you need a path from fledgling product-company to company that can afford to give half its work product away as permissively licensed open source.

The good news is that it's far, far easier to offer a software project under _more_ permissive terms, later on, than it is to restrict what you've already given away.  A company or solo hacker can develop a valuable prototype, license it under radical-copyleft or noncommercial terms, charge early commercial adopters for permission to use in proprietary software, establish a business case for a parallel product or service offering, launch it, and relicense their work under permissive terms.  Having established a user base with a demonstrated capability and willingness to pay, ongoing development becomes a loss-leader for hosting, training, custom development, paid feature work.  Whatever makes sense for the project.

Such an approach trades off some of the adoption benefits of a permissive license for the sustainability benefits of a credible business model.  But both adoption _and_ support for development are necessary for making production of software financially rational and worthwhile for many developers.  Making software production rational and worthwhile _is_ the economic problem.  Not squeezing more and more irrational contribution out of experienced developers who've already accumulated experience and reputation.  Not incentivizing production of code for which there's no demand.

License Zero implements every step of this process.  The radical-copyleft license is [Parity](https://licensezero.com/licenses/parity).  The noncommercial license is [Prosperity](https://licensezero.com/licenses/prosperity).  [licensezero.com](https://licensezero.com) automates selling private licenses, so the developer can focus one hundred percent on development.  The same system can broker a [relicensing transaction](https://guide.licensezero.com/#relicensing) to turn the project into permissively licensed open source, for a stated price.

Of course, there's no rule, in License Zero or otherwise, that projects _have_ to graduate from source-available to permissive open source.  There's no requirement to offer to relicense a License Zero project, and no obligation on the market to pay that price, when you do.  Some projects can and will remain source-available, and sustain their development through private license sales.

The benefit of the source-available approach, both to the developer and to others online, is making the source available when it otherwise wouldn't be.  Whether for audit, recruiting, teaching, or access to tooling, like vulnerability alerts, that's beneficial to both producer and consumer.  Available source and even all-rights-reserved is better than no source and all-rights-reserved.

Whether the appearance of source-available code in channels that also host permissive open source causes confusion or reduces efficiency is largely a question of information and tools.  The easier these new licenses are to read, and the more good documentation is available on them, the better for all.  The more metadata standards, license detection algorithms, and audit tools accommodate them, the more efficient ingesting mixed channels will become.  Refining that tooling is worthwhile, whether standardized third-way licenses take the scene or not.  Without it, confusion and inefficiency will rise, even if we stick with the licenses we already have.

# Centrism

Software is an industry unto itself, but it's not the only creative industry facing production, incentive, labor-relations, and self-image challenges.  The more I learn of other creative fields---from journalism, to fiction, music, film, and graphic art---the more I'm struck by how much software has to learn from its predecessors, even as those predecessors learn from software.

Software history swings like a pendulum.  From open to closed and back.  From client to server and back.  From large enterprises to small startups and back.  From public darling to public enemy and back.  It's tempting to understand each of these changes in terms of their extremes.  And it's tempting to ignore the ways all of these pendulums swing at once, overlapping and interacting.  Software as a service rose as copyleft fell.  Large companies have risen so high, but industry images now falls.

<!-- YouTube Video: Harvard Natural Sciences Lecture Demonstrations, "Pendulum Waves" -->
<iframe class="youtube" width="560" height="315" src="https://www.youtube-nocookie.com/embed/yVkdfJ9PkRQ?rel=0&amp;showinfo=0&amp;start=25" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

_Video from Harvard Natural Sciences Lecture Demonstrations, &copy; 2010 President and Fellows of Harvard College_

All of this polarized, discreet, binary self-imagery and self-understanding makes for a certain willful blindness to the messy middle where we spend most of time.  Any simple theory, or simple history, of software production, or of open source, is always too simple.  And any forceful effort to make them simple has collateral damage.
