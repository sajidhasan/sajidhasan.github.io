---
layout: post
title:  "Hands on grep practical examples"
date:   2023-10-08
category: bash
permalink: /bash/:title
---


`grep` is a powerful command-line utility for searching text using regular expressions. Here are few practical `grep` command examples for various scenarios:

#### Search for a String in a File
{% highlight bash %}
   grep "search_term" filename
{% endhighlight %}

#### Case-Insensitive Search
{% highlight bash %}
   grep -i "search_term" filename
{% endhighlight %}

#### Count the Number of Matches
{% highlight bash %}
   grep -c "search_term" filename
{% endhighlight %}

#### Search Recursively in a Directory
{% highlight bash %}
   grep -r "search_term" directory/
{% endhighlight %}

#### Search for Whole Words Only
{% highlight bash %}
   grep -w "word" filename
{% endhighlight %}

#### Search for Inverted Matches (Lines Not Containing)
{% highlight bash %}
   grep -v "search_term" filename
{% endhighlight %}

#### Display Line Numbers with Matches
{% highlight bash %}
   grep -n "search_term" filename
{% endhighlight %}

#### Search for Multiple Patterns (OR Logic)
{% highlight bash %}
   grep -e "pattern1" -e "pattern2" filename
{% endhighlight %}

#### Search for a Pattern in gzip File
{% highlight bash %}
   zgrep "search_term" filename.gz
{% endhighlight %}

#### Search for Lines Matching a Regular Expression
{% highlight bash %}
    grep -E "regex_pattern" filename
{% endhighlight %}

These examples cover a range of `grep` functionalities, from basic string searches to more advanced usage like regular expressions, case-insensitive searching, and searching in compressed files. You can adapt these commands to suit your specific needs when working with text data on the command line.
