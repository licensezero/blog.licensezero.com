---
layout: post
---

Most open source business models aren't really business models at all.  They presuppose some other, autonomous business model, and offer up open source as an add-on, to make it better.  Open's just a means of selling more of something closed.

Consider the business models summarized in Raymond's _Magic Cauldron_:

- _Loss-Leader/Market Positioner_, example Netscape's Mozilla, presupposed a proprietary server software business.

- _Widget Frosting_, example Apple Darwin, presupposed a hardware business.

- _Give Away the Recipe, Open A Restaurant_, examples Cygnus and RedHat, presupposed a professional services practice.

- _Accessorizing_, example O'Reilly Media, presupposed bookselling.

- _Free the Software, Sell the Brand_, example Star Office, now OpenOffice.org and LibreOffice, presupposed a trademark and a certification program.

- _Free the Software, Sell the Content_, no example given, presupposed a content subscription business.

But one of Raymond's models was not like the others:

- _Free the Future, Sell the Present_, key example Ghostscript, described how companies can offer their latest work on proprietary terms, but allow older versions to lapse onto open source terms. 

We see this model continue today.  Ghostscript continues to use it.  [The Business Source License](https://mariadb.com/bsl11), originally written for MariaDB, open successor to MySQL, implements it automatically, through legal terms.

We could describe this kind of delayed-release approach as a kind of _dual licensing_.  When a new version comes out, it's available on two different sets of terms: the public open source terms, usually GPL or other copyleft, and the private, commercial terms for sale.  Other dual licensing businesses release their code under open terms immediately, and offer commercial terms for sale for old as well as new contributions.

Why does this matter?  Because traditional dual-licensing and delayed-release models _make money by selling the value of the software, by selling permission to use it legally_.  Permission-based business models are business models unto themselves, no other model required or assumed.  Substantially _all_ the outputs of a business running that kind of model can be open source software, open documentation, and other parts of the open package.  Substantially _all_ the time of its engineers can go toward those outputs, rather than private services, proprietary code, or other outputs that compete with open development for time and energy.

If open source is a must, a complete plan offers all kinds of benefits, from operation simplicity to lower overhead and clarity of business mission.  There's no splitting time between open and closed software, or succumbing to incentives to make features closed, as for _Loss-Leader_, now often called _Open Core_.  There's no need to develop a capital-intensive hardware, media, or publishing business in parallel or first, or to contend with the second-rate status of software development in subservience to that primary model, as under _Widget Frosting_, _Accessorizing_, or _...Sell the Content_.  There's no call to divert time and attention to services, or to specialize developers as product people or service people, or to deal with the relatively poor scaling dynamics of services plays, as under _Give Away the Recipe..._ or _...Sell the Brand_.  Just make open software, make it as good as you can, and charge money for the right to add that value to closed projects.

Fortunately, dual-licensing and delayed release are broad categories, and not the only ones within their category.  "Pure" open source business models in fact offer quite a bit of choice.  Choice helps tailor a model to a particular kind of software or financial situation.

We can chart a course through those choices by going back to what end users need to benefit from software:

1. _Implementation_: Vaporware isn't useful.
2. _Distribution_:  Software that's been written, but not shared, isn't much use to anyone else.
3. _Permission_:  Even if the software's been written, and even if you happen on a copy or other access, you face legal trouble for using without a license.

Each of these is _necessary_, but not alone _sufficient_.  Users need all three at scale.

Developers can meet each of these needs _completely_ or _partially_. They can also meet them at different times.  Let's simplify to _before payment_ and _after payment_.  So developers can implement software before they get paid, or after payment.  They can do half an implementation before they get paid, and half after.  They can give no permission or limited permission before they get paid, and complete permission after.

If your plan is to implement, distribute, and give permission away, completely and for free, you do not have much of a business plan.  Your generosity might enhance _another_ business plan, among those Raymond mentions, but being very generous is the opposite of a plan for getting paid.  If you receive any compensation for your generosity, either the customer is practicing charity, or someone has made a mistake.  Charity if the "customer" knew they didn't owe you, mistake if they wrongly thought they did.

Permission-based business plans like dual licensing and delayed release typically don't hold back on implementation or distribution.  They implement all the code needed to make their projects complete, and distribute all of that code.  Even in terms of permission, permission-based business models still give quite a lot of away.  Typically, that means permission to use the open software as provided, but not to build closed software with open.  When the open software is a framework, library, or another unfinished components---it doesn't do anything useful on its own---its primary "use" value is building other software, and that isn't covered by the public license, if the application is closed.  Dual licensing companies sell that missing permission to customers.

But of course permission isn't the only dimension in which an open source business model can hold back.  Implementation-based business models are in fact even more broadly practiced than permission-based models.  So much so, in fact, that we often neglect to mention them in business-model conversations at all.

Selling implementation of software that you will distribute with broad permission is paid open source development.  Rather than writing a bunch of code, distributing it, and then figuring out how to charge for it, you charge first, then develop and deliver.

It's very possible, and indeed common, to combine implementation- and permission-based models.  Sign a contract for paid open source development.  Make sure you retain ownership of intellectual property in your work, especially copyright, and commit to release on the terms of an open-only license, like AGPL.  Charge a premium for the development work, since for most end-users, you won't have another opportunity to get paid for the same work.  But mention in your license notice that you'll entertain offers to dual license existing work on more permissive terms.

If there's work still to do, you can also mention that you'll happily do paid contract work to develop the project further, on the same kind of terms you used before.  If you'd already implemented that software, and sold it as proprietary software, you'd be running the _Open Core_ model, with the proprietary add-ons as the "Closed Shell".  Instead you're sticking to a pure open source model, by moving implementation after payment.  

Alternatively, implement software for which you think there will be demand, without a business deal in place.  This entails a bit of speculation on your part, both in what you think is worth making, and also in the time you take to make it.  Distribute this software under open-only terms.  But also offer to relicense some or all of your work on more permissive terms, like MIT or Apache 2.  Signing that deal is essentially a dual licensing transaction, except the alternative license, which would usually apply only to the customer in traditional dual licensing, applies to everyone, just like the public license.  Instead of giving each customer complete permission, one by one, after payment, you give everyone complete permission after payment.

The viability of _these_ particular combinations, and not others, implies some constraints within our five-dimensional paradigm.  In particular:

1. Once someone implements software, they usually don't have to implement it again.  Assignments of intellectual property rights, exclusive licenses, data loss, and lack of maintenance for compatibility, among other factors, make some exceptions from this rule.
2. If you distribute software with a standard open source license, it can be legally and practically difficult to _reduce_ the permission others receive for the same software.  On the other hand, it's relatively straightforward to reduce permission for new code, if you won the rights, as well as to _increase_ permission for code already released.  So it's difficult to change the license terms for a prior published release from MIT to GPL.  But it's often possible to apply GPL to new work on an old MIT project, or to change the terms for your old work from GPL to MIT. 
3. Once you grant permission under a standardized open source license, it's usually hard or impossible to control further distribution of that code and permission.  You can grant an MIT license for particular software to a particular customer.  They must just sit on it, and use it for themselves.  But there's no stopping them publishing the same code online, resulting in free copies and licenses for everyone.  It's up to them, unless you have some other exclusive right, like a patent, to hold over their heads.