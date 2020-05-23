---
layout: post
title:  "Iterating a set in C++"
date:   2020-05-23 02:20:00
category: Problem Solving
permalink: /problem/:title
---

If it is required to store unique elements in a specific order, we can use `set`. Sets are basically containers being a crucial part of C++ `STL (Standard Template Library)`.


{% highlight cpp %}

#include <bits/stdc++.h>
using namespace std;

int main() {
	set<int> st;
	st.insert(1);
	st.insert(5);
	st.insert(2);
	st.insert(4);
	st.insert(3);

	set<int>::iterator it;
	for(it = st.begin(); it != st.end(); it++){
		cout << *it << " ";
	}

	return 0;
}

{% endhighlight %}

[problem](http://codeforces.com/contest/1355/problem/A)
[solution](https://gist.github.com/sajidhasan/d705d7341e7cd587bd10999a6420f7d0)
