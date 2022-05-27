# Memento 

## What is a memento?

A memento holds an object’s internal state so the object can be restored to this state later.

## Where can I apply the memento Pattern?

- Saving state in game
- Supporting undo in a drawing application
- Rolling back a distributed transaction

## What problem does memento solve?

- Need to “roll back” one or more objects to a previous state
- Adding undo to existing objects would violate Single Responsibility Principle
- Providing full, direct access to objects’ internal state breaks encapsulation


## Structure

### Collaborators

- **Originator**: is the object whose state is being tracked.
- **Caretaker**: is the external object that works with the Originator. It's the caretaker's job to perform operations on the Originator, but it also need the ability to manage the Originato's State.
- **Memento**: is an object that holds the internal state of the Originator. It need to be the complete state of the Originator, so that the Originator can be restored completely to a previous state using it

![Uml Diagram2](/Behavioral/Memento/assets/uml.png)

![Uml Diagram2](/Behavioral/Memento/assets/sequence.png)



## Working with Memento

- Memento itself should be very simple
- Originator must support methods to create/restore mementos
- Caretaker is responsible for managing previous state
- Avoid giving caretaker direct access to internal memento/originator state



## Undo Operations
One common way to manage mementos in the caretaker is to keep a strack of previous state in order to support multiple undo operations.

- Store states (mementos) on an undo stack
- After each action, add new memento to undo stack
- On undo, pop previous memento from undo stack; add to redo stack
- On redo, pop from redo stack; add to undo stack

![Uml Diagram2](/Behavioral/Memento/assets/stack.png)


**Mementos should be immutable value objects with state, but no behaviors**

## Analysis

- Only Caretaker, not Originator, has to track state
- Memento may not be appropriate if state is quite large
- Can be difficult to encapsulate memento state so only Originator can access it


## Key Principles when applying Memento
- Enforce Single Responsibility Principle
- Avoids violating Encapsulation
  
## Alternate Approach

### Reverse Operations
- Works well with Command pattern
- Store operations performed
- Support undo by applying reverse operation
- Only works for operations with consistent reverse behavior

### Storing Diff (Differences)
- Instead of storing full state, just store differences
- This is how version control systems like Git work
- Requires less storage to save many states
- May require more resources to create diffs
- May require more resources to restore a state that involves many diffs


## Related Design Patterns
Command
- Provide reversal commands to undo operations

Iterator
- Each iteration can store its state using a Memento
  

## Examples

Hangman Game with Memento implemented.