# State

## What is a state?

State is the condition of something variable.

### Questions of State (Examples)

Is an order in an order processing application:
- New?
- Processing?
- Canceled?
- Complete?

Can a user edit a canceled order?

Can a completed order be canceled?

## The State Design Pattern

State is a behavioral design pattern that lets an object alter its behavior when its internal state changes. It appears as if the object changed its class.

## Problem

It addresses
- How can an object change its behavior when its internal state changes?
- How can state specific behaviors be defined so that states can be added without altering the behavior of existing states?


## Advantages

- More modular
- Easier to read and maintain
- Less difficult to debug
- More extensible

## Disadvantages

- Takes time to set up
- More moving parts
- Potentially less performant


**The State Design Pattern is a great addition to your developer’s toolkit.**
### They naive approach

There is a naive way to handle states, this way consists in adding boolean fields, such as: isProcessed, isPending, isFinished, and so on, depending of how many states we have.
This approach leads to exponential growth of complexity, since we have to add logic to code that we already wrote or implemented.
 
Some of the drawbacks of the naive approach are:

- Interdependent logic
- Time lost managing fields
- Difficult to extend
- Harder to debug and manage

**The State Design Pattern minimizes conditional complexity.**

## Addressing the challenges

- Encapsulates state-specific behaviors within separate state objects
- A class delegates the execution of its state-specific behaviors to one state object at a time


## Elements of the State Pattern

- Context
    - Maintains an instance of a concrete state as the current state
- Abstract state
    - Defines an interface which encapsulates all state-specific behaviors
- Concrete state
    - Implements behaviors specific to a particular state of context

![Uml Diagram](/Behavioral/State/assets/uml.png)

To implemente the state pattern we do the following:
- Identify a list of possible states
- The conditions for transitioning between those states
- The state its in when initialized, or its initial state


Let's suppose we have a booking event system. Our initial state is new, the we need to identify all the transitions such as, data passed, user canceled, and so on.
An example diagram of these is provided, and algo with the code along
![Uml Diagram](/Behavioral/State/assets/example.png)

## Examples

Examples are provided:

- Before apply State
- After apply State
