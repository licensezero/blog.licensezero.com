---
title: Reciprocity in Kind
description:
layout: post
---

You've realized you can't keep giving without getting anything back.  And you've found a few things you're comfortable withholding, to trade for the support you need.  Perhaps software features.  Perhaps answers to help tickets.  Perhaps permission to use commercially, or to build proprietary software.  But you still have a question to answer:

What do you want back?

Do you want want help providing services, like support or issue triage?  Promotion for your project?  Reputation and esteem?  Proprietary development contracts?  Cold, hard cash?

# Orthodoxy

In the history of open source, the righteous answer was always the same.  Developers who gave code away expected code back.  Bug fixes.  Feature additions.  Ports.  Compatibility updates.  That kind of thing.

We talk of licenses like GPL as making up a family of "reciprocal" licenses.  Historically, we could say reciprocal licenses required giving back _in kind_.  Users got source code for free, under generous terms.  Conditions required those users to share changes and new code built on top also for free, under the same generous terms.  Code for code, license for license.

# Dissension

But the deals the license drafters wanted made, and the deals the developers choosing their licenses wanted to make, often subtly differed.  Many developers chose GPLv2, the de facto "standard" open source license two decades ago, [because they wanted patches back](https://blog.licensezero.com/2018/01/25/imaginary-licenses.html#torvalds).  But GPLv2 didn't require sending patches back.

The reason why is [right up top, in the license's preamble](https://www.gnu.org/licenses/old-licenses/gpl-2.0-standalone.html#SEC2).  GPLv2 very intentionally required giving source code and license terms to recipients of changed copies, so they'd have all the source of the software they ran.  As a side effect of getting code under GPLv2 terms, recipients had the right to publish that code, or even, yes, send it back to the maintainers.  Nothing in GPLv2 required them to do so, but they did so often enough that maintainers took notice.  If you judged a license by how it worked in visible practice, rather than what it said---especially if you never read it---then GPLv2 looked for all the world like a patches-back license.

That mismatch between the purpose for which GPLv2 was written---ensuring software freedom for _users_---and the purpose for which it was often adopted---ensuring contributions back to _maintainers_---created a latent division.  Dual licensing, or selling exceptions to the requirement to share back for cash instead, widened that crack into a painful break.

# Heresy

From the software-user-freedom point of view, developers selling exceptions are selling exceptions to other people's freedom, more so even than their own.  If I sell you an exception to my GPL license, I'm selling you permission to distribute modified copies to others without giving them source.  All the money goes to me, and I'm not going to share any of it with your end-users.  I won't even know who they are.  I've sold out.

There is an inherent logic in that view.  Fundamentally, dual licensing gives users choice.  They can always accept the terms of the public license, and share source code when the license requires.  But they also have the option to buy an exception, instead.

We'd expect rational users to take that option only when they think the value of their work as proprietary software outweighs the cost of the exception.  That value is probably based on estimates of what end-users will pay for the software, and the fact that they'll need to pay to begin with, since they don't have legal copies or permission to do anything with illicit ones.  That cost-benefit call is inherently speculative, but users know their own work best.  They have the information advantage over the dual-licensing developer.

# Redemption

That view is consistent, but incomplete.  It's guilty of common, problematic tropes in early community thought: that open source maintainers always come batteries-included, with inherent motivation, and that throwing them away when they're out of juice, to be replaced by fresh new models, is acceptable, practically or ethically.

Taking money for exceptions to in-kind, reciprocal terms can and does fund more open development.  When the price of an exception is right---in other words, high---consumers of open software benefit, net of the cost of the exception.  Especially when the value of open development funded with the proceeds is concrete, and those paying for the exception are speculating.

Most startups fail.  Most startup-like projects attempted within larger companies fail.  If there's any intellectual property to liquidate when they're done, it's usually patents, if any, not copyright on code.

Maintainers of proven open projects, conversely, are already proven.  Their ability to keep working, and to stay engaged with the work, directly affect meaningful user outcomes in the short, medium, and long terms.  Open projects selling exceptions already have users confirming their value via payment.

# Competition, Or Not

We've entered an era where Microsoft owns GitHub.
