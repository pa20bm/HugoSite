---
title: Topic Modeling
description: Results of my first foray into topic modeling
toc: true
authors:
  - Paul A. Anthony
tags:
  - topic modeling
categories:
series:
date: '2019-03-05'
lastmod: '2019-03-05'
draft: false
---

For my topic modeling, I chose 12 editorials from the 1960 volume of the  Firm Foundation ending on Nov. 1, the last issue published before the presidential election. I struggled to find a background reference material. Archives of the Christian Century, America, Catholic Reporter and Billy Graham’s sermons are all either unavailable or can’t be copied into plain text documents for analysis. So in the end, I just grabbed 12 editorials from another Church of Christ journal I have, the Gospel Advocate. They redesigned in the middle of the year, and the pre-redesign text is much harder to parse, so I took 12 editorials, the first few of which overlap with the dates of the Firm Foundation  editorials.

I ran both through Topic Modeling and came up with 10 groups of topics that were slightly different, although interpreting them remains something that isn’t quite clear to me.

For the FF, topics included groups centered on missionary activity (“gospel,” “community,” “northeast,” “tent making”), the presidential election featuring eventual winner John F. Kennedy and his Catholicism (“political,” “religion,” “Catholic,” “candidate”), movement-specific issues and controversies (“brethren,” “idols,” “debaters”), the alleged decline of society (“end times,” “world,” “troubled”), and calls for new subscriptions (“special,” “issue,” “subscription,” “year”).

In GA, the topic were obviously similar, although with a topic devoted to the movement’s distinctive a cappella emphasis (“music,” “singing,” “songbooks,” “instruments”) and three topics that all revolve around the dire state of society, either the threat from Catholicism personified in JFK, or “evil” and “apostasy.”

When I combined them into 20 documents and ran them through the topic modeler, it actually became less coherent, rather than more, and I’m not sure what that means.

***

**N.B.** The above steps enable Unicode Standard emoji characters and sequences in Hugo, however the rendering of these glyphs depends on the browser and the platform. To style the emoji you can either use a third party emoji font or a font stack; e.g.

{{< highlight html >}}
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>
{{< /css.inline >}}
