# Bridge



Its purpose is to decouple an abstraction from its implementation so that the two can vary independently

![intro](/Behavioral/Bridge/assets/bridge%20intro.png)

What challenges the bridge pattern help to overcome?

The bridge pattern replaces complexity multiplication with complexity addition, and thus bring the exponential growth of that complexity under control.

## Table of Contents
- [Bridge](#bridge)
  - [Table of Contents](#table-of-contents)
  - [Explanation](#explanation)
    - [Another definition](#another-definition)
    - [Alternative implementation](#alternative-implementation)
    - [**Prefer composition over inheritance**](#prefer-composition-over-inheritance)
  - [Examples](#examples)


## Explanation

Let's suppose we what two add discounts to our movies, if we do so, using a naive approch, we will end up with let's say, 2 types of movie licenses and 3 types of discounts, we will have 6 classes in total, the growth is exponential.


![explanation image1](/Behavioral/Bridge/assets/bridge%20example.png)

If we apply the bridge pattern, we group all the variation of each aspect, such that they are only connected to their based class.

And then we introduce another connection between the base classes themselves

We isolated these two aspect from each other and therefore achieved high cohesion among elements of each aspect and loose coupling between the aspects of themselves
![explanation image2](/Behavioral/Bridge/assets/bridge%20example%202.png)

Helps prevent combinatorial explosion

### Another definition
The purpose of the bridge pattern is to split a class hierarchy through composition to reduce coupling

![explanation image3](/Behavioral/Bridge/assets/bridge%20example%203.png)

### Alternative implementation

There is another way to implement the bridge pattern, which is debatable.
It's a natural extension of the bridge pattern
![explanation image4](/Behavioral/Bridge/assets/bridge%20example%204.png)


There is an important guideline

### **Prefer composition over inheritance**

- Composition is more flexible than inheritance
- Composition is easier to understand

## Examples

Examples are provided

- Before apply bridge pattern
- After apply bridge pattern