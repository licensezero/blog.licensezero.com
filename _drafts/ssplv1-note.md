---
title: A Quick Note on SSPLv1
description: pushing the same limit for very different reasons
layout: post
---

Many readers will have seen MongoDB's announcement of the [Server Side Public License, Version 1](https://www.mongodb.com/licensing/server-side-public-license), a new copyleft license applied to the MongoDB database.  SSPLv1 is based on the AGPLv3, the Free Software Foundation's network-copyleft license.  MongoDB has submitted SSPLv1 to the Open Source Initiative for review.

Commentators have drawn comparisons to the License Zero Reciprocal Public License (L0-R), predecessor to the [Parity Public License](https://licensezero.com/licenses/parity), one of the two public licenses developers can use through License Zero.  I submitted L0-R to the OSI last year.

Parity and SSPLv1 both push the boundaries of strong copyleft in open source licensing.  Both require sharing back more code in more situations than AGPLv3, OSL 3.0, or even RPL 1.5.  Both were drafted with software businesses and business models in mind.

Parity and SSPLv1 differ in a number of ways, but the most important is when their stronger copyleft terms apply.  Parity requires contributing code back in all cases that GPLv3 and AGPLv3 do, and then some.  SSPLv1 requires sharing code in many cases that AGPLv3 does not, but also does _not_ require sharing code in many cases that AGPLv3 does.  SSPLv1 is a strong copyleft license, but also a selective copyleft license.  For some use cases, SSPLv1 is designed to work like a permissive license.

Those who favor Parity and those who favor SSPLv1 therefore share an interest in common.  Both licenses want to establish that open source copyleft can require sharing more code back, and in more situations.  But they address fundamentally different use cases, and different licensing user bases.

SSPLv1 is optimized for companies maintaining open source applications, like databases, as loss leaders for service offerings, like managed Redis hosting.