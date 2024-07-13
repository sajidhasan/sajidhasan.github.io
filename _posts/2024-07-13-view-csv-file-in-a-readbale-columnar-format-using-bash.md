---
layout: post
title:  "View CSV files in a readable columnar format using Bash"
date:   2024-07-13
category: bash
permalink: /bash/:title
---

To view a CSV file in a more readable columnar format, the `column` command can be used combined with `cat` and `tr`.

#### Command to read CSV file
{% highlight bash %}
   cat file.csv | tr ',' '\t' | column -t -s $'\t' | less -S
{% endhighlight %}

#### Explanation
`cat file.csv` reads the content of the CSV file. `tr ',' '\t'` replaces commas with tabs.

`column -t -s $'\t'` formats the output into columns using tabs as the delimiter and finally, `less -S` pipes the formatted output into `less` for easy navigation, with the `-S` option enabling horizontal scrolling.

Replace `file.csv` with the actual CSV file.

