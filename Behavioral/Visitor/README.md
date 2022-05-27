# Visitor

Represent an operation to be performed on the elements of an object structure without changing the classes of the elements on which it operates.

Behavior can be added to existing hierarchy
-	No changes to underlying classes

Behavior is class-specific

No hierarchical connection is necessary
-	As long as classes are marked as visit-able


![visitor uml diagram](/Behavioral/Visitor/assets/uml.png)
## When to use it

When a project has several different classes, with different interfaces, that need additional behavior without changing their underlying structure

### Use Cases

- Not for everything - all added class behavior doesn’t need to be implemented with the visitor pattern
- When a project has a variety of classes, with different interfaces and inheritance structures, that need added class-specific behavior
- When different and unrelated behaviors need to be applied without polluting the existing classes
- When the existing class structure is unlikely to change, but new behavior needs to be added at will

### Implications

- Adding behavior across a wide range of differing exiting classes
- Gathering related behaviors and accumulated state across differing classes
- Changing the class hierarchy while using the Visitor pattern can be costly - you’ll have to update the interface for all visitors to match
- Encapsulation can potentially be broken, as the visitor pattern often needs access to the internal state of your elements to do its job

## Examples

An example is provided:

1. Starter 
2. Final

