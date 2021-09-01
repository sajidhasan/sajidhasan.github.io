---
layout: post
title:  "Integer Palindrome Checker Program"
date:   2021-09-01
category: Problem Solving
permalink: /problem/:title
---

Given an integer, write a function to find all the factors of the number.

* Input: 121
* Output: true

* Input: -121
* Output: false

{% highlight cpp %}

#include <bits/stdc++.h>
using namespace std;



bool isPalindrome(int x) {
    bool isPal = false;
    int digit;
    long rev = 0;
    int num = x;
    if (x < 0) return isPal;
    do
    {
         digit = num % 10;
         rev = (rev * 10) + digit;
         num = num / 10;
    } while (num != 0);
    
   return rev == x ? true : false;
}

int main() {
	int n;
	cin >> a;
	if (isPalindrome(a)){
		cout << "true" << endl;
	}
	else cout << "false" << endl;
	return 0;
}

{% endhighlight %}