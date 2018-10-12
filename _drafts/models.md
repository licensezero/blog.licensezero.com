---
layout: post
---

Most open source business models aren't really business models at all.  Rather, they _presuppose some other, autonomous business model_, and offer up open source as a means to make it better.  In the end, the business isn't open source, it's just that other model.  Open's just a means of selling more of something closed.

Consider the business models summarized in Raymond's _Magic Cauldron_:

- _Loss-Leader/Market Positioner_, key example Netscape's Mozilla, presupposed a proprietary server software business.

- _Widget Frosting_, key example Apple Darwin, presupposed a hardware business.

- _Give Away the Recipe, Open A Restaurant_, key examples Cygnus and RedHat, presupposed a professional services practice.

- _Accessorizing_, key example O'Reilly Media, presupposed bookselling.

- _Free the Software, Sell the Brand_, example Star Office, now OpenOffice.org and LibreOffice, presupposed a trademark and a certification program.

- _Free the Software, Sell the Content_, no example given, presupposed a content subscription business.

There was one exception: _Free the Future, Sell the Present_, key example Ghostscript, described how companies can offer their latest work on proprietary terms, but allow older versions to lapse onto open source terms.  We see this model continue today, both for Ghostscript and through [the Business Source License](https://mariadb.com/bsl11), a license purpose-built for MariaDB, open successor to MySQL, with provisions for automatic open source release.

We could describe this kind of delayed-release approach as a kind of dual licensing.  When a new version comes out, it's available on two different sets of license terms: the public open source terms, usually GPL or other copyleft, and the private, commercial terms.  Apply the same to existing code in perpetuity, and you've got traditional dual licensing.

Why does this matter?  Because traditional dual-licensing and delayed-release models _make money by selling the software, based on its utility, by selling permission to use it legally_.  Those are business models unto themselves, no presupposition of some other plan required.  _All_ the outputs of a business running that kind of model can be open source software, open documentation, and other parts of the open package.  _All_ the time of its engineers can be directed toward those outputs, rather than private services, proprietary code, or other outputs that compete for open development for time and energy.

Completeness offers all kinds of benefits, from operation simplicity to lower overhead and clarity of business mission.  There's no splitting time between open and closed software, or succumbing to incentives to make features closed, as for _Loss-Leader_, which we now call _Open Core_.  There's no need to develop a capital-intensive hardware, media, or publishing business, as under _Widget Frosting_, _Accessorizing_, or _...Sell the Content_, or to contend with relegation to second-rate status within that kind of business.  There's no need to divert time and attention to service relationships, as under _Give Away the Recipe..._, or to suffer the relatively poor scaling dynamics of a professional services play.  And there's no need to police a trademark or provide intensive certification checks, under _...Sell the Brand_.  Just make open software, and charge money for using it in closed projects.

Boiling permission-based models down to dual-licensing and delayed release hides a lot of choices and variation within the category.  Those choices can be useful, to help tailor a model to a particular kind of software or business situation.

We can chart a course to explore those choices by going back to what end users need to get the benefit of software:

1. _Implementation_: Vaporware doesn't do users any good.
2. _Distribution_:  Code that's been written, but not shared, isn't any good to anybody else.
3. _Permission_:  Even if the software's been written, and even if you happen on a copy, you face legal trouble for making use of it without at least a copyright license.

Each of these is _necessary_, but not alone _sufficient_.  Software isn't broadly useful without all three.

Each of these can also be _complete_ or _partial_, and shifted in time from _before payment_ to _after payment_.  You can implement software before you get paid, or after payment.  You can do half an implementation before you get paid, and half after.  You can give limited permission before you get paid, and complete permission after.

If your plan is to give all three away for free, completely, you do not have a business plan.  Your generosity might enhance _another_ business plan, but it isn't itself any kind of business.  If you receive any compensation for what you do along those lines, it's either charity of a mistake.  Either the "customer" knew they didn't need to pay you for anything, or mistakenly believed they did.

Permission-based business plans like dual licensing and delayed release typically don't hold back on implementation or distribution.  They implement all the code needed to make their projects complete, and distribute all of that code.  Even in terms of permission, permission-based business models still give quite a lot of away.  Typically, that means permission to use the open software as provided, but not to build closed software with open.  When the open software is a framework, library, or another unfinished components---it doesn't do anything useful on its own---its primary "use" value is building other software, and that isn't covered by the public license, if the application is closed.  Dual licensing companies sell that missing permission to customers.

But of course permission isn't the only dimension in which an open source business model can hold back.  Implementation-based business models are in fact even more broadly practiced than permission-based models.  So much so, in fact, that we often neglect to mention them in business-model conversations at all.

Selling implementation of software that you will distribute with broad permission is paid open source development.  Rather than writing a bunch of code, distributing it, and then figuring out how to charge for it, you charge first, then develop and deliver.

It's very possible, and indeed common, to combine implementation- and permission-based models.  Sign a contract for paid open source development.  Make sure you retain ownership of intellectual property in your work, especially copyright, and commit to release on the terms of an open-only license, like AGPL.  Charge a premium for the development work, since for most end-users, you won't have another opportunity to get paid for the same work.  But add a note to the licensing information for your project, mentioning that you'll entertain offers to dual license.

Implement software for which you think there will be demand, without a business deal in place.  This entails a bit of speculation on your part, both in what you think is worth making, and also in the time you take to make it.  Distribute this software under open-only terms.  But also offer to relicense your work on more permissive terms, like MIT or Apache 2.  Signing that deal essentially 

The common practice of _these_ particular permutations of implementation, distribution, and permission, incomplete and complete, over time, and not others, imply some constraints.  In particular:

1. Once someone implements software, they usually don't have to implement it again.  Assignments of intellectual property rights, exclusive licenses, data loss, and lack of maintenance for compatibility, among other factors, make some exceptions from this rule, and compound with time.
2. If you distribute software with a standard open source license, it can be legally and practically difficult to _reduce_ the permission others receive for the same software.  On the other hand, it's relatively straightforward to reduce permission for new code, if you won the rights, as well as to _increase_ permission for code already released.  So it's difficult to change the license terms for a prior published release from MIT to GPL.  But it's often possible to apply GPL to new work on an old MIT project, or to change the terms for your old work from GPL to MIT. 
3. Once you grant permission under a standardized open source license, it's usually hard or impossible to control further distribution of that code and permission.  You can grant an MIT license for particular software to a particular customer.  They must just sit on it, and use it for themselves.  But there's no stopping them publishing the same code online, resulting in free copies and licenses for everyone.  It's up to them, unless you have some other exclusive right, like a patent, to hold over their heads.