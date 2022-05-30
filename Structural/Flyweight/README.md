# Flyweight

Use sharing to support large numbers of fine-grained objects efficiently.

Allows unchanging data to be shared 
- Referred to as intrinsic state 

Object-specific data can be passed in 
- Referred to as extrinsic state 

Shared objects act as an unchanging model 
- Reused as need 
- Significantly cuts down on storage

## Table of Contents
- [Flyweight](#flyweight)
  - [Table of Contents](#table-of-contents)
  - [Structure](#structure)
  - [Scenario](#scenario)
  - [Intrinsic State Simplified](#intrinsic-state-simplified)
  - [Extrinsic State Explained](#extrinsic-state-explained)
  - [Flyweight Use Cases](#flyweight-use-cases)
  - [Design Pattern Implications](#design-pattern-implications)
  - [Examples](#examples)


## Structure

![uml structure 1](/Structural/Flyweight/assets/uml.png)


- Keep individual rules simple
- Allow for complexity through combinations of simple rules
- Decide how rules will combine or be chosen
- Consider whether rule ordering will matter in evaluation

## Scenario

When a large number of objects need to be created and most object state is categorized as extrinsic



## Intrinsic State Simplified

- Every person has a name and inner character 
- These remain constant throughout life 
- Anything unchanging is your intrinsic state 
- Sometimes referred to as an objects context

## Extrinsic State Explained

- Age, height, weight are changing properties 
- Worldly interactions also qualify 
- This is all considered extrinsic state
- Separate from your context


## Flyweight Use Cases

- Not for everything - all object creation doesn’t have to use the flyw eight pattern
- When an application needs a lot of objects, making storage costs high
- When object state can mostly be extrinsic, and many groups of objects can be replaced with a few shared objects
- When the application doesn’t depend on object identity


## Design Pattern Implications

- Run-time costs may play a part in finding and computing a shared objects extrinsic state
- If applied in correct situations, this will be offset by the space savings from each additional shared flyweight object used Savings are at their maximum capacity when lots of shared objects are used and both stored intrinsic and computed extrinsic are substantially used
- Hierarchical relationships and communications can still be used by passing references to parent, or other hierarchy objects, in with the extrinsic state

## Examples

Examples are provided