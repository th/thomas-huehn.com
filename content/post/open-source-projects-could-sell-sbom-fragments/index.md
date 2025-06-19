---
title: 'Open Source projects could sell SBOM fragments'
description: "Musings on SBOMs and licensing woes."
date: 2025-02-17T16:08:24+00:00
tags:
  - sbom
  - open source
---
Scanning source files for licensing information (because the package managers‘ metadata is insufficient) is a lot of work, and a lot of wasted effort, because only rarely do companies pool their resources. One example is [OSSelot](https://www.osselot.org/), another is [ClearlyDefined](https://clearlydefined.io/).

But maybe Open Source projects could sell SBOM fragments, basically [a member of Components in CycloneDX](https://cyclonedx.org/docs/1.6/json/#components ) or [a Package in SPDX](https://spdx.github.io/spdx-spec/v2.3/package-information/ ) with correct licensing information:

"Instead of scanning for copyright notices and license texts yourself, just sponsor us on GitHub and get access to always up-to-date SBOM information by the people who really know what‘s inside".
