---
title: Decentralized Dual Licensing
description: the bottom-up business model for open software
---

The dual-licensing business model feels less relevant because it never spawned a corporate champion that took the industry by storm.  It never remade "open source" in its image.  That reflects dual licensing's greatest virtue---resistance to centralization---not a flaw.

Defiant decentralization is a flaw only if you want to conquer the software industry.  If you want a resilient, adaptable, autonomous open software movement, decentralization is essential.

## Paid Distribution

Selling copies of free software on physical media represented the obvious side hustle for early free software hackers.  The Free Software Foundation began selling copies of Emacs on tape, before it could count on donations to make ends meet, and insisted that free software licenses permit that kind of business, even though RMS hated business.  Meanwhile, companies like Walnut Creek CDROM sold all the free software they could find on disc.  But broad Internet expansion took the wind out of paid free software distribution just as it flooded free software with a new glut of hackers.  Walnut Creek ran the Internet's hottest FTP server, the harbinger of its own dollar doom.

If you wanted a copy of a Linux distribution, you knew where to look ... but eventually everyone's answer became "the Internet".

Quoth Walnut Creek:  Google it.  We're joining a consulting company.

## Documentation

The Free Software Foundation also sold documentation, but despite centralizing stewardship of many key early projects, a private firm, O'Reilly Media, came to dominate that model.  O'Reilly books frequently outshined official materials from the projects themselves, and O'Reilly hired many developers to produce "authoritative" books on their technologies, often at the expense of freely available docs.  In the late 1990s, the company expanded to conferences, first to promote sales of its media, then as a line of business unto itself.

If you wanted to learn a new language or technology, you looked for the animal book.

Quoth O'Reilly Media:  Open source success means a book deal with us.  If you want to stay up-to-date on fast-moving technology, ask your boss for a book budget, or better yet Safari Online.

## Professional Services

The ingredients of Red Hat---an accessories seller, a Linux distribution, and a consultancy---came together to dominate professional services and enterprise-friendly vendoring for free software, by then called "open source".  To this day, competing with Red Hat to sell commercial support for software of broad enterprise appeal remains very difficult, even if you wrote the software.  The customers you want likely already have Red Hat contracts, and the company boasts all the trappings of scale: engineers, salespeople, marketing muscle, legal boxes ticked.  Niche players can and do exist, but unless Red Hat trips on its own feet, they can expect to stay in niches.

If you wanted a contract to wrap open source in enterprise trappings, you called Red Hat, or waited for them to call you.

Quoth Red Hat:  Open source means not just a free license, but also a system of governance that allows us to insert ourselves, even at the expense of the original developers.

## Hosting

Red Hat reflected a sudden spike in enterprise demand for open source.  When software consumption preferences shifted again---from software to services---Amazon found its lane.  Beginning as a marketplace for Amazon's own relatively low-level computing resources, Amazon Web Services eventually rose to prominence as a quasi-reseller, extender, and integrator of open source services.  Just as Red Hat kept tabs on rising projects, AWS prospects the noosphere for proven "hits" and productizes them.  It remains very difficult to beat AWS on hosting, even hosting of your own software.  The customers you want likely already have AWS accounts, and the company boasts all the trappings of scale: engineers, salespeople, marketing muscle, legal boxes ticked.  Unless you hold back substantial enterprise-worthy functionality as closed software---like Amazon's own console and orchestration work---you can expect AWS to substantially limit the part of your addressable market that you get to address, once it's large enough.

If you want someone else to run open source for you, Google the generic name and bland logo Amazon has assigned to the product and open your AWS console.

Quoth Amazon:  Open source means not just a free license, but a free license for all desirable functionality and services around the core product so that AWS can productize it, even at the expense of the original developers.  No "open core" for you.  That's our model.

## Cycle

Economics and consumer preferences in software will turn again.  Perhaps end-users will come to prioritize autonomy, and insist on peer-to-peer or federated applications.  Perhaps widespread security concerns will spike consumption through app stores and other gatekeepers.  More likely, tastes will change in ways I can't possibly imagine.

If the cycle continues, those shifts will catalyze business opportunities.  But the bounties may very well accrue to a single, dominant player per model, leveraging fierce network effects against any who would follow in their wake.

## Dual Licensing

Single-firm dominance hasn't befallen dual licensing because, like open core, dual licensing requires the producer of software to retain special commercialization powers unique to them as creator.  Only open core developers can license their closed add-ons.  Only dual licensing developers can ignore the rules of their own license, like copyleft rules, and sell licenses without those rules to others.  Those special connections irk those who view all software licensing decisions through the single lens of freedom, but honor a different and very fundamental value, fairness, in addition to unlocking more software-producing potential.

To the larger point, a single company can't centralize dual licensing powers unless many, many independent developers grant those rights to a single company.  It is theirs to use or trade away.  But a single company, like this one, _could_ develop network effects in facilitating dual licensing transactions.  For example, it is far easier to download a single program and run it to buy all the licenses you need for a project than to deal with each project individually, a handful or tools, or a smattering of different facilitators.

