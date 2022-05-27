# Prototype

Specifies the kinds of objects to create
using a prototypical instance, and
creates new objects by copying this
prototype.

![Uml Diagram](/Creational/Prototype/assets/uml.png)


Client requests clone of an existing object
- Cloning logic is in the object itself
- Cuts down on subclassing
- Hides cloning implementation

## When to apply the Prototype pattern
When object creation, composition, and representation needs to be separate from a given system


Prototype works well with Object Pool
- Especially if manager class is used


Works with indefinite variety of prototypes
- As long as they all inherit from Prototype

## Use cases

- Not for everything - all classes don’t need copy behaviors
- When classes to instantiate are specified at run time
- Avoiding a class hierarchy of factories that mirrors the class hierarchy of your products
- When class instances can only have a small, finite combination of
states

## Variants

The prototype design pattern can be implemented using a Prototype Manager, all this does is keep track of a dictionary of prototype objects by key value pair, making it easier for client code to reference them and takes out the need for the objects to be created on the fly.

## Design Pattern Implications
- Concrete prototype classes are hidden from the client code
- Products can be added or removed at run time by the client
- Using cloned objects with varying configurations means your system will be more dynamic through object composition
- Prototype objects can be used as parts in a larger object creation design, which increases modularity

## Examples

With Prototype Manager and without it, all in the same solution