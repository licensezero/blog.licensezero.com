---
title: Commons Club
description: open source as accessory, copyleft as network
layout: post
---

For fellow software developers, today's public hand-wringing
about privacy, security, and user manipulation comes
comically, pitiably late.  The tech-savvy have long taken
extra steps when using the big online platforms, from
privacy settings to browser extensions to Tor.  Those steps tell
what insiders know about their industry.

But the tech-savvy also know that it's a losing fight.
We're tracked, profiled, and hacked all the same.  We know
technology, but we might as well be plumbers, insurance
brokers, or grandma as far as other devs' apps are
concerned.  They're about as opaque to us as to anyone else.
Quite despite the rise of open source.

Open source software is _winning_.  Software freedom---the
power to be both developer and user of the applications that
matter to you---is not.  If there were ever a short case for
a difference, there it is.

# Commons

Many programmers believe that open source doesn't belong in
conversations about privacy, transparency, or end-user
choice.  They're right.  Open source chooses not to belong
in those conversations.  Free software takes a stand on
user-facing issues like transparency, access to code, and
modification.  Apart from the right to _be_ an end-user,
open source takes a stand on user-facing issues if and only
if the users happen to be programmers.

That makes open source something of a club.  Within the
club, there's camaraderie, a more refined code of conduct,
and benefits---the mythified software commons.  Common
practices inside the club, like forking, happen only rarely
outside it.  Common practices outside the club, like
invasive ads, earn scorn and protest within it.  Membership
in the club is an exclusive privilege of programmers.
Non-programmers benefit only by invitation, which usually
costs: time, money, privacy, or the lot.

[kite]: https://github.com/atom-minimap/minimap/issues/588

# Accessory

That's why open source _wins_ today.  It wins, dilutely, as
accessory to proprietary software, which is winning bigger.
It's more efficient to build proprietary code---social
networks, marketplaces, locked-in user communities---on open
source freebies.  But it's more profitable, prevailing
wisdom says, to deny users of those networks meaningful
rights to set policy, guide development, or defect.  As
standard operating procedure, a profitable app or service
creates its own laity, so it can conspire against it.

But isn't _all_ software these days really open source, or
heading that way?  After all, proprietary software is ever
more made of open source, and even made _like_ open source,
as innersource.  When we look at proprietary apps and
services as a whole, the layer of closed, proprietary
integration, application, and design code on top of the
open, common stack often measures relatively shallow.  At
least technically speaking.

[usage]: https://www.blackducksoftware.com/about/news-events/releases/companies-lack-open-source-policies

[innersource]: https://en.wikipedia.org/wiki/Inner_source

