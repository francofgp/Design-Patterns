# Null Object 
The intent of a Null Object is to encapsulate the absence of an object by providing a substitutable alternative that offers suitable default do nothing behavior. In short, a design where "nothing will come of nothing"

Use the Null Object pattern when

- an object requires a collaborator. The Null Object pattern does not introduce this collaboration--it makes use of a collaboration that already exists
- some collaborator instances should do nothing
- you want to abstract the handling of null away from the client

## Problem
Given that an object reference may be optionally null, and that the result of a null check is to do nothing or use some default value, how can the absence of an object — the presence of a null reference — be treated transparently?

![Uml Diagram](/Behavioral/Null%20Object/assets/uml.png)

## Advantages

- Use Null Object to avoid null checks 
- Returned object is not null
- Use interface or inheritance as appropriate
- Cleaner code

**If you think the Null Object Pattern as the "Default object pattern", it makes more sense, at least to me. Basically is just an object with default properties, non-null properties, to be precice**

## Examples

Examples are provided:

- Before apply Null Object
- After apply Null Object
