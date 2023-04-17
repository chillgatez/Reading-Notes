1. A function ____________ loads before any code is executed. 
Declaration 
 
2.  In the line of code 
var turtle = newAnimal("Michelangelo",1); 
"Michelangelo" and 1 are: 
Arguments 
 
3.  Assuming there are no other CSS declarations, and no inline CSS styles, what will the following CSS declaration do to 
the body element and other HTML elements inside the body tag? 
Change background color of all HTML elements within body to black and change color of all text to white 
 
4.  In JavaScript, what is the difference between the "==" and "===" operators? 
"===" means equality without type coersion, meaning the two values being compared must be of the same data type (and 
value) to return true. 
 
5.  Please pick the statement that best describes the default display for the HTML elements listed below: 
<span> 
<div> 
<h1>, <h2>, <h3>, <h3>, <h5>, <h6> 
<ul> 
All listed elements, except <span>, are block elements by default 
 
6.  Consider the following CSS rule: 
h1 {  
  border-width: 5px; 
  border: dashed blue; 
} 
After adding the CSS properties listed above, at 100% zoom, what will be the computed width of the border around 
an <h1>? 
Consider rendering it in your browser and checking it with the inspector. 
3px  
7.  What does DOM stand for? 
Document Object Model 
 
8.  Pick the statement that best describes the following JavaScript code 
 
var movies = ["The Matrix", "Frozen"]; 
typeof(typeof(movies)); 
The code will produce valid results as both typeof calls are invoked with valid JavaScript types 
 
9.  Which of the following is/are true about JavaScript object properties? 
A. All properties can be accessed through "." operation 
B. All properties are automatically locally scoped but may be accessed by using ‘prototype’ 
C. Variables declared inside constructor functions are locally scoped and cannot be directly accessed as properties 
D. Variables declared inside constructor functions are globally scoped 
E. Properties that contain Boolean values may not be accessed with bracket notation and are only accessible through “.” 
Operation 
C 
10. Which of the following statements about the CSS float property are true? 
A. The CSS "float" property affects the layout of elements in a page 
B. Content flows down the right side of a left-floated box 
C. Adding a "float" CSS property allows an element to be positioned outside its containing element 
D. "float" CSS property can have pixel values such as "10px" or string values such as "left", "right" 
E. "clear" CSS property can prevent content from trying to flow around or alongside a floated element 
A, B & E 
 
11. Which of the following statements would evaluate as truthy, given the below variable definitions? 
var dog = { 
 breed: "Beagle", 
 weight: 30, 
 group: "Hound" 
} 
var key = "weight"; 
A. dog[key] === 30 
B. dog["weight"] == "30"; 
C. "weight" in dog 
D. dog.weight 
E. dog.key === 30; 
F. dog.hasOwnProperty('weight'); 
A, B, C, D, & F 
 
12. What is the term we use for a function that is associated with (or, attached to) an object? 
A method 
 
13. True/false: An object is a collection of properties and methods. 
True 
 
14. The elements we need to put inside of a form are: input, button and _____? 
label 
 
 
15. In the following code which line shows the conflicting code from your working branch? 
1    <<<<<<<<<<< HEAD 
2    <h1>Code Fellows</h1> 
3    =========== 
4    <p>Code Fellows</p> 
5    >>>>>>>>>>> master 
Line 2 
 
16. What does Math.floor() do? 
Returns the largest integer less than or equal to a given number 
 
17. When used inside of an object, this refers to: 
The object that it is used in 
var rabbit = {};  
This line of code creates an object by using: 
Object literal notation 
 
18. True/false: Figuring out your problem domain should only be done after you start writing code; otherwise you do not 
know whether the code actually works. 
False 
 
19. Check out the JavaScript code below: 
var units = "years"; 
var davidAge = 65; 
var johnAge = 40; 
var ageDifference = davidAge - johnAge; 
alert("The age difference is " + ageDifference + " " + units); 
Why should we make a separate variable for the age difference? 
The code is more readable with an appropriately named variable, rather than including an arithmetic expression inside of 
parentheses inside of a concatenation. 
 
20. What type of CSS positioning takes an element out of normal flow and positions it in relation to its containing 
element? 
Absolute positioning 