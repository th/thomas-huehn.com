---
title: "Answers to questions about upstreaming patches"
date: 2026-04-14T12:42:36+02:00
tags:
  - security
  - open source
description: "The EU draft guidance about the Cyber Resilience Act answers my questions."
image: ""
aliases: []
draft: false
---
Recently I wrote about discussions I've experienced about a year ago, where lawyers and open source practitioners wondered what the reporting obligations of the Cyber Resilience Act [meant in edge cases.](https://www.thomas-huehn.com/upstreaming-patches-and-cra/)

In the meantime the EU has published [a draft of a guidance document](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/16959-Draft-Commission-guidance-on-the-Cyber-Resilience-Act_en) for manufacturers. I had already read it, but did not connect it with the article I wrote in my mind. And it turns out, the EU answers those questions! Let's see what it says:

**It is not entirely clear whether this means that the security fix itself must be upstreamed, but considering the purpose of the CRA I tend to see it that way.**

> Furthermore, under Article 13(6) manufacturers that have developed a software
modification to address a vulnerability in an integrated component are required to share
that software modification (‘security fix’) with the person or entity manufacturing or
maintaining the component (‘sharing upstream’).

**If you contribute your security fix, do you need to license it? Under the project’s main license? Under a compatible license? At all?**

> Where the component is a free and open-source component, the security fix should be shared in
a manner compatible with that component’s licence, for example by sharing it under the
same licence or under a licence that allows the maintainer to distribute the fix under its
own licence.

**If the original project (say, the GitHub project) is gone, what do you do?**

> “Finally, manufacturers are also not required to report the vulnerability upstream where
the component no longer has a maintainer, or when the manufacturer has itself
duplicated (‘forked’) the free and open-source component and no longer relies on the
original maintainer for new versions or security fixes.”

**If the original project is still there, but looks like it has been inactive for years, is sending a pull request or creating a bugtracker issue enough for CRA compliance?**

I'd consider that to fall under the provisions of the previous passage, as well.

**f the project is still there, has been active fairly recently, but never replies or acknowledges your security fix, do you have an obligation to enquire further?**

> However, manufacturers are not required by the CRA to ensure that their security fixes
are necessarily accepted by the person or entity manufacturing or maintaining the
component. Nor are they required to ensure that those fixes are necessarily integrated
into the component’s code repository, for instance where the maintainer may prefer a
different option to fix the issue.

**Does that make you an Open Source Steward in the sense of the Cyber Resilience Act, with its sundry obligations?**

Nothing to find in the guidance, but probably not.
