---
layout: post
title:  "Octave For Machine Learning"
date:   2018-11-09 00:09:47
category: Machine Learning
permalink: /machine-learning/:title
---

### Create Matrices of Different Dimensions
Let's start with generating a matrix. The following code in octave will generate
a `3x3` matrix and store it in variable `A`.
{% highlight octave %}
A = [1 2 3; 4 5 6; 7 8 9]
{% endhighlight %}
The semicolon seperates the rows and space seperates the elements of a row.
{% raw %}
$ A = \begin{bmatrix}1 & 2 & 3 \\\ 4 & 5 & 6 \\\ 7 & 8 & 9\end{bmatrix}$
{% endraw %}

Let's see another example of how to create a matrix. This time the size is `6x2`.
{% highlight octave %}
A = [1 2; 3 4; 5 6; 7 8; 9 10; 11 12]
{% endhighlight %}

{% raw %}
$ A = \begin{bmatrix} 1 & 2 \\\ 3 & 4 \\\ 5 & 6 \\\ 7 & 8 \\\ 9 & 10 \\\ 11 & 12\end{bmatrix}$
{% endraw %}
### Create A Vector
Now, how do we create a vector like the following one?
{% raw %}
$ A = \begin{bmatrix} 1 \\\ 3 \\\ 5 \\\ 7 \\\ 9 \\\ 11\end{bmatrix}$
{% endraw %}
As you can infer, the code will be like following. Just one element in each row will let us
create a vector of any size.
{% highlight octave %}
A = [1; 3; 5; 7; 9; 11]
{% endhighlight %}

### Create A Matrix of Consecutive Values
Try the following command to easily create matrix:
{% highlight octave %}
A = [1:6; 7:12]
{% endhighlight %}
{% raw %}
$ A = \begin{bmatrix}1 & 2 & 3 & 4 & 5 & 6\\\ 7 & 8 & 9 & 10 & 11 & 12\end{bmatrix}$
{% endraw %}
You can add several rows by delimiting the rows with a semicolon.
### Create A Matrix With Fixed Step Size
If you want to create a matrix with values that increases by some fixed value,
you can try the code below.
{% highlight octave %}
A = [1 : 0.2 : 2; 2 : 0.2 : 3]
{% endhighlight %}
The above code generates a matrix where the first row starts from 1, increases by 0.2 upto 2.
So, we get 6 columns in the row. The same thing happens to the second row where it starts
from 2 and ends at 3. This is a convenient way to generate matrix with a fixed step size.
{% raw %}
$ A = \begin{bmatrix}
1.0000 & 1.2000 & 1.4000 & 1.6000 & 1.8000 & 2.0000 \\\
2.0000 & 2.2000 & 2.4000 & 2.6000 & 2.8000 & 3.0000
\end{bmatrix}$
{% endraw %}

### Create A Matrix of Ones
{% highlight octave %}
A = ones (4, 4)
{% endhighlight %}
The above code create a `4x4` matrix of all ones.
{% raw %}
$ A = \begin{bmatrix}1 & 1 & 1 & 1 \\\ 1 & 1 & 1 & 1 \\\ 1 & 1 & 1 & 1 \\\ 1 & 1 & 1 & 1\end{bmatrix}$
{% endraw %}

### Create A Matrix of Zeroes
{% highlight octave %}
A = zeros (4, 4)
{% endhighlight %}
The above code create a `4x4` matrix of all zeroes.
{% raw %}
$ A = \begin{bmatrix}0 & 0 & 0 & 0 \\\ 0 & 0 & 0 & 0 \\\ 0 & 0 & 0 & 0 \\\ 0 & 0 & 0 & 0 \end{bmatrix}$
{% endraw %}

### Create Identity Matrix
{% highlight octave %}
A = eye (4, 4)
{% endhighlight %}
The above code create a `4x4` identity matrix.
{% raw %}
$ A = \begin{bmatrix}1 & 0 & 0 & 0 \\\ 0 & 1 & 0 & 0 \\\ 0 & 0 & 1 & 0 \\\ 0 & 0 & 0 & 1 \end{bmatrix}$
{% endraw %}

### Create A Matrix With Random Values
{% highlight octave %}
A = rand (4, 4)
{% endhighlight %}
The above code create a `4x4` matrix where every element has a random value between 0 and 1.
{% raw %}
$ A = \begin{bmatrix}
0.873222 & 0.190867 & 0.408141 & 0.424057 \\\
0.626970 & 0.337635 & 0.639046 & 0.247549 \\\
0.255936 & 0.901785 & 0.583927 & 0.192788 \\\
0.047349 & 0.858707 & 0.055897 & 0.023689
\end{bmatrix}$
{% endraw %}

### Create A Matrix With Gaussian Random Distribution
{% highlight octave %}
A = randn (4, 4)
{% endhighlight %}
The above code create a `4x4` matrix where every element is drawn from a Gaussian random distribution
with mean 0 and variance/standard deviation 1.

{% raw %}
$ A = \begin{bmatrix}
-2.723828 & -0.060662 & 1.026164 & 0.410187 \\\
 1.174451 & 1.401109 & -1.574397 & 0.897547 \\\
-1.104706 & -1.490367 & 0.636317 & -0.938956 \\\
 2.108468 & 0.966823 & 0.348221 & 0.106186
\end{bmatrix}$
{% endraw %}
