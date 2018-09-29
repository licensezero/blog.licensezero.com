---
title: Coded Language
description: shoot your foot with open source today
layout: post
---

A couple weeks back, I ran across an old argument for open source I hadn't seen in years. Reading with fresh eyes, it struck me as a perfect example of a theory of contribution that's either seductively cogent or painfully bunk, empowering or debilitating, fair or utterly rigged, depending on how you come to it.

The argument goes essentially thus:  Companies use technology to offer valuable products and services. Some of their technology is _differentiating_, setting them apart from their competitors. But a great deal more is _nondifferentiating_, enabling them to meet baseline business needs shared with many other firms. Since there's no competitive advantage in nondifferentiating technology, there's no competitive disadvantage in sharing it across company lines. In fact, the only advantage to be had is paying less, via cost sharing, more efficient production, or both. That's what open source does for software. So if your nondifferentiating technology is software, make it open source.

Despite apparent flaws---cost reduction and efficiency in basic business needs also afford competitive advantage, and meeting those needs for would-be competitors gratis reduces barriers to entry---I have no doubt it has got substantial software released as open source. But more troubling than its logical flaws, this argument embeds a highly selective view of industry reality. One company's nondifferentiating technology is another company's product. That product had better be differentiating, or the vendor is sunk. But as it turns out, many vendors of generic software differentiate themselves quite competitively. And earn substantial fees.

# Specialization

In two words: specialist vendors. Databases come most readily to mind.

At LinkedIn, Kafka is an enabler, not a product. Into the Apache Foundation it went, under a permissive license. And Kafka has done very well by house standards, picking up new enterprise users and improving LinkedIn's technical name. That success doubtless vindicates LinkedIn's decision to release.

At Redis Labs, Redis isn't an enabler. It's _the_ product. Out on GitHub it all stood, under open source licenses. Those licenses had the effect of _rendering Redis Labs' differentiating technology nondifferentiating_. Thanks to the licenses, everyone could use Redis and all its add-ons, even offer them as a service to other companies.

As a result of dedifferentiating its technology, Redis Labs has had extra trouble differentiating its business. Meanwhile, AWS has no such trouble, given its established mindshare, budget, personnel, and other, preexisting advantages. So Redis Labs resolved to continue part of its development---Redis add-ons---under limited commercial-use terms, backing itself into an "open core" business model, the newly closed shell of add-ons serving as a kind of competitive armor.

The fact that a database is "nondifferentiating" to one firm does not mean that databases, as a category of software, are or ought to be nondifferentiating to all firms. Some of the best examples of successful, long-term database offerings aren't open source. Oracle is proprietary, and did well enough to buy out MySQL. MySQL's prime mover forked as MariaDB when Oracle took over, but later presaged Commons Clause with the Business Source License. MongoDB is as far from permissive as uncontroversially open source software can be, under AGPL, and has done well. But Elastic, the most recent open-source-database company to file for IPO, faces unfavorable comparisons. Elastic's core is Apache-licensed. That places it closer to BSD Redis and Apache Riak, and the Amazon problem, than to GPL MariaDB, AGPL MongoDB, or proprietary Oracle.

Nondifferentiating as Oracle and Mongo databases may seem, abstractly, customers are willing to pay for what Oracle and Mongo, and only Oracle and Mongo, can provide. That implies Oracle and Mongo have differentiated themselves from competitors, including permissively licensed open source alternatives. But also that there _is_ some competitive advantage to be had in one database offering over another. Judging by how they spend their dollars, Oracle and Mongo, which forgo many putatively cost-saving benefits of permissive open source, are often worth the money. If there weren't a business difference, why would businesses pay?

Integrated Development Environments. Project management tools. Developer tools, from static analyzers to compilers. A lot of internal teams create or improve these in house, and release them. Large enough companies dedicate whole teams to such production. But those efforts pale in comparison to those of specialized vendors, who make a particular tool or technology their whole work. Releasing at least parts of those specialized business products under open source terms can make sense

# Infrastructure

"Nondifferentiating technology" makes this whole analysis sound old-fashioned. These days, we say "infrastructure" again.

What distinguishes infrastructure from non-infrastructure? In the greater conversation about open source, I would argue: a presupposition that it shouldn't be funded like other software, a presupposition that it can and should be permissively licensed open source.

That reflects the most common personal experience of infrastructure, as public infrastructure funded by universal tax without direct accounting for usage, like public roads and bridges. But there is a whole world of private infrastructure, from oil and gas pipelines to technical schools, facilitated by markets. That private infrastructure undergirds industries from construction to software to dentistry.

Squint a bit even at public infrastructure, and it's easy to find money-for-use exchanges in plain sight. The electricity meter on your home. The toll booths at the bridge. There are also invisible meters, like licensing fees for commercial use of otherwise toll-free roads. These are public goods only insofar as the public has an option to pay to use them.

# Fashion

Any conversation about funding open source development is an improvement over assuming that it will fund itself, that it doesn't need funding, or that funding will ruin it for everybody. In that, the return to infrastructure metaphors is a giant leap. But infrastructure imagery, like other metaphors of open source that come in and out of fashion, gives permission for bad answers, even as it begs the funding question.

Open source as infrastructure. Open source as ecology. Open source as a public good. Open source as philanthropy. In dialog with industry, we use these metaphors of open source to start otherwise unwelcome conversations about distributing money down to open source suppliers, until they lose their novelty, and we have to rotate on to another one. But in order to entice, we have to hold back, can't seem too radical, and therefore fail to take the essential step from the idea that open software development ought to be funded to the idea that funding open software development ought to be funded like other software. We fail to broach the question without permitting exceptionalism in the answer.

Meanwhile, the arsenal of justifications for funding open source production differently---and worse---remains constant.  Software is "information", and should therefore be free. Software is worth nothing, and only services count. What matters is customer relationships, close to the money, not generic inputs. The result: [profit for us, sustainability for you](https://blog.licensezero.com/2018/06/14/profit-sustainability.html), in whatever vocabulary currently prevails.

All of these distinctions seek to justify deviation from the usual rules and expectations about finance, work, and fairness. All step around acknowledging all software as the fruit of individual investment, labor, and nonrenewable time. All apply selectively, to the work we want free or cheap from others, not to the work we do ourselves. All encourage differentiated projects and companies to dedifferentiate themselves, to the benefit of incumbents with advantages new players can't replicate.

Beware of theories that make open source, or software economics, seem simple. Beware of generalizations that don't adequately account for you and your particular situation. There are very good reasons to contribute to open source, altruistic and ruthlessly self-interested. But there are also very strong incentives to convince others to contribute for you, to one's own benefit, at their expense.
