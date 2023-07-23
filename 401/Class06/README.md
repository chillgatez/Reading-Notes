# Class 06: Readings: Object Oriented Principles

## OOP Principles

- Abstraction: Modeling relevant attributes and interactions of entities as classes to define an abstract representation of a system.

- Encapsulation: Hiding the internal state and functionality of an object and only allowing access through a public set of functions.

- Inheritance: Ability to create new abstractions based on existing abstractions, enabling classes to inherit behavior and properties from their base class.

- Polymorphism: Ability to implement inherited properties or methods in different ways across multiple abstractions, allowing for flexibility and dynamic method dispatch.

This article builds on the concepts covered in previous tutorials and extends the example of a BankAccount class to demonstrate inheritance and polymorphism. It introduces three new account types: InterestEarningAccount, LineOfCreditAccount, and GiftCardAccount. Each of these classes inherits from the BankAccount class and provides its own unique behavior.

To facilitate the various account types' month-end transactions, a virtual method called "PerformMonthEndTransactions" is added to the BankAccount class. The derived classes (InterestEarningAccount, LineOfCreditAccount, and GiftCardAccount) override this method to implement their specific month-end behaviors.

Additionally, the LineOfCreditAccount class introduces a new overdraft rule using a virtual method "CheckWithdrawalLimit." This method allows the LineOfCreditAccount to charge a fee for overdrawn accounts instead of rejecting the transaction.

Overall, this article demonstrates how to apply object-oriented programming principles effectively to create flexible and extensible code with reusable components. By using inheritance and polymorphism, developers can create specialized classes that build on existing functionality, leading to more maintainable and scalable codebases.

-----

## Inheritance

Inheritance is one of the three primary characteristics of object-oriented programming, along with encapsulation and polymorphism. It enables the creation of new classes that reuse, extend, and modify behavior defined in other classes. Inheritance establishes a relationship between a base class and a derived class. The derived class can have only one direct base class, but inheritance is transitive, allowing it to inherit members declared in multiple levels of base classes.

Conceptually, a derived class represents a specialization of the base class. For instance, if we have a base class "Animal," we can create derived classes like "Mammal" and "Reptile," where each derived class represents a different specialization of the base class "Animal."

Interfaces play a crucial role in inheritance as well. They define a set of members that classes and structs must implement if they inherit the interface. Interfaces enable defining specific capabilities for classes that may not have an "is a" relationship, offering flexibility in defining class relationships.

Additionally, inheritance supports abstract and virtual methods, which allow derived classes to override methods from the base class, providing the foundation for polymorphism.

-----

## Abstract and Sealed Classes and Class Members

In C# programming, abstract classes and class members, as well as sealed classes and class members, play important roles in class hierarchy and inheritance.

**Abstract Classes and Class Members:**

- An abstract class is declared using the "abstract" keyword before the class definition, and it cannot be instantiated directly.

- The purpose of an abstract class is to provide a common base definition that multiple derived classes can share.

- Abstract classes may contain abstract methods, which are methods declared with the "abstract" keyword and have no implementation.

- Derived classes of an abstract class must implement all the abstract methods defined in the base abstract class.

- An abstract class can override virtual methods inherited from a base class with its own abstract methods.

**Sealed Classes and Class Members:**

- A sealed class is declared using the "sealed" keyword before the class definition, and it cannot be used as a base class.

- Sealed classes prevent derivation, meaning they cannot be further subclassed.

- Some run-time optimizations can make calling sealed class members slightly faster.

- In a derived class, you can use the "sealed" keyword before an overridden virtual method declaration to prevent further derived classes from overriding it.

- The use of abstract and sealed classes and members allows developers to design more controlled and structured class hierarchies and inheritance patterns in C# programs.

-----

## Polymorphism

Polymorphism is a fundamental concept in object-oriented programming and is often considered the third pillar alongside encapsulation and inheritance. The term "polymorphism" comes from the Greek words "poly" (many) and "morphe" (shape), and it has two main aspects:

**Run-time Polymorphism:**

- Objects of a derived class can be treated as objects of a base class at run time, meaning they can be used interchangeably in places like method parameters and collections or arrays.

- This run-time polymorphism occurs when the object's declared type is not identical to its run-time type, allowing for flexible handling of different derived classes as instances of the same base class.

**Virtual Methods and Overrides:**

- Base classes can define and implement virtual methods, which can be overridden by derived classes to provide their own implementation.

- When client code calls a virtual method, the Common Language Runtime (CLR) looks up the run-time type of the object and invokes the appropriate override of the virtual method, allowing for dynamic method dispatch.

- This enables you to work with groups of related objects in a uniform way, as demonstrated in the example of a drawing application with different shape classes that all inherit from a common Shape base class and override the Draw method.

In C#, every type is polymorphic because all types, including user-defined types, inherit from Object. Polymorphism allows for flexible and extensible code by enabling different classes to be treated uniformly through their shared base class, and it is a key concept in achieving reusable and maintainable object-oriented designs.

-----

## Summary

Imagine a bustling bakery as a representation of a software system. The bakery owner aims to expand their business by offering a wide variety of baked goods to cater to different tastes and preferences. To achieve this, they take inspiration from object-oriented programming principles.

In the bakery, the process begins with abstraction. The bakery owner creates abstract recipes for each type of baked item, such as cakes, cookies, and bread. These recipes serve as a high-level blueprint, defining the relevant attributes and interactions common to each product. The abstract recipes provide a clear definition of what each baked good should include, without diving into specific details.

Encapsulation is key to the bakery's smooth operation. Each baker has their own workstation, complete with specialized tools and ingredients. They work independently, managing the intricate baking processes hidden from the customers' view. When customers visit the bakery, they interact only through a service counter, placing orders and receiving their freshly baked goods. The internal complexities of baking are encapsulated, ensuring a consistent and secure experience for the customers.

To offer a premium line of cakes with unique flavors and features, the bakery leverages the concept of inheritance. The bakery introduces a new class of premium cakes that builds upon the existing cake recipe. The premium cakes inherit the core attributes and functionalities of regular cakes but introduce additional features and flavors. By doing so, the bakery can create specialized and high-end products without starting from scratch. This inheritance allows them to reuse the existing cake recipe while extending it to meet specific customer demands.

During holidays and special events, the bakery attracts customers with customized cakes shaped like animals, vehicles, or other objects. This creativity is achieved through the concept of polymorphism. While these custom cakes have unique external appearances, they all follow the same fundamental methods of preparation and baking. The bakery uses polymorphism to create diverse designs while retaining the core functionality of the underlying cake. This flexibility allows them to cater to various customer preferences without compromising on the baking process.

In conclusion, the bakery analogy illustrates how object-oriented programming principles empower the business to offer a diverse range of baked goods while maintaining consistency and reusability across its products. The abstraction of recipes, encapsulation of baking processes, inheritance of premium cakes, and polymorphism of customized cakes mirror the key concepts of object-oriented programming in a real-world scenario, facilitating the bakery's success and growth in the competitive market.
