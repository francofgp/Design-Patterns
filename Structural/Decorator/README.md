# Decorator 


A structural design pattern used for dynamically adding behavior to a class, without making changes to that class.


![Uml Diagram2](/Structural/Decorator/assets/uml.png)


## Table of Contents
- [Decorator](#decorator)
  - [Table of Contents](#table-of-contents)
  - [Example explanation](#example-explanation)
    - [Using Decorator Objects](#using-decorator-objects)
  - [To keep in mind](#to-keep-in-mind)
  - [Use Cases](#use-cases)
  - [Examples](#examples)


## Example explanation

In the example solution, we will have a IWeatherService interface with one concrete class and two decorator classes.

![Uml Diagram2](/Structural/Decorator/assets/example.png)

- LogginDecorator: Log how often a method was called, how long it took parameters and response

- CachingDecorator: Cache weather conditions, forecasts for a city to reduce the number of external API calls

Examples are provided in the *decorator folder*

### Using Decorator Objects
```cs
// Standard component instantiation
IWeatherService weatherService = new WeatherService();

// Instantiation with decorator objects
IWeatherService weatherService =
                new CachingDecorator(
                    new LoggingDecorator(
                        new WeatherService()));

```
## To keep in mind

- Multiple decorators can be used in conjunction with one another
- Each decorator can focus on a single task, promoting separation of concerns
- Decorator classes allow functionality to be added dynamically

## Use Cases
- Cross cutting concerns (i.e. logging)
- Manipulate data going to/from component
  

## Examples

The following examples are provided:

1. Initial Project
2. Logging decorator added
3. Caching decorator added
4. Dependency injection initial state
5. Dependency injection - Scrutor
5. Dependency injection - Lambda Function