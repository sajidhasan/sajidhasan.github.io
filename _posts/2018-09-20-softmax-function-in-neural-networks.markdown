---
layout: post
title:  "Softmax Function In Neural Networks"
date:   2018-09-20 00:10:00
tags: Machine Learning, Deep Learning, Neural Network, Softmax, Python, Numpy
permalink: /ml/:title
---

In Neural Networks an interesting function named `Softmax` function is used to calculate probabilities of Logits Scores that sum to 1. After applying the `Softmax Function`, the logits scores become probabilities which helps to classify among the scores.

Here we will see how the `Softmax Function` works. We will also code our own softmax function in python.

Let us consider the probabilities that we get after applying Softmax function represent different classes. The one with highest probability or very close to 1 is the correct class and the other classes will be close to 0 or less than the correct class. Also the probabilities sum to 1.

![Softmax Function](/assets/softmax.png){:class="img-responsive"}

Above, we can see the logits scores [2.0, 1.0, 0.1] becomes [0.7, 0.2, 0.1] after applying the softmax function. Here, y refers to the logits vector. The function simply takes the `i-th` element of logits vector as a power of `e` and divides it by the sum of `e` to the power `y`.

Suppose, we have an one dimensional array `scores`:
{% highlight python %}
scores = [3.0, 4.0, 2.0]
{% endhighlight %}
After applying the softmax function it should return an array of same length:
{% highlight python %}
probabilities = softmax(scores)
#softmax function returns an array of 3 elements
{% endhighlight %}

Now, let's code our very own softmax function:
{% highlight python %}
import numpy as np
def softmax(logits):

    exp_y = []
    probabilities = []

    for i in logits:
        exp_y.append(np.exp(i))

    sum_exp_y = sum(exp_y)

    for j in exp_y:
        probabilities.append(j/sum_exp_y)

    return probabilities

scores = [3.0, 4.0, 2.0]
print softmax(scores)
print sum(softmax(scores))

#[0.24472847105479764, 0.6652409557748218, 0.09003057317038045]
#0.9999999999999999
{% endhighlight %}



First of all, we import the `numpy` module as `np`. We pass one parameter called `scores` for the `softmax` function. There are two lists - `exp_y` and `probabilities`. The former will hold the values of `e` to the power `i-th` y and the latter will hold the probabilities.

{% highlight python %}
for i in logits:
    exp_y.append(np.exp(i))
{% endhighlight %}

The above code simply calculates the `e` to the powe `i-th y` and appends to our `exp_y` list. It could be done by using python's list comprehension technique. The code would look like the following.

{% highlight python %}
exp_y = [np.exp(i) for i in logits]
{% endhighlight %}

Then we get the sum of the `exp_y`s as we need to divide each `exp_y` with the sum. When we have the sum, we start calculating the probabilities. This task could also be done by applying list comprehension.

{% highlight python %}
probabilities = [j/sum_exp_y for j in exp_y]
{% endhighlight %}

Thus, you can pass scores array of any length to this softmax function and get the probabilities.
