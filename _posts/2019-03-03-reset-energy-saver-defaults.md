---
layout: post
title: Reset Energy Saver defaults in OS X
image: 
tags: [OS X, crontab]
---

My corporate laptop has Janf on it to enforce policies from IT. Unfortunately they're not able to completely control all those policies, and couldn't figure out how to keep my sleep time from being set to 30 minutes when it is on battery power.

I have root priviledges on the laptop. I could just delete Janf (and get a phone call), or I can create a root crontab entry that forces the Energy Saver preferences to be reset to the perfectly reasonable defaults.

Open the root crontab and edit with `sudo crontab -e` and then add a line

```*/5 * * * * pmset -a restoredefaults```

Now every five minutes the Energy Saver preferences will be reset to factory defaults, no matter what Janf does. It's a bodge but it works.