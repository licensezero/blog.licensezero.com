---
title: Open Source Border Control
layout: post
---

Two new licensing ideas, two new licensing dramas.  [Commons Clause](https://commonsclause.org) patches existing open source licenses, limiting commercial use and resale.  [Lerna](https://github.com/lerna/lerna/blob/19a7f5d4bd88b9cc50b603adcf171623227ec554/LICENSE) added a preamble to their license to prevent it applying to a list of companies contracting for US Immigration and Customs Enforcement, then reverted their protest gesture under protest by angry developers.

As terms, Commons Clause and Lerna-style exclusions fill small niches, and matter little in the grand scheme.  Many companies fork their own open projects, continuing development as proprietary software.  But relatively few of those continue developing in the open, or want to allow the specific, narrow kind of free commercial use that Commons Clause permits.  Corporate bad behavior offends many a conscience.  But relatively few developers will pick that battle in `LICENSE`.  Or frankly, do anything at all.

As lessons in open source politics, however, both Commons Clause and Lerna teach a great deal.  And what they teach is deeply disturbing.  Each extends two developing trends:

1. Open source rallies more dramatically against new licensing and development approaches that are too close to open source orthodoxy for their comfort than to closed and proprietary software, on the other end of the spectrum.  Make proprietary software with open source, the community will honor your choice.  Offer open source terms, but not to everyone, or offer somewhat different terms, and the pious will flood your social media with scorn.
2. Incorrect legal statements, flawed legal reasoning, and the imputed legal soundness of foundation-blessed policy positions create fear, uncertainty, and doubt in developers without legal support of their own.  Bombardment by misinformation and uncertainty leaves a false impression that's often the inverse of law and policy in actual effect.

Both Commons Clause and Lerna could have done far better to minimize needless drama and confusion.  But anyone trying something new in the community, even carefully, should expect heat.  As an attorney, legal misinformation and empty legal threats worry me most.  But the more pressing issue, for anyone attempting to solve urgent problems with the distributed, individual power of licensing terms, is the insistence on a kind of dead, innovation-free zone around current open source practice.

We should take these recent opportunities to examine that reticence.

# The Lay of the Land

We often speak of software in terms of _open_ or _closed_, as if all software lay along one continuum:

```
closed                                           open
|---------------------------------------------------|
proprietary                               open source
software                                     software
```

On that line, we could further subdivide free and open source software into _permissive software_ under terms like MIT, BSD, and Apache, and _copyleft software_ under terms like GPL and EPL.  How those subtypes relate on the spectrum depends on your politics.  

Software freedom advocates describe copyleft software as not just "open", like permissive software, but "locked open", in that it can't be put into proprietary software, at least in particular ways.  In their view, additional conditions make copyleft software more open than permissive software:

```
closed                                           open
|---------------------------------------|-----------|
proprietary                    permissive    copyleft
software                         software    software
```

Conversely, permissive-license advocates, often associated with the BSD school, see the share-alike conditions of copyleft licenses as restrictions on what can be done with the software.  Since permissive software is less restricted than copyleft software, that makes permissive software the more open:

```
closed                                           open
|---------------------------------------|-----------|
proprietary                      copyleft  permissive
software                         software    software
```

The one-dimensional view of open source expresses this, the classic debate _within_ free and open source software.  But like a cartoon, this one-dimensional view oversimplifies reality, and the way free and open source software fit within it.  We can reach its limit by asking where to plot _source-available software_: software for which source code is available, but without any permissive or copyleft license.

To plot source-available software, we need both of the dimensions that affect our abilities to use and reuse software: _availability_ of source in the preferred form for making changes, from open to closed, and _permission_, from all-rights-reserved to all-rights-granted.

```
                    │source              
                    │open                
                    │                    
    source          │     open source    
    available       │     software       
    software        │                    
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

<!--Within the quadrants for proprietary and open source software, we could plot specific projects at different points along the two axes.  Some open source software licenses grant more rights than others.  Some open source code is easy to find online, while some is not.-->

Availability and permission run like warp and weft through the history of software.

Consider RMS' parable of the malfunctioning printer.  RMS is a programmer.  He could have fixed the printer's software.  But he never got the chance.  First because he couldn't get the source code.  The manufacturer wouldn't make it available to him.  Second because even if he had got the source code, perhaps by a leak from an employee at the manufacturer, the manufacturer wouldn't have given him permission to fix it, or to share his fix with others.  To fix the printer's software, RMS needed both source and permission to work with it.  Source code without permission wouldn't do, and neither would permission without source code.

We see the same two dimensions in the Open Source Definition, adapted from the Debian Free Software Guidelines.  The Definition begins:

> Open source doesn't just mean access to the source code. The distribution terms of open-source software must comply with the following criteria: ...

It isn't enough to use distribution terms, otherwise known as a license, that meets the criteria.  The license has to apply to source code that's available.

The choice of the term "open source", and attempts to trademark it, run into trouble precisely because "open source" has natural meaning in just one dimension, but tries to cover two.  The phrase "open source software" is plain, common English for software with source that is open, as in available.  "Open" doesn't naturally say anything about permission to modify, distribute, and so on, though that's just as essential.

In this, at least, there is progress.  The phrase "free software" also has a common, natural meaning.  But it's in the wrong dimension---price---and free doesn't necessarily describe free software in that dimension.  The _L_ for _libre_ in FLOSS tries to correct this misstep.  Nobody wants to write FLOSARGS for "free/libre or open-source and all-rights-granted software".

# Mapping New Places

Commons Clause, the Lerna exclusion, and the public licenses for License Zero, [Parity](https://licensezero.com/licenses/parity) and [Prosperity](https://licensezero.com/licenses/prosperity), demonstrate that the availability and permission dimensions of software vary independently.  Mixing and matching has important practical and business ramifications.  But each of these new licensing tools is designed to work with fully available source code, published and shared on the same platforms, with the very same tools.  Software under these new terms departs from open source orthodoxy only in permission granted.

Commons Clause and Prosperity depart from open source orthodoxy by restricting certain kinds of commercial use.  In that, they serve the same roles as noncommercial licenses published by Creative Commons, which offers a full menu of licenses, including permissive- and copyleft-style options.  By long tradition in free and open source software, software under terms that limit commercial use and resale aren't part of the movement.  Open source developers don't readily mix software under licenses with commercial use limits and open source in projects they publish.

Discriminatory license terms, like the Lerna exclusion, receive the same treatment.  Free and open source licenses have often imposed conditions that discriminate in a practical way against proprietary software developers.  But the community as a whole has not accepted terms that deny license terms to specific people, companies, governments, or organizations, or categories of them.  Intellectual property laws, like copyright law and patent law, give developers the legal power to do so.  But community licenses, as a rule, haven't exercised that power.

Parity differs from Commons Clause, the Lerna exclusion, and Prosperity by extending a well established kind of licensing term---copyleft conditions---to a logical extreme.  Parity was written specifically to be an open source software license, but to go further than any open source license had gone before in demanding that users share their own software work back to the community.

From the permissive or BSD point of view, that would make Parity the least open open-source-style ever written.  Conversely, from the software freedom or GPL point of view, Parity's thrust could make it more open even than AGPL, by locking code open against more kinds of proprietary closure.

Here is one view of the licenses discussed so far, plotted along the _permission_ dimension only:

```
all rights                                 all rights
reserved                                   granted
|-------|-----|-|--------------|------|----|
No      Lerna | Commons Clause Parity AGPL Unlicense
License       Prosperity
```

As it happens, some free software advocates reject Parity on different grounds: Parity requires contributing code back even if that code was written for private use, and not shared.  The Open Source Initiative has approved licenses that require contributing back private changes, but The Free Software Foundation has rejected such licenses as "non-free".

# Buffer Zones

I began by noting that the reactions to Commons Clause and the Lerna exclusion show that vocal members of the greater community seem to be more comfortable with proprietary software, closed source and no rights granted, than with source-available approaches.  In other words, when a project takes a position _between_ proprietary software and orthodox open source software, on either underlying dimension, the project tends to hear either that it should close its source code, or that it should revert to a standard open source license.  Nobody seems to shout loudly that the project should go ahead and experiment in new territory, to see if it works.

Thus, by vote of applause and rotten tomatoes, the wisdom of the unsolicited social media masses seemed to hold that Redis Labs should continue development of its Redis modules in private, or at least fork its own projects to different repos, to mark the taking-off points for work under new terms, and that Lerna should revert to an unadorned MIT license.  One in each direction.  We can theorize grounds for the difference.  But to theorize, we need a theory.

I've done my best to understand the dynamic at play.  As I've read, reread, and debated others, the _buffer zone_ has risen to the top of the metaphor pile.

Both in terms of where free and open source software gets done, especially its Internet infrastructure, and in terms of license conditions, open source advocates aren't satisfied to guard the border walls of their movements, be they definitions, stated principles, or shared norms.  On spotting any credible or even feeble threat within sight of their walls, some open source advocates draw down the gate and charge on horseback to meet it and either chase it away or stab it dead.  Rather than simply ignore software under terms that fails to meet their standards, or to avoid incorporating it into their own projects, they set out to eliminate it, like a heresy.

When pressed, defenders of the open source realm tend to express very directly that these innovations pose threats to their community as the understand it, even if its walls remain strong.  To my ear, concerns nearly always sound in a theme of _confusion_ or of _efficiency_.

On the infrastructure side, confusion manifests as worry that users who come to open source will have their expectations frustrated, or fall prey to a kind of bait-and-switch.  Among the properly open source code they find through a system distribution, repository, source code host, or search platform, they may unwittingly find software they don't have permission to use in their particular way, for their particular client, or for their particular purpose.  Infrastructure-based efficiency concerns lament that even users who become aware of these pitfalls will have to spend substantial time assessing what they find, to make sure it is what they hope it is, or were told to expect.

On license terms, often framed within the Open Source Definition or the Free Software Definition, confusion concerns sound much as they would from a marketing man concerned for a well known brand he minds.  Experimenters shouldn't be permitted to skim value off the good name of open source.  Experiments shouldn't raise doubts about where the borders of open source or free software lie, for the benefit of consumers.  As for efficiency, no consumer wants another license to read.

# Preoccupied Territory

As with many border zones drawn abstractly, from afar, the trouble is what's already there, and that natural and social forces tend to ignore straight lines.  The buffer zones that some members of the community adamantly defend might do well for open source, were they respected.  But as one part of the community repulses all encroachments on one front, other parts of the community practice open borders at the rear.

A preponderance of vital and popular open source infrastructure services of the current generation, from GitHub to npm to Travis CI, _require_ open source in only one dimension: availability.  If you're willing to publish your code, the service stands open to your project, free of charge.  If you want to use the same service and tooling to work privately, you pay for that privilege.

As for what license terms apply to the work you share, the services take the licenses they need for themselves in their terms of service.  They don't rely on you to pick a license that gives them the permission they need.  Neither do they police what terms to offer to others.  They are more than happy to count even totally unlicensed code, and users who publish only unlicensed code, toward their stratospheric, growing numbers.

With the partial exception of Stack Overflow, which poses unique problems, the most popular sources of open source today don't make any guarantees about licensing.  It's up to users to search, filter, and audit what they find.  The platforms do provide functionality related to licensing, but only functionality to make licensing information more visible, and to facilitate independent analysis, as with software tools that process standardized licensing metadata.  In other words, the current generation of platforms has emphasized software tooling to cope with diversity, and to some extent encouraging well accepted choices, instead of enforcing uniformity.

On the license side, we also see diversity embraced.  Standards like SPDX define identifiers not just for FSF- or OSI-approved licenses, but for licenses of various kinds, including noncommercial licenses.