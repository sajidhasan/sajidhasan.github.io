---
layout: post
title:  "Insertion Sort Implementation In Swift 4"
date:   2018-10-29
category: Algorithms
permalink: /algorithms/:title
---
Following is the Swift 4 implementation of insertion sort algorithm.

{% highlight swift%}
import UIKit
var arr = [12, 9, 14, 31, 11, 4, 34, 13, 18, 21, 19]
func insertion_sort(arr: [Int])->[Int]{
    var n = arr.count, A = arr
    for j in 1..<n{
        let key = A[j]
        var i = j - 1
        while i >= 0 && A[i] > key{
            A[i+1] = A[i]
            i -= 1
        }
        A[i+1] = key
    }
    return A
}

insertion_sort(arr: arr)
{% endhighlight %}
