---
layout: post
---

Most open source business models aren't really business models at all.  They presuppose some other business model, and proffer open source as a way to make it better.  Selective openness is just a way to sell more of something closed.

If you start from a desire to work in the open, and want to work backwards from there, to a business model, it's worth identifying, focusing on, and exploring the business models that actually stand on their own.

Consider the business models summarized in Raymond's _Magic Cauldron_:

- _Loss-Leader/Market Positioner_, example Netscape's Mozilla, presupposes a proprietary software business.

- _Widget Frosting_, example Apple Darwin, presupposes a hardware business.

- _Give Away the Recipe, Open A Restaurant_, examples Cygnus and RedHat, presupposes a professional services business.

- _Accessorizing_, example O'Reilly Media, presupposes a hard goods business.

- _Free the Software, Sell the Brand_, example Star Office, now OpenOffice.org and LibreOffice, presupposes a certification business.

- _Free the Software, Sell the Content_, no example given, presupposes an intangible media business.

But one of Raymond's models was not like the others:

- _Free the Future, Sell the Present_, key example Ghostscript, describes companies that offer their latest work on proprietary terms, but release older versions as open source.

Like _Loss-Leader_, _...Sell the Present_ presupposes a proprietary software business to lead into.  It's just there's a silver lining: closed work opens up in time.  Rather than relying on scheduled publication of formerly closed work, [The Business Source License](https://mariadb.com/bsl11), originally written for MariaDB, open successor to MySQL, implements the transition in legal terms.  The company can therefore publish its latest immediately, or even work in the open to begin with, and see its work "released" automatically. That puts the project on a kind of treadmill.  It must always keep developing, keep maintaining, keep offering new functionality worth licensing, to have a business model.  On the other hand, real-time publication and automatic release ensure the community's ability to work with the code will outlive the company, should it fail.

For incomplete software like libraries and frameworks, useful when built into other programs, this treadmill proved unnecessary.  By choosing an open license that prohibits reuse in closed software, the developer withholds an opportunity to sell licenses for closed reuse.  It can license not just its latest and greatest software, which it's also free to release as open source as soon as it's developed, but also old work.  Ghostcript itself eventually adopted this approach, releasing its latest and greatest under GPL terms in real time, while charing commercial users for permission to build on and distribute Ghostscript as part of closed systems, especially printers.  Like MySQL before it, Ghostscript became _dual-licensed_: available on both public open source terms, usually GPL or other copyleft, and private, commercial terms.

Crucially, dual licensing makes money by selling the value of software, in the form of deals for permission to reuse in closed systems.  That makes dual licensing, and the class of permission-based models more broadly, complete in themselves.  Permission-based business models don't have to presuppose any other business model, to bring money into the picture.  Nonetheless, substantially _all_ the outputs of a dual-licensing business can be open source software, open documentation, and other parts of the open package.  Substantially _all_ the time of its engineers can go toward open outputs, rather than private services, closed code, or other efforts that compete with open development for time and energy.

A complete plan offers all kinds of benefits, from operation simplicity to lower overhead and clarity of business mission.  There's no splitting time between open and closed software, or succumbing to incentives to make features closed, as for _Loss-Leader_, now often called _Open Core_.  There's no need to develop a capital-intensive hardware, media, or publishing business in parallel or first, or to contend with the second-rate status of software development in subservience to that primary model, as under _Widget Frosting_, _Accessorizing_, or _...Sell the Content_.  There's no call to divert time and attention to services, or to specialize developers as product people or service people, or to deal with the relatively poor scaling dynamics of services plays, as under _Give Away the Recipe..._ or _...Sell the Brand_.  Just make open software, make it as good as you can, and charge money for the right to add that value to closed projects.

# Variations

Fortunately, dual-licensing and delayed release are broad categories, and representative of a larger "pure" open source family.  Pure models offer quite a bit of choice, which makes it possible to tailor a model to particular software and particular business situations.

We can map those choices by generalizing what end users need to benefit from software:

1. _Implementation_: Vaporware isn't useful.
2. _Distribution_:  Software that's been written, but not shared, isn't much use to anyone else.
3. _Permission_:  Even if the software's been written, and even if you happen on a copy or other access, you face legal trouble for using without a license.

Each of these is _necessary_, but not alone _sufficient_.  Users need all three at any significant scale.

Developers can meet each of these needs _completely_ or _partially_. They can also meet them at different times, _before payment_ and _after payment_.  Developers can implement software before they get paid, or after payment.  They can also do half an implementation before they get paid, and half after.  They can give limited permission before they get paid, or none at all, and complete permission after.

If your plan is to implement, distribute, and give permission away, completely and for nothing, full stop, you do not have a business plan.  If you have additional plans, perhaps they add up to such a plan.  Perhaps one of those Raymond lists.  Perhaps a plan for more personal benefit, social enjoyment, like educational value or reputation.  But charity, on its own is the antithesis of a plan for getting paid.  If you receive compensation for charity, either you weren't actually practicing charity, your "customer" was, or one of you made a mistake.

Archetypical permission-based business plans like dual licensing typically don't hold back on implementation or distribution.  They implement all the code needed to make their projects complete, and distribute all of that code.  Even in terms of permission, permission-based business models still give quite a lot of away.  Their business model is selling whatever permission is "missing" form their choice of public license, from their customers' points of view.  But even common public license choices come riddled with known loopholes, especially for internal and software-as-a-service use.

But of course permission isn't the only dimension in which an open source business model can hold back.  Implementation-based business models are in fact even more broadly practiced than permission-based models.  So much so, in fact, that we often neglect to mention them in business-model conversations at all.

Selling implementation of software that you will distribute with broad permission is paid open source development.  Rather than writing a bunch of code, distributing it, and then figuring out how to charge for it, you charge first, then develop and deliver.

It's very possible, and indeed common, to combine implementation- and permission-based models.  Sign a contract for paid open source development.  Make sure you retain ownership of intellectual property in your work, especially copyright, and commit to release on the terms of an open-only license, like AGPL.  Charge a premium for the development work, since for most end-users, you won't have another opportunity to get paid for the same work.  But mention in your license notice that you'll entertain offers to dual license existing work on more permissive terms.

If there's work still to do, you can also mention that you'll happily do paid contract work to develop the project further, on the same kind of terms you used before.  If you'd already implemented that software, and sold it as proprietary software, you'd be running the _Open Core_ model, with the proprietary add-ons as the "Closed Shell".  Instead you're sticking to a pure open source model, by moving implementation after payment.  

Alternatively, implement software for which you think there will be demand, without a business deal in place.  This entails a bit of speculation on your part, both in what you think is worth making, and also in the time you take to make it.  Distribute this software under open-only terms.  But also offer to relicense some or all of your work on more permissive terms, like MIT or Apache 2.  Signing that deal is essentially a dual licensing transaction, except the alternative license, which would usually apply only to the customer in traditional dual licensing, applies to everyone, just like the public license.  Instead of giving each customer complete permission, one by one, after payment, you give everyone complete permission after payment.

The viability of _these_ particular combinations, and not others, implies some constraints within our five-dimensional paradigm.  In particular:

1. Once someone implements software, they usually don't have to implement it again.  Assignments of intellectual property rights, exclusive licenses, data loss, and lack of maintenance for compatibility, among other factors, make some exceptions from this rule.
2. If you distribute software with a standard open source license, it can be legally and practically difficult to _reduce_ the permission others receive for the same software.  On the other hand, it's relatively straightforward to reduce permission for new code, if you won the rights, as well as to _increase_ permission for code already released.  So it's difficult to change the license terms for a prior published release from MIT to GPL.  But it's often possible to apply GPL to new work on an old MIT project, or to change the terms for your old work from GPL to MIT. 
3. Once you grant permission under a standardized open source license, it's usually hard or impossible to control further distribution of that code and permission.  You can grant an MIT license for particular software to a particular customer.  They must just sit on it, and use it for themselves.  But there's no stopping them publishing the same code online, resulting in free copies and licenses for everyone.  It's up to them, unless you have some other exclusive right, like a patent, to hold over their heads.
4. Conversely, keeping permission incomplete by granting alternative, private licenses only to specific customers is very common, and robust.