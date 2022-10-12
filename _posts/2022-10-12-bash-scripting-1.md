---
layout: post
title:  "Bash Scripting - 1"
date:   2022-10-12
category: BASH
permalink: /bash/:title
---

Post contains only Bash script sample.

`hello_bash.sh`

{% highlight bash %}

#!/bin/bash
echo "Hello, Bourne Again Shell!"

{% endhighlight %}

`variables.sh`

{% highlight bash %}

#!/bin/bash
FIRST_NAME="Sajid"
LAST_NAME="Hasan"
LOCATION=London
FILE_LOCATION=`pwd`


echo My name is $FIRST_NAME $LAST_NAME
echo "Friends call me $FIRST_NAME!"
echo "I am based in ${LOCATION}"
echo $FILE_LOCATION
echo Name of this file is $0
echo "This file is located in directory $FILE_LOCATION"
echo "Other files in this directory: $(ls)"

{% endhighlight %}

`variable_arguments.sh`
{% highlight bash %}

#!/bin/bash
echo "Name of the file $0"
echo "Given name: $1"
echo "Surname: $2"
echo "Number of arguments: $#"
echo "List of argument(s): $@"

{% endhighlight %}
