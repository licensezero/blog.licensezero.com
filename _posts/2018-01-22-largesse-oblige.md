---
title: Largesse Oblige
description: follow the money, note where it stops
layout: post
---

Some see "open source sustainability" as a problem of getting companies to pay the developers.  If I didn't know better, I'd say that sounds pretty easy.  Companies pay developers lots of money all the time.

Consider data from the [Bureau of Labor Statistics](https://www.bls.gov/ooh/computer-and-information-technology/home.htm) for the US in 2016:

<table>
  <thead>
    <tr>
      <th>Occupation</th>
      <th>Median Pay</th>
      <th>Number of Jobs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Computer and Information Research Scientists</td>
      <td>$111,840</td>
      <td>27,900</td>
    </tr>
    <tr>
      <td>Computer Programmers</td>
      <td>$79,840</td>
      <td>294,900</td>
    </tr>
    <tr>
      <td>Computer Systems Analysts</td>
      <td>$87,220</td>
      <td>600,500</td>
    </tr>
    <tr>
      <td>Software Developers</td>
      <td>$102,280</td>
      <td>1,256,200</td>
    </tr>
    <tr>
      <td>Web Developers</td>
      <td>$66,130</td>
      <td>162,900</td>
    </tr>
  </tbody>
</table>

As you might expect from those figures, the country is sprouting code schools like mushrooms.  A glut of eager students fill their cohorts, rushing to enter software-developer work and make software-developer money.  I've met gaggles of these folks mentoring at [NodeSchool](https://nodeschool.io).  Enter [freeCodeCamp](http://freecodecamp.com/).

One model of open source sustainability holds that a company paying forty computer programmers to build proprietary software should hire, say, ten of the open source programmers behind the work they rely on.  Or should allow its forty programmers to spend a day a week on open source.

From the smokey, wood-paneled back room of my mind, where I role-play an ambitious, mid-level manager, a growl:

> What do _I_ need to hear about "open source"?  That's engineering business.  If the engineers we're paying use open source to create value and get away with it, that's part of the value we're paying them for.
>
> You insist?  Well, sure!  We can hire ten new open source developers.  We'll just pay the other forty less, to make the budget.

A contrarian narrative of financial sustenance for open source:  Companies are already paying out the money open source needs.  They are paying it to programmers writing proprietary software.  Those programmers take the value of open source up to their employers, but don't pass their employers' financial support down.

# Uh-Oh

This argument feels dangerous.  It has some very disturbing properties.

It ignores non-financial benefits of employment or even stable contracting.  Large companies hiring open source developers give those developers a semblance of predictability.  They'll receive some check each month, and may receive benefits.  There's also a certain reputational bonus, first from getting hired to do open source to begin, and second, perhaps, from getting hired by a reputable company.

Giving open source developers those benefits could improve the open source they churn out.  Perhaps they'd be more responsive to bug reports.  More careful to code securely.  Quicker to take up new features.  Faster to maintain compatibility.  The companies providing benefits---and relying upon the open source software---might even profit by the exchange.  [Or not.](http://david.heinemeierhansson.com/2013/the-perils-of-mixing-open-source-and-money.html)  [It's complicated.](https://medium.com/@mikeal/great-post-8a4dfe7ee550)

Politically, this view divides the community, and not in a happy way.  Rather than one, united trade of open source contributors, current and potential, it's givers and it's takers.  Pardoning those who give back in kind---proprietary developers who do open source off the clock---we know we're still left with many, many developers who use open source to build proprietary software without so much as picking up a beer tab.  Meanwhile, what solidarity do the unpaid have with the paid, to drive a harder bargain with employers?  Dark picture.

But if we take compensating value delivered, or giving as one has received, as a _moral_ prescription, it makes perfect sense to leave that obligation with people, rather than corporations.  Start with a collective action challenge, like funding public goods, and add corporate structure.  Now you have _two_ collective action challenges, one tied up with the other.  We don't expect corporations to reciprocate gifts, to balance out windfalls, to greet good fortune with commensurate, selfless generosity.  We know better.

The Bill and Melinda Gates Foundation, not Microsoft, kills the mosquitoes, pays off the debts, writes the curriculum standards.  The Ford Foundation, not Ford Motor, [supports seminal work on open source and its discontents](https://www.fordfoundation.org/library/reports-and-studies/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/).  Rockefeller, not Standard Oil.  Howard Hughes Medical Institute, not Hughes Aircraft.  Personal vehicles with tax advantages that hemorrhage personal wealth, not collective, hierarchical organizations that hoard it.  It's a pattern.

# 92.1% − 30¢

All of a sudden, patronage makes sense.  [Patreon](https://patreon.com) accounts for highly reputed open source developers, funded by small-dollar donations from other developers, let the paid prop up the unpaid they rely on.  [Sell a private mailing list and timely access to security bulletins.](https://www.patreon.com/eranhammer)  It's the in-house dev's neck if there's a problem, a missed deadline, or a breach.  [Sell laptop stickers.](https://www.patreon.com/feross)  Coders love those.  Suits do not. [Sell ads to corporations if you can](https://www.patreon.com/mafintosh), sure.  Especially [for large amounts](https://www.patreon.com/evanyou).  But mostly, focus on driving as many small-dollar, fellow-dev contributors to your page as you can.  Low friction, for aggregate volumes of dollars you otherwise wouldn't see, is the only way the high fees make sense.  [Become an anonymous cactus, if that's what the kids will fund.](https://patreon.com/typicode)

And wouldn't you know, unified reputation systems, like [GitHub activity](https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/), also start to make sense.  So does gaming them.  Fellow shows up in your repo's issues, asking for feature.  Is he on your patrons list?  No.  Is he active in open source?  No.  Give him his choice:  Show me commits, or show me coin, or I'll show you `#wontfix`.  [I don't need to know who you're working for.](https://blog.licensezero.com/2017/10/16/mercenary-rapport.html).  This is between you and me.

Basically, it's the coins from [John Wick](https://en.wikipedia.org/wiki/John_Wick_(film_series)).  Give a favor, take a favor, end up rich in favors, or dead to the guild.  But instead of murder for hire, it's the dirty work of rigging up software that straight folk don't need to see.

[The whole thing makes me queasy.](https://twitter.com/kemitchell/status/937720688462278657)  [It all seems a bit absurd.](https://twitter.com/kemitchell/status/946929942633345024)


# Subaltern

This view comports nicely with open source as mere adjunct to proprietary software development.  In essence, open source becomes a performance enhancer for system integrators making proprietary products and services: things people other than programmers actually interact with and derive value from.  More and more free software gets written, but it gets harder and harder to make do without proprietary apps and services.

A single, additional ray of hope shines through: open source developers can trade on reputation developed within open source development for cash, while remaining within open source.  They don't have to write proprietary code to pay rent.  They can stay pure.

Kind of.  The cash they earn flows down mostly from proprietary enterprises, like water down from a mountain snow cap.  There are glorious, glorious exceptions, like [service](https://wso2.com) and [hosting](https://discourse.org) companies.  But the thrust of industry is proprietary services, even if all that's proprietary in those services is [application-specific, brackish residue that can't be so easily abstracted away](https://github.com/substack/blog/blame/9d89edcd55b7424d8c0f65d5c0dfd2dec34993c0/module_steps.markdown#L75).  Some devs get to make open source, and open source alone, but they're not working toward a world where the systems they use and care about are open source.

In this world, License Zero still has work to do, in making open source competitively viable.  Open source companies can reap [L0-R](https://licensezero.com/licenses/reciprocal) software for free, while proprietary shops pay its price.  Theoretically, licensing could track usage better than patronage, by carrying the big stick called intellectual property infringement.

License Zero could also [restructure toward developer-to-developer licenses](https://github.com/licensezero/licensezero-questions/issues/10) easily enough, with companies licensed if the developers they're paying are.   Even smaller transactions.  One per developer, perhaps.  Everyone on the web team pays for a private license for the framework, rather than sharing a private license in the name of the company.  Mere implementation details.  \[_I've addressed those details in [a later blog post](https://blog.licensezero.com/2018/01/26/developer-licensing.html)._\]

# SOS

I know the open source party line, and even if, someday, I come to see that it's irreparably wrong-headed, a part of me will always want to believe it.  I can quote Lessig, invoke Raymond, and cite the GPL in several versions, extemp.  And I suppose I could make a career, of sorts, articulating and refining the now orthodox counter-economy, commons-utopian gestalt of open source née free software.  A steward's duty.  A relatively quiet life.

I'm not cut out for it.  I wouldn't consider myself truly paid forward if I didn't go hunting for contrary views, build them up as far as they'll go, and put them to the test.  Open source has plenty of cheerleaders.  I'm here to hunt bugs, find exploits, patch, and upgrade.

I still root for the team.  If the point of view presented here irks you, well, it irks me, too.  Help me argue it down, consistently and rigorously.

So far, I can't.
