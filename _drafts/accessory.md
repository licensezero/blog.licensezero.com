---
title: Commons Club
description: open source as proprietary accessory
layout: post
---

Today's public hand-wringing about privacy, security, and
user manipulation comes comically, pitiably late.  Software
people have long taken extra steps when using the big online
platforms, from privacy settings to browser extensions to
throwaway addresses and Tor, that show what they know about
the industry.  But they also know all of that's mostly
theater.  Developers know technology, but they might as well
be plumbers, insurance brokers, or grandma---in a word,
marks---as far as other devs' apps are concerned. That's
more and more true, even as more and more software gets made
with open source.

Open source software is _winning_.  Software freedom---the
power to be both developer and user of the applications that
matter in your life---is not.  If there were ever a short
case for a difference, there it is.

Those of us looking beyond our own developer experiences to
those of all the folks affected by software need to take
stock of how we got here, and think strategically about what
to do next.

# In Crowd

Many programmers believe that open source doesn't belong in
conversations about privacy, transparency, or end-user
choice.  They're right.  Open source chooses not to belong.
Free software takes a stand on user-facing issues. Open
source takes a stand on user-facing issues, beyond the right
to _be_ a user, only when users happen to be programmers.

That makes open source a club.  Within the club, there's
camaraderie, a more refined code of conduct, and
benefits---the mythified software commons.  Everyday
practices outside the club, like invasive ads and expecting
pay for work, are strongly discouraged within it.  But
membership is extended exclusively to programmers.
Non-programmers benefit only by member invitation.
Invitations usually cost time, money, privacy, or the lot.

[kite]: https://github.com/atom-minimap/minimap/issues/588

# Accessory

That's why open source _wins_ today.  It wins, dilutely, as
accessory to proprietary software, which is winning bigger.
It's more efficient to build proprietary code---social
networks, marketplaces, locked-in user communities---on open
source freebies.  But it's more profitable, so they say, to
deny users of those networks meaningful rights to patch,
fork, and set policy. Each new app conspires to create its
own laity.

But isn't _all_ software these days really open source, or
heading that way?  After all, proprietary software is ever
more made of open source, and even _like_ open source, as
innersource.  When we look at proprietary apps and services
from top to bottom, the layer of closed, proprietary
integration, application, and design code on top of the
stack---often open and common---measures relatively thin. At
least technically speaking.

[usage]: https://www.blackducksoftware.com/about/news-events/releases/companies-lack-open-source-policies

[innersource]: https://en.wikipedia.org/wiki/Inner_source

