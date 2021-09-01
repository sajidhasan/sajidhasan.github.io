---
layout: post
title:  "Finding the factors of a number in O(sqrt(n))"
date:   2019-04-08 06:20:00
category: Problem Solving
permalink: /problem/:title
---

Given an integer, write a function to find if it is palindrome or not.

* Input: 121
* Output: true


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



