# Passing Functions as Props

## React Docs - lists and keys

1. What does .map() return?
    - map returns a new array of the same length as the mapped array
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    - use the .map() function
3. Each list item needs a unique ____.
    - key
4. What is the purpose of a key?
    - keys help React identify which items have changed, are added, or are removed

-----
## The Spread Operator

1. What is the spread operator?
    - The spread operator ```...``` is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments

2. List 4 things that the spread operator can do.
    - You can use to copy, concatenate or combine arrays. You can use to combine objects. It can be used when adding state in React or adding an item to a list. 
3. Give an example of using the spread operator to combine two arrays.
    - ```
        const someArray = [1,2,3,4]
        const anotherArray = [5,6,7,8]
        const someOtherArray = [...someArray, ...anotherArray]
        console.log(someOtherArray)
        ```
        The ```console.log``` should render an array that looks like ```[1,2,3,4,5,6,7,8]```

4. Give an example of using the spread operator to add a new item to an array.
    - ``` 
        const someArray = [1,2,3,4]
        const someMoreArray = [0, ...someArray]
        console.log(someMoreArray)
        ```
         The ```console.log``` should render an array that looks like ```[0,1,2,3,4]```

5. Give an example of using the spread operator to combine two objects into one.
    - ```
        const someObject = {name: "Kelsee"}
        const anotherObject = {age: "27"}
        const someOtherObject = {...someObject, ...anotherObject}
        console.log(someOtherObject)
        ```
         The ```console.log``` should return an object that looks like ```{name: Kelsee, Age: 27}```

## How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between components?
    - create a function
2. In your own words, what does the increment function do?
    - The increment function takes in a value and if the value matches the value of the one that is passed through, it updates the count by 1
3. How can you pass a method from a parent component into a child component?
    - you can use props to pass amehtod froma parent to a child component
4. How does the child component invoke a method that was passed to it from a parent component?
    - ```props.method``` 