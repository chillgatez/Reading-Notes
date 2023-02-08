## Class 5 Reading Notes

### Designing web pages w CSS
______
#### What is CSS?
**_CSS (Cascading Style Sheet)_**
- is a rule based language for specifying how documents are presented to users 
- .css file extention
- rules are defined by specifying groups of styles that should be applied to particular elements or groups of elements 
- allows you to control exactly how HTML elements appear through the user agent
- can be used for basic document text styling (color and size)
- can be used to create layouts
- can be used for effects such like animations
**_CSS Syntax_**
-Use this example code  
    ```
    h1 {
  color: red;
  font-size: 5em;
    }
    ```  
    - the CSS rule opens with a __selector__ which indicates the HTML element to be styled  
    - Inside the braces are a pair of __declorations__-- color and font size  
    - Each declaration has a __property__ (specified before the colon) and __value__ (specified after the colon)  
- CSS properties have differnt allowable values depending on which porperty is being specified
- A CSS stylesheet will contain rules written one after the other  
    ```
    h1 {
  color: red;
  font-size: 5em;
    }

    p {
  color: black;
    }
    ```
