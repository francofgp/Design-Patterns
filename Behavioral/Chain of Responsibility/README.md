# Chain of Responsibility

Chain of Responsibility is behavioral design pattern that allows passing request along the chain of potential handlers until one of them handles request.

The pattern allows multiple objects to handle the request without coupling sender class to the concrete classes of the receivers. The chain can be composed dynamically at runtime with any handler that follows a standard handler interface.


![uml](/Behavioral/Chain%20of%20Responsibility/assets/uml.png)

## Characteristics

- Sender
  - Invokes the Handler
- Receiver
  - Handles the given command
- Handler
  - Runs through the chain of receivers


### Takeaways

- Decouples the sender and receiver
- One or many handlers can act on a given request
- Allows for clean and single responsibility handlers
- An object oriented way to express a chain of “if”, “else if” and “else” statements
- Easily extend a chain to add additional handlers

## Examples

Examples are provided:

- First Example
- Payment processing
- Payment processing improved
- ILloger
- ASP.NET Core Example
