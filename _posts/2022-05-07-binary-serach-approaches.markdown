---
layout: post
title:  "Binary Search Approaches"
date:   2022-05-07 15:00:00
category: Problem Solving
permalink: /problem/:title
---

## Iterative
{% highlight cpp %}
int binarySearch(vector<int>& nums, int target) {
    int n = nums.size();
    
    int mid, left = 0, right = n - 1;
    
    while (left <= right){
        mid = left + (right - left) / 2;
        if (nums[mid] == target) return mid;
        if(nums[mid] > target) right = mid - 1;
        else left = mid + 1;
    }
 return -1;   
}
{% endhighlight %}

## Recursive
{% highlight cpp %}
int helper(vector<int>& nums, int left, int right, int target){
    int mid = left + (right - left) / 2;
    if(left <= right){
        if(nums[mid] ==  target)
            return mid;
        else if (nums[mid] < target){
            return helper(nums, mid + 1, right, target);
        }
        else{
            return helper(nums, left, mid - 1, target);    
        }
    }
    return -1;
}

int binarySearch(vector<int>& nums, int target) {
    int left = 0;
    int right = nums.size() - 1;
    return helper(nums, left, right, target);
}
{% endhighlight %}