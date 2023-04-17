# Introduction to React and Components

## Component-Based Architecture

1. What is a “component”?
    - A set of well-defined functionalities. Components are intended to interact with each other. They encapsulate a function's implementation and exports it as a higher-level interface. They are modular, portable, replaceable, and resuable.

2. What are the characteristics of a component?
    - Reusability - designed to be used in differnt situations in differnt applications.
    - Replacable - may be freely substituted w similar components.
    -Not Context Specific - designed to operate in differnt enviornments and contexts.
    - Extensible - can be extended from existing components to provide new behavior.
    - Encapsulated - allows caller to use its functionality, and do not expose details of the internal processes or any internal variables or state
    - Independent - designed to have minimal dependencies on other components
    
3. What are the advantages of using component-based architecture?
    - Ease of deployment and development, reduced cost, reusability, reliability, etc...

-----
## What is Props and How to Use it in React

1. What is “props” short for?
    - Properties
2. How are props used in React?
    - Props are used for passing data from one component to another.
3. What is the flow of props?
    - unidrectional from parent to child