# The MVP Pattern
---

## What is the MVP Pattern?

**MVP** stands for *Model-View-Presenter*. It derives from the [[MVC Pattern]], just like the [[MVVM Pattern]]. **MVP** is the pattern of choice when working with [[Windows Forms|WinForms]] or [[WPF]].


## Components:

The MVP Pattern has three main components:
- The Model
- The Presenter
- The View

The Model represents the domain objects/business entities that encapsulate data and implement business logic. Its the component of the MVP Pattern where the data lies. It contains all the information relevant to business logic and gives the system access to your different [[Database|databases]]. The user never interacts with the data directly.
The View is responsible for displaying data on the screen and interacting with user events. It should also be as dumb as possible and should have no business logic. 
The Presenter is the main component. It is responsible for interpreting user events, refresh the view and the communication between the View and the Model. 

### Overview: 
![[MVP Pattern Overview.png]]

### Flow of Control:
![[MVP Pattern flow.png]]



## Benefits and Downsides

### Benefits:
- Clear separation of concerns
- Modularity
- Easier to test code

### Downsides:
- The controller is often omitted. Because of the lack of a controller, control flow has also to be handled by the presenter. This makes the presenter responsible for two concerns: updating the model and presenting the model
- We cant utilize data binding. If binding is possible with the UI framework, we should utilize it to simply the presenter