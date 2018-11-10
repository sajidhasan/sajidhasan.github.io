---
layout: post
title:  "Insertion Sort Implementation In C++ & Swift 4"
date:   2018-10-29
category: Algorithms
permalink: /algorithms/:title
---

Insertion sort is the simplest of sorting algorithms. It is not considered
an efficient sorting algorithm for large datasets. Many of us have applied this algorithm
without being conscious about it. If you can sort playing cards in your
hand then you already know the inner mechanism of the algorithm.

### C++ Implementation of Insertion Sort
{% highlight cpp%}

#include<iostream>
using namespace std;

void print(int a[], int length){
    for(int i = 0; i < length; i++)
        cout << a[i] <<" ";
    cout <<endl;
}

void insertionSort(int A[], int length){
    int key, i;
    for(int j = 1; j < length; j++){
        key = A[j];
        i = j - 1;
        while(i > -1 && A[i] > key){
            A[i+1] = A[i];
            i = i - 1;
        }
        A[i+1] = key;
    }
}

int main(){
    int arr[] = {10, 6, 3, 2, 1, 8};
    int l = sizeof(arr)/sizeof(*arr);
    print(arr, l);
    insertionSort(arr, l);
    print(arr, l);

}
{% endhighlight %}


In one iteration, an element from a sequence is picked up and inserted into the
right position for the element. It is required to keep iterating until all the elements
are sorted.


### Swift4 Implementation of Insertion Sort
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

Insertion sort is a stable sorting algorithm and also, it sorts the element
in place. Thus, it does not require any auxiliary memory. This algorithm can be
useful when either the dataset is comparatively small or the elements are already
in a almost sorted order.

***Time complexity:*** {% raw %}$ T(n) = O(n^2) ${% endraw %}

***Auxiliary Space:*** O(1)
