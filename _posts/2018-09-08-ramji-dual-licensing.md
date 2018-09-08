---
title:  Google's Sam Ramji on Dual Licensing
description:  a very clear strategy for open source companies that is still working
layout: post
---

From [Salil Deshpande's Q&A with Sam Ramji, VP of GCP, at RedisConf17 ](https://www.youtube.com/watch?v=2PkZ3hoYIeM&t=16m):

> Deshpande:  Let's talk about AGPL.
>
> Ramji:  That's a fun topic.
>
> Deshpande:  The Redis Modules are AGPL.  There has to be some way for the commercial entity behind an open source project to make money, and that's one way.  Then there's some closed-source features in Redis Enterprise.
>
> But Google's banned AGPL.  MongoDB is AGPL, so is that a mistake, or pure genius?
>
> Ramji:  It's a case-by-case issue.  It's something that you have to look at.  What does it mean for the packager?  What are the requirements?  What does it mean to consumer software?  So I think "ban" is probably a strong word.  We're very thoughtful about how intellectual property flows between the users of the software, the virtual machines they run on, the cloud infrastructure beneath it.
>
> As you know, Mongo runs MongoDB directly on GCP as a first-class citizen.  So, these things are solvable.
>
> Often companies are running GPL have a dual-licensing strategy, so AGPL is also a mode to make sure that you can be protected and make money, because when it's hosted, if you don't want to give away those rights, then you pay for them differentially.  So it's not that different from the world of the dual-licensing GPL model that we had pre-cloud.
>
> So I think there's a very clear strategy for monetization for open source companies that is still working.  Obviously, AGPL raises the complexity of actually figuring out how to do business deals, but it's not impossible.