However, I'm not aware of anything proprietary in that form of facilitation, and part of my reason for taking License Zero public as early as I could was to create prior art.  My primary goal remains teaching developers the dual licensing model.  But I'm also teaching everybody how to automate a software licensing agency, best I know how.

## Not Yet

Among open software business models, dual licensing offers a unique strength.  So why does it feel like the runt of the litter?  I suspect three major factors: one political, two practical.

Politically, dual licensing has enjoyed staunch enemies and only halfhearted friends.  RMS has long supported dual licensing.  Dual licensing models, by their nature, rely on copyleft like FSF's GPLs, rather than permissive licenses like MIT or BSD.  But RMS, FSF, and the school they represented have at best tolerated business interests as morally admissible concessions.  There's no orthodox enthusiasm for dual licensing or any business model.

Compare the political bona fides of the dominant rising model, "open core".  As a general rule, open core companies tend to come from permissive licensing communities, and to deploy copyleft, if at all, only for patches back, rather than to compel the release of full applications.  Their banner license is Apache 2.0, the enterprise-friendly permissive license.  Their social sphere, largely composed of the enterprises they hope to sell to, and perhaps recently worked for, often make closed software, and don't object to others doing so.  Being businesses themselves, there's no question about business models.

Practically, I see two issues: the weakening of copyleft licenses and troubles welcoming outside contribution.

Dual licensing relies on strong-copyleft licenses that require users for the primary use case to share their work alike.  If copyleft only requires sharing back in rare cases, very few users need to buy exceptions.  They can simply use the software under the free public license.  Likewise, if the primary use case of the software---compiling other programs, providing a service over a network---happens to fall outside copyleft, there will be very few potential customers for paid exceptions to the copyleft rule.

I've written extensively on the limits copyleft license drafters self-imposed in the past, such as rules permitting even enormous, multinational companies to distribute code in-house without disclosing, or running software services without sharing back.  I have also surveyed "loopholes" that opened up in once strong copyleft licenses due to changes in software practice and background law.  Overall, many strong-copyleft licenses were not maintained over time, and grew weaker.  Even the strongest avoided specific use cases to start, like developer tools, for the sake of broader adoption and a taller pulpit to preach from.  As a result, developers who needed stronger terms for dual licensing couldn't find them.  When they wrote such licenses for themselves, as [I did](https://paritylicense.com) for users of License Zero, they faced stiff resistance.  Stiffest, often, from proponents of crippled copyleft.

Dual licensing also suffers from friction on outside contributors.  Unlike open core, where the core is often permissive, and all that's needed from outsiders is a commitment to license their work on the same permissive terms, dual licensing developers must preserve their special right to license the whole project, including outside contributions, on other terms.  That means receiving licenses for others' contributions on more permissive terms than they offer for their own work.

Historically, dual licensing companies solved this problem best by hiring many contributors to their projects.  MySQL famously did so, and L. Peter Deutsch's sale of Ghostscript to Artifex increased the number of developers devoted to the code.  But employment isn't for everyone, and often simply impractical, especially when the company and the developer live far apart, or the contributor devotes only a little time and attention.  Speaking recently at the Open Core Summit in San Francisco, Peter lamented that the dual licensing model, which he otherwise recommended wholeheartedly, remained incompatible with "community-driven development" of other projects, most notably Linux, funded otherwise.

The community-hiring problem is symptomatic of a broader class of problems: the transaction costs of various aspects of dual licensing, both contributor-facing and customer-facing, remain high.  Those costs weighed dual licensing down.  Analysts typed it to solo-developer and financed-company projects.

## Why Now?

The high transaction costs of dual licensing are coming down.

License Zero is first and foremost an experiment in reducing the transaction costs between dual licensing developers and their customers.  Terms are standardized.  Payment is familiar.  A single program automates identifying, pricing, and buying all licenses needed for a project.

The purpose of that effort was to make dual licensing accessible to independent developers who can't or won't hire salespeople, specialist lawyers, payment managers, and the rest.  Much as a small business might hire a service bureau to manage payroll, developers can hire License Zero as their dual licensing back office.

More recently, I've turned more attention to the transaction costs among contributors to dual licensed projects.  That led eventually to [cross-license collaboratives](https://xlcollaborative.com), a new kind of contributor license agreement that contributors grant to each other, not one centralized company or foundation.  Each contributor receives the right to license the project as a whole, so long as they get approval from a majority of fellow contributors, by vote.  When a contributor makes money on a license for the project, they must split the payment equally among fellow contributors.  Informed by cooperative principles, collaboratives require equal votes, equal communication, and equal pay.

Cross-license collaboratives thus provide a lightweight, Internet-ready alternative to forming a corporation or other legal entity.  Unlike many cooperatives structured as corporations or LLCs, collaboratives don't provide a legal shield against liability, but individuals making contributions to open software don't have that protection, either.  It doesn't seem they need it.  All common open software licenses disclaim any liability for licensing software, which is all that collaboratives do.

In short, Parity and cross-license collaboratives make community-driven dual licensing of nearly all software used to make other software possible.  And cheap.  And easy.  Dual licensing has never been more ready to put small, defiantly independent developer projects in business.
