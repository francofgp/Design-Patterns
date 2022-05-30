# Mediator

Mediator is a behavioral design pattern that lets you reduce chaotic dependencies between objects. The pattern restricts direct communications between the objects and forces them to collaborate only via a mediator object.

- Encapsulate how objects interact and communicate with each other
- Promote loose coupling between objects 
- Mediator avoids objects referring to directly each other


![With and without mediator](/Behavioral/Mediator/assets/with.png)


## Components

- Mediator
    - I define communication between colleagues
- Concrete Mediator
    - I im plem ent com m unication between colleagues
- Colleague
    - I communicate only with the Mediator
- Concrete Colleague
  - I receive messages from the mediator

![With and without mediator](/Behavioral/Mediator/assets/uml.png)

## Benefits

- Encapsulate object interaction with loose coupling
- 
## Examples

An example is provided













