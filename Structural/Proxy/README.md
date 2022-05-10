# Proxy

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


- Protective Proxy: It controls accesss to a sensitive resource by checking for whether or not the client is authorized to perform those operations.