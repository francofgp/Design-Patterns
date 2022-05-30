# Unit of Work

Allows us to referece multiple repositories inside our unit of work class.


**Our unity of work class will make sure that we reduce the communication to our database.**

When we apply the unit of work pattern in our application, instead of having to talk to the database for each insert or update, we can simple group that in one single transaction

## Table of Contents
- [Unit of Work](#unit-of-work)
  - [Table of Contents](#table-of-contents)
  - [Structure](#structure)
  - [Benefits](#benefits)
  - [Drawbacks](#drawbacks)
  - [Examples](#examples)

## Structure

![uml structure 1](/Behavioral/Data%20Access/Unit%20of%20Work/assets/uml.png)

## Benefits 
- In high performant environments limiting the communication can be crucial

## Drawbacks

- When writing a test for a controller leveraging the unit of work you will no longer know which repositories it really uses


## Examples

- Before
- After