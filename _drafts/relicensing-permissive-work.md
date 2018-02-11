---
title: Relicensing Permissive Work
description:
layout: post
---

Several folks have asked whether they can change the license terms for open source work they've already released under a permissive license like [MIT](https://spdx.org/licenses/MIT) to [L0's reciprocal license](https://licensezero.com/licenses/reciprocal) or [noncommercial license](https://licensezero.com/licenses/noncommercial).  The short answer is that they probably can ... and probably shouldn't.

A few quick notes, [first about "can"](#can), [then about "shouldn't"](#shouldnt).

# Relicensing <a id="can"></a>

In general, when you write software for yourself, you own any copyright in it.  Unless you assign your copyright to someone else, like a company, client, or open source foundation, in writing, the copyright remains yours.  More or less the same is true of rights in any patentable inventions you come up with and implement in your software.

As the owner of rights in your code, you can license others under pretty much whatever terms you like.  You can license to one person under one set of terms, to another person on different terms, and the public under yet another set of terms.  You can license under one set of terms today, and another set of terms tomorrow.

It's a bit like inviting folks to your home.  When people show up uninvited, they commit trespass, and you can sue them.  You can invite one friend over for dinner tomorrow.  If he shows up for dinner, you can't sue him for trespass.  You _can_ sue him if he shows up two weeks later to steel your television.  You can invite the kids in the neighborhood to play our front.  You can change your mind, post a sign, and tell them to stay away.  Speaking very generally, it's up to you who you invite onto your real property, and its up to you who you license to utilize your intellectual property.

## Same Code, Different Terms

There's a lot of legal uncertainty about changing public license terms, like open source terms, for old code.

Say you sit down tomorrow and write a nifty SVG visualization library in JavaScript.  You write the library for fun, in your free time, with your own  computer, starting from scratch.  You're not doing related work for any company or client under contract.  You own the rights.

You cut a 1.0.0 release and publish your code on GitHub and npm with MIT terms in `LICENSE` and `package.json`.

The next day, you realize that your code may have implemented a novel approach to visualization.  You're not sure, but you suspect you could get a patent.  To head off concerns about whether you'll apply for a patent and start suing users for infringement, you decide to cut a new release with a different license that gives clear patent permission.  You also decide that you'd like to see source for changes that others make to your work, in return.

You cut a 1.0.1 release of your library and publish under The Mozilla Public License, Version 2.0.  MPL gives an explicit patent license, in addition to a copyright license, and it's also a copyleft license, so if fits your bill.

License aside, 1.0.0 and 1.0.1 are the same code.  1.0.0 has MIT terms in `LICENSE`.  1.0.1 has MPL terms in `LICENSE`.  As a user, what are my license terms for your library?

There are a few possibilities:

1.  MPL `AND NOT` MIT

    Perhaps MPL applies to everybody.  That's your most recent choice, and publishing the new version shows that MPL, not MIT, is what you intend.  It's as if you never licensed under MIT terms, even though there's a published version floating around with MIT terms in `LICENSE`.

2.  MIT `XOR` MPL

    Perhaps folks get their choice of MIT and MPL terms.  They can change freely, without sharing back, under MIT.  But if you come after them for patent infringement, they're stuck without clear patent permission.  If they want the clear patent permission under MPL, they have to follow MPL's copyleft conditions.

3.  MIT `OR` MPL

    Perhaps folks get MIT and MPL added together: permission to modify without sharing back under MIT, and clear patent permission under MPL.

How would the law decide?  At least two legal concepts apply: "reliance" and "revocation".

If I download version 1.0.0 of your library, best I can tell, based on your actions, you intend to license me and everyone else under MIT terms.  I might rely on the terms in `LICENSE` for 1.0.0, and make changes that I don't share.  If you sue me for infringement, claiming that I didn't meet your MPL conditions, I'll protest that I didn't see your version 1.0.1, or hear about your license change, and that MIT still applies, at least to 1.0.0.  You set me up to rely on an MIT license.  The law generally protects reliance on clear, outward signs of permission.  It disfavors sneaky traps.

What if you send me a message, before dragging me into court, that says the MIT license no longer applies?  Can you "revoke" your MIT license?  Some open source licenses, like Apache 2.0, say explicitly that permissions granted are "irrevocable", and can't be revoked.  It's isn't clear whether other open source licenses can be revoked at will.

In the end, the law isn't clear.  The outcome for a particular piece of software might have as much to do with context---whether the user knew of the license change, how that change was documented, separate communications between user and developer---as with what license terms say.

## New Code, New Terms

In my opinion, the situation's a bit clearer for new license terms applied to new code.

Say you sit down tomorrow and write a nifty text formatting library.  Again, you own all the relevant rights for the library.  It's 10 commits worth of work.

You cut a 1.0.0 release and publish your code on GitHub and npm with MIT terms in `LICENSE`.

A week later, you add some new functionality to the library, and quite a bit more code.  You own all the relevant rights in this new work, too.  It's another 10 commits.  Before publishing that new work, you decide that you want to make this new work, and your work going forward, available under [GPLv2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html).

You cut a 1.1.0 release with GPLv2 in `LICENSE`, instead of MIT.

The same questions new terms for old code apply to your first 10 commits.  It isn't perfectly clear whether users get just GPLv2 terms for that work, an exclusive choice of MIT or GPLv2 terms, or the right to cherry-pick permissions from MIT and GPLv2.  It's isn't clear whether you've revoked the MIT license for your first 10 commits.

It's a bit clearer that GPLv2 terms apply to code you added in your last 10 commits.

The evidence is clearer.  You haven't released any version containing both the work from the last 10 commits and MIT terms.  As a user, if I download a release with your new work, that release also contains the new GPLv2 terms.  In terms of reliance, users downloading your releases will always see the terms they need to be aware of for your new code.

Your intent is clearer.  First you wrote your MIT code, then you released it under MIT terms, only then did you write your new code, and you released that new code only under GPLv2.  In terms of revocation, you haven't sent any signal that GPLv2 no longer applies to your new work.

In C, C++, Java, and some other languages, developers commonly put license terms, or header comments identifying license terms, in individual source files, rather than at the root of the repository or in package metadata.  Projects in those languages often combine code under different license terms.  Methods for dealing with that diversity of terms, like header comments, also work for different terms applied to different work by a single developer.  New work, especially in a new file, can have its own header comment, notifying readers that different license terms apply to work in that file.

If the effect you want is to keep your original 10 commits worth of work on MIT terms, and license only your new work on GPLv2 terms, you could do so with comments in the code indicating which work you license under which terms.  At a higher level, you could change license metadata in `package.json` from `MIT` to `(MIT AND GPL-2.0-only)`, and rely on notes in `README` or even Git history to help clarify which parts of the code are MIT-licensed, and which parts are GPLv2-licensed.

# Expectations <a id="shouldnt"></a>
