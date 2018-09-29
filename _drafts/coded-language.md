---
title: Coded Language
description: against the timid imagery of open source exceptionalism
layout: post
---

A couple weeks back, I ran across an old argument for open source I hadn't seen in years. Reading with fresh eyes, it struck me as a perfect example of a theory of contribution that's either seductively cogent or painfully bunk, empowering or debilitating, fair or utterly rigged, depending on how you come to it.

The argument goes essentially thus:  Companies use technology to offer valuable products and services. Some of their technology is _differentiating_, setting them apart from their competitors in customers' eyes. But a great deal more is _nondifferentiating_, enabling them to meet baseline business needs shared with many other firms. Since there's no competitive advantage in nondifferentiating technology, there's no competitive disadvantage in sharing it across company lines. In fact, the only advantage to be had is paying less, via cost sharing, more efficient production, or both. That's what open source does for software. So if software is nondifferentiating, it ought to be open source.

Despite apparent flaws---cost reduction and efficiency in basic needs also afford competitive advantage, and meeting those needs for would-be competitors gratis reduces barriers to entry---I have no doubt this argument has got substantial software released as open source. But more troubling than its apparent logical flaws, this argument embeds a highly selective view of industry reality. One company's nondifferentiating technology is another company's product. That product had better be differentiating, or the vendor is sunk. But as it turns out, many vendors of generic software differentiate themselves quite competitively, and earn substantial fees, even though their customers' customers haven't any clue what lies beneath.

# Specialization

In two words: specialist vendors. Databases come most readily to mind.

At LinkedIn, Kafka is an enabler, not a product. Into the Apache Foundation it went, under a permissive license. And Kafka has done very well by house standards, picking up new enterprise users and improving LinkedIn's technical name. That success doubtless vindicates LinkedIn's decision to release.

At Redis Labs, Redis isn't an enabler. It's _the_ product. Out on GitHub it all stood, under open source licenses. Those licenses had the effect of _rendering Redis Labs' differentiating technology nondifferentiating_. Thanks to the licenses, everyone could use Redis and all its add-ons, and even offer them as services to other companies.

Having dedifferentiated its technology---the technology the company could offer, not Redis itself---Redis Labs has had trouble differentiating its business. Meanwhile, AWS has no such trouble, given its established mindshare, budget, personnel, and other, preexisting advantages. So Redis Labs resolved to continue part of its development, Redis add-ons, under terms that limit competitive commercial use, backing itself into an "open core" business model, the newly closed shell of add-ons serving as a kind of armor.

The fact that a database is "nondifferentiating" to one firm does not mean that databases, as a category of software, are or ought to be nondifferentiating to all firms. Some of the best examples of successful, long-term database offerings aren't open source. Oracle is proprietary, and did well enough to buy out MySQL. MySQL's prime mover forked as MariaDB when Oracle took over, but later presaged Commons Clause with the Business Source License. MongoDB is as far from permissive as uncontroversially open source software can be, under AGPL, and has done well. But Elastic, the most recent open-source-database company to file for IPO, faces unfavorable comparisons. Elastic's core is Apache-licensed. That places it closer to BSD Redis, Apache Riak, mixed-permissive CockroachDB, and the associated Amazon problem, than to GPL MariaDB, AGPL MongoDB, or proprietary Oracle and IBM products.

Nondifferentiating as Oracle, IBM, and Mongo databases may seem, abstractly, customers are willing to pay for what Oracle, IBM, and Mongo, and only Oracle, IBM, and Mongo, can provide. That implies the vendors have differentiated themselves from competitors, including permissively licensed open source alternatives. But also that there _is_ some competitive advantage to be had in one database offering over another. Judging by how businesses spend their dollars, Oracle, IBM, and Mongo, which forgo many putatively cost-saving benefits of permissive open source, are often worth the money. If there weren't a business difference, why would businesses pay?

