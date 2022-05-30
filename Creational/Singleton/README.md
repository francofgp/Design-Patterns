# Singleton

A singleton is a class designed to only ever have one instance.

![Uml Diagram](/Creational/Singleton/Singleton/assets/uml.png)
The singleton pattern make the class itself responsible for enforcing Singleton behavior

## Table of Contents
- [Singleton](#singleton)
  - [Table of Contents](#table-of-contents)
  - [Single Instance Examples](#single-instance-examples)

## Single Instance Examples

- Access to File System
- Access to Shared Network Resource
- Expensive One-Time Configuration

There are several way to implement this pattern, like the followings:

- Naive (The basic one, without Thread Safety)
- Locking (Thread Safety)
- Better locking
- Less Lazy 
- Nested Lazy Source: https://csharpindepth.com/articles/singleton
- LazyOfT (The cleanest way)

Test are included in each scenario