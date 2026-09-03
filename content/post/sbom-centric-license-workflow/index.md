---
title: "SBOM-centric license workflow"
date: 2026-08-29
tags: 
  - sbom
description: "Having an SBOM-centric license compliance workflow sounds good to me."
image: ""
aliases: []
---
The idea about an “SBOM-first” or maybe even “SBOM-only” workflow already [teased earlier](https://www.thomas-huehn.com/sbom-centric-workflows/) still appeals to me.

In principle I don’t see why it couldn’t work, but I haven’t put it in practice, yet.

My thinking is mostly CycloneDX-centric since that’s what I'm using right now. Generally, CycloneDX has free-form key-value properties where you can put everything SPDX-specific into, and SPDX has the CdxPropertiesExtension which is basically the same, so *if* you control the tooling you can do anything in either formats.

Several thoughts and questions:

1. All tools love to emit SBOMs, especially in the security field. Few tools like to use existing SBOMs and *enrich* them. SBOM import ist often just reading out components and never looking at the provided SBOM again or reusing any other information from it. Do you know a public enrichment tool or framework other than parlay?

2. In CycloneDX tools like FOSSology seem to model files (component type = file) as siblings to packages (component type = library) and then model references between them. I don’t understand why. SBOMs should be flat, yes (don’t model your internal software architecture, please), but in CycloneDX the members in the components array can simply declare their own components array, making the association between files and packages very clear and nice to parse out again.

3. CycloneDX has component attributes for licenses, license texts, copyright notices, and even evidence. You can put the complete ScanCode output in the latter, so that the concluded license is traceable and reviewable at a later point.

4. Speaking of which: I have no qualms about putting 12k lines of ScanCode output into every SBOM component, but people look at me funny. Do downstream tools choke on large SBOMs? What is large? Compared to RAM in even old computers SBOMs are tiny.

5. I don’t think an SBOM alone is really enough to fulfil license obligations, but you're only a pretty simple Python script away from README_OSS.txt, web pages and whatever you want. If *everything* is in the SBOM.

6. Is there a good JSON viewer that understands SBOMs and allows filtering for licenses, copyrights, jumping to the next component etc.? Does everyone just use VScode?
