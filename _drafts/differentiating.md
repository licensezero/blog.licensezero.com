---
title: Coded Language
description: shoot your foot with open source today
layout: post
---

This week, I ran across an old argument for open source I hadn't seen in years. Reading with fresh eyes, it struck me as a perfect example of a theory of contribution that's either seductively accurate or painfully false, empowering or profoundly dangerous, fair or utterly rigged, depending on how you come to it.

The argument goes essentially thus:  Companies use technology to offer valuable products and services. Some of their technology is _differentiating_, setting them apart from their competitors. But a great deal more is _nondifferentiating_, enabling them to meet baseline business needs shared with many other firms. Since there's no competitive advantage in nondifferentiating technology, it's just table stakes for competing to begin with, there's no competitive disadvantage in sharing it across company lines. In fact, the only advantage to be had is paying less, via cost sharing, more efficient production, or both. That's what open source does for software. So if your nondifferentiating technology is software, make it open source.

I have no doubt this argument has got substantial source code released as open source. But the argument also embeds a very selective view of industry reality. One company's nondifferentiating software is another software company's product. That product had better be differentiating, or the vendor is sunk. But as it turns out, many software-component vendors differentiate themselves in competitive ways. We can see that in the fees they earn.

---

In two words: specialist vendors. Databases come most readily to mind.

At LinkedIn, Kafka is an enabler, not a product. Into the Apache Foundation it went, under a permissive license. And Kafka has done very well by Apache house standards, picking up new enterprise users and improving LinkedIn's technical name. That success doubtless vindicates LinkedIn's decision to release.

At Redis Labs, Redis isn't an enabler. It's _the_ product. Out on GitHub it all stood, under open source licenses. Those licenses had the effect of _rendering Redis Labs' differentiating technology nondifferentiating_. Thanks to the licenses, everyone could use Redis and all its add-ons, and offer them as a service.

As a result of de-differentiating its technology, Redis Labs has had extra trouble differentiating its business. Meanwhile, AWS faces no such problem, given its mindshare, budget, personnel, and other, preexisting advantages. So Redis Labs resolved to continue part of its development---Redis add-ons---under limited commercial-use terms, backing itself into an "open core" business model. A new closed shell around the remaining open core could help it compete.

The fact that a database is "nondifferentiating" to one firm does not mean that databases, as a category of software, are or ought to be nondifferentiating to all firms. Some of the best examples of successful, long-term database offerings aren't open source. Oracle is proprietary, and did well enough to buy out MySQL. MySQL's prime mover forked as MariaDB when Oracle took over, and later presaged Commons Clause with the Business Source License. MongoDB is as far from permissive as uncontroversially open source software can be, under AGPL, and has done well. But Elastic, the most recent open-source-database company to file for IPO, faces unfavorable comparisons. Elastic's core is Apache-licensed. That places it closer to BSD Redis, and the Amazon problem, than to GPL MariaDB, AGPL MongoDB, or proprietary Oracle.

Nondifferentiated as Oracle and Mongo databases may seem to users, customers are willing to pay for what Oracle and Mongo, and only Oracle and Mongo, provide. That implies Oracle and Mongo have differentiated themselves from competitors, including permissively licensed, open source alternatives. But also that there _is_ some competitive advantage to be had in one database over another. Judging by how they spend their dollars, Oracle and Mongo, which forgo many putatively cost-saving benefits of permissive open source, are often worth the extra money. If there weren't a business difference, why would businesses pay?

---

"Nondifferentiating technology" makes this whole analysis sound old-fashioned. These days, we're saying "infrastructure" again.

What distinguishes infrastructure from non-infrastructure? In the greater conversation about open source, I would argue: a presupposition that it can and should be funded unlike other software. In other words: a presupposition that it can and should be open source, especially permissively licensed open source.

That reflects the most common personal experience of infrastructure, as public infrastructure funded by universal tax without direct accounting for usage, like public roads and bridges. But there is a whole world of private infrastructure, from oil and gas pipelines to technical schools, facilitated by markets. That private infrastructure undergirds industries from construction to software.

Squint a bit even at public infrastructure, and it's easy to find money-for-use exchanges in plain sight. The electricity meter on your home. The toll booths at the bridge. There are also invisible meters, like commercial vehicle licensing fees for commercial use of otherwise toll-free roads. These are public goods only insofar as the public has an option to pay to use them.

There is a kind of fashion in rhetorical flourishes that mask the economic exceptionalism "infrastructure" entails. Open source discourse uses and abuses these flourishes for a while, until they wear out, and then replaces them. Software is "information", and should therefore be free. Software is worth nothing; only services count. What matters is customer relationships, close to the money, not back-office tools like software. All the money's in integration and custom work, meeting direct client needs. [Profit for us, sustainability for you.](https://blog.licensezero.com/2018/06/14/profit-sustainability.html)

All of these distinctions seek to justify deviation from the usual rules and expectations about finance, work, and equity. All step around acknowledging software as the fruit of an individual's educational investment and labor, their limited, nonrenewable time. All are applied selectively, to the work one wants free or cheap from others, but not to the work one produces oneself. All encourage differentiated projects and companies to de-differentiate themselves, to the benefit of incumbents with advantages new players can't replicate. None of these rhetorical devices justifies treating the user-company relationship as a rightfully negotiated market transaction, and the company-supplier relationship as something else, by anything but benefit to the company.

Beware of theories that make open source, or software economics, seem simple. Beware of generalizations that don't adequately account for you and your particular situation. There are very good reasons to contribute to open source, altruistic and ruthlessly self-interested. But there are also very strong incentives to convince others to contribute for you, to one's own benefit, at their expense.
