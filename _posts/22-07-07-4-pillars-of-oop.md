---
layout: post
title:  "4 Pillars of Object Oriented Programming"
date:   2022-07-07
category: OOP
permalink: /java/:title
---

## Encapsulation

## Inheritance

### Hierarchical Inheritance
### Multi-level Inheritance

## Abstraction

Abstraction is a process of creating generalized class with some common features that can be inherited by specialized classes. When there is an obvious situation to implement a method in a 

If method overriding is compulsory in a specialized class innherited from a generalized class then there is no point of writing a complete implementation of a method in the generalized class. In this case, we declare an abstract method in the generalized class which is not implemented.

### Abstract Class


- Abstract class can have variables
- Abstract class can have constructors
- Abstract class can have concrete methods (fully implemented methods)
- An abstract class can have one or more anstract methods
- An abstract class can define a common specification (method signature/declaration without method body) so that the subclasses can override or implement the methods according to their requirement.
- Abstract classes cannot be instantiated which means it is not possible to create object from an abstract class.

- Abstract class can be extended and the child class can implement or override the abstract methods of its superclass.
- The child class must implement all the abstract methods in the abstract class that it enxtends, otherwise the child class needs to be declared as abstract class as well. In other words, a child class that partially implements the abstract superclass is also an abstract class and needs to declared as abstract class.



## Polymorphism


### Interface in Java

Interfaces in Java represents pure abstract class. Interfaces allow us to wrtie a common specification or outline that can be implemented by various implementation providers.

(Prior to Java 8) Java interfaces can have only abstract methods. 

A specification of method signatures.

Q: Can Java interfaces have variables?
A: Yes, but the variables have to be pulblic, static and final (constant)

Q: Can interface extend another interface?
A: Yes, An interface can extend other interfaces, just as a class subclass or extend another class. However, whereas a class can extend only one other class, an interface can extend any number of interfaces. The interface declaration includes a comma-separated list of all the interfaces that it extends.



Method signature indicates a method indication which reveals access specifier, return type, name of the method and parameter list (if any).

Interface declaration syntax:

{% highlight java %}

interface Calculator{

	public abstract double add(double x, double y);
	public abstract double subtract(double x, double y);
	public abstract double divide(double x, double y);
	public abstract double multiply(double x, double y);

}

{% endhighlight %}

Q: Can a class extend an interface?
A: No, class can implement an interface.

s

