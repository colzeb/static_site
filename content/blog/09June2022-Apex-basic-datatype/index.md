+++
title = "List Data Type Apex"
date = 2022-06-09

[taxonomies]
tags = ["salesforce"]
+++

List Comman practice

<!-- more -->

## LIST

* Hold Multiple value of same type of data. eg to store 10 names.
* Have index for each element start with 0.

```java
// Basic List to hold String Value
List<String> names = new List<String>();

// to check number of element in List
System.assertEquals(0, names.size());

// to add element in list
names.add('Hello');

// to access the value in list
// use the index value which start from 0
System.assertEquals('Hello', names[0]);
System.assertEquals('Hello', names.get(0));
```

```java
// if you give index greater than its size
// you will get exception
try {
    String temp = names.get(1);
}catch(ListException le){
    System.assertEquals('List index out of bounds: 1', le.getMessage());
}
```

```java
// you can pass list or set in constructor of list
List<String> a =new List<String>{'zero', 'one', 'two'};
List<String> b =new List<String>(a);
System.assertEquals(a.get(0), b.get(0));
        
Set<String> aSet = new Set<String>();
aSet.add('one');
        
List<String> aList = new List<String>(aSet);
System.assert(aSet.contains(aList.get(0)) );
```
