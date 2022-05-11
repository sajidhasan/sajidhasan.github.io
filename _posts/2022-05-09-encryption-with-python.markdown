---
layout: post
title:  "Encryption with Python"
date:   2022-05-09
category: Algorithms
permalink: /algorithms/:title
---

SHA256 is a set of cryptographic hash functions that produces 256 bits hashed value. It was designed by United States National Security Agency.  

The following code converts text data to SHA256 encrypted data.

{% highlight python %}
import hashlib
a_string = 'BATMAN'
hashed_string = hashlib.sha256(a_string.encode('utf-8')).hexdigest()
print(hashed_string)
{% endhighlight %}