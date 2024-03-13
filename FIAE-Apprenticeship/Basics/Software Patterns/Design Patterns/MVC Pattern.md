# The MVC Pattern
---

## What is the MVC Pattern?

The MVC is a Pattern, with the primary goal of separating concerns to ease testability.

## Components:

In the MVC Pattern, features are divided into three main components:
- The View
- The Controller
- The Model
The View is responsible for rendering UI elements. 
The Controller responds to UI Actions from the user.
The Model handles business behaviors and state management.

### Flow of Control:
![[MVC Pattern flow.png]]

MVC does not specify how the view and the model should be structured internally. Usually, the view layer is implemented in a single class though.
In that case, a couple of problems might arise:
- The view and the model are tightly coupled.  As a result, feature requirements of the view can easily drip down to the model and pollute the business logic layer
- The view is monolithic and usually couples tightly with the UI framework. Thus, unit testing the view becomes difficult.


## Benefits and Downsides

### Benefits:
- Clean separation of concerns
- Makes it easier to test the applications code
- Accelerated parallel development
- Promotes de-coupling of the application’s layers
- Facilitates Better code organization, extensibility, and reuse

### Downsides:
- It is quite complex to implement
- It is not a good choice for small applications