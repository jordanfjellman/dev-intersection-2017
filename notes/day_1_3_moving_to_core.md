# Moving to ASP.NET Core from ASP.NET 4.6

- Jay Schmelzer (jaysch@microsoft.com)

## .NET World

There are for the for-seeable future, there will be three members of the family: 

- .NET Framework (not going anywhere)
- .NET Core
- .Xamarin

## Standard Approach to Modernization

1. Articulate the business goals (Why are you moving to core?)
2. Evaluate modernization strategies
3. Do it!

## Why would you want to move? 

- Multi-platform support
- Performance challenges
- Transforming from monolithic app to microservices
- Adopting open source strategy

## Common Modernization Strategies

Evolution - Extend and Transform over time

- Add new capabilities enabled by ASP.NET Core
- Transform a monolithic app to services over time

Full Transformation - "Lift and Shift"

- Expand addressable customer segments - support Windows and Linux
- Employ moder patterns and practices - containers, Dev/Ops, etc.

Hybid

- Add new cpabilities using modern patterns
- Transform select functionality - scale certain pain points

## Common Constraints

Move only pieces that make sense

- If there's not a good reason to move, don't move

Identify key integration points

- Regardless of conversion of migration, enable progressing in stages

Re-evaluate existing code/logic

- Dont' take code wholesale

Understand where you need to share business logic

- Libraries - .NET Standard
- Code -shared projects, #ifdef, separate solutions

## Standard Approach

1. Identify
2. Analyze 
3. Build

### Identify

What do we need to move?

### Analyze

How difficult will it be/what is needing to change?

__Portablility Analyzer__Tool to analyze current project for Core conversion - https://github.com/microsoft/dotnet-apiport.
Can integrate the tool into CI systems.
Could be installed as an extension in Visual Studio.

### Build

What are common patterns that need to be removed/changed in what we do? (Utilities, logging, etc.)

Convert configuration using a CustomConfigurationProvider.
Will allow you to slowly move over configs.

## What is .NET Standard

Defines a collection of .NET APIs

.NET standard 2.0 is coming, should I wait? 

- Are we dependent on old frameworks?
- It adds a lot of common APIs back into core.

## Summary

- Understand why you are moving
- Evaluate the options
    - ASP.NET on .NET Framework
    - ASP.NET Core on .NET Framework
    - ASP.NET Core on .NET Core

Note: They all work in containers, they are just different sizes.
Note: .NET Core has things that the .NET standard does not have.