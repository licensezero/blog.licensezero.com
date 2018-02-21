---
title: Relicensing Permissive Work
description:
layout: post
---

Several folks have asked whether they can change the license terms for open source work they've already released under a permissive license like [MIT](https://spdx.org/licenses/MIT) to [L0's reciprocal license](https://licensezero.com/licenses/reciprocal) or [noncommercial license](https://licensezero.com/licenses/noncommercial).  The short answer is that they probably can ... and probably shouldn't.  I would fork the existing project, give it a new name, and license new contributions under License Zero terms, instead.

A few quick notes, [first about "can"](#can), [then about "shouldn't"](#shouldnt).

# Relicensing <a id="can"></a>

In general, when you write software for yourself, you own any copyright in it.  Unless you assign your copyright to someone else, like a company, client, or open source foundation, in writing, the copyright remains yours.  More or less the same is true of rights in any patentable inventions you come up with and implement in your software.

As the owner of rights in your code, you can license others under pretty much whatever terms you like.  You can license to one person under one set of terms, to another person on different terms, and the public---everybody---under yet another set of terms.  You can license under one set of terms today, and another set of terms tomorrow.  You can give one person more than one license.

It's a bit like inviting folks to your home.  When people show up uninvited, they commit trespass, and you can sue them.  But if you invite someone over for dinner, and they show up, you can't sue them for trespass.  You _can_ sue your dinner guest if they show up two weeks later to steal your television.  You can invite the kids in the neighborhood to play in your yard.  You can change your mind, post a sign, and tell them to stay away.

Speaking very generally, it's up to you who you invite onto your real property, like land, and it's up to you who you license to use your intellectual property, like rights in software.

## Same Code, Different Terms

There's a lot of legal uncertainty about changing public license terms, like open source terms, for old code.

Say you sit down tomorrow and write a nifty SVG visualization library in JavaScript.  You write the library for fun, in your free time, with your own  computer, starting from scratch.  You're not doing related work for any company or client under contract.  You own the rights.

You cut a 1.0.0 release and publish your code on GitHub and npm with MIT terms in `LICENSE` and `package.json`.

The next day, you realize that your code may have implemented a novel approach to visualization.  You're not sure, but you suspect you could get a patent.  To head off concerns that you'll apply for a patent and start suing users for infringement, you decide to cut a new release with a different license that gives clear patent permission.  You also decide that you'd like to see source for changes that others make to your work, in return.

You cut a 1.0.1 release of your library and publish with The License Zero Reciprocal Public License.  L0-R gives an explicit patent license, in addition to a copyright license, and it's also a copyleft license.  L0-R fits your bill.

License aside, 1.0.0 and 1.0.1 are the same code.  1.0.0 has MIT terms in `LICENSE`.  1.0.1 has L0-R terms in `LICENSE`.  As a user, what are my license terms for your library?

There are a few possibilities:

1.  MIT `AND NOT` L0-R

    Perhaps L0-R, and only L0-R, applies to everybody.  That's your most recent choice, and publishing the new version shows that L0-R, not MIT, is what you intend.  It's as if you never licensed under MIT terms, even though there's a published version floating around with MIT terms in `LICENSE`.

2.  MIT `XOR` L0-R

    Perhaps folks get their choice of MIT and L0-R terms.  They can change freely, without sharing back, under MIT.  But if you come after them for patent infringement, they're stuck without clear patent permission, because MIT doesn't give clear patent permission.  If they want the clear patent permission under L0-R, they have to follow L0-R, which has copyleft conditions.

3.  MIT `OR` L0-R

    Perhaps folks get MIT and L0-R added together: permission to modify without sharing back under MIT, and clear patent permission under L0-R.

How would the law decide?  At least two legal concepts apply: "reliance" and "revocation".

If I download version 1.0.0 of your library, best I can tell, based on what you put in that release, you intend to license me and everyone else under MIT terms.  I might rely on the terms in `LICENSE` for 1.0.0, and make changes that I distribute to others, but don't share.  If you sue me for infringement, claiming that I didn't meet L0-R's copyleft conditions, I'll protest that I didn't see your version 1.0.1, or hear about your license change, and that MIT still applies, at least to 1.0.0.  You set me up to rely on an MIT license.  The law generally protects relying on signs of permission.  It disfavors sneaky traps.

What if you send me a direct message that says the MIT license no longer applies?  Can you "revoke" your MIT license?  Some open source licenses, like Apache 2.0 and GPLv3, say explicitly that permissions granted are "irrevocable", and can't be revoked outside specific circumstances.  It isn't clear whether other open source licenses can be revoked at will like that.

In the end, the law isn't clear.  The outcome for a particular license for a particular piece of software might have as much to do with particular context---whether the user knew of the license change, how that change was documented, what communications about developer intentions the user actually received---as with what any particular open source license terms say.

## New Code, New Terms

In my opinion, the situation's clearer for new license terms applied to new code.

Say you sit down tomorrow and write a nifty text formatting library.  Again, you own all the relevant rights for the library.  It's 10 commits worth of work.

You cut a 1.0.0 release and publish your code on GitHub and npm with MIT terms in `LICENSE`.

A week later, you add some new functionality to the library, and quite a bit more code.  You own all the relevant rights in this new code, too.  It's another 10 commits.  Before publishing that new code, you decide that you want to make the new code, and your work going forward, available under L0-R.

You cut a 1.1.0 release with L0-R in `LICENSE`, instead of MIT.

The same questions about new terms for old code apply to your first 10 commits.  It isn't perfectly clear whether users get just L0-R terms for that code, an exclusive choice of MIT or L0-R terms, or the right to cherry-pick permissions from MIT and L0-R.  It's isn't clear whether you've revoked the MIT license for your first 10 commits.

But in my opinion, L0-R terms clearly apply to code you added in your last 10 commits.

The evidence is clearer.  You haven't released any version containing both the code from the last 10 commits and MIT terms.  As a user, if I download a release with your new code, that release also contains the new L0-R terms.  In terms of reliance, users downloading your releases will always see the terms they need to be aware of for the code in the release.

Your intent is clearer.  First you wrote your MIT code, then you released it under MIT terms, only then did you write your new code, and you released that new code only along with L0-R terms.  In terms of revocation, you haven't sent any signal that L0-R no longer applies to your new code.

In C, C++, Java, and some other languages, developers commonly put license terms, or header comments identifying license terms, in individual source files, rather than at the root of the repository or in package metadata.  Packages in those language tend to contain more code, and often combine code under different license terms.  Methods for dealing with that diversity, like header comments, also work for different terms applied to different code by the same developer.  New code, especially in a new file, can have its own header comment, notifying readers that different license terms apply to code in that file.

If the effect you want is to keep your original 10 commits worth of code on MIT terms, and license only your new code on L0-R terms, you could show that intent with comments in the code indicating which code you license under which terms.  At a higher level, you could list both sets of terms in `LICENSE`, and rely on notes in `README` or even Git history to help clarify which parts of the code are MIT-licensed, and which parts are L0-R-licensed.

## MIT to License Zero

As the owner of rights in code, you have the right to license under whatever terms you like.  But it isn't clear whether you can revoke licenses under MIT terms that you've already given.  Attempting to do so, or even making changes to license terms that seem to suggest that you want to, can cause a lot of legal confusion.  So you could change all license terms in your project to License Zero terms, deprecate or unpublish old versions under MIT terms, post messages online, and even notify current users that you're revoking your MIT license privately.  But even then, it wouldn't necessarily become clear that your old work is only available on License Zero terms.

On the other hand, if you want to apply different terms to _new_ work that you do, building on your own MIT-license code, which remains MIT-licensed, you can do so, and pretty clearly.  I'm not aware of any general legal requirement that you keep licensing new code for an old project on the same license terms you chose for your old code.  And you have some fairly explicit ways to document your choice, and make it clear to users.  Explain in `README`.  Add comments to code files.

If users need both your old MIT code and your new License Zero code to use the project as a whole, they'll need to meet the conditions of both licenses, including your License Zero reciprocal or noncommercial license.  If they can get by with just your old MIT-licensed code, they can stick to the old versions, and ignore the License Zero terms for your new code.

# Expectations <a id="shouldnt"></a>

License Zero calls out unfair expectations in software development.  The goal is expectation change.

Users expect contributors' work will be free, under permissive licenses like MIT.  Past work for nothing.  Users expect support and timely responses to bug reports, free.  Present work for nothing.  Users expect contributors to keep making new software, as bug fixes, security patches, feature additions, and so on, and to put that new work out under the same permissive license, for free.  Future work for nothing.  Users expect free past, present, and future work for any open source software they find online.  It's a [shopping spree](https://blog.licensezero.com/2017/09/12/manifesto.html).  Nothing in the shop's off limits.

The gap between current expectations and healthy expectations is wide.  Closing that gap is not a one-and-done proposition.  It will take time, and some work. To create new, healthy expectations, we will have to defy current, unhealthy expectations.  We will have to work through frustration to get conversation.

Putting anything other than permissively licensed open source code in some source code repositories defies expectations.  We see this with GPL-licensed code on npm.  Users open pull requests relicensing onto MIT terms, sometimes without so much as a comment to the patch.  From my point of view, those pull requests are disrespectful, aggressive, and rude.  But from the users' point of view, they were promised all-you-can-eat permissive software, and got something else.  In a mountain of MIT, BSD, and Apache 2.0, GPL feels like a mistake, or even a trap.  L0-NC and L0-R will defy those expectations, too.

Changing code licenses between releases defies expectations.  We see this in arguments about SemVer.  Is a license change a major, breaking change, or just a patch?  Users choose frameworks, tools, and libraries, and build them into their projects.  They rely.  If the license terms change to something they won't accept, they get cut out of updates, and have to reimplement or replace.  Changing MIT-licensed code to L0-R-licensed code will defy those expectations, too.

Changing license terms for a project, and changing them to non-permissive terms like L0-R or L0-NC, will make double trouble.  We have to ask whether it's better to frustrate expectations one at a time, to make change in increments, or to drop all the bombs we have, to make change by shock and awe.

Licensing is the tool that makes past work in software free to use or not free to use.  License Zero empowers developers to use that tool in a new way.  But developers, as a whole, don't feel in command of software licensing generally.  They rely on it.  But for most, licensing is strange, and a bit mysterious.  Reliance and mystery have a way of adding up to anxiety.  Anxiety you may have noticed in your grandparents, as you fix their computer.  Anxiety you may have felt yourself, when a mechanic fixes your car, or a plumber works at your home.

If License Zero were merely a matter of software, just a digital vending machine for licenses, a Stripe app, I'd be all in favor of taking a hard stance.  But since licensing's involved, and has to be involved, I prefer picking battles one at a time.

Forking an existing project, giving it a new name, and licensing new work on it under L0-R or L0-NC will beg the conversation about what those licenses do, and how that differs from old choices like MIT and AGPL.  That's a big enough conversation on its own, and one we'll need to get good at having.  Switching the existing project code onto L0 terms at the same time feels like too much.  The conversation about developers' right to pick their terms is just as necessary, and just as fundamental.  But I suspect it will be much harder to have both those conversations at once than separately.
