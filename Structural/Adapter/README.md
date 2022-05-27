# Adapter 


## Understanding the problem

Incompatible interfaces between a client and a service-provider.

## Real world example

- Electrical outlets provide electricity
- United States’ outlets have a specific interface and voltage
- Other countries have differing interfaces
- Appliances with one kind of plug may not be able to (safely) use incompatible outlets

An **adapter** is used to allow devices with incompatible interfaces to work together
A specific adapter works between two specific interfaces


**Adapters convert the interface of one class into an interface a client expects.** 



## Kind of adapters

### Object Adapters
- Hold an instance of the Adaptee
- Implement or Inherit the Adapter type
- Use composition and single inheritance

*Object adapters*
![Uml Diagram2](/Structural/Adapter/assets/objectAdapter.png)


### Class Adapters
- Inherit from the Adaptee
- Inherit from the Adapter type
- Require multiple inheritance

*Multiple inheritance*
![Uml Diagram2](/Structural/Adapter/assets/classAdapter.png)

## Key takeaways

- An adapter converts an incompatible interface into a compatible one
- In C#, the adapter pattern uses composition and is known as an object adapter
- Adapters are similar to many other design patterns
- Adapters can work with service providers but can also wrap result types

## Examples

An example is provided in sequential steps

1. Initial 
2. Two provider
3. Two provider classes
4. Adapter introduction
5. Add dependecy injention
