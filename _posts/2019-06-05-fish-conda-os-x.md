---
layout: post
title: Using fish with OS X and conda
image: 
tags: [OS X, anaconda, conda, fish]
---

I found [this post](https://lobster1234.github.io/2017/04/08/setting-up-fish-and-iterm2/) on setting up [fish](https://fishshell.com), the friendly interactive shell, in OS X.

I followed the instructions in the post, works great.

The last thing I needed was conda/anaconda integration, since I use that for managing data science packages and environments.

It turns out it is as easy as adding `/miniconda3/etc/fish/conf.d/conda.fish` to `.config/fish/config.fish`.

Now like before I can change environments with

`$ conda activate some_env`

