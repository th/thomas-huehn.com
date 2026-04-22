---
title: "What I heard at the Legal & Licensing Workshop 2026"
date: 2026-04-22T12:14:09+02:00
tags: 
  - conference
  - open source
  - sbom
  - llm
  - law
description: "Stuff people said at the Legal & Licensing Workshop 2026."
image: ""
aliases: []
draft: false
---
These are some things I heard at last week‘s FSFE Legal & Licensing Workshop in Berlin. Since the event operated under Chatham House Rules, nobody is credited.

# Open Source
**What I heard:** Software Heritage is going to scan the whole archive for licensing and vulnerability information. At least a ScanCode scan will be done (I think being managed with the Open Source Review Toolkit). They have only one-time access to a French supercomputer and are asking for use cases and kinds of metadata that people find useful.

**What I heard:** A huge ScanCode improvement may be in the works.<br>
*I have no further information, and it's not my story to tell anyway.*

**What I heard:** There is an unfair business practices based lawsuit about Open Source licensing currently in Germany.<br>
*I have long wondered why nobody seems to go that route. Asking around, the German lawyers said that it is a viable route, but rarely attractive.*

**What I heard:** Vizio has challenged the tentative ruling, so the third-party beneficiary doctrine is still in play.<br>
*The tentative ruling was mostly a win for Software Freedom Conservancy, but it was declining to apply the third-party beneficiary doctrine for procedural reasons. But that is the whole point of the lawsuit!*

**What I heard:** Lawyers comments on [Chan-jo Jun's lawsuit](https://www.thomas-huehn.de/lizenzverstoss-als-rechtsmangel/) about the Chinese electric car ranged from “I would argue exactly the same way” to “it's not that simple, and the case looks like marketing for the law firm to me.”<br>
*I cannot offer a well-founded opinion myself.*<br>
**What I heard:** The Chinese automotive industry has been alerted by that case.

**What I said:** “With the CRA requiring manufacturers to upstream security fixes, and the draft guidance requiring them to use a “license acceptable to the project”, isn't that kind of the first statutory copyleft?”<br>
*All of the lawyers I asked laughed and agreed. [I'm aware there are nuances,](https://www.thomas-huehn.com/statutory-copyleft/) and it is only half-serious, but I stand by it.*

**What I said:** A technology lawyer stood up, telling his experience with AI rejecting his prompt presumably for copyright reasons, and said it was his [“printer moment”,](https://www.fsf.org/blogs/community/201cthe-printer-story201d-redux-a-testimonial-about-the-injustice-of-proprietary-firmware) and that he now understood the philosophical underpinnings of Free Software much better.

# AI
**What I heard:** AI-generated code will probably turn out to be non-copyrightable.<br>
*That's in America and Europe.*<br>
**What I heard:** AI-generated works will probably be copyrightable in China on a case-by-case basis, if there is substantial original contribution by a natural person. That model's user has got copyright, not the model or the model's designer.<br>
*Several cases were shortly presented: Ultraman, Medusa, SpringBreeze, Cat crystal pendant*<br>
*The courts seem to consider whether a model's user claiming copyright can almost identically reproduce the works. It has gone so far that claimants submit video footage of AI interactions and prompting.*

**What I heard:** Maybe we should take a copyright minimalism stand in the AI age. Isn't overcoming copyright what the movement once stood for?

**What I heard:**
You could re-implement the Apache webserver using AI, but why would you? Maybe trusted communities become more important.

**What I heard:** Marking/tagging of AI-generated code is important.Developers don't like source code comments, because it clutters the source, so they use commit messages and pull request messages.<br>
**What I heard:** This works only if inserted automatiacally, so that the deduction “no tag --> written by human” is correct.<br>
*I repeatedly [talked about that,](https://www.thomas-huehn.com/what-i-heard-at-openchain-friends-2026/#ai) and it's the second time I've heard of a company doing that. The speaker strongly suggested everyone apply this strategy.*<br>
**What I heard:** When the whole file is AI-generated, best not include a copyright header.<br>
**What I heard:** It also has copyright registration implications<br>
*In America copyright needs to be registered if you want to sue. I think that registration can also be done retroactively. But registering your copyright you are asked for AI contributions.*

# Miscellaneous
**What I heard:** It was bold to kick the workshop off with a presentation on quantum computing!

**What I heard:** [Cool Shirt!](https://crowdmade.com/products/pbsspacetime-unisex-with-great-power-tee)

**What I heard:** Hyperscalers can expect to have around hundreds to low thousands of PDEs (products with digital elements – what the Cyber Resilience Act regulates), tens of thousands to hundreds of thousands of component-level SBOMs that will be processed into PDE's SBOMs, and dozens of distribution points to consider.<br>
*At FOSDEM 2026 Deutsche Bahn said they handle around half a million SBOMs.*

**What I heard:** Not using Word may be malpractice.<br>
*In a discussion about replacing Word with LibreOffice in law firms*

**What I heard:** It's a bit uncomfortable to have a big-tech sponsored event in a space that explicitly sprang up from resistance against a big-tech office in the neighbourhood.

**What I heard:** It's important to frame questions ourselves. When it comes to end-to-end encryption many people think devices should be scannable by authorities, in order to keep children safe.<br> Reframed: But children will send pictures they probably shouldn't. Let's not have those pictures in a government database.
