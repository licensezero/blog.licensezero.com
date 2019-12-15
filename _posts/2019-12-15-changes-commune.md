---
title: No Private Changes in the Commune
description: RMS and Linus both wanted patches back
---

Before the Free Software Foundation, before the GNU General Public License, before the GOSMACS kerfuffle and the LISP Machine Wars, Richard Stallman was benevolent dictator of the Emacs Commune.  Stallman shared Emacs freely, but demanded that patches and improvements be sent back to him, so that he could share them with others.

Emacs, short for "editor macros", had grown up as a set of programmable macros for TECO, an early text editor.  Another hacker, Carl Mikkelsen, had added a command to TECO supporting real-time, interactive input and display.  Stallman extended that facility with programmable macros, creating the first programmable interactive text editor widely available.

But hackers' zest for customization led to incompatibility.  One hacker could no longer sit down before another hacker's editor and just start getting work done.  They had to learn all their macros first.  Seeing this, Guy Steele set out to synthesize a common macro set.  Stallman took that project up and completed it.  Emacs was born.

In order to prevent hackers erecting another "tower of babel" by rampant, wayward customization, Stallman announced what he called the "Emacs Commune".  The Emacs Commune offered no software license---that was still to come---but RMS expressed and enforced terms of membership, of access to Emacs.  As Stallman wrote later:

> Emacs was distributed on a basis of communal sharing, which means all improvements must be given back to me to be incorporated and distributed.

All commune members were free to patch Emacs, but they had to send their patches back to Stallman.  The largely unremarked "fifth freedom" of later RMS doctrine---the right to make and use private, closed changes, even within sprawling for-profit organizations---wouldn't appear until later.

As Sam Williams recounts in [_Free as in Freedom_](https://www.oreilly.com/openbook/freedom/ch09.html):

> Where he had once demanded that Commune members publish any and all changes, Stallman now demanded publication only in instances when programmers circulated their derivative versions in the same public manner as Stallman.  In other words, programmers who simply modified Emacs for private user no longer needed to send the source-code changes back to Stallman.  In what would become a rare compromise of free software doctrine, Stallman slashed the price tag for free software.  Users could innovate without Stallman looking over their shoulders just so long as they didn't bar Stallman and the rest of the hacker community from future exchanges of the same program.
>
> Looking back, Stallman says the GPL compromise was fueled by his own dissatisfaction with the Big Brother aspect of the original Emacs Commune social contract.  As much as he like peering into other hackers' systems, the knowledge that some future source-code maintainer might use that power to ill effect forced him to temper the GPL.
>
> "It was wrong to require people to publish all changes," says Stallman.  "It was wrong to require them to be sent to one privileged developer.  That kind of centralization and privilege for one was not consistent with a society in which all had equal rights."

I've [written about the fifth freedom before](https://blog.licensezero.com/2018/09/14/free-to-take-freedom.html#extra-freedom).  I still don't understand it.

Stallman's quote above offers two justifications for compromising prior principle.

One is conclusory: "It was wrong to require people to publish all changes."  In support, RMS offers not a reason, but a vague notion that it might be used for ill, backed by name-calling.  To give credit where due, this was self-criticism.  If there was a "Big Brother" of the Emacs Commune, it was RMS himself.

The second argument for private changes comes somewhat more fleshed out.  Requiring patches back to one privileged developer works centralization and inequality.  Centralization and inequality are bad, so requiring patches back to one developer is bad.

[Parity 7.0.0](https://paritylicense.com/versions/7.0.0.html) requires sharing back, whether you "distribute" or not:

> Contribute software you develop, operate, or analyze with this software, including changes or additions to this software. When in doubt, contribute.

Parity also includes instructions for how to "contribute" software.  Those instructions require making code available not just to the original author or official project, but to everyone:

> Publish all source code for the software in the preferred form for making changes through a freely accessible distribution system widely used for similar source code so the contributor and others can find and copy it.

Parity doesn't reach prototypes:

> You don’t have to contribute any change, addition, or other software that meets all these criteria:
>
> 1. You don’t use it for more than thirty days.
> 2. You don’t share it outside the team developing it, other than for non-production user testing.
> 3. You don’t develop, operate, or analyze other software with it for anyone outside the team developing it.

As a result, Parity _doesn't_ give the right to hover over the shoulder of everyone hacking your code.  But as soon as a prototype becomes more than a prototype, as soon as it begins affecting the software world and software users, it must be shared.

It's not a matter of whether the work is "public" or "private".  That's circular: public things should be shared and private things shouldn't.  A license like Parity treats some code as public and some code as private based on its real and potential effects.  "Prototype" draws that line in practical terms.  "Private changes" tries to draw it in terms of pure ideology, and reduces to pure tautology.

All of this was apparently lost on Linus Torvalds.  From his own words, it seems clear Linus wanted more or less what RMS had wanted.  He wanted a commune.

> I wanted people to be able to see it, and to make changes and improvements to their hearts' content.  But I also wanted to make that what I got out of it was what they were doing.  I wanted to always have access to the sources so that if they made improvements I could use those improvements myself.
>
> --- Linus Torvalds, _Just for Fun_

That is not what GPLv2, the license Linus ended up taking from Stallman, says.  And Linus has become aware.  But whatever the rules of the license he picked---and is now stuck with---he knows and expresses the rule he wants:

> You don't have to use Linux.  If you do use Linux, the only thing I ask for is source code back.  And then there's all the other verbiage in the GPL version 2.0 about exact details, and those aren’t important.  And that was always my standpoint.
>
> --- [Linus Torvalds at DebConf 14](https://youtu.be/1Mg5_gxNXTo?t=47m20s)

There is nothing wrong, nonfree, closed, or proprietary about wanting a commune.  Parity can help you express what you want in license terms.