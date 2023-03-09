# Readings: Forms and JS Events

## HTML Forms: How to structure a web Forms

1. Why are forms so important in web development?  
    - Web forms are a tool for interacting with users. Commonly they are used to collect data from users or allow users to control a user interface. Its a direct point of contact for user input.

2. When designing a form, what are some key things to keep in mind when it comes to user experience?  
    -  Accessability as well as functionality and relevance.

3. List 5 form elements and explain their importance.  
    - ```<feildset>``` creates a group of widgets that share the same purpose.

    - ```<legend>``` formally describes the purpose of the ```<feildset>``` element. assistive technologies will use this element as if it is part of the label. Usually peaking the legend's conent before the label

    - ```<label>``` formally defines a label for an HTML form widget. It creates accesiblity within the form. When implemented properly screen readers will speak the lable along with related instructions.

    -```<textarea>``` is a multi-line plain-text editing control. Can be used to allow users to enter large amounts of text.

    - ```<button>``` 

-----

## Learn JS: Intorduction to Events
1. How would you describe events to a non-technical friend?  
    - 

2. When using the addEventListener() method, what 2 arguments will you need to provide?
    - the type of event and a fucntion to call when it occurs

3. Describe the event object. Why is the target within the event object useful?
    -  Event objects contain methods and properties of the event that has occured. Event objects are automatically passed to event handlers to provide extra features and information. The taraget property of the event object is always a reference to the element the event occured upon.

4. What is the difference between event bubbling and event capturing?
    - They are similar in how they fire off. Event bubbling starts from where the event is called and goes up the DOM tree. Event ccapture works in reverse.