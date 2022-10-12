---
layout: post
title:  "Exception Handling in Java"
date:   2022-09-01
category: Java
permalink: /java/:title
---

# What is an Exception?

If Java Runtime Environment (JRE) encounters any exception it simply terminates the execution and returns an exception message stating the error message. 

## Exception Clauses

`1. try`  
Program statements that are expected to throw/raise exception should be written in the `try` block.

`2. catch`  
Catch block is responsible for catching the exceptions thrown by `try` block. JRE throws exceptions implicitly.

`3. throw`  
To throw exception manually `throw` clause is used.

`4. throws`  
To indicate that a method may throw exception we use `throws` clause.

`5. finally`  
This block is executed regardless of exception state, does not depend if the exception is handled or not.


## Basic Structure of Exception Handling in Java

{% highlight java %}

try{

}

catch(){

}

finally{
	
}

{% endhighlight %}

