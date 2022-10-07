---
layout: post
title:  "Java Collection Framework"
date:   2022-10-05
category: Java
permalink: /java/:title
---

Java collection framework provides all the interfaces and their implementation to manipulate data and reflect the common data structures used in computer science. In other words, collection framework is a representation of the data structures used in computer sciennce. The key points that needs to be considered while learning Java Collection Framework are following:

+ Java collections can store only `"Objects"`
+ Collections are made based on a list of interfaces and implementation classes
+ All standard Java collection classes and interfaces are defined in a package called `java.util`

## Collection Interfaces

`1. List` - List focuses on index and allows duplicate values to be inserted in the collection. List also ensures the order of the collection.

`2. Set` - Set focuses on hashcode and does not allow duplicate value. It does not retain any order (unordered collection).

`3. Map` - Map represents a dictionary which contains key-value pair. Any key-value pair is maintained in Map category.

## Implementation Classes of List Interface

+ `ArrayList` - Index based dynamically growable array, most suitable for READ operations, not suitable for write operations
+ `LinkedList` - Node based collection, suitable for WRITE operations, not suitable for READ operations
+ `Vector` - Vector is similar to ArrayList but Vector is `synchronized`.

{% highlight java %}

public class Main {

    public static void main(String[] args){
        ArrayList<Integer> evenNumbers = new ArrayList<>();

        evenNumbers.add(2);
        evenNumbers.add(4);

        System.out.println("Size of the list: " + evenNumbers.size());

        for (int value : evenNumbers) {
            System.out.println(value);
        }
    }
}

{% endhighlight %}

## Implementation Classes of Set Interface

`1. HashSet ` - Unordered collection, focuses on hashing, avoids duplicates

`2. LinkedHashSet` - Maintain order based on insertion, avoid duplicates

`3. TreeSet` - Implements `SortedSet` (a subtype of Set interface)


## Implementation Classes of Map Interface

`1. HashMap` - Similar to `HashSet` maintaining Key-Value pair, unordered

`2. LinkedHashMap` - Similar to `LinkedHashSet`, maintains key-value pair, retain insertion order

`3. TreeMap ` - Similar to `TreeSet`, maintains ascending order(Items are sorted based on Key)

`4. Hashtable` - Legacy class which is unordered, maintains unique keys but synchronized (thread-safe)