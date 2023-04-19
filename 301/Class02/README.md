# State and Props

## React lifecycle

1. Based off the diagram, what happens first, the ```render``` or the ```componentDidMount```?
    - ```render``` happens first
2. What is the very first thing to happen in the lifecycle of React?
    - Constustor occurs during the mounting phase of the lifecycle.
3. Put the following things in the order that they happen: ```componentDidMount```, ```render```, ```constructor```, ```componentWillUnmount```, ```React Updates```
    -```constructor``` > ```render``` > ```componentDidMount``` > ```React Updates``` >```componentWillUnmount```
4. What does ```componentDidMount``` do?
    - It is a method that is invoked immediately after a component is mounted. 

-----

## React State Vs Props

1. What types of things can you pass in the props?
    - things you want to initialize your component to or what you want it to render. you can pass in any javaScript data type as props. 
2. What is the big difference between props and state?
    - Props are handled externally while State is handled internally. When you change the state inside of your application its going to re-render that section of the application. Props are likily state stored somewhere else in the app and is being passed down as props. Props can be inherited while state will only be accessible in the component it is defined in.
3. When do we re-render our application?
    -
4. What are some examples of things that we could store in state?
    -forms and input data