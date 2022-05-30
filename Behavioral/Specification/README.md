# Specification
Specification pattern is a pattern that allows us to encapsulate some piece of domain knowledge into a single unit - specification - and reuse it in different parts of the code base.


The basic idea behind this pattern is that when you have some piece of domain knowledge you can encapsulate this knowledge into a single unit, specification, and then reuse in different parts of your code base

## Table of Contents
- [Specification](#specification)
  - [Table of Contents](#table-of-contents)
  - [Use cases](#use-cases)
  - [Advantages](#advantages)
  - [Purpose of the specification pattern:](#purpose-of-the-specification-pattern)
  - [Proper encapsulation and efficient database queries](#proper-encapsulation-and-efficient-database-queries)
  - [General guidelines](#general-guidelines)
  - [Combining specifications together](#combining-specifications-together)
  - [When not to use the Specification pattern](#when-not-to-use-the-specification-pattern)
  - [Examples](#examples)


## Use cases

- In-memory validation
- Retrieving data from the database
- Construction-to-order
- Creation of new objects

## Advantages

- Avoid domain knowledge duplication
- Enables declarative approach


## Purpose of the specification pattern:
- Encapsulate domain knowledge into a single unit
- Reuse in various scenarios

![Uml Diagram](/Behavioral/Specification/assets/uml.png)


## Proper encapsulation and efficient database queries
- Specifications should contain the domain
knowledge

## General guidelines
- Don’t use the ISpecification interface
- Make specifications as specific as possible
- Make specifications immutable

## Combining specifications together
- And, Or, and Not
- Identity specification

## When not to use the Specification pattern
- Code base is simple enough


**If you think the Null Object Pattern as the "Default object pattern", it makes more sense, at least to me. Basically is just an object with default properties, non-null properties, to be precice**

## Examples

Examples are provided

- Initial
- Second refactoring
- Final refactoring
