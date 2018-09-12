---
layout: post
title: Saving conda environments
image: 
tags: [Python, conda]
---

I'm trying to get into the habit of exporting my environment every time I install a new package:

`conda env export --no-builds > environment.yml`

(`--no-builds` since I'm on OS X locally and Ubuntu on AWS.)