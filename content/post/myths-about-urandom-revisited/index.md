---
title: 'Myths about /dev/urandom, revisited'
description: "Looking back at my most viewed article."
date: 2025-04-13T05:06:00+00:00
tags:
  - linux
  - writing
---
[Myths about /dev/urandom](https://www.thomas-huehn.com/myths-about-urandom/) is my only post that ever got somewhat popular. It has been over ten years ago by now.

And it's incredible how much and fast the Linux kernel improves, even when things look static and resistance to change seems high. First the man pages finally, thankfully got better [1], and then Jason Donenfeld came and restructured the random number handling.

For years I had tried to keep up with the changes and update the essay. But what used to be a structured essay turned into a mess of notes, info boxes, “if kernel version > 4.8 then... else”, and “well actually”s.

It felt impossible to keep up with not only the pace, but also the scope of changes. So I reverted everything to its original 2014 version. You can still find the “newer” versions of the essay on the Wayback Machine.

[1] the German-language Wikipedia article still claims something about /dev/urandom's “pseudo” random numbers being possibly computable, but that's the usual problem of a clique of editors that consider the lemma “theirs” and all outside contributions as “vandalism”.
