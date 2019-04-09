---
layout: post
title:  "Finding the factors of a number in O(sqrt(n))"
date:   2019-04-08 06:20:00
category: Problem Solving
permalink: /problem/:title
---

Given an integer, write a function to find all the factors of the number.

* Input: 36
* Output: 1 2 3 4 6 9 12 18 36

Finding the factors of an integer can be done in some other ways too, but, this solution
has less time complexity than others.

This below algorithm runs in O(sqrt(n)).

{% highlight cpp %}

#include <bits/stdc++.h>
using namespace std;

vector<int> factors(int a){
	vector<int> result;
	int i = 1;
	while(i <= sqrt(a)){
		if(a % i == 0){
			result.push_back(i);
			if(i != sqrt(a)){
				result.push_back(a/i);
			}
		}
		i++;
	}
	sort(result.begin(), result.end());
	return result;
}

int main() {
	int a;
	cin >> a;
	vector<int> f = factors(a);
	for(int i = 0; i < f.size(); i++){
		cout << f[i] << " ";
	}
	return 0;
}

{% endhighlight %}



