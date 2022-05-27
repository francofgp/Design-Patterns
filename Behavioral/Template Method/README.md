# Template Method

A template method is a method in a superclass that defines the skeleton of an operation in terms of higher level steps.


Subclasses implement these steps.


**"Template methods are a fundamental technique for code reuse."**

## Examples of Operations

- Managing a game and determining a winner
- Following a recipe
- Rendering a page or control in a UI framework
- Migrating data using Extract-Transform-Load process
- Application/document framework

## What problems does it solve?

- Lock down a process while allowing clients to alter certain steps in the process
- Generalize duplicate behavior among methods in several classes (see DRY)
- Create and control extension points for future code implementations

## Structure

![uml structure 1](/Behavioral/Template%20Method/assets/uml.png)

- Implement one or more specific steps
- Don't implement the template method itself
- Extend behavior using hooks if available and needed
- Follow the Hollywood Principle


## Examples

Examples are provided