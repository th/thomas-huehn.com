---
title: "Beautifully illustrated children's books"
description: "I curated a list of beautifully illustrated childrens' books."
date: 2019-08-11T22:00:00+00:00
tags:
  - book
---
Back in 2015 [DanBC](https://news.ycombinator.com/user?id=DanBC) [wrote on Hackernews:](https://news.ycombinator.com/item?id=9848031)

> 2\) I buy many books for my child. Amazon is pretty hopeless at recommending books to me, even though I've seeded it with knowledge of the books I've bought. So I turn to human curation: the Kate Greenaway medal focuses on excellent illustration in books for children. That list is an excellent source for books. Then one or two degrees of separation (eg, other books the illustrator has worked on, or other books the author of the winning book has written) get you hundreds of excellent books. Someone scraping this list and using affiliate links could probably make a bit of passive income.

I finally got around [to doing something like that](https://www.thomas-huehn.de/schoene-kinderbuecher/) (although it's in German and won't help him much).

I started, as he recommended, with the Kate Greenaway Medal, and the Caldecott Medal as the American counterpart. Unfortunately, many or even most of these books were never translated into German.

I perused the laureate lists of some German awards, as well. The protestant church has one or two awards in that general space, the state of Northrhine-Westphalia has another.

Everything was done manually (and took much longer than I expected): Browsing award lists, collecting the information, writing HTML and CSS, finding out what the books are about. No neural networks involved…

What I found out doing this:

1. People block ads. *I* block ads. And I was wondering why those Amazon image links didn't work. Until I remembered uBlock Origin. And then remembered Privacy Badger. And then remembered my Pi-Hole.

   So my solution was to download the cover images and host them myself. Under Amazon's affiliate terms  I'm allowed to download no more than 100 images. I have 66. So there goes "hundreds of excellent books".

   (At first I wanted to stay ad-free, because I don't see a lot of ad income here, but writing to all the publishers asking for permission to use their cover images? No, thank you, Amazon Partnernet is giving me blanket permission – with harsh restrictions, of course).

2. Web design is a catastrophe. I took it as an excuse to learn a little bit of CSS Grid or Flexbox, failed with both for a long time, then combined both. And in the end I had to give special treatment to IE11, because it should work with prefixes, but everything was on top of everything else and I did not feel like spending another evening on that problem.

3. Even if it weren't a catastrophe, I'm no designer. I tried to make the web page a bit less cliché "Hacker News minimalist". It's astonishing how much of a difference a simple box shadow with rounded corners makes!

4. Regarding "affiliate links could probably make a bit of passive income", I doubt it will be even in the "a coffee a day" range. There are many blogs and sites reviewing children's books, I have absolutely no talent for marketing, and I'm not well-known.

   I may throw twenty Euros at Google or Facebook ads, more because I'm interested how the advertiser point of view is than because I think it'll help much.

5. Book descriptions are *hard.* Especially when you don't have the book physically present. My descriptions are short and pretty anodyne. You'd think I had just looked at the covers. But I did read lots of reviews, trying to get the gist. Sometimes it was impossible.

6. My privacy statement is probably still not good enough, though at least understandable by a layperson. When you start putting affiliate links to web pages you feel some urgency to get that right. And I like the &lt;details&gt; tag, it gives you a nice click-open arrow without any Javascript.

When I told him about my site, DanBC graciously commended me on it and suggested I submit it as an Show HN.

Unfortunately, that's out of the question, since only things that can be "tried out" are allowed there, not just any web page that happens to be written by a regular. A normal submission is also futile, I guess, because foreign language submissions are kind of pointless.
