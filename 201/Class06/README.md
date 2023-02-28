# Problem Domain, Objects, and the DOM

## JavaScript Object Basics

1. How would you describe an object to a non-technical friend you grew up with?
    - An object is like a gift basket. It is a collection of related data. Within the objects are variables and functions called properties and methods. These are the contents of the basket. There can be any number or combination of properties and methods within an obeject.

2. What are some advantages to creating object literals?
    -  

3. How do objects differ from arrays?
    - An array can exist within an objects, but an object can not be an element of an array.

4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
    - If an object property name is held in a variable, then you can't use dot notation to access the value, but you can access the value using bracket notation.

5. Evaluate the code below. What does the term ```this``` refer to and what is the advantage to using ```this```?  
     ``` 
     const dog = {  
        name: 'Spot',  
        age: 2,  
        color: 'white with black spots',  
        humanAge: function (){  
            console.log(`${this.name} is ${this.age*7} in human years`);
        }
    }   
     ```
    - ```this``` refers to the current object the code is the being written inside. In this case ```this``` is refering to ```dog```. If you create more than one object literal ```this``` enables you to use the same method definition for every object you create.