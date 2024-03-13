# Introduction to DTOs
---

## What are DTOs?

A DTO (Data Transfer Object) is an object that carries data between processes/applications. 
You use it when you want to provide some data, but not every other data of an object aswell. In this situation you can use DTOs to transfer only the information required.
Its used only to send and receive data and does not contain any business logic within itself.


## Advantages of DTOs

DTOs isolate the domain model from the presentation, resulting in both loose coupling and optimized data transfer.
In loose coupling, you can change one service without changing the other by reducing interdependencies. 
DTOs also help to eliminate overposting. Overposting is a cyber security threat that targets controllers, which expect an input from a user, but also have other variables that are hidden from the user. Someone who knows this information can manually add an extra field to an input that would allow them to change those hidden variables. DTOs can prevent this by not even providing these other variables.