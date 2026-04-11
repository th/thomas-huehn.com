---
title: "Upstreaming patches and the Cyber Resilience Act"
date: 2026-04-11T13:20:08+02:00
tags:
  - security
  - open source
description: "What are you supposed to do when upstream projects are not responsive?"
image: ""
aliases: []
draft: false
---
Article 13 (6) in the Cyber Resilience Act requires manufacturers to report security vulnerabilities they find in an Open Source component they use to the upstream project. It also requires them to share “relevant code or documentation”. It is not entirely clear whether this means that the security fix itself must be upstreamed, but considering the purpose of the CRA I tend to see it that way.

Now that's all fine when there is a clear “upstream project” and it is still active. Send a patch or a pull request, reply to further questions, done.

But we can imagine many complications, and nobody really knows what they entail. I've seen a room full of lawyers discuss the implications lively.

If you contribute your security fix, do you need to license it? Under the project's main license? Under a compatible license? At all?

And some questions about the project's state:

- If the original project (say, the GitHub project) is gone, what do you do?
- If the original project is still there, but looks like it has been inactive for years, is sending a pull request or creating a bugtracker issue enough for CRA compliance?
- If the project is still there, has been active fairly recently, but never replies or acknowledges your security fix, do you have an obligation to enquire further?

If the project is gone or inactive, a popular notion among the lawyers seemed to be that you should probably just fork the repo or create a new repo, put your fixed component there, and be done with it.

This leads to a followup question: Does that make you an Open Source Steward in the sense of the Cyber Resilience Act, with its sundry obligations?

I tend to “no”, because I see it at a one-time code drop, I wouldn't have the intention to hold myself out as the new project for that component.

But the issue of “commercial activities” on a “sustained basis” makes companies generally nervous. It is indeed not clear at all if you can just put out a code drop and forget about it if you intend to use that component on an ongoing basis.

Starting December 2027 we are going to see how companies decide to handle it in practice.
