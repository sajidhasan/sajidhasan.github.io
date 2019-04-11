---
layout: post
title:  "Traversing a 2D array in spiral order"
date:   2019-04-11 06:20:00
category: Problem Solving
permalink: /problem/:title
---

Given an array of dimension `m x n`, traverse the array in spiral order.
* Input: A = [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]
* Output: [1, 2, 3, 4, 8, 12, 11, 10, 9, 5, 6, 7]

{% highlight cpp %}

#include <bits/stdc++.h>
using namespace std;

vector<int> spiralOrder(const vector<vector<int> > &A) {
    int m = A.size(), n = A[0].size();
    vector<int> ret;
    int t = 0, b = m - 1, l = 0, r = n -1, dir = 0;
    while(t <= b && l <= r){
        if(dir == 0){
            for(int i = l; i<=r; i++){
                ret.push_back(A[t][i]);
            }
            t++;
        }
        if(dir == 1){
            for(int i = t; i<=b; i++){
                ret.push_back(A[i][r]);
            }
            r--;
        }
        if(dir == 2){
            for(int i = r; i>=l; i--){
                ret.push_back(A[b][i]);
            }
            b--;
        }
        if(dir == 3){
            for(int i = b; i>=t; i--){
                ret.push_back(A[i][l]);
            }
            l++;
        }
        dir = (dir+1) % 4;
    }
    return ret;
}


int main() {
	vector<vector<int>> v(4, vector<int> (4));
	int x = 0;
	for(int i=0; i<4; i++){
		for(int j=0; j<4; j++){
			v[i][j] = ++x;
			cout << v[i][j] << " ";
		}
		cout << endl;
	}
	
	vector<int> res = spiralOrder(v);
	for(int i=0; i<res.size(); i++){
		cout << res[i] << " ";
	}
	cout << endl;
	
	return 0;
}

{% endhighlight %}



