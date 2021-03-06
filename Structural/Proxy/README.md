# Proxy

## Table of Contents
- [Proxy](#proxy)
  - [Table of Contents](#table-of-contents)
  - [Problem](#problem)
  - [Structure](#structure)
    - [Option 1](#option-1)
    - [Option 2](#option-2)
  - [Proxy Variants](#proxy-variants)
  - [To keep in mind](#to-keep-in-mind)
  - [Related Principles](#related-principles)
  - [Examples](#examples)

## Problem

Need to control access to a type for performance, security, or other reasons.

It is about controlling access to another instance.

## Structure

![uml structure 1](/Structural/Proxy/assets/uml.png)

### Option 1

![uml structure 2](/Structural/Proxy/assets/structure.png)

### Option 2

![uml structure 2](/Structural/Proxy/assets/structure2.png)

## Proxy Variants
- Virtual Proxy: It is used to stand in for expensive-to-create objects.
  - Stands in for an expensive-to-create object
  - Typically responsible for getting real object
  - UI Placeholders
  - Lazy-Loaded Entity Properties


- Remote Proxy: It is used to hide the details of working with remote data or services.

  - Client works with proxy as if remote
resource were local
  - Hides network details from client
  - Centralizes knowledge of network details


- Smart Proxy: It permorms additional actions when a resource is accessed.
  - Performs additional logic around resource
access
  - Resource counting
  - Cache management
  - Locking shared resources

- Protective Proxy: It controls accesss to a sensitive resource by checking for whether or not the client is authorized to perform those operations.
  - Manages access to a resource based on
authorization rules
  - Eliminates repetitive security checks from
client code and the resource itself
  - Acts as a gatekeeper around a resource


## To keep in mind

When used properly, proxy implementations help you to follow Separation of Concerns and the Single Responsibility Principle.

## Related Principles

Some principles suggest the use of a Proxy as the solution in certain cases.

- Separation of concerns: Avoid mixing separate
concerns or ideas in the same class or method
- Loose Coupling: Prefer loose coupling to third party dependencies
- Single Responsibility: Classes should have only one responsibility; one reason to change

## Examples

Examples are provided:

- Remote Proxy
- Smart Proxy
- Virtual Proxy
- Protective Proxy