But that's a distinction falling conveniently short of a
user difference.  I can improve [Facebook's front-end
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
users, that define user' relationships to the owner and each
other.  Patching that implementation, the network itself, is
network-owner prerogative.

# Network

Network-owner prerogative is a pervasive kind of power.
Networks are value propositions, but the one making the
proposition isn't the one making most of the value.  Rather,
lots of valuable users make a beneficial network.

That collective benefit can overwhelm the cost of even an
irksome or incompetent facilitator.  So we'll abide a creepy
social network to socialize with the right people. And we'll
abide a shifty marketplace to buy the right product at the
right price. We'll even abide social networks and market
makers who get creepier, shiftier, or simply bungle over
time, as long as network effects stack up faster than the
ambiance takes a dive.

_Network effect_ is Valley Speak, not a hacker term.  But
software freedom advocates bid consciously for network
effect, explicitly to benefit end-user rights, in 1989.
Quoth GPLv1:

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
get nuttier and license combinatorics explode.  Even though
giving users code and a license meaningfully shifts the
balance power.

That is exactly the promise of network power.  A free
software network affects not just the software that freedom
advocates write or choose to use, but software that anyone
writes.  The cost, if any, is a set of structural
constraints that enforce transparency, adaptability, and the
ability to secede from a network and start one's own if the
mad monarch of your current network becomes insufferable.
But we'll suffer a lot to avoid disturbance to our networks.

# Past

Copyleft-based software freedom was a sound network play,
and it achieved significant network-level results.  It's
also succumbing to the signature crumbling decadence of
networks: backward-looking hubris.  When network
participants mire down in reverence for past
accomplishments, secure in the belief that their network is
too big now not to matter forever, we dub them _incumbents_.
And we wait.

It's famously easy to topple unwary incumbents in software.
Opportunity costs are relatively low, and with patents again
in decline, it's often possible to clone, reimplement, and
otherwise run with what you find...or sit around until
someone else does.  That dynamic bites software networks of
all kinds, both open and proprietary. Techniques, standards,
conventions, and usability lessons from GCC or Linux end up
not just in proprietary compilers and kernels, but also
permissively licensed, freedom-indifferent alternatives like
[LLVM] and [Fuschia]. Entire toolchains get rebuilt
likewise, as with [Go].

[LLVM]: https://llvm.org

[Fuschia]: https://en.wikipedia.org/wiki/Google_Fuchsia

[Go]: https://golang.org

Figuring out what to code is damn hard.  Rebuilding what's
been done and proven, slightly better this time, is standard
operating procedure.

# Present

That dynamic partially explains why pillars of the copyleft
network feel ever more like legacy systems.  That's not to
say stagnant or doomed.  Far from it: GPL software remains
much of the most mature and battle-tested, with the broadest
supporting constituencies.  But the content of `LICENSE` no
longer seems to define those projects or their successes, if
it ever did.  It dates them.

A combination of factors conspire against vanguard spirit in
the free software movement.  For one, the licenses don't
seem to evolve with the times.  The application service
provider loophole, which allowed creators of proprietary
software services to avoid the requirement to share source
code under copyleft licenses, especially GPLv2, represented
a practical vulnerability. FSF patched it in AGPL, but
failed to merge into mainline GPL, in part due to threats to
fork development of existing GPLv2 projects. We're left with
GPLv3, which suffers from a known, unpatchable software
freedom vulnerability, and AGPLv3, a separate license under
a distinct name that can be identified, isolated, scorned,
and written off as an extremist excursion, rather than a
necessary adaptation.

Meanwhile, the ASP business model, rebranded _software as a
service_, exploded again.  As did proprietary use of
software development tools, which slide through a loophole
no GPL has ever tried to close.  Software developers see
these dynamics, but lack a public license tool with which to
respond.

Licenses without teeth---and a lot of unhelpful
complexity---don't make or keep strong reputations.  In
time, that perception ferments into a widely held,
ahistorical belief that licensing _can't_ effectively
express or protect software freedom values.  Many active
developers feel not just that open source doesn't belong in
conversations about software freedom, but that copyleft or
licensing in general doesn't really belong.  No wonder.
They've never seen them coupled with efficacy.

# Future

Over time, we should expect a repeating pattern of
permissively licensed software, funded or blessed by
industry, cloning or replacing software first proven by
developers more devoted to software freedom.  Copyleft
licenses impose some additional friction over permissive
licenses, by their nature.  When a concept is proven, demand
for similar functionality under lower-friction terms
increases, and lower friction terms themselves bestow
marginal competitive advantage.

The free software movement was born cloning proprietary
software, and refining its clones.  When permissive software
can as easily clone copyleft software, the software freedom
network can't expect to survive with vitality in a permanent
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
about public licensing in the last ten years.  [Dual
licensing through licensezero.com with
L0‑R](https://guide.licensezero.com) replaces prevailing,
permissive norms with infrastructure for sustainable
development.

Copyleft, permissively licensed, and proprietary software
overlap, and therefore compete with one another.  It's
equally important to acknowledge and account for that
natural competition.  By encouraging those advancing the
state of the art to stand up for user rights in their
licensing choices. By building out infrastructure, support
networks, and methods to make free software programs and
services viable competitors to both permissive and
proprietary alternatives.

Free software values and objectives haven't changed.  With
time, experience, and changes in the industry, we've come to
understand them better.  The methods of expressing those
values, and supporting those objectives, have to evolve with
our understanding.

Software freedom is a movement.  Movements have to move.
