---
title: 'SBOM-centric workflows'
description: "Musings on SBOM tooling."
date: 2025-02-23T16:19:00+00:00
tags:
  - sbom
---
I‘m a bit surprised that in the world of SBOM tooling many tools seem to insist on creating a whole SBOM and thus giving me yet another, but incomplete view of my software. Something like Yocto I understand, it really has the structural information and complete view needed to create an SBOM and is the starting point. But then fossology scans for licensing information and… I have another SBOM. ScanCode… yet another SBOM.

Why don‘t they by default (fossology can import SBOMs, but it seems to be not a core workflow) accept an SBOM as input and **enrich** that SBOM with their additional information?

Sure, identifying components with one another is hard (the naming problem) and not completely solved with PURLs or CPEs, but I‘d be willing to click the mapping manually in some tool, if every tool played together in one SBOM file.

There is [Parlay](https://github.com/snyk/parlay), but it can mostly enrich with its commercial backer’s service, and precious little else.

Do people have SBOM-only workflows that are pipelines adding successively more information to a single SBOM, and where the SBOM is the single source of truth, not some external tool’s database? And does it somehow work without magic [jq](https://jqlang.org/) invocations, but some reliable enrichment or augmentation framework?
