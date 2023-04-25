# Readings: React and Forms

## React Docs - Forms

1. What is a ‘Controlled Component’?
    - controlled components are controlled by React state. 

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    - We should update the state with their responses. This creates a constant reactive imput.

3. How do we target what the user is entering if we have an event handler on an input field?
    - set it to state so that it reacts to user input

-----

## The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?
    - to keep your code clean and dry.
2. Rewrite the following statement using a ternary statement:
    ```
        if(x===y){
        console.log(true);
        } else {
        console.log(false);
        } 
    ```
    -   ```
         x===y ? console.log(true) : console.log(false)

        ```