Integrated Development Environments. Project management tools. Developer tools, from static analyzers to compilers. A lot of internal teams create or improve these in house, and release them in hopes of attracting free help. Large enough companies dedicate whole teams to internal-tools production. But with very rare exception, those efforts pale in comparison to those of specialized vendors, who make a particular tool or technology their whole focus, and bring the talent and resources necessary into their folds. Releasing at least parts of those specialized business products under open source terms can make sense, in [very specific, demonstrable ways](https://writing.kemitchell.com/2018/08/23/Selective-Mythology.html). But releasing too large a "core" as open source, where "open source" means a permissive license like Apache or MIT, is similarly demonstrable folly, if you're not a market incumbent selling, primarily, something else.

# Infrastructure

"Nondifferentiating technology" makes this whole analysis sound old-fashioned. These days, we say "infrastructure" again.

What distinguishes infrastructure from non-infrastructure? In the greater conversation about open source, I would argue: a presupposition that it shouldn't be funded like other software, a presupposition that it can and should be permissively licensed open source.

That reflects the most common personal experience of infrastructure, as public infrastructure funded by universal tax without direct accounting for usage, like public roads and bridges. That kind of infrastructure stands outside the private market system, at least partially. But there is a whole world of private infrastructure, from oil and gas pipelines to technical schools, facilitated by markets. That private infrastructure undergirds industries from construction to software to dentistry.

Squint a bit even at prototypically public infrastructure, and it's easy to find money-for-use exchanges in plain sight. The electricity meter on your home. The toll booths at the bridge. There are also invisible meters, like licensing fees for commercial use of otherwise toll-free roads. These are public goods only insofar as the public has the option to pay to use them.

No metaphor for open source can be perfect, or needs to be. Infrastructure is pretty good, especially in how it plays to both sides, evoking reliability for consumers, and a certain civic-minded nobility for producers. But how do its limitations affect what we can say about open source's funding problem, in its terms?

# Fashion

Any conversation about funding open source development is an improvement over assuming that it will fund itself, that it doesn't need funding, or that funding will ruin it for everybody. In that, the return to infrastructure metaphors is a giant leap. But infrastructure imagery, like other metaphors of open source that come in and out of fashion, gives permission for bad answers, even as it begs the right question.

Open source as infrastructure. Open source as ecology. Open source as a public good. Open source as philanthropy. In dialog with industry, we use these metaphors to start otherwise unwelcome conversations about distributing money down to match value coming up, until they lose their novelty, and we have to swap them out for fresh ones. But in order to entice, we have to hold back, can't seem too radical, and therefore fail to take the essential step from the idea that open software development ought to be funded to the idea that funding open software ought to be funded like other software. We fail to broach the question without permitting exceptionalism in the answer. We fail to present open source as software, like the companies failing to support it are software. 

Meanwhile, the arsenal of justifications for funding open source production differently, and worse, holds constant.  Software is "information", and should therefore be free. Software is worth nothing, and only services count. What matters is customer relationships, close to the money, not generic inputs. The result: [profit for us, sustainability for you](https://blog.licensezero.com/2018/06/14/profit-sustainability.html), in whatever vocabulary currently prevails.

All of these distinctions seek to justify deviation from the usual rules and expectations about finance, work, and fairness. All step around acknowledging all software as the fruit of individual investment, labor, and nonrenewable time. All apply selectively, to the work we want free from others, but not the work we do ourselves. All encourage differentiated projects and companies to dedifferentiate themselves, to the benefit of incumbents with advantages new players can't reproduce.

# Exit

When I write that open source producers have to get comfortable talking business, talking about money and their needs, when I write about overcoming the financial infantilization of developers, I'm pointing to a way out of a cycle.

Industry ignores the production side of open source, adopting en masse, and squeezing for value. The community reinforces demanding, hungry behavior, training industry to overdo it. Bad, predictable outcomes of demand and neglect---industry neglect of open source developers, and developers' enabling neglect of themselves---boil over into a perceived crisis.

Industry knows how to talk about money, and how to pay who it has to pay. But rather than opt into it, we articulate the crisis, each time, in timid, metaphoric terms that signal us out of coequal, transactional, businesslike conversation. The results are ad hoc, nonstructural, little-repeatable, and paltry, in dollar terms. A few enlightened champions at large firms with budgets gain leverage, internally, to do something. A few smaller players seize the marketing and community signaling opportunity, which exists only so long as paying anything back is abnormal enough to set a company apart. When the crisis is perceived to pass, the trickle of dollars industry _chose_ to pay, but never _had_ to pay, dries up.

Beware of vocabulary that perpetuates this cycle. Beware of theories that make open source, or software economics, seem simple. Beware of generalizations that don't adequately account for you and your particular situation, that don't give your effort a legitimate, accounted place.

There are very good reasons to contribute to open source, altruistic and ruthlessly self-interested. But there are also very strong incentives to convince others to contribute, not to their benefit, but at their own substantial expense. When you contribute, know why, and how that's justified. Your basic needs are no different than those of proprietary software developers and businessmen. Don't be relegated to a category, rhetorically or practically, where your equal needs are less equal than others'.