# HTML Lists, Control Flow with JS, and the CSS Box Model

__*Notes discription*__

## Learn HTML: Ordered and Unordered lists  
1. When should you use an unordered list in your HTML document?
    -  When it lsit items are not required to have a particular order.

2. How do you change the bullet style of unordered list items?  
    -  Changing the list style in CSS style sheet.

3. When should you use an ordered list vs an unorder list in your HTML document?  
    -  Use an ordered list when list items are required to be in a certain order or chronological order. Use an unorderedd lost when it doesn't matter. 

4. Describe two ways you can change the numbers on list items provided by an ordered list?  
    -  You can order list items with letters or roman numerals but changing the ```type``` attribute. Or you can start an ordered list on a specified number with the ```start``` attribute

-----

## Learn CSS: The Box Model
1. Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?  
    -  

2. List and describe the four parts of an HTML elements box as referred to by the box model.  
    - Margin: the space between a box and boxes around it.
    - Border: wraps around padding
    - Padding: the space directly surrounding the content.
    - Content: the heart of the box. where content is actually displayed.

-----

## Learn JS: Arrays. Operators and Expressions. Conditionals. Loops.

1. What data types can you store inside of an Array?
    - integer, string, boolean, array, and object

2. Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?  
    ``` 
    const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];
    ```
     - Yes. You can call values from the array with ```[arr][]``` for example if you wanted to access ```'artist'``` from this array of arrys, you would call ```[people][2][2]```  

3. List five shorthand operators for assignment in javascript and describe what they do.
    - Addition ```-=``` :subtrcts the value on the right from the value stored in the variable to the left
    - Multiplication ```*=``` : multiplies the value on the right by the value stored in the variable to the left then stores the new value in the variable
    - Addition ```+=``` :
    - Division ```/=``` :divides the variable on the left by the value on the right then stores that value in the variable
    - Remainder ```%=``` :store

4. Read the code below and evaluate the last expression and explain what the result would be and why.
    ```  
    let a = 10;
    let b = 'dog';
    let c = false;

    // evaluate this
    (a + c) + b;
    ```   
    - Because```false``` is a boolean no value will be returned for that. ```10``` is a number and ```'dog'``` is as string. This evaluates to "10dog" because these are all different data types and JavaScript defaults to returning the values as a string.

5. Describe a real world example of when a conditional statement should be used in a JavaScript program.
    - If you had a blog and wanted users to subscribe to your reading list. You could use a conditional statement to ensure user is not leaving the input field blank. 

6. Give an example of when a Loop is useful in JavaScript. 
    - from the previous example you would use a loop to to ensure the user is input is a valid email address. 