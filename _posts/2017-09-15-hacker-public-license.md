---
title: A Hacker Public License
description: free for open source
layout: post
---

The hardest criticism of [License Zero](https://licensezero.com) to take, by far, has come from friends devoted to [Free Software](https://www.gnu.org/philosophy/free-sw.en.html). Largely thanks to their input, I'm pleased to announce a [new public license for License Zero projects](https://github.com/licensezero/licensezero-reciprocal-public-license/blob/master/LICENSE.mustache) that I think speaks directly to what they fear I've forgotten. I'll be making it available as a public license choice through the command-line interface shortly, probably behind a flag like `l0-license --reciprocal`.

# Troublesome

Free Software values are values of mine. [I still believe](https://writing.kemitchell.com/2016/05/13/What-Open-Source-Means.html). But decades of software and more recently legal practice impressed the serious and unfortunate ways in which those ideals, and implementations of copyleft, run aground on reality and their own inherent complexity. Partly out of despair for the project of righting those fundamental wrongs, License Zero as originally proposed addressed newer pangs of conscience, fallout from the relatively recent "victory" of Open Source in the commercial world.

I want to see independent developers respected and supported for the work they do. But on a more fundamental level---the one on which I'd debate how software ought to be produced, and whether it ought to accept and subvert or attack outright the frame of modern intellectual property---it felt like backsliding. An unfortunate, if expedient, concession to circumstance and limited scope.

The License Zero Public License departs from Open Source to achieve a more effective wedge driving commercial users to purchase private licenses. By doing so, it calls out current practice, which is to pick licenses, like the GPLs, that are Open Source licenses, but discourage business users in practice, and drive them to private terms. Somehow the licenses themselves aren't discriminatory under the [Open Source Definition](https://opensource.org/osd), at least when reviewed on their own terms, while the choice of those licenses is evidently discriminatory, else a well-known and celebrated Open Source business model just wouldn't work. It squeaks by today.

The License Zero Public License dove away from, not toward, copyleft, [because of its inherent complexity](https://medium.com/@kemitchell/null-value-aa4fd24e152b). Its long political history and attendant political baggage. But I'm hard on nobody like I'm hard on myself, and in the back of my mind, I heard a dare: Could I write a clear and simple copyleft license from scratch? Could the benefit of that clarity possibly outweigh the complexity cost of a new license---["unavoidably incompatible, unless they have explicit compatibility provisions"](https://www.gnu.org/licenses/license-compatibility.en.html)---to worry about?

The answer, looking at the way GPL, AGPL, MPL-2.0, and EPL-1.0 attempted to draw the line where copyleft stops and starts, was no. The balances those licenses try to strike are inherently complex, and subject to all manner of late-onset ambiguity as the ways code is written and recombined evolve. But in conversation with friends, many stalwart copyleft warrior-monks in their number, I was reminded again that those compromises aren't identical with the values Free Software hackers hold dear to faith. They're compromises, too.

# Prolific

Put all that in a pot, and stir. Out comes [The License Zero Reciprocal Public License](https://github.com/licensezero/licensezero-reciprocal-public-license/blob/master/LICENSE.mustache), a stronger-than-strong copyleft license with a 90-day grace period and an automatic fallback to permissive, two-clause BSD terms if dual licensing shuts down. This thing makes AGPL look like a kitty-cat, and the average GPL-based dual-licensing play look like a lemonade stand.

The architectural approach is fundamentally the same as the non-commercial License Zero Public License. Two-clause BSD served as starting point. From there:

1. In addition to the copyright notice, I've added a notice with the URL of a repository where the source code is available. The new source-available notice has to be retained, just like the copyright notice.

2. Use "in the execution or development of any computer program" that isn't published and licensed under Open Source terms is limited to 90 days. As with the non-commercial License Zero Public License, this condition falls away if licenses aren't available from a named agent. What's left isn't exactly two-clause BSD, because of the new source-available notice. But it's very close.

Note the copyleft trigger. It's not tied to distribution or modification, so there's no pondering to do about whether this kind of linking, that kind of packaging, use as a build tool, and so on trigger copyleft. It's not tied up in means of delivery, so there's no ASP loophole to close. Rather, it closes the "we only used our modifications internally" loophole. It closes the "we modified it, but only through its extension interface" loophole. The terms for the trigger---"execute" and "develop"---aren't broad, they're semantic black holes, and clear borrowings from industry parlance. And so much the better. Share your code or buy a license.

The kicker? I think it's Open Source, with and without the copyleft condition. The copyleft license isn't inherently discriminatory against commercial use or non-contributors, on its face. The wedge effect is all in context: commercial users stockpiling value in proprietary code, and users hoarding modifications in private code, operate models that discriminate against open development, so it's natural they'll need and want paid exceptions. But OSI approval is as much a procedural question as a substantive one, so I'm going to ask. At a minimum, that should make for some interesting mailing list discussion.

# Responsive

Developers can use the non-commercial License Zero Public License to reassert and support themselves today. For some maintainers, I think that option will send exactly the kind of message they've long wanted to express, but couldn't in any operative way. Especially for those who lean permissive in their licenses, and see today's tensions first and foremost as symptomatic of the voracious, often antisocial appetites of company-structured software consumers.

But many of the folks I've spoken to like what License Zero stands for and the direct way it's addressing problems they feel viscerally, but care first and foremost whether License Zero can help them express their more fundamental concerns about what software is. They'll freely admit that material support for inspired, independent developers is a vital problem, and one they'd like solved for themselves. But not at the expense of the greater challenge they see in intellectual property laws and their effect on software development as a culture. A few of my friends would gladly martyr themselves for that cause, economically and otherwise. Some are well on their way. Here's hoping License Zero can make that an unnecessary and fundamentally false choice.

What's more, I think an astute and workable combination of uncompromising software liberty and a robust, code-cultivating business model could welcome many who left the copyleft fold for the ease of permissive licenses, such as myself, back into the fold. It's been a long time since many of us really believed that licensing, of all things, could express and implement values that we actually care about. I'm motivated, more than by anything else, to show that power isn't lost to our community.
