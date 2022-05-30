# Lazy Load

Don’t eagerly load data you won’t use!

Load things, only when some requests that particular property. And lazy load patterns come in 👇

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


### Drawbacks

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

## Benefits 
- In high performant environments limiting the communication can be crucial

## Drawbacks

- The entity is now coupled with logic to load additional data


## Examples

- Before
- After