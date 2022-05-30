# Lazy Load

Don’t eagerly load data you won’t use!

Load things, only when some requests that particular property. And lazy load patterns come in 👇

## Table of Contents
- [Lazy Load](#lazy-load)
  - [Table of Contents](#table-of-contents)
  - [Different Flavors of Lazy Loading](#different-flavors-of-lazy-loading)
    - [Lazy Initialization](#lazy-initialization)
      - [Drawbacks](#drawbacks)
    - [Value Holders](#value-holders)
      - [Benefits](#benefits)
    - [Virtual Proxies](#virtual-proxies)
    - [Ghost Objects](#ghost-objects)
  - [Examples](#examples)



## Different Flavors of Lazy Loading

- Lazy Initialization 
- Virtual proxies
- Value holders 
- Ghost objects

### Lazy Initialization

The idea is that we only procede to initialize our backing field to an exposed property the first time someone tries to access that particular property

Only loads the data:
- When the value is null we try to load the data
- This requires the entity to know about accessing the services or databases


Example
```csharp
private byte[] profilePicture; 
public byte[] ProfilePicture 
    {
        get 
        {
            if (profilePicture == null) 
            { 
                profilePicture = ProfilePictureService.GetFor(Name); 
            }
        return profilePicture; 
        }
        set { profilePicture = value; } 
    }
```


#### Drawbacks

- The entity is now coupled with logic to load additional data


### Value Holders

With this the entity is not coupled with logic to load additional data

```csharp
var customer = context.Customers.Single(c => c.CustomerId == entity.CustomerId)

customer.ProfilePictureValueHolder = new ValueHolder<byte[]>(() => {
return ProfilePictureService.GetFor(customer.Name); })
```

#### Benefits
- Not coupled with the code to load the data
- The properties on the entity uses the value holder to lazily retrieve the data

![uml structure 1](/Behavioral/Data%20Access/Unit%20of%20Work/assets/uml.png)


### Virtual Proxies


The repository can map the entity to a proxy class to return to its caller
This will allow the proxy to intercept calls to a property and load the data when necessary


```csharp
public class CustomerProxy : Customer
{
    public override byte[] ProfilePicture
    {
    get {
        if (base.ProfilePicture == null) 
        { 
            base.ProfilePicture = ProfilePictureService.GetFor(Name); 
        }
        return base.ProfilePicture; 
        }
    }
}

var customer = context.Customers .Single(c => c.CustomerId == entity.CustomerId);
var proxy = new CustomerProxy
{
    Name = customer.Name, City = customer.City, PostalCode = customer.PostalCode, ShippingAddress = customer.ShippingAddress, Country = customer.Country, 
};
return proxy;

```

### Ghost Objects

- The entity is loaded in a partial state which
- It is fully loaded when a property is accessed


```csharp
public class CustomerGhost : Customer
{
    public override string Name { 
        get {
                Load();
                return base.Name;
            }
        set {
                Load();
                base.Name = value;
            }
    }
}

```
## Examples

- Before
- After