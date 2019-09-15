---
title: Developer Licensing
description: should License Zero stay between developers?
author: K.E. Mitchell
layout: post
---

_[Largesse Oblige](https://blog.licensezero.com/2018/01/22/largesse-oblige.html)_ asked whether License Zero should restructure from licensing companies toward licensing developers.  I'd like to sketch out what that might look like, as a bridge to asking:

_As a developer considering License Zero for your work, would you prefer a system for selling licenses to other developers, rather than to their companies and clients?_

Feel free to weigh in [on this GitHub issue](https://github.com/licensezero/licensezero-questions/issues/10).

# Just Enough Background

License Zero gives you a choice of public license to put in `LICENSE`.  One option, the [noncommercial license](https://licensezero.com/licenses/noncommercial), limits use for commercial purposes to thirty-two days.  The other option, the [reciprocal license](https://licensezero.com/licenses/reciprocal), lets anyone use for any purpose, but requires that anyone building with or on your software to make their own work open source.  Through [licensezero.com](https://licensezero.com), others can buy [private licenses](https://licensezero.com/licenses/private) that allow them to do what your public license doesn't: use for commercial purposes and build closed source.

# Company Licensing

Right now, both individuals and companies can buy private licenses, but the system focuses on companies.  Private licenses for companies cover a number of company employees and contractors, depending on the tier of license purchased.

Private licenses _don't_ cover customers of the company who may need a license.  So buying a private license for a library allows the company (and its developers) to use that library in a web app without making it open source.  But buying a private license for a library used in a proprietary front-end browser application does _not_ cover customers using that application.  The company would need to buy a private licenses for each of its customers, or have each customer buy a private license for themself.

# Developer Licensing

The proposal is to eliminate company private licenses.  Only individuals would be able to buy private licenses.  The terms of individual private licenses would change:

1.  A private license for a project would enable the licensed developer to sublicense employers and clients to whom they deliver work that uses the License Zero project, or builds on it.

2.  Sublicensed companies and clients would be able to sublicense their customers in turn, to cover their use of software built on the project.

3.  A private license for a project would _not_ allow developers to sublicense other developers.  Each developer would need their own private license for commercial or closed-source work.

# Effects

Moving from company licensing to developer licensing would have a few profound effects.  Let's have a look at a few in the context of a hypothetical:

_Anna and Bob work at ComputerCo, building Ducky Emulator._

_Ducky Emulator uses Fred's goey-gui library._

_goey-gui is a License Zero project._

_Herbert, Ingrid, and Jake pay ComputerCo to use Ducky._

## Who must buy licenses?

Under company licensing, ComputerCo could buy a single private license for gooey-gui that would cover Anna and Bob.  ComputerCo would also have to buy private licenses for its customers, Herbert, Ingrid, and Jake, or they would have to buy private licenses for themselves.

Under developer licensing, both Anna and Bob need to buy a private license for goeuy-gui.  Those licenses entitle them to sublicense ComputerCo, and ComputerCo to sublicense its customers, Herbert, Ingrid, and Jake.  As a result, ComputerCo won't have to buy a private license.  Neither will Herbert, Ingrid, and Jake.

Under company licensing, companies and customers must buy private licenses.  Under developer licensing, developers must buy private licenses.

Company licensing seems to work better for those who want support in proportion to use of their projects.  The number of those who need private licenses for a project tracks the number of companies and customers using the project.

Developer licensing seems to work better for those who want support in proportion to demands on their time.  The number of those who need private licenses for a project tracks the number of developers likely to submit bug reports, feature requests, and other technical feedback.

## Who buys?

Under company licensing, companies pay for private licenses, and private licenses cost more for large companies with lots of developers.  A company employee would have to work through the expense reporting or procurement process for their company.  Having bought the license, the company then needs to distribute the License Zero bundle to its developers.

Under developer licensing, companies pay employees and contractors, and employees and contractors pay License Zero developers.  There is just one price, the price for a private license covering one individual developer.  Each developer manages their own license data.

There are two major advantages here, one very practical, one more conceptual.

Practically, it's often far easier to pay for small-dollar, individual-license transactions in a company context.  At low enough amounts, the cost might come under limits for company credit cards, discretionary budgets, and expense reimbursement.  Even when a company requires approval, the process of paying for a single-employee need is often much easier than for a company-wide site license.  All of that means less friction and delay in sending cash to License Zero developers.  Anecdotally, many employees buy text editors, IDEs, and specialist software this way already.

Conceptually, this approach abstracts developer relationships, from the company point of view.  Companies hire employees and contractors to make software.  They pay those people for work, without peering into every aspect of how the work gets done.  If the work involves paying for private licenses, the worker either eats the cost or passes it through to the company, like any number of other expenses.  Like a technical book, a conference ticket, a keyboard, or an app.

Abstracting the licensing transaction away from management's point of view doesn't mean the licensing transaction disappears for developers.  Rather, developer-to-developer licensing becomes something that developers handle among themselves, primarily as a matter between peers.  Identity remains independent of affiliation, [as on GitHub, npm, and other current-generation platforms](https://blog.licensezero.com/2017/10/16/mercenary-rapport.html#everyone).

## Who's responsible?

As with open source licensing, private licensing between developers tends to shift more decision making to developers.  As with open source licensing, the abstraction leaks a bit.

Companies need to ensure they have all the intellectual property rights they need for themselves and for their customers.  Diligent companies want to scrutinize the terms of licenses, be they public open source licenses or private License Zero licenses, that affect whether employees and contractors can meet their obligations to assign or license all the intellectual property rights needed for their work.

License enforcement is rare, across the board.  Legally, both developers using License Zero projects and companies expecting to be sublicensed could be sued for infringement without a valid license.  Practically, we would expect companies to receive more complaints and demands for payment than individuals, because companies tend to have more money to pay.  Practically, we would also expect most complaints to end in settlement, rather than in court.  Practically, it will be pretty difficult to tell whether a company or customer has some relationship with a developer who has a private license.

Hopefully, not much of that would matter.  Developer licensing might help to avoid the legal system---lawyers, cease-and-desist letters, and the like---by giving developers larger roles in the process.  Many license violations, like failure to provide attribution under permissive licenses, get sorted out on GitHub and via e-mail, by developers.  Reputation, correctness, and a sense of fair play go a long way.
