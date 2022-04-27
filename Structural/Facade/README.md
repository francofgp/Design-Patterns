# Façade

Façade is a structural design pattern that provides a simplified interface to a library, a framework, or any other complex set of classes.

## Problem

You may heard of the big ball of mud class. It is a class that tries to solve all of the world problems, it is too bloated

Like classA.
My program may need only 4 method, and I can put a "facade" in the middle of my program to solve this; and the ball of mud, having the facade only an internal referece to the giant class.
![Uml Diagram](/Structural/Facade/assets/uml.png)


**There is another variance of the problem** see the image below:

![Uml Diagram](/Structural/Facade/assets/uml1.png)

This is a more common situacion, we have several service class, with method that can be called by another program.
This program must know this services, and sometimes the ordern of calling the methods, even across classes is sometimes signicant.

Example of the program in code:

```cs
static void Main(string[] args)
{
    var serviceA = new ServiceA();
    serviceA.Method1();

    var serviceB = new ServiceB();
    string serviceBString = serviceB.Method2();

    var serviceC = new ServiceC();
    string serviceCString = serviceC.Method2();

    Console.WriteLine($"{serviceBString} - {serviceCString}");
}
```

If you put this code behind a facade we could get away with one class and one function call.
We could do the following.
![Uml Diagram](/Structural/Facade/assets/uml3.png)

The interface here could be optional

## When to use Façade

- Use Façade to provide a single interface to multiple worker classes
- Using a Façade interface is a best practice
- Can be used to mask giant classes with lots of methods


## Examples

Examples are provided:

- Before apply Façade
- After apply Façade
