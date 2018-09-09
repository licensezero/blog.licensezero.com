# Overture

Before GitHub, open source, and free software, before even hacks and hackers and hacking as we know them, there has always been a movement of computer people demanding something back from the industry. Hackers and hobbyists wanted community. Academics wanted collaboration. Craftsmen wanted reputation. Free software wanted purpose. Open source, having inherited community, collaboration, reputation, and purpose, wanted to keep those things, but also wanted acceptance back into the corporate fold. And got it.

Having met its own definition of success, open source can no longer call itself a counterculture. Self-styled opposites---closed, proprietary software, on the one hand, and open, permissive software, on the other---now operate in symbiosis, at least for those who bought in from a position of strength.

If that includes you, these are heady days, with fulfillment aplenty, and money to boot. If that doesn't include you, you may have good reason, like those before you, to demand something back from the industry, open source now included. Perhaps accountability for corporate misconduct. Perhaps respect for users. Perhaps patches back, or a fair wage.

But do you have the means to get it?

# Conflict

React, Redis, Lerna. Three license tiffs in less than one year. Each reaffirming a troubling trend in open source politics: eroding respect for contributors' rights to choose the terms that apply to their work. Eroding respect for the very lever the law gives individuals to demand something back from bigger interests for their work.

Taking licensing power out of developers' hands sets the community police on a collision course with those solving practical community problems. Practical problems that include financial inequity and the erosion of copyleft. Solutions that include License Zero, with licenses like [Prosperity](https://licensezero.com/licenses/prosperity) and [Parity](https://licensezero.com/licenses/parity).

I'll be frank. Facebook's `PATENTS` file, Commons Clause, and Lerna-style blacklists don't matter that much, in the grand scheme. They address niche concerns, and few others will want to use them. But you wouldn't know that from the reaction.

The purported existential threat to open source from these experiments can have little to do with the practical effects of the changes. It has everything to do with the power to make changes being exercised. For some, the very prospect of license innovation harms open source, as they define it. That being the case, it isn't enough to defend a definition, proclaim whether new licenses meet it, and avoid those that don't. If a new approach falls outside, and especially if it falls _just_ outside, what's acceptable, a preemptive attack must be launched to rebuke it, reverse it, and if at all possible, eliminate it from the field of developer choice. Even if that means telling an open project to "just go proprietary", and actually close their source.

As I've followed responses to React, the Redis modules, and Lerna, I've been most disturbed by the use of legal fear, uncertainty, and doubt to cow developers experimenting with their rights. As a lawyer, those tactics offend me, morally. I have to say that, and I'm not done writing about it. But in the end, appeal to fear is just a tactic, incidental to the broader program.

The broader program leads to a disciplined, two-party system that constrains developer choice to market-optimized "proprietary", at one extreme, or community-policed "open", at the other, with nothing between. Within that system, third parties, especially third parties that take positions near to one or the other major party, threaten to split attention, loyalty, and credit for benefits away from the incumbents. At a higher level, third parties threaten the ability of the bipartite system to claim effective representation of the whole community, despite failing to address widely held needs.

Projects that make source available, but effectively hold back permission, like permission for commercial, closed-source, or unethical use, prove that you don't have to buy the whole orthodox open source line to share and build code publicly, online. Public code without the rest of the program brings many, many of the benefits currently held out out as exclusive to open source under licenses like MIT. Moreover, you needn't rely on any other organization's help or approval to prepare and approve your terms. The political-system metaphor breaks down, because you don't need anyone to represent you. Licensing gives you individual power, and how you use it is your individual choice.

In the end, license experiments _are_ a threat. But the threat isn't to open source in and of itself: your choice to "patch" MIT doesn't change how effective standard MIT terms are for other work. Rather, the threat is to the symbiosis of open source and proprietary software institutions. Holding permission back reduces what those holding themselves out as open source shepherds can offer to proprietary industry. Offering a compelling middle way will reduce the number of projects that end up under pushover licenses, ready for proprietary assimilation, for lack of a better choice.

# Spectrum

The broad program of diametric choice is not always a matter of explicit policy. It doesn't have to be. The way that free and open source software advocates have learned to talk about free and open source software---mostly by talking amongst themselves, long before industry was interested---reinforces the dichotomy. Third options and new approaches buck that vocabulary, and threaten the accompanying mindset. To have a better conversation, we need a better vocabulary.

Open source community members often speak in terms of _open_ or _closed_, as if all software lay along one straight line:

```
closed                                           open
├───────────────────────────────────────────────────┤
proprietary                               open source
software                                     software
```

On that line, we could split open source into _permissive software_ under terms like MIT, BSD, and Apache, and _copyleft software_ under terms like GPL, MPL, and EPL.  Where to plot them depends on your politics.

Software freedom advocates describe copyleft software as not only open, like permissive software, but locked open, unable to be put in proprietary software.  In their view, these additional license rules make copyleft the more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                    permissive    copyleft
software                         software    software
```

Conversely, permissive-license advocates, sometimes called the BSD school, see the share-alike rules of copyleft licenses as restrictions on what can be done with software.  Permissive software comes with fewer rules. That makes permissive the more open:

```
closed                                           open
├───────────────────────────────────────┼───────────┤
proprietary                      copyleft  permissive
software                         software    software
```

The one-dimensional view of open source correctly renders this, the classic debate _within_ free and open source software.  But like a cartoon, this one-dimensional view oversimplifies to make large of small differences.  We start to reveal what this view hides by asking where to put _source-available software_: software for which source code is available, but under different license terms, not permissive or copyleft.

In terms of whether we can find source code, open source software and source-available software are near neighbors.  In terms of the permission we have to work with the software, proprietary software and source-available software are near neighbors.  That puts source-available software somewhere between proprietary and open source, but for two different reasons.

# Compass

To render source-available software's relationship to permissive, copyleft, and proprietary software faithfully, we need a dimension for each of those reasons:

1. _availability_ of source in the preferred form for making changes, from completely open to completely closed
2. _permission_ to work with source code available to us, from rights-reserved to public-domain

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
rights              │
reserved            │
                    │
         closed     │     public
    proprietary     │     patent
       software     │     grants
                    │
              source│
              closed│
```

Because these intersecting lines of availability and permission affect programmers' ability to work with software, they run like warp and weft through the whole history of the software industry.

Consider RMS' parable of the malfunctioning printer.  RMS could have fixed the printer's software.  But he never got the chance.  First because he couldn't get the source code.  The manufacturer wouldn't make it available to him.  Second because even if he had got the source code somehow, the manufacturer wouldn't have given him permission to fix it, or to share his fix with others.  To fix the printer's software, RMS needed both source and permission to work with it.  Source code without permission wouldn't do, and neither would permission without source code.

We see the same two dimensions in the Open Source Definition, adapted from the Debian Free Software Guidelines.  The Definition begins:

> Open source doesn't just mean access to the source code. The distribution terms of open-source software must comply with the following criteria: ...

It isn't enough to use distribution terms, otherwise known as a license, to meet the criteria.  The license has to apply to source code Debian can actually get its hands on.

Of course, both dimensions are in full effect with traditional proprietary software, as well.  A software company collects all rights in its products, through intellectual property agreements with employees and contractors.  Those terms also require personnel to keep technology, including source code, secret.  Software only travels from vendor to customer under specific, very limited licenses, and then often only in compiled or obfuscated form.  The combination ensures minimum availability and maximum rights reserved, making the vendor the only efficient source not just for licenses and copies, but maintenance, improvements, and support, as well.