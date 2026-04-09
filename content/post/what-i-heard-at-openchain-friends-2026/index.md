---
title: "What I heard at OpenChain & Friends 2026"
date: 2026-03-30T19:46:55+02:00
tags:
  - conference
  - open source
  - sbom
  - security
description: "Stuff people said at OpenChain & Friends 2026."
image: ""
aliases: []
---
These are some things I heard (and some things I said) at last week‘s OpenChain & Friends Event in Stuttgart. The quotes are approximately correct, but not necessarily absolutely literal. Since the event operated under Chatham House Rules, even speakers I know the name of are not credited.

# Open Source
**What I heard:** the claim in the MG lawsuit (missing license text and copyright notices in an electric car) is wholly based on the Rechtsmangel of § 435 BGB (German civil law; defect of title in US law). It is especially not based on the third-party beneficiary doctrine advanced by Software Freedom Conservancy against Vizio (and its German analog advanced in the AVM case). That is because a Rechtsmangel is a very strong lever, since reimbursement of the buying price can follow. For expensive items like a car this will make manufacturers pay attention.<br>
**What I heard:** what we’re trying: every customer can get his money back, if he finds only one flaw in license compliance

**What I heard regarding the chardet issue:** we believe courts will look at the process, not just the results<br>
This is speculative.

**What I heard:** Samsung is very good with Open Source license compliance for their phones. You write them asking for source code, and get a 3 GB source code archive, no questions asked.<br>
**What I heard:** Another participant confirming that experience<br>
**What I heard:** Huawei is also very good in that regard.

**What I heard:** If you only distribute a Dockerfile, not the software itself, do you need to distribute compliance artefacts for the software?<br>
The whole questions revolves around who is in control of the software download (=distribution). It happens on the user‘s PC, after the user issues a “docker build”, but if you assign control over downloading to the Dockerfile‘s author (and there‘s a good argument to be made), the Dockerfile must be accompanied by compliance documents like copyright notices and license texts.

**What I heard:** Mercedes-Benz has open sourced their compliance tooling. Internally it is called disko, but that is bad branding clashing with other things, so they called their external project disuko (Japanese for disco). The u is silent, so it‘s disco again.

# AI
**What I said:** how can tech companies ever sue for copyright infringement again? The defendent will immediately point to press interviews of tech companies‘ management saying that substantive portions if their code is AI generated. And AI generated code enjoys no copyright protection.<br>
**What I heard:** if you want code that‘s copyrighted, document every step..<br>
**What I heard:** “If you cannot solve the problem, make it someone else‘s problem” (contractually).<br>
**What I said:** Do companies track what code portions were human-written?.<br>
**What I heard:** When our company introduced CoPilot all generated code blocks were (automatically?) marked with comment blocks. That policy was rescinded later.

# Cybersecurity
**What I heard:** It is important to integrate your supply chain into your supply chain security.<br>
That means you should talk to your suppliers. But what I thought is, yeah, if you‘re top of the food chain that‘s cool. Otherwise you get integrated in someone else‘s supply chain. Or to be more precise: into multiple someones elses‘ supply chains.

**What I heard:** fast-fashion software.<br>
This term does not refer to vibe-coding, but to the practice of dropping code and not caring about further maintenance.<br>
**What I heard:** You create it and you dump it after release.<br>
This was in the context of the Software Defined Vehicle, and it made me gulp.

**What I heard:** I’m not a fan of responding to complexity with complexity.<br>
**What I heard:** But we must fight AI (offensive) with AI (defensive). There is no other way.<br>
It's all about speed now, not about accuracy.

**What I heard:** Use the OSPO route for security contact, because it‘s close to engineering.

# SBOM
**What I said:** a JSON file is a bad source of truth<br>
**What I heard:** JSON in git is nice for business continuity<br>
**What we agreed on:** as an archival/backup option, it is a good last resort

**What I said:** Every tool wants to create an SBOM, no tool wants to read an SBOM. Tools that take an SBOM as input just use it as a flat package list and throw away all other information.<br>
**What I heard:** Yes. But one reason is that there is so much variation in parsing SBOMs. There are at least 7 ways to map a very simple Maven app with only one dependency to an SBOM.

**What I heard about SPDX 3:** This is a graph database. Is that what we need?<br>
**What I heard:** It‘s too heavy and Google-scale.<br>
**What I heard:** People have lower goals, they are happy they made an SBOM.

**What I said:** It’s too bad that SBOM people start their explanations usually with taxonomy. Is anybody even using design SBOMs?

**What I heard:** OpenChain has a project called SBOM-sg-SEPIA. It can be used to validate SBOMs (probably against the telco quality guide and NTIA Minimum Elements), converting between formats, and merging SBOMs.

# Stuff
**What I thought:** It used to be cool to say “talk to my agent”…
