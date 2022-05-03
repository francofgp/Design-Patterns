# Factory

Factory Method is a creational design pattern that provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created.

## What Is a Factory?
A factory is an object for creating objects

## Purpose of the factory

- Allow you to reuse code
- Introducing extensibility

## Factory Pattern Flavors

There are three different versions of the factory pattern

- Simple Factory
- Abstract Factory
- Factory Method

## Facory Pattern Characteristicas

- Client
  - Asks for a created product
- Creator
  - Facilitates a creation
- Product
  - The product of the creation

**The client no longer needs to know how to create an object or exactly what flavor of that class it will use**


### Simple Factory Example

![simple factory](/Creational/Builder/assets/simpleFactory.png)

**Introduce a factory to make code in the application more reusable**

### Factory Method

Example
**The factory pattern is introduced to allow for a flexible and extensible application**

```cs
public abstract class ShippingProviderFactory
{
  public abstract ShippingProvider CreateShippingProvider(string country);
  public ShippingProvider GetShippingProvider(string country)
  {
    var provider = CreateShippingProvider(country);
    return provider;
  }
}
```

![simple factory](/Creational/Builder/assets/factoryMethod.png)

**Extend the creator to override the default factory method**


**In many cases the simple factory and factory method will be sufficient**

### Abstract factory
The abstract factory pattern provides a way to encapsulate a group of individual factories that have a common theme without specifying their concrete classes

![simple factory](/Creational/Builder/assets/abstractFactory.png)

```cs
var shippingProvider = purchaseProviderFactory.CreateShippingProvider(order);
var invoice = purchaseProviderFactory.CreateInvoice(order);
```

```cs

PurchaseProviderFactory purchaseProviderFactory;
if (order.Sender.Country == "Australia")
{
  purchaseProviderFactory = new AustraliaPurchaseProviderFactory();
}
else if (order.Sender.Country == "Sweden")
{
  purchaseProviderFactory = new SwedenPurchaseProviderFactory();
}
var cart = new ShoppingCart(purchaseProviderFactory);
```

## Summary

- Separates the client from the creation
- Less duplication of code
- Introduce subclasses and concrete implementations to add functionality
- Very common when writing tests
- Code becomes easier to maintain and navigate
- Factory Method and Abstract Factory are very common patterns

## Examples

Examples are provided:

- Simple Factory before/after
- Factory Method  before/after
- Abstract Factory  before/after
- Factory pattern in testing  before/after
- Factory Provider (reflection)  before/after