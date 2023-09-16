---
layout: post
title:  "Connfigure VIM to Show Line Number"
date:   2023-09-16
category: VIM
permalink: /vim/:title
---

Use `:set number` command within the editor to see the line numbers in the vim editor. This should work as a temporary solution.

For vim to show the line number permanently it has to be configured from `.vimrc` so that it show the line number in the editor.
One need to edit the `.vimrc` file to add `set number`.

`.vimrc`

{% highlight bash %}

set number

{% endhighlight %}

`.vimrc` file is usually located in the `home` directory. To go to home directory use command `cd ~`. So, the vimrc file directory would be `cd ~/.vimrc`.