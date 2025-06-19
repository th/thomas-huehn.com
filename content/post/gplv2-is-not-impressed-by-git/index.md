---
title: 'GPLv2 is not impressed by git'
description: "A strange little problem with the GPLv2."
date: 2025-03-28T16:38:08+00:00
tags:
  - open source
---
There is this strange little clause in the GNU General Public License, version 2 – but not version 3 – that pretty much everybody ignores. When distributing a modified program in source form,
> You must cause the modified files to carry prominent notices stating that you changed the files and the date of any change.

That means you must effectively maintain a changelog in the file header. Almost nobody does that. We have git and other revision control systems going back to… well, the [Revision Control System](https://en.wikipedia.org/wiki/Revision_Control_System) and even earlier. Those make it much easier and convenient to drill down into who changed what how.

But still, the clause is there. And legal commentaries do something like this about it:

1. The GPLv2 says there must be a modification notice in the modified file itself.
2. As far as we can see, our developers don’t do that, and they even laugh such a suggestion off as antiquated.
3. The use of a version control system instead does not comply with the GPLv2.
3. *shrug*

That's a rather informal summary of O’Reilly’s [“Die GPL erklärt und kommentiert”](https://www.ifross.org/Druckfassung/Die_GPL_kommentiert_und_erklaert.pdf), pages 61–63, and [“Open Source Software”](https://www.beck-shop.de/jaeger-metzger-open-source-software/product/26549144), marginal 50.