But that's a distinction falling conveniently short of a
difference for non-technical people.  I can improve
[Facebook's framework][react], making it easier to develop
facebook.com, and drawing in more developers Facebook might
like to hire for the job.  I can optimize [LinkedIn's
database][kafka], making linkedin.com cheaper to run, and
fewer tickets for LinkedIn staff to handle.  But Facebook
isn't a front-end framework, and LinkedIn isn't a database.

[react]: https://reactjs.org

[kafka]: https://kafka.apache.org

Not really.  Not even close.  Even if sloughing away all the
open source leaves but a thin film of proprietary code, that
code implements the choices that meaningfully affect users.
Patches to that layer, to the network itself, aren't
welcome.  Patching is network-owner prerogative, whether it
affects users' relationships to users or users'
relationships to the owner.

# Network Power

Network-owner prerogative is a pervasive kind of power.
Networks are value propositions like any other, but network
owners work more like brokers than retailers.  Lots of
valuable users make a beneficial network, and that benefit
can overwhelm the cost of an irksome or incompetent broker.
We'll abide a creepy social network to socialize with the
right people.  We'll abide a slimy marketplace to buy the
right product at the right price.  We'll even abide social
networks and market makers who get creepier, slimier, and
clumsier over time, as long as network effects stack up
faster than the owner gets worse.

_Network effect_ is Valley Speak, not a hacker term.  But
software freedom advocates bid consciously for network
effect, explicitly to benefit end-user rights, in 1989. That
was GPLv1:

> The license agreements of most software companies try to
> keep users at the mercy of those companies.  By contrast,
> our General Public License is intended to guarantee your
> freedom to share and change free software---to make sure
> the software is free for all its users.

In specific domains, newer GPLs still reign.  It's easier to
port GCC to your new architecture than to write a compiler
from scratch, even if you think RMS is nuts.  It's easier to
tweak WordPress than to seed you own blog-platform
community, even if copyleft gives you migraines.  The
freedom-indifferent abide GPL politics and GPL legal for
free code and documentation all the time.  Even as old hands
get nuttier and license combinatorics explode.

That is exactly the promise of network power.  A free
software network affects not just the software that freedom
advocates write or choose to use, but software that anyone
writes, and software that ends up chewing data about
software freedom advocates without their knowing it.  It
affects incentives for nearly anyone writing software in a
domain touched by the network, even managers openly hostile
to software freedom.

# Past

Copyleft-based software freedom was a sound network play,
and it achieved network-level results.  It's also succumbing
to the signature crumbling decadence of networks, too:
backward-looking hubris.  When network owners mire down in
reverence for past accomplishments, secure in the thought
that their network is too big not to matter forever, we dub
them _incumbents_.  And we wait.

It's famously easy to topple unwary incumbents in software.
Marginal costs are low, and with patents again in decline,
it's relatively easy to clone, reimplement, and otherwise
run with whatever you find.  That dynamic bites software
networks of all kinds, open and proprietary.  Techniques,
standards, conventions, and usability lessons from GCC or
Linux end up not just in proprietary compilers and kernels,
but also permissively licensed, freedom-indifferent
alternatives like [LLVM] and [Fuschia]. Entire toolchains
get rebuilt from scratch, as with [Go], which compiles
native binaries without external libraries, all under
permissive terms.

[LLVM]: https://llvm.org

[Fuschia]: https://en.wikipedia.org/wiki/Google_Fuchsia

[Go]: https://golang.org

# Present

That dynamic partially explains why so many pillars of the
GPL network feel ever more like legacy systems.  That's not
to say stagnant or doomed.  Far from it: GPL software
remains much of the most mature and battle-tested, with the
broadest supporting constituencies.  But a combination of
factors conspire against the movement.  The license terms
for those projects ever more seem to date them.

Nearest to my interest is license obsolescence.  The ASP
loophole, which allowed creators of proprietary software
services to avoid the requirement to share source code under
copyleft licenses, especially GPLv2, was legally awkward to
close by nature.  FSF closed it in AGPL, but failed to merge
AGPL and GPL in GPLv3, in part due to fork threats to keep
development of existing GPLv2 code under those more
permissive terms.  We now have a GPLv3 with a known loophole
and an AGPLv3 that's very easy to isolate, ban, and scorn.

Meanwhile, the ASP business model, rebranded "Software as a
Service", exploded again.  As did the use of small software
libraries and development tools, which slide through
loopholes neither GPL closes.  The situation left many
staunch software freedom advocates without an effective
public license.  Licenses without teeth---and a lot of
unhelpful complexity---don't acquire strong reputations in
the field.

# Future

Over time, we should expect a repeating pattern of
permissively licensed software, funded or blessed by
industry, cloning or replacing and refining tools first
popularized under copyleft terms.  Copyleft licenses impose
some additional friction over permissive licenses, by their
nature.  When a concept is proven, demand for lower-friction
terms increases, and lower friction itself creates a
competitive advantage.  For reference: MySQL and PostgreSQL.

Software freedom advocacy in software development cannot
depend on reinforcing its bulwarks to remain relevant and
continue to exerting network power for end-user rights.  It
must hold a position---a moving position---at the knife's
edge of the state of the art.  Free software was born
cloning proprietary programs.  It can't survive that way,
with proprietary software companies paying to reimplement
copyleft work as permissive open source.

<!-- TODO: Strengthen licenses. L0-R -->

<!-- TODO: competition. open source apps -->
