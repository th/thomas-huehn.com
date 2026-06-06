---
title: "Rationales for Standards"
date: 2026-06-06T09:50:59+02:00
tags:
  - standardisation
description: "Few standards have rationales available. But they would be really helpful."
image: ""
aliases: []
draft: true
---
Some working groups for the standardisation of programming languages (like [Ada](http://www.ada-auth.org/standards/rationale12.html) or [C](https://www.open-std.org/jtc1/sc22/wg14/www/docs/n802.pdf)) publish rationales. They explain the broader goals of their respective standard (or the current iteration of the standard), roads not taken, non-obvious problems with other approaches, and so on. Of course, they are only informative, not normative, because you want the normative part to be rather concise. That's not only because normative parts carry greater burdens of effort, but also because you want to make sure that explaining things in an easier way or giving a second, duplicative approach towards one issue should really not lead to contradictions.

And I really wish the security standards world would do rationales.

The rather old draft of IEC 62443-1-1 that I've seen actually had a rationale annex which was super helpful in explaining why the standard is moving from IACS (industrial automation control system) to ACS (automation and control system).

But the other parts leave questions open, at least to me. Let's look at the last -4-2 draft:

- Why has the wording in the “Protection from malicious code” requirement changed from “protect from” to “prevent and detect”? Maybe it was simply a native English speaker thinking it sounds better. But maybe – and that's my interpretation only – protection includes simply not doing anything about it, but in analysis you have concluded that for some reason (maybe even by chance) nothing bad happens. Prevention, on the other hand, means you need an active countermeasure. Detection might mean you have to diagnose the condition, and possibly signal it to another system, like a SIEM.
- Why is -4-1 basically recapitulated fully, but in abbreviated form, in thirty pages of a **normative** -4-2 annex, but formally directed at evaluators? Is it feared that companies get their process certified under -4-1, and in the product project they tell the evaluator that the process is out of scope for the current evaluation because it has already been certified? So that the working group really wanted to force product projects to prove they are following their certified project **in the concrete product project, as well?**
- Why does applicability get its own sub chapter in all the component requirements chapters, but integration into the system doesn't? Both are axes in looking at component requirements that invite discussions, especially when a component requirements feels too burdensome. Was only applicability a much debated point in practice? As an aside, how does it really fit with the applicability procedure in Annex D of the -4-1 draft, where even a clear “The requirement is applicable for all components.” (for example in CR 3.2) does not mean it really is.

Sure, if you're a member of the working group, or are reasonable close to it, you might immediately understand all those points. But I don’t, yet. And since not every company is represented in the working group (and individuals in practice have no access at all), it would be really valuable for the wider ecosystem of IEC 62443 users if the working groups would explain their thinking much more publically.