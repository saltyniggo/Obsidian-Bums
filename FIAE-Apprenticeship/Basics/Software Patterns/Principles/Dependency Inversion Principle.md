# What is the Dependency Inversion Principle?
---

## Keypoints of the DIP Principle

Most [[Introduction to Design Patterns|Design Patterns]] are build upon the DIP Principle. Dependency Inversion talks about the *coupling* between different classes or modules. It focuses on the approach that higher classes are not dependent on lower classes, instead upon the [[Abstraction|abstraction]] of those lower classes.

>*Any higher classes should always depend upon the abstraction of the class rather than the detail*

This reduces the coupling between the classes by introducing an [[abstraction]] between the layers.

## An Example of the DIP Principle

Say you are a manager having some persons as an employee of which some are developers and some are graphic designers and rest are testers. Now let’s see how a naive design would look without any dependency inversion and what are the loopholes in that design.

### Code Snippet:
![[DIP Principle - bad example.png]]
### UML Diagram:
![[DIP Principle - bad example UML.png]]

This source code does lack the Dependency Inversion and it shows. Firstly it exposes everything about the lower layers to the upper layer, so there is no real [[abstraction]].
This results in a dependency where the manager must already know about the type of workers he may supervise. If a new type of worker comes under the manager, the whole class needs to be rejigged. 

### Code Snippet - With DIP:
![[DIP Principle - good example.png]]

### UML Diagram:
![[DIP Principle - good example UML.png]]

Implemented like this any other kind of employee can be added without making the manager explicitly aware of it.
