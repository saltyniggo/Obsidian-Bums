# C-Sharp
---


## What is C# ?

**C#** is a modern, [[Object Oriented Programming|object-oriented]], and [[Type-safe Languages|type-safe]] programming language. **C#** enables developers to build many types of secure and robust applications that run in [[Introduction to dotnet|.NET]]. **C#** has its roots in the [[Introduction to C|C]] family of languages and will be immediately familiar to [[Introduction to C|C]], [[Introduction to C++|C++]], [[Introduction to Java|Java]], and [[Introduction to JavaScript|JavaScript]] programmers. 
**C#** provides language constructs to directly support *object-oriented* and *component-oriented concepts*, making **C#** a natural language in which to create and use software components.
Since its origin, C# has added features to support new workloads and emerging software design practices. At its core, C# is an _**object-oriented**_ language. You define types and their behavior.


---


## Features of C# 

Several features help create robust and durable applications. [[Garbage Collection]] automatically reclaims memory occupied by unreachable unused objects. **Nullable** types guard against variables that don't refer to allocated objects. [[Exception Handling]] provides a structured and extensible approach to error detection and recovery. [[Lambda Expressions]] support functional programming techniques. [[Language Integrated Query]] (*LINQ*) syntax creates a common pattern for working with data from any source. Language support for [[Async|asynchronous operations]] provides syntax for building distributed systems. C# has a [[Type System Unification|unified type system]]. All C# types, including [[Primitive Types]] such as ==int== and ==double==, inherit from a single root ==object== type. All types share a set of common operations. Values of any type can be stored, transported, and operated upon in a consistent manner. Furthermore, C# supports both user-defined *reference types* and *value types*. C# allows dynamic allocation of objects and in-line storage of lightweight structures. C# supports generic methods and types, which provide increased type safety and performance. C# provides iterators, which enable implementers of collection classes to define custom behaviors for client code.

C# emphasizes _**versioning**_ to ensure programs and libraries can evolve over time in a compatible manner. Aspects of C#'s design that were directly influenced by versioning considerations include the separate ==virtual== and ==override== modifiers, the rules for method overload resolution, and support for explicit interface member declarations.


---


## Hello World

Here is the `Hello World` program in C#:

> using System;
> 
> class HelloWorld
> {
> 	static void Main()
> 	Console.WriteLine("Hello World");
> }

The `Hello World` program starts with a `using` directive that references the `System` **namespace**. **Namespaces** provide a hierarchical means of organizing C# programs and libraries. **Namespaces** contain types and other **namespaces**—for example, the `System` namespace contains a number of types, such as the `Console` class referenced in the program, and many other **namespaces**, such as `IO` and `Collections`. A `using` directive that references a given **namespace** enables unqualified use of the types that are members of that **namespace**. Because of the `using` directive, the program can use `Console.WriteLine` as shorthand for `System.Console.WriteLine`.

The `Hello` class declared by the `Hello World` program has a single member, the method named `Main`. The `Main` method is declared with the `static` modifier. While instance methods can reference a particular enclosing object instance using the keyword `this`, static methods operate without reference to a particular object. By convention, a static method named `Main` serves as the entry point of a **C#** program.

The line starting with `//` is a _single line comment_. **C#** single line comments start with `//` continue to the end of the current line. **C#** also supports _multi-line comments_. Multi-line comments start with `/*` and end with `*/`. The output of the program is produced by the `WriteLine` method of the `Console` class in the `System` namespace. This class is provided by the standard class libraries, which, by default, are automatically referenced by the compiler.






###### External Links:
---
[W3 C# Tutorial](https://www.w3schools.com/cs/index.php)
[C# 101 - Video](https://learn.microsoft.com/en-us/shows/CSharp-101/?WT.mc_id=Educationalcsharp-c9-scottha)
[C# for Beginners - Video](https://www.youtube.com/watch?v=gfkTfcpWqAY&list=PLTjRvDozrdlz3_FPXwb6lX_HoGXa09Yef)
[A tour of the C# language](https://learn.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/)

---
