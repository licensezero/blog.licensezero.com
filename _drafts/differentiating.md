---
title: Coded Language
description: shoot your foot with open source today
layout: post
---

This week, I ran across an old argument for open source I hadn't seen in years. Reading it with fresh eyes, it struck me as a perfect example of a model of corporate open source contribution that's either seductively accurate or painfully false, empowering or profoundly dangerous, fair or utterly rigged, depending on how you come to it.

The argument goes essentially thus: Companies use technology to offer valuable products and services. Some of their technology is _differentiating_, setting them apart from their competitors. But a great deal more is _nondifferentiating_, enabling them to meet baseline business needs shared by many other firms. Since there's no competitive advantage in nondifferentiating technology, there's no competitive disadvantage in sharing it across company lines. In fact, the only advantage to be had is paying less, via cost sharing, more efficient production, or both. That's what open source does for software. So if your nondifferentiating technology is software, make it open source.

I have no doubt this argument has got substantial source code released as open source. But the argument also embeds a very choosy view of industry reality. One company's nondifferentiating software is another company's product. That product had better be differentiating, or the vendor is sunk. As it turns out, many vendors do differentiate themselves in software for software. We can see this in the fees they command.

---

In two words: specialist vendors. Databases come most readily to mind.

At LinkedIn, Kafka is an enabler, not a product. Into the Apache Foundation it went, and came out under a permissive license. And it has done very well by house standards, picking up many additional enterprise-scale users, and improving LinkedIn's technical name. That success doubtless vindicates LinkedIn's decision to release.

Meanwhile, at Redis Labs, Redis isn't an enabler. It's the product. Out on GitHub it all stood, under open source licenses. Those licenses had the effect of _rendering Redis Labs' differentiating technology nondifferentiating_. Thanks to the licenses, everyone could use it all. As a result of de-differentiating its technology, Redis Labs has had extra trouble differentiating its business. AWS faces no such problem, given its mindshare, budget, personnel, and other preexisting advantages. So Redis Labs resolved to continue part of its development---Redis add-ons---under limited commercial-use terms, backing itself onto an "open core" business model. A new closed shell around the open core could help it compete.

The fact that a database is "nondifferentiating" to one firm does not mean that databases, as a category of software, are or ought to be nondifferentiating to all firms. Some of the best examples of successful, long-term database offerings aren't open source. Oracle is proprietary, and did well enough to buy out MySQL. MySQL's open source prime mover forked as MariaDB, which presaged Commons Clause with its Business Source License. MongoDB is as far from permissive as uncontroversially open source software can be, under AGPL. But Elastic, the most recent open-source-database company to file for IPO, faces unfavorable comparisons, since its Elasticsearch core is Apache-licensed, placing it closer to BSD Redis than to GPL MariaDB, AGPL MongoDB, or proprietary Oracle.

Nondifferentiated as stalwarts Oracle and Mongo may seem to the companies that use them, customers are willing to pay for what Oracle and Mongo, and only Oracle and Mongo, can provide. That implies Oracle and Mongo have differentiated themselves from competitors, including open source alternatives. But also that there _is_ some competitive advantage to be had in one database over another. In the assessment of customers, judged by how they spend their dollars, Oracle and Mongo, which forgo many putatively cost-saving benefits of permissive open source, are worth the extra dollars down.

---

All of this sounds mightily old-fashioned. "Nondifferentiating technology" is dated. Today, we say "infrastructure".

What distinguishes infrastructure from non-infrastructure? In the greater conversation about open source, I would argue: a presupposition that it can and should be funded unlike other software. That connotation reflects the most common, shallow experience of "infrastructure": public infrastructure funded by universal tax without direct accounting for usage, like open roads and bridges. But there is a whole world of private infrastructure, from oil and gas pipelines to technical schools, facilitated by markets, not universal grants or charity. That private industry facilitates industries from construction to software. Squint a bit at even public infrastructure, and it's easy to find usage meters in plain sight, from kilowatt-hour-counters to bridge toll booths, as well invisible meters, like commercial vehicle licensing fees for commercial use of otherwise toll-free roads. These are public goods only insofar as the public has an option to pay for them.

There are a slew of other rhetorical distinctions masking essentially the same  economic exceptionalism. Software is "information", and should therefore be free. Inert software is worth nothing; only services count. What matters is customer relationships, close to the money, not back-office tools like software. The base is nothing; all the money's in integration and custom work.

All of these distinctions seek to justify deviation from the usual rules and expectations about finance, work, and equity. All step around acknowledging software as the fruit of an individual's educational investment and labor, their limited, nonrenewable time. All are applied selectively, to the work one wants, but not to the work one produces oneself. All encourage differentiated projects and companies to de-differentiate themselves, to the benefit of incumbents with advantages new players can't replicate.

Beware of generalizations that justify open source release, and make the trade-offs seem simple. Beware especially of generalizations that don't adequately account for you and your particular situation. There are very good reasons to contribute to open source. But also very good reasons to convince others to contribute not for their benefit, but for one's own.