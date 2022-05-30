# Builder
Separate the construction of a complex object from its representation so that the same construction process can create different representations


Abstracts out initialization code

Representations created as concrete classes
- Constructed from interface blueprint


Director class handles actual object creation
- Controls where & what data is used


![Uml Diagram](/Creational/Builder/assets/uml.png)

## Table of Contents
- [Builder](#builder)
  - [Table of Contents](#table-of-contents)
  - [When to use it](#when-to-use-it)
  - [Keep in mind](#keep-in-mind)
  - [Implications](#implications)
  - [Examples](#examples)



## When to use it

- Builder is useful when creating complex objects
- When object creation needs to be separate from its assembly
- When different representations need to be created with finer control


## Keep in mind
- Not for everything - it’s overkill for most classes where subclassing, refactoring, or abstracted interfaces would be a better solution
- Bloated class constructors are a dead giveaway
- Lots of computation logic in class constructors needed to set class field values
- Finite number of related classes that perform similar functions with different representations

## Implications

- Lets you vary a products internal representation
- It isolates code for construction and representation
- It gives you finer control over the construction process
- Shares similarities with the Factory pattern


## Examples

Examples are provided:

- Before apply Builder
- After apply Builder