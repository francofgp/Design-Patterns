# Repository

A repository encapsulates the data access so the consumer no longer has to know about the underlying data structure

## Table of Contents
- [Repository](#repository)
  - [Table of Contents](#table-of-contents)
  - [Structure](#structure)
    - [Without Repository](#without-repository)
      - [Problems](#problems)
    - [With Repository](#with-repository)
      - [Benefits](#benefits)
      - [Drawbacks](#drawbacks)
  - [To keep in mind](#to-keep-in-mind)
  - [Examples](#examples)



## Structure

### Without Repository

![uml structure 1](/Behavioral/Data%20Access/Repository/assets/without.png)

#### Problems 
- The controller is tightly coupled with the data access layer
- It is d ifficu lt to w rite a test for the controller w ithout side effects
- Hard to extend entities with domain specific behaviour

### With Repository

![uml structure 1](/Behavioral/Data%20Access/Repository/assets/with.png)


In code 

```csharp
public interface IRepository<T>
{
    T Add(T entity); 
    T Update(T entity); 
    T Get(Guid id);
    IEnumerable<T> All();
    IEnumerable<T> Find(Expression<Func<T bool>> predicate);
    void SaveChanges();
}
```

#### Benefits

- The consumer (controller) is now separated (decoupled) from the data access
- Easy to write a test w ithout side-effects
- Modify and extend entities before they are passed on to the consumer
- A sharable abstraction resulting in less duplication of code
- Improved m aintainability

#### Drawbacks

- Adding more layers is not always better

## To keep in mind

An abstraction that encapsulates data access, making your code testable, reusable as well as maintainable

The data access patterns can be applied in any type of application

## Examples

- Before
- After