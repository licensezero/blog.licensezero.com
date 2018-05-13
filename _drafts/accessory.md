---
title: Commons Club
description: open source as proprietary accessory, software freedom as network
layout: post
---

For software developers, today's public hand-wringing about
privacy, security, and user manipulation comes comically,
pitiably late.  Software people have long taken extra steps
when using the big online platforms, from privacy settings
to browser extensions to throwaway addresses and Tor, that
show what they know about the industry.

But we also know that's mostly theater.  We know technology,
but we might as well be plumbers, insurance brokers, or
grandma as far as other devs' apps are concerned.  Others'
apps are nearly as opaque, proprietary, and closed to us as
to anyone else.  Despite the rise of open source.

Open source software is _winning_.  Software freedom---the
power to be both developer and user of the applications that
matter to you---is not.  If there were ever a short case for
a difference, there it is.

# In Crowd

Many programmers believe that open source doesn't belong in
conversations about privacy, transparency, or end-user
choice.  They're right.  Open source chooses not to belong
in those conversations.  Free software makes a stand on
user-facing issues.  Apart from the right to _be_ a user,
open source makes a stand on user-facing issues if and only
if the users are programming.

Open source works like a club.  Within the club, there's
camaraderie, a more refined code of conduct, and
benefits---the mythified software commons.  Common practices
inside the club, like forking, happen only rarely outside
it.  Common practices outside the club, like [invasive
ads][kite], earn scorn and protest within it.

[kite]: https://github.com/atom-minimap/minimap/issues/588

Membership in the club is an exclusive privilege of
programmers.  Non-programmers benefit only by invitation,
which usually costs: time, money, privacy, or the lot.

# Accessory

That's why open source _wins_ today.  It wins, dilutely, as
accessory to proprietary software, which is winning bigger.
Open source is a tool of those winning by selling
proprietary software.  It's more efficient to build
proprietary code---social networks, marketplaces, locked-in
user communities---on open source freebies.  But it's more
profitable, prevailing wisdom says, to deny users of those
networks meaningful rights to patch, fork, and set policy. A
new app or service creates its own laity, then conspires
against it.

But isn't _all_ software these days really open source, or
heading that way?  After all, proprietary software is ever
more made of open source, and even made _like_ open source,
as innersource.  When we look at proprietary apps and
services from top to bottom, the layer of closed,
proprietary integration, application, and design code on top
of the open, common stack measures relatively shallow.  At
least technically speaking.

[usage]: https://www.blackducksoftware.com/about/news-events/releases/companies-lack-open-source-policies

[innersource]: https://en.wikipedia.org/wiki/Inner_source

But that's a distinction falling conveniently short of a
difference for users.  I can improve [Facebook's front-end
framework][react], making it easier to develop facebook.com,
and drawing in more developers Facebook might like to hire
for the job.  I can optimize [LinkedIn's database][kafka],
making linkedin.com cheaper to run, and fewer tickets for
LinkedIn staff to handle.  But Facebook isn't a front-end
framework, and LinkedIn isn't a database.

[react]: https://reactjs.org

[kafka]: https://kafka.apache.org

Not really.  Not even close.  Even if sloughing away all the
open source leaves but a thin residue of proprietary code,
that code implements the choices that meaningfully affect
users, that defines user' relationships to the owner and
each other.  Patches to that layer, to the network itself,
aren't welcome.  Patching is network-owner prerogative.

# Network Power

Network-owner prerogative is a pervasive kind of power.
Networks are value propositions like any other.  Lots of
valuable users make a beneficial network, and that benefit
can overwhelm the cost of an irksome or incompetent
facilitator.  So we'll abide a creepy social network to
socialize with the right people.  And we'll abide a shifty
marketplace to buy the right product at the right price.
We'll even abide social networks and market makers who get
creepier, shiftier, or simply more bungling over time, as
long as network effects stack up faster than the owner goes
downhill.

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
writes.  Even software that ends up crunching data about
software freedom advocates without their knowing it.  It
affects incentives for nearly anyone writing software in a
domain touched by the network.  The cost, if any, is
respecting end-user freedom.  The benefits outweigh it.

# Past

Copyleft-based software freedom was a sound network play,
and it achieved significant network-level results.  It's
also succumbing to the signature crumbling decadence of
networks: backward-looking hubris.  When network
participants mire down in reverence for past
accomplishments, secure in the thought that their network is
too big not to matter forever, we dub them _incumbents_. And
we wait.

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
native binaries.

[LLVM]: https://llvm.org

[Fuschia]: https://en.wikipedia.org/wiki/Google_Fuchsia

[Go]: https://golang.org

# Present

That dynamic partially explains why pillars of the copyleft
network feel ever more like legacy systems.  That's not to
say stagnant or doomed.  Far from it: GPL software remains
much of the most mature and battle-tested, with the broadest
supporting constituencies.  But the content of `LICENSE` no
longer seems to define those projects or their successes, if
it ever did.  It dates them.

A combination of factors conspire against free software
esprit de corps.  For one, the licenses don't really seem to
work any more.  The ASP loophole, which allowed creators of
proprietary software services to avoid the requirement to
share source code under copyleft licenses, especially GPLv2,
represented a practical vulnerability.  FSF patched it in
AGPL, but failed to merge to mainline, bringing GPL and AGPL
together as GPLv3, in part due to threats to fork
development of existing GPLv2 projects.  We're left with
GPLv3, suffering a known, unpatchable vulnerability, and
AGPLv3, a separate license under a separate name that can be
identified, isolate, scorned, and banned as an extremist
excursion, rather than a necessary evolution.

Meanwhile, the ASP business model, rebranded "Software as a
Service", exploded again.  As did proprietary use of
software development tools, which slide through a loophole
no GPL has ever tried to close.  That left many software
developers who'd otherwise leverage their work for software
freedom without a public license tool perceived as vital and
effective.

Licenses without teeth---and a lot of unhelpful
complexity---don't make or keep strong reputations in the
field.  In time, those reputations fermented into a widely
held, ahistorical belief that licensing _can't_ effectively
express or protect software freedom values.  That not just
open source doesn't belong in conversations about software
freedom, but that even copyleft and other reciprocal
licenses don't really belong, either.

# Future

Over time, we should expect a repeating pattern of
permissively licensed software, funded or blessed by
industry, cloning or replacing software first proven by
developers who care about software freedom.  Share-alike
licenses impose some additional friction over permissive
licenses, by their nature.  When a concept is proven, demand
for similar functionality under lower-friction terms
increases, and lower friction terms themselves bestow
marginal competitive advantage.  MySQL and PostgreSQL often
come to mind.

The free software movement was born cloning proprietary
software, and refining its clones.  When permissive software
can as easily clone copyleft software, the software freedom
network can't expect survive with vitality in a permanent
defensive position.  Rather, software freedom has to stay at
the front lines, pushing the state of the art, and offering
developers a compelling proposition: enjoy the state of the
art, on an ongoing basis, but respect user rights as you do.

Part of that project is making sure software freedom's tools
remain state of the art.  That means reassessing licenses
and norms about sharing and consuming code with others. [The
License Zero Reciprocal Public
License](https://licensezero.com/licenses/reciprocal) closes
loopholes, reduces legalese, and reflects what we've learned
about public licensing in the last ten years.

Reciprocally licensed, permissively licensed, and
proprietary software compete with one another.  It's equally
important to acknowledge and embrace that competition.  By
encouraging those advancing the state of the art to stand up
for user rights in their licensing choices. By building out
infrastructure, support networks, and methods to make free
software programs and services viable competitors to both
permissive and proprietary alternatives.
