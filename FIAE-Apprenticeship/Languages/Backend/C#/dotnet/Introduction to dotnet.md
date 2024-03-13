# .NET 
---

## What is .NET?

.NET is a free, cross platform platform for building all kinds of applications. Multiple languages are supported, but [[Introduction to C-Sharp|C#]] is the most popular by far.
The idea behind the .NET platform was to deliver **productivity**, **performance**, **security** and **reliability**. It provides a *garbage collector*, its *type-safe* and *memory-safe* and offers concurrency via ==async/await== and ==Task== primitives.


## .NET Architecture

**.NET** is a virtual execution system called the [[Common Language Runtime]] (*CLR*) and a set of class libraries. The *CLR* is the implementation by Microsoft of the [[Common Language Infrastructure]] (*CLI*), an international standard. The *CLI* is the basis for creating execution and development environments in which languages and libraries work together seamlessly.

Source code written in **C#** is compiled into an [[Intermediate Language]] (*IL*) that conforms to the *CLI* specification. The *IL* code and resources, such as bitmaps and strings, are stored in an assembly, typically with an extension of _.dll_. An assembly contains a manifest that provides information about the assembly's types, version, and culture.

When the **C**# program is executed, the assembly is loaded into the *CLR*. The *CLR* performs [[Just-In-Time Compilation|Just-In-Time]] (*JIT*) compilation to convert the *IL* code to native machine instructions. The *CLR* provides other services related to [[Introduction to C-Sharp#Features of C|automatic garbage collection, exception handling, and resource management]]. Code that's executed by the *CLR* is sometimes referred to as "**managed code**." "**Unmanaged code**," is compiled into native machine language that targets a specific platform.

Language interoperability is a key feature of **.NET**. *IL* code produced by the **C#** compiler conforms to the [[Common Type Specification]] (*CTS*). *IL* code generated from **C#** can interact with code that was generated from the **.NET** versions of *F#, Visual Basic, C++*. There are **more than 20** other *CTS*-compliant languages. A single assembly may contain multiple modules written in different **.NET** languages. The types can reference each other as if they were written in the same language.

In addition to the runtime services, **.NET** also includes extensive libraries. These libraries support many different workloads. They're organized into namespaces that provide a wide variety of useful functionality. The libraries include everything from file input and output to string manipulation to [[XML]] parsing, to web application frameworks to [[Windows Forms]] controls. The typical **C#** application uses the **.NET** class library extensively to handle common "plumbing" chores.