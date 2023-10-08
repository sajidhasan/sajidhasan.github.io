---
layout: post
title:  "Add abbreviation in vim"
date:   2023-10-08
category: bash
permalink: /vim/:title
---

Abbreviations in the vim editor saves you from typing the same thing repeatedly.

`.vimrc`

{% highlight bash %}

iabbrev plbang /usr/bin/perl
iabbrev shbang /usr/bin/bash

{% endhighlight %}

`.vimrc` file is usually located in the `home` directory. To go to home directory use command `cd ~`. So, the vimrc file directory would be `cd ~/.vimrc`.