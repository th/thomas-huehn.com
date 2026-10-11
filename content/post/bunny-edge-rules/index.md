---
title: "Edge rules in bunny.net"
date: 2026-10-11
tags: 
  - web
  - hugo
description: "I was involved in a little fight over trailing slashes with bunny.net."
---
# The problem

Yesterday my [Knuth check post](https://www.thomas-huehn.com/knuth-reward-check/) spent some time on the [Hacker News front page](https://news.ycombinator.com/item?id=50034081). The submitter left off the trailing slash, and no images were displayed. It took me a bit of time to fix the problem, and in the end I did two different things:

# The solution

First, I tried doing a redirect from slashless to trailing slash using bunny.net's Edge rules, but couldn't get it to work. How do you express “has no trailing slash” when all you seem to have are wildcards? I abandoned that idea for the moment.

Second, I fixed my Hugo markdown image render hook, so that the img  tag always uses a full path in its src attribute. I achieved this using the page bundle resource instead of the pure `.Destination`. At first I wanted to completely remove the hook, because I don't really need it anymore, but that alone did not help, which surprised me. Hugo is a beast, and it doesn't help that you find comments on the community forum that you should really put all your images into assets/, not the page bundle.

That fixed the immediate problem, but I wasn't satisfied. There are still URL variations serving the same content, like adding index.html to the URL etc. I  decied to look into Edge rules documentation a bit closer, found Lua style regular expressions (and learned that you escape magic characters using % in Lua), and in a crucial last discovery, the attribute ``{{empty}}`` that can filter out files in the “File extension” condition.

In the end I settled on this, and fingers crossed, it seems to work:

## The Edge rules

### Trailing slash
- Action: Redirect
  - Redirect URL: `https://%{Url.Hostname}%{Url.Directory}%{Url.FileName}/`
  - Status Code: `301 - Default
- Conditions (Match All)
  - Request URL (Match All): `pattern:^https?://www%.thomas%-huehn%.com/.+[^/]$`
  - File Extension (Match Any): `{{empty}}`

### Redirect index.html
- Action: Redirect
  - Redirect URL: `https://%{Url.Hostname}%{Url.Directory}`
  - Status Code: `301 - Default
- Conditions (Match All)
  - Request URL (Match Any): `*/index.html*`

It's quite possible I'll have to add further conditions to the index.html rule, there are probably still other variations of URLs that serve the same content. But for now I'm fine with it.
