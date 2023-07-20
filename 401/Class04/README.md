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

Garbage collection in the Common Language Runtime (CLR) of C# serves as an automatic memory manager, relieving developers of manual memory management tasks. The garbage collector efficiently allocates and frees memory for objects, preventing memory leaks and unauthorized access to freed memory.

**Key Concepts and Benefits:**
1. *Memory Management Benefits:*
   - The garbage collector frees developers from manual memory release, reducing the risk of memory leaks.
   - Objects are efficiently allocated on the managed heap, and unused objects are reclaimed to keep memory available for future allocations.
   - Memory safety is ensured by preventing objects from accessing memory allocated for other objects.

2. *Memory Fundamentals:*
   - Each process has its own virtual address space, and the garbage collector allocates and frees virtual memory on the managed heap.
   - Virtual memory can be in three states: Free, Reserved, and Committed. The page file is used for backing up data when physical memory pressure is high.
   - Memory allocation on the managed heap is faster than unmanaged memory allocation, and objects are stored contiguously for quick access.

3. *Memory Release (Garbage Collection Process):*
   - Garbage collection occurs when low physical memory is detected, the memory usage surpasses a threshold, or explicitly called using `GC.Collect()`.
   - The garbage collector examines application roots (e.g., static fields, local variables, CPU registers) to find all reachable objects in a graph.
   - Unreachable objects (garbage) are identified and released through memory compaction, optimizing memory usage.
   - Large objects are usually not compacted to avoid performance penalties.

4. *Generations:*
   - The managed heap is divided into three generations (0, 1, and 2) to handle short-lived and long-lived objects separately.
   - Generation 0 contains short-lived objects, generation 1 is a buffer between short-lived and long-lived, and generation 2 contains long-lived objects.
   - Garbage collections primarily target short-lived objects in generation 0, and objects surviving collections are promoted to higher generations.

5. *Ephemeral Generations and Segments:*
   - Generations 0 and 1 are ephemeral generations allocated in the ephemeral segment.
   - When an ephemeral garbage collection occurs, surviving objects are moved to the new ephemeral segment, and the old one becomes generation 2 segment.

6. *Garbage Collection Phases:*
   - Garbage collection involves marking, relocating, and compacting phases.
   - Marking phase identifies live objects, relocating phase updates references to objects to be compacted, and compacting phase reclaims memory and compacts surviving objects.

7. *Handling Unmanaged Resources:*
   - While garbage collection manages most objects automatically, unmanaged resources require explicit cleanup.
   - Developers should provide a Dispose method to release unmanaged resources explicitly and use safe handles or override `Object.Finalize()` as a backup.

**Comparison of Garbage Collection with the Lifecycle of Normal Household Items:**

Imagine managing the objects in your home as if it were garbage collection in C#. In your house, you have various items, each with its lifecycle:

1. *Object Acquisition:*
   - Just like the CLR reserves a contiguous region of address space (managed heap) for an application, you allocate specific areas in your house for different items (e.g., shelves for books, cabinets for dishes).

2. *Usage and Release:*
   - As you use items, they might become unnecessary or outdated (e.g., old magazines, broken toys). You decide to release these items and free up space.

3. *Memory (Storage) Management:*
   - You have a limited amount of storage space in your house. When you acquire new items, you organize them efficiently to make the best use of available space.

4. *Garbage Collection:*
   - When you decide to declutter your house, you perform garbage collection. You identify objects (items) that are no longer being used (garbage) and remove them from your living space to free up room.

5. *Generations and Lifespan:*
   - Objects in your home can have different lifespans based on their usage. Everyday items (generation 0) like food containers get removed more frequently, while long-lived items (generation 2) such as furniture stay in use for longer periods.

6. *Unmanaged Resources:*
   - Some items require explicit cleanup when you no longer need them (e.g., expired food, old batteries). You must dispose of these items properly to avoid clutter and ensure safety.

By comparing garbage collection in C# with the lifecycle of household items, you can better understand how the CLR efficiently manages memory in your applications, just as you manage space and resources in your home.

## Summary

Imagine you are the architect of a grand library, and the process of building and managing this library represents "Classes & Memory Management."

1. **Classes:**
   In this analogy, think of "Classes" as different types of rooms in the library, each serving a specific purpose. For instance, you have rooms for books (Book class), rooms for magazines (Magazine class), and rooms for multimedia materials (Media class). Each room (class) is designed with its unique attributes and functionalities to store and organize the respective materials efficiently.

2. **Memory Management:**
   Memory management in the library corresponds to how you allocate and utilize space in each room. You must be mindful of the available space, ensuring that each room (class) has enough capacity to accommodate the materials it holds. When new books or materials arrive, you must allocate space for them appropriately. Similarly, when materials become outdated or no longer needed, you clear space by removing them (garbage collection) from the shelves, making room for new additions.

3. **Object Lifecycle:**
   Each book, magazine, or multimedia material (object) has its lifecycle within the library. When a new book (object) arrives, it is registered in the library's database (instantiation), assigned to the relevant room (class), and becomes accessible to library visitors (referencing). When the book is no longer popular or relevant (unreferenced), it might be moved to the archives (memory deallocation) or discarded during a decluttering process (garbage collection).

4. **Inheritance and Polymorphism:**
   Just as a library might have different types of rooms that share common features (e.g., a study area in multiple room types), "Inheritance" allows classes to inherit properties and methods from a common base class. "Polymorphism" enables flexibility in handling various materials, like different checkout procedures for books and multimedia items, adapting to the specific needs of each class.

By building and managing the library with efficient memory allocation and a well-organized classification system, you can ensure the smooth functioning of the library, just like managing memory in a program using classes and proper memory management techniques. The analogy helps us understand the significance of classes and memory management in creating and maintaining well-structured and efficient software systems.
