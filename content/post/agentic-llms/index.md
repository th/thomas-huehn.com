---
title: "Agentic LLMs"
description: ""
date: 2025-06-19T18:24:52+00:00
tags:
  - llm
aliases: []
featured_image: ""
---
I feel a bit late to the party, but after some time with Claude Code, I like agentic LLM systems. It’s really no comparison to CoPilot or a web chat interface.

Of course, you save copying and pasting error messages and the like, because the agentic systems just reads them and fixes the code. But that’s not even it. It’s much more ergonomic for complete workflows. A chat interface could give you instructions, but then only the happy path (probably), and you’re back to typing what you’re seeing. An agent sees the result itself.

And it can use tools! I don't mean fancy MCP servers and stuff, I mean grep. Or sed. Or ls. I’ve seen multiple times now that Claude Code got confused about the project's structure, but I didn’t have to do anything. It just did a few ls or git rev-parse HEAD, and off it went again.

Apropos tools: I told it in the CLAUDE.md file about a few tools I have installed (ripgrep), and it uses them. It may have tried it anyway, at least some other time I saw an amusing sequence "using Imagemagick"—"not installed"—"using $othertool"—"not installed"—"let’s write a Python script". And that’s the best part. It writes one-off scripts, mostly in Python, sometimes in bash. Usually it deletes them afterwards, but I told Claude Code to put them in a special directory and keep them. You never know when you might use them yourself. 

Today I used it for something conceptually simple, but I really wasn’t looking forward to it: I have two statically generated weblogs with almost-but-not-quite the same templating, and wanted to extract those two nearly identical templates into its own theme. Claude didn’t get through it completely on its own, in the end I had to remind it that soft-linking the theme’s repo on my disk isn’t so clever, but it obligingly made a git submodule out of it.

git submodule. How I dread that phrase! But now git is easy, no matter how inconsistent its commands and arguments are. I just tell Claude Code precisely (with all the “professional git terminology”) what I want. And it shows me the proper command. For anything more complicated than what I know by heart or what lazygit surfaces, Claude Code will be my git porcelain in the future. Also for ffmpeg, I think.

I haven’t really used it for programming so far, for want of a personal side project that involves a lot of programming, but right now I’m not so much interested in vibe-coding (although it might help *tons* at work — think about weird Artifactory or proxy errors that it might just solve itself). I’m more interested in having the LLM be more of a low-key data wrangling and shell driving agent.

