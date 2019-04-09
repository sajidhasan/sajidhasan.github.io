---
layout: post
title:  "Rotating an array A by N position"
date:   2019-04-08 06:20:00
category: Problem Solving
permalink: /problem/:title
---

Given an array A of integers. Write a function to rotate the array by n position;
* n = 1
* Input: [5, 6, 3, 2]
* Output: [6, 3, 2, 5]

{% highlight cpp %}

#include <bits/stdc++.h>
using namespace std;
//function to rotate an array
vector<int> rotateArray(vector<int> A, int n){
	vector<int> ret;
	int s = A.size();
	for(int i = 0; i < s; i++)
		ret.push_back(A[(i + n) % s]);
	return ret;
}
//driver
int main() {
	vector<int> A = {5, 6, 3, 2};
	//before rotation
	for(int i = 0; i < A.size(); i++)
		cout << A[i] << " ";
	cout << endl;
	//rotate by arbitrairy position
	int n = 1;
	A = rotateArray(A, n);
	//after rotation
	for(int i = 0; i < A.size(); i++)
		cout << A[i] << " ";
	return 0;
}

{% endhighlight %}



