---
layout: post
title:  "Two Sum and Variations"
date:   2022-05-09
category: Algorithms
permalink: /problem/:title
---

Given an array of integers `numbers`,  return the indices of the two integers that add up to `target`.

{% highlight cpp %}
vector<int> twoSum(vector<int>& nums, int target) {
    unordered_map<int, int> m;
    
    for(int i = 0; i < nums.size(); i++){
        
        int complement = target - nums[i];
        
        if(m.count(complement)) return {m[complement], i};
        
        m[nums[i]] = i;
    }
    
    return {};
}
{% endhighlight cpp %}

How to solve it when the array is sorted? The following code shows a two pointers approach to solve the problem when the array is sorted.
{% highlight cpp %}
vector<int> twoSum(vector<int>& numbers, int target) {
    int left = 0;
    int right = numbers.size() - 1;
    
    while(left < right){
        int sum = numbers[left] + numbers[right];
        if ( sum == target){
            return {left+1, right+1};
        }else{
            if(sum < target) left++;
            else right--;
        }
    }
    
    return {};
}
{% endhighlight cpp %}


There are other variations of the problem. For example, the problem can ask to find 3 or 4 numbers that add up to traget.
