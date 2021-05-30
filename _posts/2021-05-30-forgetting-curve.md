---
layout: post
title:  "Forgetting curve and spacing effect"
date:   2021-05-30 03:00:00
tags: ["Tech", "Science"]
---

[Memoet][0] is a free and open source spaced repetition software, and the
problems which we are trying to solve have a historical connection to the
forgetting curve and the spacing effect which was discovered by [Hermann
Ebbinghaus][1] - a German psychologist in 19th century.

![Forgetting curve][2]

> The forgetting curve hypothesizes the decline of memory retention in time, and
> the spacing effect demonstrates that learning is more effective when study
> sessions are spaced out.
>
> _- Wikipedia_

The best methods proposed by Ebbinghaus to increase the strength of memory
are:

- Better memory representation, such as mnemonic techniques

- Repetition base on active recall, especially spaced repetition


Mnemonic skills are effective but hard to attain. A more simple solution to
significantly decrease the effects of the forgetting curve is to spend time
each day to remember things.

Nevertheless, the frequency of repeating will be different depends on how new
and how hard a concept is. That's how spacing effect works and the reason we
got spaced repetition algorithms to help.

As it turned out, there are serveral families of algorithms for scheduling
repetition:

- Neural networks based

- Leitner system

- SuperMemo family, most popular is SM2, which Memoet implements.


Whatever methods you choose to combat with forgetting curve, you should make
that a daily habit to exploit the spacing effect. Oh and give [Memoet][0]
a try!


[0]: https://memoet.com
[1]: https://en.wikipedia.org/wiki/Hermann_Ebbinghaus
[2]: /assets/images/ForgettingCurve.png
