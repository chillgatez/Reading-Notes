# Class 04 Readings: Classes & Memory Management

## Introduction to Classes

- As it relates to Classes & Memory Management, understanding the concept of reference types is crucial. In C#, a type defined as a class is considered a reference type. When you declare a variable of a reference type, it initially holds a value of null until you explicitly create an instance of the class using the new operator or assign it an object of a compatible type created elsewhere. Memory for the object is allocated on the managed heap, and the variable only contains a reference to the object's location.

- Classes in C# are declared using the class keyword followed by a unique identifier. They can include fields, properties, methods, and events, which are collectively known as class members. Objects, on the other hand, are concrete entities based on classes and are instances of those classes. You can create objects using the new keyword followed by the class name. Objects are passed to the programmer as references, and multiple object references can refer to the same object, allowing changes made through one reference to be reflected in others.

-----

## Constructors (C# Programming Guide)

- In the context of Classes & Memory Management, constructors play a crucial role as they are called whenever an instance of a class or a struct is created. Constructors allow you to set default values, control instantiation, and create flexible and readable code. A class or struct can have multiple constructors that take different arguments, enabling you to customize object creation based on specific scenarios.

- The process of initializing a new instance in C# follows a specific order:

  - Instance fields are set to their default values (usually 0).
  - Field initializers in the most derived type run.
  - Base type field initializers run, starting from the direct base through each base type to System.Object.
  - Base instance constructors run, starting from Object.- Object through each base class to the direct base class.
  - The instance constructor for the type runs, initializing the object.
  - Object initializers run if there are any, in the textual order.

- Constructors have a specific syntax: their name is the same as the name of the class or struct, and they don't have a return type. They may have an optional access modifier, and their parameter list defines the arguments needed to initialize the object. Additionally, C# supports expression body definitions for constructors, allowing a single statement implementation.

- Furthermore, there are static constructors, which initialize static members of a class or struct. Static constructors are parameterless and run before any instance constructor actions if they haven't run yet. They are defined using the static keyword and play a vital role in setting up the static members of a type.

-----

## Properties (C# Programming Guide)

- Properties in C# provide a flexible mechanism to read, write, or compute the value of private fields in a class. They act as special methods called accessors, allowing data to be accessed easily while still promoting the safety and flexibility of methods.

- *Difference between a static and an instance constructor:*

  - A static constructor is used to initialize static members of a class or struct and runs before any instance constructor actions if it hasn't run yet. It is parameterless and defined using the static keyword.

  - An instance constructor is called whenever an instance of a class or a struct is created. It can have multiple overloads that take different arguments, enabling customized object initialization based on specific scenarios.

- *How the use of a static constructor differs from setting properties/values:*

  - The purpose of a static constructor is to initialize static members, which are shared among all instances of a class. It is executed only once before any instance of the class is created and is not tied to any particular object's properties or values.

  - Setting properties/values, on the other hand, involves assigning specific values to the properties of an individual object. These values are unique to each instance of the class and can be set or changed independently.

- The article discusses various types of properties, including those with backing fields, expression body definitions, and auto-implemented properties. Properties with backing fields involve using private fields to set and retrieve property values, allowing for data validation and conversion. Expression body definitions simplify property accessors with single-line expressions, while auto-implemented properties provide a concise way to define properties without explicit backing fields. Beginning with C# 11, you can also use the ```required``` modifier to force client code to initialize specific properties.

## Stack v Heap: Introduction to Memory Management in .NET

- The Stack and Heap are two areas in memory where the .NET framework stores data and objects during program execution. Understanding how these areas work can help optimize the performance of applications and explain the behavior of variables used in programs.

- Difference between Stack and Heap:

  - The Stack is responsible for keeping track of what's executing in the code and is used for method calls and local variables. It follows the Last In First Out (LIFO) structure, where the most recently called method is at the top and gets executed first.

  - The Heap, on the other hand, is responsible for storing objects and data that can be accessed at any time. It is used for Reference Types and dynamically allocated objects. Memory management in the Heap is handled by the garbage collector, which periodically identifies and removes unused objects to reclaim memory.

- The article explains the distinction between Value Types and Reference Types, with Value Types being stored on the Stack and Reference Types on the Heap. It also introduces Pointers (References) as a type that indirectly accesses data in the Heap. The use of the Stack for method calls and local variables provides fast access and automatic cleanup, while the Heap's management involves garbage collection to handle unused objects and optimize memory usage.

- Review Question: How might you rethink the way you did projects in previous courses (HTML, JavaScript, React) to make more efficient use of memory?

## Fundamentals of Garbage Collection
