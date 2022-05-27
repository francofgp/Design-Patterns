# Rules Engine

A rules engine processes a set of rules and applies them to produce a result.

A rule describes a condition and may calculate a value.

## Examples of Operations

- Scoring games
- Calculating Discounts for Customer Purchases
- Diagnosing Health Concerns

## What problems does it solve?

- The Open/Closed Principle
  - Code should be open to extension, but closed for modification
  - Adding more complexity repeatedly may be a sign a rules engine could help
  - Prefer maintaining existing software through new classes

## Defining Rules

- Each rule you extract should follow Single Responsibility Principle
- Rules are managed using an engine that chooses which rule(s) to apply
- Rules may be ordered, aggregated, or filtered as appropriate

## Rules Engine Collaborators

- Rule Collection
- Rule Engine
- System Input


## Structure

![uml structure 1](/Behavioral/Rules%20Engine/assets/uml.png)


- Keep individual rules simple
- Allow for complexity through combinations of simple rules
- Decide how rules will combine or be chosen
- Consider whether rule ordering will matter in evaluation

## Implementing a Rules Engine
- Accept rules collection in engine constructor
- Allow adding/removing rules or swapping sets of rules via methods
- Apply the rules to a given context or system state
- Choose correct rule to apply or aggregate rules

## Examples

Examples are provided