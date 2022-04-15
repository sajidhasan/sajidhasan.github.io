---
layout: post
title:  "Reverse A Linked List"
date:   2022-04-15 00:00:10
category: Problem Solving
permalink: /problem/:title
---
### Approach: Iteration

It is possible to reverse a linked list by reversing the reference direction of the linked list. First, we take a `prev` node and assign `nullptr` to it. This pointer will be assigned as head node's reference as it will become the last node in the linked list when the list is reversed.  

Now, we start iterating over the linked list untill `current != nullptr`. We take a temporary `temp` node to store the reference of `current->next`. To iterate, we move forward by assigning `current` to `prev` node and finally assign previously stored `temp` to `current`.  

Lastly, we return the head `prev`.


{% highlight cpp %}
 struct ListNode {
      int val;
      ListNode *next;
      ListNode() : val(0), next(nullptr) {}
      ListNode(int x) : val(x), next(nullptr) {}
      ListNode(int x, ListNode *next) : val(x), next(next) {}
 };
{% endhighlight %}

Above is the definition of a signly-linked-list.

{% highlight cpp %}


ListNode* reverseList(ListNode* head) {
    ListNode* prev = nullptr;
    ListNode* current = head;
    
    while(current){
        ListNode* temp = current->next;
        current->next = prev;
        prev = current;
        current = temp;
    }
    return prev;
}

{% endhighlight %}

Time complexity: {% raw %}$ O(n) ${% endraw %}

Space Complexity: {% raw %}$ O(1) ${% endraw %}

### Approach: Recursive

{% highlight cpp %}

ListNode* reverseList(ListNode* head) {
    if (head == nullptr || head->next == nullptr) {
        return head;
    }
    ListNode* p = reverseList(head->next);
    head->next->next = head;
    head->next = nullptr;
    return p;
}
{% endhighlight %}

Time complexity: {% raw %}$ O(n) ${% endraw %}  

Space complexity: {% raw %}$ O(n) ${% endraw %}
