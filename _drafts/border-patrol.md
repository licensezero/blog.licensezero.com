---
title: Border Patrol
description: Commons Clause, Lerna, and the software demilitarized zone
layout: post
---

Two new license texts, two new license dramas.  [Commons Clause](https://commonsclause.com) patches existing open source terms, taking back permission for commercial resale.  [Lerna](https://github.com/lerna/lerna/blob/19a7f5d4bd88b9cc50b603adcf171623227ec554/LICENSE) added a preamble to their license to cut out companies contracting for US Immigration and Customs Enforcement, then reverted, facing a developer protest of their own.

As legal tools, Commons Clause and Lerna-style exclusions fill small niches.  They matter little in the grand scheme.  Many companies fork their own open projects, continuing development as proprietary software.  Few of those keep code in the open, or allow the specific, narrow kind of unattended commercial use that Commons Clause permits, gratis.  Corporate behavior offends many a conscience.  But relatively few developers pick a battle in `LICENSE`, or frankly, do anything at all.

As episodes of open source politics, however, both Commons Clause and Lerna reveal a great deal.  And what they reveal is deeply disturbing for anyone who sees not just the promise, but the problems of open source today.  Each episode adds a new dot on two long-developing trend lines:

1. Vocal open source partisans lash out more fervently against new licensing and development approaches that come close to open source orthodoxy than they do against closed and proprietary software.  Offer open source terms, but not to everyone, or offer public terms for public code that aren't quite open source as consumers expect, and the pious will flood your social media with scorn.  Some will demand that you take your code fully closed.

2. Incorrect legal statements, flawed legal reasoning, and the imputed legal soundness of foundation-blessed policy positions create fear, uncertainty, and doubt in developers without legal support of their own.  Bombardment leaves an impression of the law that's often exactly wrong.

The prime movers behind Commons Clause and the Lerna change could have done better at minimizing needless drama and confusion.  Much better.  But anyone trying something new in the community, even carefully, should expect heat.  As an attorney, legal misinformation and empty legal threats worry me most.  But the more pressing issue, for anyone attempting to solve open source problems that require licensing power, is the insistence on a kind of dead, innovation-free zone around current open source practice.

We should examine why some feel compelled not just to guard the walls of the Open Source or Free Software Definition, but to sortie outside them, routing anything that comes close.  We should understand the insecurity behind such preemptive attack.

# Flatland

We often speak of software in terms of _open_ or _closed_, as if all software lay along one straight line:

```
closed                                           open
├───────────────────────────────────────────────────┤
proprietary                               open source
software                                     software
```

On that line, we could split open source into _permissive software_ under terms like MIT, BSD, and Apache, and _copyleft software_ under terms like GPL, MPL, and EPL.  Where to plot them depends on your politics.

Software freedom advocates describe copyleft software as not only open, like permissive software, but locked open, in that it can't be put into proprietary software.  In their view, the additional license conditions make copyleft software the more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                    permissive    copyleft
software                         software    software
```

Conversely, permissive-license advocates, sometimes called the BSD school, see the share-alike conditions of copyleft licenses as restrictions on what can be done with the software.  Since permissive software comes with fewer restrictions, permissive software is the more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                      copyleft  permissive
software                         software    software
```

The one-dimensional view of open source correctly renders this, the classic debate _within_ free and open source software.  But like a cartoon, this one-dimensional view massively oversimplifies, in order to emphasize differences.  We start to reveal what the one-dimensional view hides by asking where to plot _source-available software_: software for which source code is available, but without any permissive or copyleft license attached.

In terms of whether we can find source code, open source software and source-available software are they same.  In terms of the permission we have to work with the software, proprietary software and source-available software are the same.  That puts source-available software somewhere between proprietary and open source, but for two different reasons.

# Topography

To render source-available software's relationship to permissive, copyleft, and proprietary software, we need _two_ dimensions that affect programmers' ability to work with software:

1. _availability_ of source in the preferred form for making changes, from completely open to completely closed

2. _permission_ to work with source code available to us, from all-rights-reserved to all-rights-granted

As perpendicular axes:

```
                    │source
                    │open
                    │
    source          │     open
    available       │     source
    software        │     software
                    │
                    │          all rights
                    │             granted
────────────────────┼────────────────────
all rights          │
reserved            │
                    │
    proprietary     │
    software        │
                    │
              source│
              closed│
```

These intersecting lines of availability and permission run like warp and weft through the whole history of the industry.

Consider RMS' parable of the malfunctioning printer.  RMS is a programmer.  He could have fixed the printer's software.  But he never got the chance.  First because he couldn't get the source code.  The manufacturer wouldn't make it available to him.  Second because even if he had got the source code, perhaps by a leak from a sympathetic employee, the manufacturer wouldn't have given him permission to fix it, or to share his fix with others.  To fix the printer's software, RMS needed both source and permission to work with it.  Source code without permission wouldn't do, and neither would permission without source code.

We see the same two dimensions in the Open Source Definition, adapted from the Debian Free Software Guidelines.  The Definition begins:

> Open source doesn't just mean access to the source code. The distribution terms of open-source software must comply with the following criteria: ...

It isn't enough to use distribution terms, otherwise known as a license, to meet the criteria.  The license has to apply to source code we can actually get our hands on.

# Terra Cognita

Commons Clause and the Lerna exclusion, as well as the public licenses for License Zero, [Parity](https://licensezero.com/licenses/parity) and [Prosperity](https://licensezero.com/licenses/prosperity), demonstrate that developers can vary availability and permission for their software independently.  There's no rule that if you make your source available, you have give everybody every permission to work with it.

As specific examples, these new approaches challenge the one-dimensional view of software, like the category of source-available software more generally.   That challenge can feel very present and real, since each of these new licensing tools is designed to apply to fully available source code, published and shared on the same platforms, and with the same tools, as open source.  For those who hold the one-dimensional model near and dear, the challenge is both theoretical and very practical.  This stuff exists, and it's on GitHub.

Commons Clause and Prosperity depart from open source orthodoxy by restricting certain kinds of commercial use.  In that, they serve the same roles as the noncommercial licenses long offered by Creative Commons, which publishes a full spectrum of public license choices for other kinds of creative work, including permissive- and copyleft-style options.  There are many, many creative works online under noncommercial Creative Commons licenses.  But software developers don't readily mix software under licenses with commercial use limits and open source in projects they publish.

Discriminatory license terms, like the Lerna exclusion, receive the same treatment.  Free and open source licenses have often imposed conditions that discriminate in a practical way against proprietary software developers.  But the community as a whole has not accepted terms that deny permission to specific people, companies, governments, or organizations, or categories of them.  Intellectual property laws, like copyright laws and patent laws, give developers the legal power to do so.  But popular public licenses for software, as a rule, haven't exercised that power.

Parity differs from Commons Clause, the Lerna exclusion, and Prosperity by extending a well established and broadly accepted kind of open source licensing term: copyleft conditions, which require developers who change or build on software to share their own source code on similarly generous terms.  Parity was written specifically to be an open source software license, but to go further than any open source license had gone before, demanding that developers share more code in more situations.  In other words, to update copyleft, extending it to a logical extreme.

From the permissive or BSD point of view, that would make Parity the least open open-source-style license ever written.  Conversely, from the software freedom or GPL point of view, Parity's thrust could make it more open even than AGPL, by locking code open against more kinds of proprietary closure.

As it happens, some free software advocates reject Parity, but not because it wants to be extreme.  Parity requires contributing code back even if that code was written for private use, and not shared.  The Open Source Initiative has approved licenses that require contributing back private changes, but The Free Software Foundation has rejected such licenses as "non-free".

From the FSF point of view, as I'm able to understand it, forcing contribution of private changes disqualifies a license categorically, like explicit commercial use limits or discrimination.  That means the FSF's categorical exclusions, best I can tell, prevent it from ever approving any license that would effectively implement "free for open source" for developer tools projects, as distinct from libraries and frameworks.  If I could write a license that closes the developer-tools loophole _and_ meets FSF's criteria, I would.

# Istanbul, Constantinople

It's important to look at new license experiments soberly, and to appreciate the sins, however esoteric or minor, for which they can be condemned by informed members of the community.  But recent history also teaches that the community's instinct to bite a novel license comes first, and the hunt for reasons only later.

Facebook's `PATENTS` file for React tacked terms onto a three-clause BSD license, much as Commons Clause tacks terms onto any standard license, and the Lerna team tacked terms onto MIT.  The part of Facebook's `PATENTS` file that offended some concerned defensive termination, a common open source license term that takes away your license if you sue others under patents.  In the end, Facebook combined an approach to defensive termination previously known and accepted as valid in open source, but in a new looking way.  That was enough for pitchfork and torches.

Defensive termination terms in open source licenses vary, both in how much license they take away, and when they're triggered.  Some disliked that Facebook's original defensive termination provision triggered on any legal claim trying to invalidate a Facebook patent, and applied even if Facebook sued you under patents first.  In a rare show of legal responsiveness, Facebook actually updated their `PATENTS` file to address and clarify the trigger.  They took community feedback on their new terms.

There are good reasons for specific companies to dislike even the revised terms, but not good reasons to condemn them as outside open source practice.  Terms to much the same effect have long been approved both by Open Source Initiative and by the Free Software Foundation, as in the Common Public License written by IBM.  Furor came all the same.  OSI approved a variant of the BSD license---there are many---with Apache-style patent language bolted on, offering Facebook a chance to kiss the OSI ring for absolution.  Community commentators, for their part, preferred MIT, a dusty, old, but exceedingly popular form that never even says the word "patent".  And they got it.  Uniformity prevailed over substance, twice.

# Buffer Zones

I began by noting that the reactions to Commons Clause and the Lerna exclusion show that vocal members of the open source community seem to be more comfortable with proprietary software---unavailable source and all rights reserved---than with source-available approaches that come close to open source.  When a project attempts to occupy territory _between_ proprietary and open source as practiced today, it hears either that it should close its source code, or that it should revert to a standard open source license.

On social media that I reviewed, by vote of applause and rotten tomatoes, the wisdom of unsolicited opinion seemed to hold that Redis Labs should continue development of its Redis modules in private, or take down its repositories entirely, and that Lerna should revert to unadorned MIT terms.  One in each direction.

I've done my best to understand the dynamic at play.  As I've read, reread, and debated others, the concept that's come to work best is the _buffer zone_.  The practical effect of social pressure in the community, if it has its way, would be that projects retreat either to the proprietary stronghold, or to the open source camp, and leave the space between a bare, unsettled DMZ with clear lines of sight from one extreme to the other.  So rather than ignore or shun software under terms that fall outside their community boundaries, activists lower their gates and charge out to meet each one, like an invading army, even if it's just three guys who landed a PR to a repo they'd never heard of.

# Dominoes

When pressed, defenders of the open source realm tend to express explicitly that these innovations pose threats to their community as they understand it.  It's often difficult to get past those assertions, to the why.  The reasons I've heard sound in two recurring themes: _confusion_ and _efficiency_.

On the infrastructure side, confusion manifests as worry that users who come to open source will have their expectations frustrated, or fall prey to a kind of bait-and-switch.  Among the properly open source code users find through a distribution, repository, source code host, or search platform, they may unwittingly find software they don't have permission to use in their particular way, for their particular business, or for their particular purpose.  Infrastructure-based efficiency concerns lament that even users who become aware these traps exist will have to spend time looking where they step.

On license terms, beyond invocation of the Open Source Definition or the Free Software Definition, confusion concerns sound much as they would from a marketer tending a well known brand.  Experimenters shouldn't be permitted to skim value off the good name of open source.  Experiments shouldn't raise doubts about where the borders of open source or free software fall.  All for the benefit of consumers.  As for efficiency, no consumer wants another license to read.  Even if it says something new, or might enable more developers to make more software available.

# Preoccupied Territory

As with many buffer zones imposed strategically, from aloft, the open source dead zone's double-troubled: the DMZ is currently inhabited, and social forces abhor invisible, made-up lines.  The buffer zone that some members of the community adamantly defend might fortify open source.  But as one part of the community encroaches abroad, the rest of the community embraces open borders at home.

A preponderance of vital and popular open source infrastructure services of the current generation, from GitHub to npm to Travis CI, _require_ "openness" in only one dimension: availability.  If you're willing to publish your code, these services welcome your project, free of charge.  If you want to use the same service and tooling to work privately, you pay for that privilege.

As for what license terms apply to the work you share, the services take the licenses they need for themselves, in terms of service.  They don't rely on users to pick open source or other licenses that give the permission required to fulfill their functions.  Neither do they police what additional permission, if any, users offer to other users.  Service providers are more than happy to count even totally unlicensed projects, and users who publish only unlicensed projects, toward their stratospheric numbers, all the while flying the flag of open source.

So with the partial exception of Stack Overflow, which poses unique problems, the most popular service providers of open source today don't make any guarantees about licensing.  It's up to users to search, filter, and audit what they find.  Service providers do provide functionality related to licensing, but only functionality to make licensing information more visible, and to facilitate independent analysis, as with software tools that process standardized licensing metadata.  In other words, current-generation open source infrastructure encourages diversity, rather than enforcing uniformity.  Both because diversity is good for growth and business, and because enforcing uniformity means diving head first into the mire of definitional disputes, throwing a lot of structural power to one side or the other, exacerbating those divisions, and alienating everybody else.

On the license side, we also see accommodation, rather than control.  Standards like SPDX embrace not just FSF- or OSI-approved licenses, but public licenses of all kinds, including noncommercial and proprietary licenses.  Packaging standards tackle the problem of multiply-licensed projects, which incorporate code under a variety of terms, head on.  Many provide escape valves for specifying non-standard terms, by reference to files or Web pages.  Meanwhile, data consuming audit tools almost universally support configuration to whitelist specific third-party artifacts, not just on determination that a standard license wasn't coded correctly, but when use is approved on other grounds.  After all, the consumers taking open source consumption this seriously tend to be corporations making proprietary software.  Those work environments have long grappled with one-off and privately-licensed components.  And long feared particular open source licenses---the "viral" ones---more than any other terms.

# GPS

Considering all these developments at once, I'm struck by _how far behind_ other industries software has lagged in developing software to accommodate that diversity.  It's no wonder open source has so-called sustainability problems with no clear solutions, and can't transfer learnings from parallel industries.

Many creative industries, like art, architecture, and music, produce at least some output that's publicly available and adaptable, by its nature.  In part inspired by open source, groups like Creative Commons have "ported" permissive and copyleft licensing to those fields, by systematizing it over Internet distribution.  But before open source and before Creative Commons, licensing diversity, including the public domain, as well as a gamut of correlated funding models, were already their norms.

From content fingerprinting to royalty management to cross-licensing to protection against plagiarism, established creative fields built institutions and systems that afford a long, smooth continuum of licensing and distribution choices, plus an ability to slide along it over time.  They've modernized those systems, albeit slowly, with software.

The software industry itself had no such preexisting systems of its own.  It began with closed-proprietary, because that is the legal default.  It systematized the other, open-permissive extreme, seeded from academe, to offset the known limitations of closed-by-default.  Meantime, there have always been individuals, projects, and companies finding happiness near something like the median.  But the infrastructure built up to support those approaches took the form of specific companies and inter-company practices, not public infrastructure.

# Middle Ground

Over time, selective systematization of extremes produced a bipolar, black-or-white distribution in the software community.  Open source---permissive software and copyleft software with known, practical loopholes---"won" by allying with proprietary software, shedding the morality of software freedom, and embracing a role as zero-dollar component supplier.  That bipartite alliance has become its own justification, threatening a common ethic that software long shared with other creative fields: respect for the creator's right to choose the terms for their work.

Consensus on that point is broad, and few feel comfortable challenging it overtly.  But selective social pressure, discriminatory tooling and platform support, and unequal access to legal counsel erode it in practice.  When pressure forces creators off the terms that best express their goals and needs, not by convincing them that another approach better achieves those ends, but by disparaging their purpose and threatening sanction, it sets up and wins a zero-sum game at the creator's expense.  Even if the winner in the game is some definition of the common good, that only begs the question of why any individual creator should play in the first place.

# Erosion

Some creator goals, like those behind the Lerna change, go to ethics, or politics, or social change.  Some, like those behind Commons Clause, go to funding and fair play, as does License Zero.  It's vitally important for those with goals that don't fit into the two-party, proprietary-or-permissive system to realize that taking the leverage of license terms away from them, as a tool, forces David to fight Goliath without his sling.  It's vitally important to anticipate the heat that anyone doing anything new with license power will face, and to plan for it, so David doesn't have his sling taken away in the middle of the fight.

License Zero explicitly aims to take as much heat as possible for individual developers who adopt its methods.  The project was set up as a company, and a distinct website, in part to insulate those who might otherwise look to be acting alone.  This [blog](https://blog.licensezero.com), as well as the [guide](https://guide.licensezero.com) are easy to link to, and head off much legal misunderstanding and misinformation.  [licensezero.com](https://licensezero.com) provides missing public infrastructure for the dual-licensing model, accessible even to individual developers who'd never set up a company like MySQL, Trolltech, or Artifex.  I submitted an early version of the Parity license to OSI for approval, to focus and centralize the inevitable debate.

The Commons Clause website and FAQ attempted to run some interference for adopters, on very short notice.  Effort at a shared, reusable reversion of the Lerna `LICENSE` text popped up within hours of the change.  Attempts were made to connect unrepresented maintainers with legal support.  All of that came too late.  Given the lay of the land, mitigation had to be as much a part of the plan going in as the changes and their purposes.

There are deep, structural problems to solve in software, open source included.  Some of those problems pit small, dispersed players and firms against large and established interests, organized in firms and in communities.  Intellectual property law bestows creators with substantial power to solve some of these problems, from making a living to preventing misuse of our work against our politics or religions.  Such power must absolutely be wielded with care.