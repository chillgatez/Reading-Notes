# Functional Programming

## Functional Programming Concepts

1. What is functional programming?
    - Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions.

2. What is a pure function and how do we know if something is a pure function?
    - A pure function is a function that satisfies two main criteria:
        1. It returns the same result if given the same arguments, meaning it is deterministic.
        2. It does not cause any observable side effects, such as modifying external objects or relying on mutable state.

3. What are the benefits of a pure function?
    - They are easier to reason about and understand since they have no hidden dependencies or side effects.
    - They are more testable because they produce consistent results for the same inputs.
    = They can be safely reused and composed, allowing for modular and maintainable code.
    - They facilitate parallel and concurrent programming, as they eliminate concerns related to shared mutable state.

4. What is immutability?
    = Immutability refers to the property of data that cannot be changed once it is created. 

5. What is Referential transparency?
    - Referential transparency is a property of a function or expression that consistently yields the same result for the same input, regardless of where and when it is called. It allows replacing a function call with its evaluated value without affecting the program's behavior. 
------

## Node JS Tutorial for Beginners #6 - Modules and require()

1. What is a module?
    - A module is a self-contained unit of code in Node.js that contains functions, variables, and classes with a specific functionality. Modules are used to organize and split up code into logical components, making it easier to manage, maintain, and reuse in an application.

2. What does the word ```require``` do?
    - The word ```require``` is a function in Node.js used to import or include modules into the current file.

3. How do we bring another module into the file the we are working in?
    - To bring another module into the file you are working in, you use the ```require``` function and provide the path to the module as a string.

4. What do we have to do to make a module available?
    - To make a module available for use in other files, you need to explicitly define what part of the module should be accessible outside of the module. 