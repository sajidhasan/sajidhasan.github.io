---
layout: post
title:  "Groping Anagrams"
date:   2022-04-29 00:00:10
category: Problem Solving
permalink: /problem/:title
---
### Problem statement

An array of string `words` is given, the task is to group the anagrams together and return the answer as an array.

Anagram is a word formed by rearranging the letters of a different word using all the original letters exactly once.


### Approach: Categorize by counting the letters in the word

In this approach, we will legerage map from C++ Standard Template Library (STL) to come up with efficient solution that can solve the grouping anagram problem in linear time. 

Time complexity: O(nk), were n is the lenngth of the `words`, and k is the maximum length of a string in `words`.

Space Complexity: O(nk), all the information stored in the `answer` variable.


First, we create a 2 dimensional vector to store the anagrams as a groups. We create another map for which the key will also be a map and values will be be vector of string type. 

Now, we iterate over the input array. For every word/phrase in the input array, we further iterate over all the letters of the array and update the count for each letter.

After iterating over the letters of the phrase and storing the count values, we use the map as a key to the previously created map. We push back the word from the input array after getting out of this loop.

By this time, all of our anagrams are already grouped and stored in the nestes map. So, we just have to take the values of the map and store it in our answer varibale which will be returned when the loop is complete.

The following code is the implementation of the above explanation.


{% highlight cpp %}
vector<vector<string>> groupAnagrams(vector<string>& strs) {
    vector<vector<string>> answer;
    //map of char and int as a key and vector of string as value
    map<map<char, int>, vector<string>> mp;
    
    for(int i = 0; i < strs.size(); i++){
        map<char, int> m;
        
        for(auto s: strs[i]){
            m[s]++;
        }
        
        mp[m].push_back(strs[i]);
    }
    
    for(auto i: mp) answer.push_back(i.second);
    
    return answer;
}
{% endhighlight %}