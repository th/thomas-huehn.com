---
title: "Protecting copyright with AI"
date: 2026-04-07T16:00:00+02:00
tags:
  - llm
  - law
description: "How can you protect your copyright in the age of LLM generated code?"
image: ""
aliases: []
---
I'm still thinking about something I touched on in [the OpenChain & Friends post](/what-i-heard-at-openchain-friends-2026/#ai):

AI generated code isn't copyrightable, because only human creations are eligible for copyright. In the past that used to be easy. Who if not a human programmer could have written the code? Today LLMs generate large parts of many code bases. 

And saying that I as a human reviewed every single line doesn't count. The generative work, the concrete expression of the output is protected, not the after-the-fact approval.

So how do large companies expect to ever do copyright litigation again? Because in pretty much all jurisdictions you will have to at least make your claim plausible before the defendant even has to reply. Imagine you copy some Microsoft mobile app. No AI rewriting, just a plain copy. Microsoft sues you.

You will certainly break out all those press interviews with Microsoft's managers, all those news postings how they are ahead of the AI curve and use LLMs all the time for all of their code bases. And the incentive has been strong to exaggerate wildly, just to look future-proof. It doesn't have to be Microsoft. Most even vaguely tech-related companies have probably made claims like these, if only in the local press. Microsoft will have to show that their app is even copyright protected.

And now what? Of course, just having some human-written code is enough for some protection. But how do they plan to do even that little bit?

Sure, if you did not switch off the “Co-Authored-By: Claude Code” line in commit messages, you have a way to at least find out which commits were AI generated. But OpenAI Codex does not mark its commits like that, and many developers simply use CoPilot in their IDE and commit under their own name. So having a human's name as the commit's author isn't terribly conclusive, either. And if you intend to sue, you'll have the burden of proof.

Marking LLM generated parts of the source code seems prudent. But current tooling does not do it by default. Anecdotally I've heard that a large German Company enforced such automatic “AI generated“ comments when introducing CoPilot, but they have since given up on that.

Is it simply of no concern to the big tech companies, because code is cheap now and all that matters is velocity? So that copying something wholesale isn't even that big an advantage compared to generating new code that does something similar? Doesn't seem satisfactory, though.