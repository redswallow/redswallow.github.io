title: fail-fast 和 fail-safe 机制
slug: fail-fast-and-fail-safe-iterators
date: 2014-11-19
tags: Java 

fail-fast 机制是 Java 集合 (Collection) 中的一种是一种错误检测机制，JDK 并不保证 fail-fast 机制一定会发生。如果在迭代器迭代的过程中会检查对集合的结构进行任何的修改，每次获得下一个元素时，如果发现有任何修改，会立刻抛出异常 ConcurrentModificationException，而不是等遍历完了再抛出异常。所有迭代器的实现都是快速失败的设计。

快速失败 fail-fast 和故障安全 fail-safe 之间的不同是什么？

迭代器故障安全 fail-safe 以克隆方式工作，因此它不会影响集合中的任何修改。所有 java.util 包中的集合类都是 fail-fast，而 java.util.concurrent 中的类比如 CopyOnWriteArrayList 都是 fail-safe。

`Contrary to fail-fast Iterator, fail-safe iterator doesn't throw any Exception if Collection is modified structurally
while one thread is Iterating over it because they work on clone of Collection instead of original collection and that’s why they are called as fail-safe iterator. Iterator of CopyOnWriteArrayList is an example of fail-safe Iterator also iterator written by ConcurrentHashMap keySet is also fail-safe iterator.`
