---
title: Border Patrol
description: Commons Clause, Lerna, and the open source dead zone
layout: post
---

Two new licensing ideas, two new licensing dramas.  [Commons Clause](https://commonsclause.com) patches existing open source licenses, limiting commercial use and resale.  [Lerna](https://github.com/lerna/lerna/blob/19a7f5d4bd88b9cc50b603adcf171623227ec554/LICENSE) added a preamble to their license to cut out companies contracting for US Immigration and Customs Enforcement, then reverted the change under protest themselves.

As legal tools, Commons Clause and Lerna-style exclusions fill small niches.  They matter little in the grand scheme.  Many companies fork their own open projects, continuing development as proprietary software.  But relatively few of those continue developing in the open, or want to allow the specific, narrow kind of free, unattended commercial use that Commons Clause permits, the second time.  Corporate bad behavior offends many a conscience.  But relatively few developers will pick that battle in `LICENSE`, or frankly, do anything about it at all.

As episodes of open source politics, however, both Commons Clause and Lerna reveal a great deal.  And what they reveal is deeply disturbing.  Each incident extends two developing trends:

1. Vocal open source partisans lash out more fervently against new licensing and development approaches that come close to open source orthodoxy than they do against closed and proprietary approaches.  Make proprietary software with open source, the community will honor your choice.  Offer open source terms, but not to everyone, or offer public terms that aren't quite open source, and the pious will flood your social media with scorn.  Many will tell you to go fully closed.
2. Incorrect legal statements, flawed legal reasoning, and the imputed legal soundness of foundation-blessed policy positions create fear, uncertainty, and doubt in developers without legal support of their own.  Mental and emotional bombardment leaves a false impression of the law that's often exactly wrong, favoring conservatism and conformity.

The prime movers behind Commons Clause and the Lerna change  could have done better at minimizing needless drama and confusion.  So much better.  But anyone trying something new in the community, even carefully, should expect heat.  As an attorney, legal misinformation and empty legal threats worry me most.  But the more pressing issue, for anyone attempting to solve urgent open source problems that take the power of licensing, is the insistence on a kind of dead, innovation-free zone around current open source practice.

We should take this opportunity to examine why partisans feel compelled not just to guard the walls of their definitions, but to sortie against anything that comes close.

# Flatland

We often speak of software in terms of _open_ or _closed_, as if all software lay along one straight line:

```
closed                                           open
├───────────────────────────────────────────────────┤
proprietary                               open source
software                                     software
```

On that line, we could further subdivide free and open source software into _permissive software_ under terms like MIT, BSD, and Apache, and _copyleft software_ under terms like GPL, MPL, and EPL.  How you order those subtypes depends on your politics.  

Software freedom advocates describe copyleft software as not just open, like permissive software, but locked open, in that it can't be put into proprietary software, at least in particular ways.  In their view, additional conditions make copyleft software more open than permissive software:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                    permissive    copyleft
software                         software    software
```

Conversely, permissive-license advocates, often associated with the BSD school, see the share-alike conditions of copyleft licenses as restrictions on what can be done with the software.  Since permissive software is less restricted than copyleft software, permissive software is more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                      copyleft  permissive
software                         software    software
```

The one-dimensional view of open source correctly renders this, the classic debate _within_ free and open source software.  But like a cartoon, this one-dimensional view massively oversimplifies, in order to emphasize.  We can make it fail just by asking where to plot _source-available software_: software for which source code is available, but without any permissive or copyleft license.

# Topography

To render source-available software's relationship to permissive, copyleft, and proprietary software, we need both dimensions that affect our ability as programmers to use and reuse software:

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

Perpendicular, intersecting lines of availability and permission run like warp and weft through the whole history of software.

Consider RMS' parable of the malfunctioning printer.  RMS is a programmer.  He could have fixed the busted printer's software.  But he never got the chance.  First because he couldn't get the source code.  The manufacturer wouldn't make it available to him.  Second because even if he had got the source code, perhaps by a leak from an employee at the manufacturer, the manufacturer wouldn't have given him permission to fix it, or to share his fix with others.  To fix the printer's software, RMS needed both source and permission to work with it.  Source code without permission wouldn't do, and neither would permission without source code.

We see the same two dimensions in the Open Source Definition, adapted from the Debian Free Software Guidelines.  The Definition begins:

> Open source doesn't just mean access to the source code. The distribution terms of open-source software must comply with the following criteria: ...

It isn't enough to use distribution terms, otherwise known as a license, that meets the criteria.  The license has to apply to source code we can get our hands on.

The choice of the term "open source", and attempts to trademark it, run into trouble precisely because "open source" has natural meaning in just one dimension, but tries to cover two.  The phrase "open source software" is plain, common English for software with source that is open, as in available.  "Open" doesn't naturally say anything about permission to modify, distribute, and so on, though that's just as essential.  So activists have spent twenty years repeating over and over that software isn't open source software just because its source is open.

<!--In this, at least, there is progress.  The phrase "free software" also has a common, natural meaning.  But it's in the wrong dimension---price---and free doesn't necessarily describe free software in that dimension.  The _L_ for _libre_ in FLOSS tries to correct this misstep.  Nobody wants to write FLOSARGS for "free/libre or open-source and all-rights-granted software".-->

# Terra Cognita

Commons Clause, the Lerna exclusion, and the public licenses for License Zero, [Parity](https://licensezero.com/licenses/parity) and [Prosperity](https://licensezero.com/licenses/prosperity), demonstrate that developers can vary availability and permission for their software independently.  You can make your source code public without giving everybody every permission to work with it.  Mixing and matching has important practical and business ramifications.  But each of these new licensing tools works fine with fully available source code, published and shared on the same platforms, with the same tools, as open source.  Only permission differs, in different ways, and to different extents.

Commons Clause and Prosperity depart from open source orthodoxy by restricting certain kinds of commercial use.  In that, they serve the same roles as noncommercial licenses published by Creative Commons, which offers a full spectrum of public licenses for other kinds of creative work, including permissive- and copyleft-style options.  By long tradition in free and open source software, software under terms that limit commercial use and resale aren't part of the movement.  Open source developers don't readily mix software under licenses with commercial use limits and open source in projects they publish.

Discriminatory license terms, like the Lerna exclusion, receive the same treatment.  Free and open source licenses have often imposed conditions that discriminate in a practical way against proprietary software developers.  But the community as a whole has not accepted terms that deny license terms to specific people, companies, governments, or organizations, or categories of them.  Intellectual property laws, like copyright law and patent law, give developers the legal power to do so.  But popular public licenses for software, as a rule, haven't exercised that power.

Parity differs from Commons Clause, the Lerna exclusion, and Prosperity by extending a well established and broadly accepted kind of open source licensing term: copyleft conditions.  Parity was written specifically to be an open source software license, but to go further than any open source license had gone before in demanding that users share their own software work back to the community.  In other words, to max out copyleft.

From the permissive or BSD point of view, that would make Parity the least open open-source-style license ever written.  Conversely, from the software freedom or GPL point of view, Parity's thrust could make it more open even than AGPL, by locking code open against more kinds of proprietary closure.

Here is one view of these licenses, plus The Unlicense, plotted in the _permission_ dimension only:

```
all rights                                 all rights
reserved                                   granted
├───────┼─────┼─┼──────────────┼──────┼────┤
No      Lerna │ Commons Clause Parity AGPL Unlicense
License       Prosperity
```

As it happens, some free software advocates reject Parity, but not because it requires contributing code back.  Parity requires contributing code back even if that code was written for private use, and not shared.  The Open Source Initiative has approved licenses that require contributing back private changes, but The Free Software Foundation has rejected such licenses as "non-free".

From the FSF point of view, best I can understand it, forcing contribution of private changes disqualifies a license categorically, like explicit commercial use limits or discrimination.  Best I can tell, the FSF's categorical exclusions prevent it from ever approving any license, like Parity, that would effectively close the share-alike loophole for closed-source use of developer tools.  If I could write a license that closes that loophole and meets FSF's criteria, I would.

# Istanbul, Constantinople

So in the end, there's some sin for which to condemn all these recent license approaches, however esoteric or apparently minor.  But recent history also teaches that the instinct to bite a license comes first.  The hunt for charges to press comes later.

Facebook's `PATENTS` file for React tacked terms onto a three-clause BSD license, much as Commons Clause tacks terms onto any standard license, and the Lerna team tacked terms onto MIT.  The part of Facebook's `PATENTS` file that offended the masses concerned defensive termination, a common open source license term that takes away your license if you sue others under patents.  In the end, Facebook combined terms previously known and accepted as open source, but in a new looking way.  That was enough to pose a perceived threat.

Defensive termination terms in open source licenses vary, both in how much license they take away, and when they're triggered.  Some disliked that Facebook's original defensive termination provision triggered on any legal claim trying to invalidate a Facebook patent, and applied even if Facebook sued you under patents first.  In response, Facebook updated their `PATENTS` file to address and clarify the trigger.

There are good reasons for specific companies to dislike the end result, but the approach was much in line with provisions already approved both by OSI and by the FSF, as in the Common Public License, for IBM.  Furor came all the same.  OSI approved a variant of the BSD license---there are many---with Apache-style patent language bolted on, offering Facebook a chance to kiss OSI's ring for absolution.  The social media masses, for their part, demanded MIT, a dusty, old form with no clear patent license at all.  And they got it.  Uniformity prevailed over substance, twice.

# Buffer Zones

I began by noting that the reactions to Commons Clause and the Lerna exclusion show that vocal members of the open source community seem to be more comfortable with proprietary software---unavailable source and all rights reserved---than with source-available approaches.  When a project attempts to occupy territory _between_ proprietary and open source as practiced today, it hears either that it should close its source code, or that it should revert to a standard open source license.

By vote of applause and rotten tomatoes, the wisdom of the unsolicited social media opinion seemed to hold that Redis Labs should continue development of its Redis modules in private, and that Lerna should revert to an unadorned MIT license.  One in each direction.  We can guess at grounds for the difference.  But to guess responsibly, we need a theory.

I've done my best to understand the dynamic at play.  As I've read, reread, and debated others, the concept that fits best is _buffer zone_.  Projects should retreat either to the proprietary stronghold, or to the open source camp, and leave the space between a bare, unsettled DMZ, offering clear lines of sight through which each extreme can eye the other.  Rather than simply ignore software under terms that fall outside their community walls, activists lower their gates and charge out to meet them, like encroaching armies, even if it's just three guys who landed one PR to one repo.

# Dominoes

When pressed, defenders of the open source realm tend to express very directly that these innovations pose threats to their community as they understand it.  It's often very difficult to find out why.  The theories I've been able to suss out sound in two recurring themes: _confusion_ and _efficiency_.

On the infrastructure side, confusion manifests as worry that users who come to open source will have their expectations frustrated, or fall prey to a kind of bait-and-switch.  Among the properly open source code users find through a system distribution, repository, source code host, or search platform, they may unwittingly find software they don't have permission to use in their particular way, for their particular business, or for their particular purpose.  Infrastructure-based efficiency concerns lament that even users who become aware these traps exist will have to spend substantial time looking where they step.

On license terms, beyond invocation of the Open Source Definition or the Free Software Definition, confusion concerns sound much as they would from a marketer tending a well known brand.  Experimenters shouldn't be permitted to skim value off the good name of open source.  Experiments shouldn't raise doubts about where the borders of open source or free software fall.  All for the benefit of consumers.  As for efficiency, no consumer wants another license to read.  Even if it says something new.

# Preoccupied Territory

As with many buffer zones imposed strategically, from aloft, the open source dead zone's double-troubled: the DMZ is currently inhabited territory, and social forces abhor invisible, made-up lines.  The buffer zone that some members of the community adamantly defend might fortify open source.  But as one part of the community encroaches abroad, the rest of the community embraces diversity and openness at home.

A preponderance of vital and popular open source infrastructure services of the current generation, from GitHub to npm to Travis CI, _require_ open source in only one dimension: availability.  If you're willing to publish your code, these services welcome your project, free of charge.  If you want to use the same service and tooling to work privately, you pay for that privilege.

As for what license terms apply to the work you share, the services take the licenses they need for themselves in their terms of service.  They don't rely on users to pick open source or other licenses that give the permission they need.  Neither do they police what additional permission users offer other users.  Service providers are more than happy to count even totally unlicensed code, and users who publish only source-available software, toward their stratospheric numbers, all the while flying the flag of open source more visibly than any foundation.

So with the partial exception of Stack Overflow, which poses unique problems, the most popular distributors of open source today don't make any guarantees about licensing.  It's up to users to search, filter, and audit what they find.  Distributors do provide functionality related to licensing, but only functionality to make licensing information more visible, and to facilitate independent analysis, as with software tools that process standardized licensing metadata.  In other words, current-generation open source infrastructure mitigates and encourages diversity, rather than enforcing uniformity.  Both because diversity is good for growth and business, and because enforcing uniformity means diving head first into the mire of definitional disputes, taking sides with a lot of structural power, and alienating a lot of people.

On the license side, we also see accommodation for diversity.  Standards like SPDX embrace not just FSF- or OSI-approved licenses, but public licenses of all kinds, including noncommercial and proprietary licenses.  Packaging standards tackle the problem of multiply-licensed projects, which incorporate code under a variety of terms, head on.  Many provide escape valves for specifying non-standard terms.  Meanwhile, data consuming audit tools almost universally support configuration to whitelist specific third-party artifacts, not just on determination that a standard license applies, but when use is approved on other grounds.

# GPS

...