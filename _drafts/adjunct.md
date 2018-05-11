---
title: Commons Club
description: open source as proprietary accessory
layout: post
---

To software developers, today's hand-wringing about privacy,
security, and manipulation comes comically, pitiably late.
Software people know how software gets made, and why.  When
we join up to mainstream networks, services, and apps, we
take steps, from privacy settings to browser extensions to
Tor, that come easily only to our kind.  But all-in, we know
they're just half-measures.  We're tech people, but we might
as well be plumbers or insurance brokers, as far as other
devs' apps are concerned.  Other devs' apps made
increasingly with open source.

Open source software is winning.  Software freedom---the
power to be both developer and user of the apps that matter
to you---is not.  If there were ever a short cased for a
difference, there it is.

Perhaps open source doesn't belong in conversations about
user rights, privacy protection, transparency, or choice.
But it chooses not to belong.  Free software takes positions
on user-facing issues.  Open source takes positions on
user-facing issues when the users happen to be programmers.

That's why open source "wins".  It wins, dilutely, as
accessory to proprietary software.  It's more efficient to
build proprietary code---social networks, commercial
networks, locked-in user communities---on open source
freebies.  But it's more profitable, so they say, to deny
users of those systems no meaningful rights to patch, fork,
and set policy.

It's tempting to avoid this reality by reassuring ourselves
that all software is open source these days, or nearly so,
because it's increasingly made both [of open source][usage]
and [like open source][innersource].  Compared to the heavy
intellectual lifting done in the stack---often open
source---the layer of closed integration, application, and
design on top of most offerings measures relatively thin.
At least from a chauvinistic programmer point of view.

[usage]: https://www.blackducksoftware.com/about/news-events/releases/companies-lack-open-source-policies

[innersource]: https://en.wikipedia.org/wiki/Inner_source

But that's a distinction falling conveniently short of a
difference for anyone else.  I can improve [Facebook's
front-end framework][react], making it easier to change
facebook.com, and drawing in more developers Facebook might
hire or acquire. I can optimize [LinkedIn's
database][kafka], making linkedin.com cheaper to run, and
fewer tickets for LinkedIn staff to handle.  But Facebook
isn't a front-end framework, and LinkedIn isn't a database.

[react]: https://reactjs.org

[kafka]: https://kafka.apache.org

Not really.  Not even close.  Even if sloughing away all the
open source leaves but a thin film of proprietary code, that
code implements the choices that meaningfully affect users.
Patches to that layer, to the network itself, aren't
welcome. Patching is network-owner prerogative.

Network-owner prerogative is a pervasive kind of power.
Networks are simple value propositions, but simple
propositions that many, many people can take at will.
Network power compels less by what network owners offer than
by what users offer, and there can be many, many users.  The
value can seem overwhelming.  We'll abide a creepy social
network to socialize with the right people. We'll abide a
slimy market to buy the rights product at the right price.

"Network effect" still has a new shine on it, and calls to
mind Valley business culture, not hacker counterculture. But
software freedom advocates bid consciously for network
effects in [1989].  In specific domains, their license, the
GPL still reigns.  It's easier to port GCC to your new
architecture than to write a compiler from scratch. It's
easier to tweak WordPress than to seed you own blog-platform
community. Software freedom isn't so much enforced in these
domains, emphasis on _force_.  Life and business are just
better with free run of GPL software, and without cease and
desist letters or public shaming by a community.  Even the
utterly indifferent abide GPL conditions and GPL politics
for free code and documentation.

[1989]: https://www.gnu.org/licenses/old-licenses/gpl-1.0.en.html

And that is exactly the promise of network power.  A free
software network affects not just the software that freedom
advocates write, but software that anyone writes, and
software freedom advocates end up having to run. It affects
incentives for nearly anyone writing software in a domain
touched by the network, even managers openly hostile to
software freedom.

The fatal flaw of network power, for freedom or for
leverage, is hubris.  Hubris looks to accomplishments of the
past and position in the present, forgetting that present
value is always an estimate of the future.  Incumbency's at
risk as soon as you stop doing what made you the incumbent,
and start acting like an incumbent.

It's famously easy to topple incumbents in software.
Incremental costs are low, and with patents again in
decline, it's relatively easy to clone, reimplement, and
otherwise run with whatever you find.  That dynamic bites
both proprietary and software-freedom networks.  Techniques,
standards, conventions, and usability lessons from GCC or
Linux end up not just in proprietary compilers and kernels,
but also permissively licensed, freedom-indifferent
alternatives like [LLVM] and [Fuschia].

[LLVM]: https://llvm.org

[Fuschia]: https://en.wikipedia.org/wiki/Google_Fuchsia

That dynamic partially explains why so many pillars of the
GPL network feel ever more like legacy systems.  That's not
to say stagnant or doomed.  Far from it: GPL software
remains much of the most mature and battle-tested, with the
broadest supporting constituencies.  But license
obsolescence---especially the ASP loophole, and [GPLv3's
choice not to close it][GPLv3]---permissive licensing
seepage---[Go] compiles native binaries without external
libraries---and ease of reimplementation all erode the
freedom-for-code cost-benefit proposition.  If
freedom-preserving licenses impose friction on those who
might join a project's supporting constituency, we should
expect a trend toward permissive licensing over time, at
least as long as contributors and would-be contributors
remain indifferent to the goals copyleft licenses suffer
friction to achieve, and especially if copyleft licenses
aren't seen as particularly effective in achieving those
goals to begin with.

[Go]: https://golang.org

[GPLv3]: http://redmonk.com/sogrady/2009/04/15/open-source-licensing-in-a-networked-age/
