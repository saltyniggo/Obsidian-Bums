# Introduction to the AutoMapper
---

## What is the AutoMapper?

The AutoMapper is a popular open-source library in [[Introduction to C-Sharp|C#]] that simplifies *mapping* data between different classes or objects. It helps to eliminate repetitive and error-prone code when copying data from one object to another. AutoMapper is especially useful in scenarios like mapping database entities to [[DTOs]] or [[MVVM Pattern|ViewModel objects]].
It maps the properties of two different objects by transforming the input object of one type to the output type of another.


## Advantages and Disadvantages

| **Advantages**                               | **Disadvantages**                       |
| -------------------------------------------- | --------------------------------------- |
| Reduce Repetitive Code                       | Performance Overhead                    |
| Improve Code Readability and Maintainability | Complexity in Debugging                 |
| Consistency in Mapping                       | Learning Curve                          |
| Custom Mapping Capabilities                  | Overreliance on Convention              |
| Ease of Use                                  | Unnecessary Complexity for Simple Tasks |
| Reduce Human Error                           |                                         |


## Do's and Dont's

As with most other components in an application, there are certain guidelines and best practices that you should follow, when using the AutoMapper:
### Do's:
- Always use the -  `AutoMapper.Extensions.Microsoft.DependencyInjection` package in [[Introduction to dotnet|ASP.NET Core]] with `services.AddAutoMapper(assembly[])`. This package will perform all the scanning and dependency injection registration. We only need to declare the Profile configurations.
- Always organize configuration into *Profiles*. *Profiles* allow us to group a common configuration and organize mappings by usage. This lets us put mapping configuration closer to where it is used, instead of a single file of configuration that becomes difficult to edit/maintain.
- Always use configuration options supported by [[LINQ]] over their counterparts as [[LINQ]] query extensions have the best performance of any mapping strategy.
- Always flatten [[DTOs]]. AutoMapper can handle mapping properties A.B.C into ABC. By flattening our model, we create a more simplified object that won’t require a lot of navigation to get at data.
- Always put common simple computed properties into the source model. Similarly, we need to place computed properties specific to the destination model in the destination model.

### Dont's:
- Do not call `CreateMap()` on each request. It is not a good practice to create the configuration for each mapping request. Mapping configuration should be done once at startup.
- Do not use inline maps. Inline maps may seem easier for very simple scenarios, but we lose the ease of configuration.
- If we have to write a complex mapping behavior, it might be better to avoid using `AutoMapper` for that scenario.
- Do not put any logic that is not strictly mapping behavior into the configuration. `AutoMapper` should not perform any business logic, it should only handle the mapping.
- Avoid sharing [[DTOs]] across multiple maps. Model your [[DTOs]] around individual actions, and if you need to change it, you only affect that action.
- Do not create [[DTOs]] with circular associations. `AutoMapper` does support it, but it’s confusing and can result in quite bad performance. Instead, we can create separate [[DTOs]] for each level of the hierarchy we want.

## When to use the AutoMapper

There are quite a few situations in which you should consider to use the AutoMapper:
- **Large Projects with Complex Object Models:** In large-scale applications with complex domain models and [[DTOs]], AutoMapper can save significant time and effort by automating the mapping process.
- **Projects with Repetitive Mapping Code:** If your project involves a lot of repetitive and tedious mapping code (like copying properties from one object to another), AutoMapper can help reduce this boilerplate code, making your codebase cleaner and easier to maintain.
- **When Consistency in Mapping Rules is Important:** AutoMapper helps maintain consistent mapping rules across your application. This is particularly useful in team environments or large projects where different developers might otherwise implement mappings inconsistently.
- **CRUD Operations in Layered Architecture:** In applications with a clear separation of concerns, such as [[MVC Pattern|MVC]] applications, AutoMapper is valuable for transforming data between layers (e.g., from data access objects to business logic objects or business logic objects to view models).
- **When You Need Customizable Mapping Logic:** AutoMapper is not just for straightforward mappings; it also allows for complex and custom mapping logic. This is useful when you have specific rules for how certain properties should be mapped or transformed.
- **In Applications Where Development Speed is a Priority:** Rapid application development can benefit from AutoMapper, as it speeds up writing and updating code involving object mappings.

However, not in all scenarios AutoMapper will be the best choice:
- **For Simple Projects:** If your project is simple, with few mappings, or if the mappings are straightforward, the overhead of introducing a third-party library might not be justified.
- **Performance-Critical Applications:** Be cautious in performance-sensitive applications, as AutoMapper can introduce some overhead, especially if not configured optimally.
- **When Explicit Control is Preferred:** In cases where you need or prefer explicit control over every aspect of the mapping, or if you want to avoid the abstraction introduced by AutoMapper, manual mapping might be a better choice.