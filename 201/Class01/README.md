# Getting Started: How the web works, design and process basics
__*In this class reading we will be addressing foundational material in regards to website design and processing standards. These readings are meant to establish a fundemental understanding of web development*__

## Getting Started 
1. Compose a short poem describing how HTTP sends data between computers.  
    - The browser sends an HTTP resquest  
    The server answers at its behest  
    using TCP/IP 
    This message and data is sent across the internet 
2. Describe how HTML, CSS, and JS files are “parsed” in the browser.  
    - HTML file is parsed first. Once the browser recognizes elements that reference stylesheets and script files it sends a request back to the server and then parses the CSS and JavaScript. An in-memory DOM tree and CSSOM is generated by the browser from the parsed HTML and CSS respectively. It complies and executes. 
3. How can you find images to add to a Website?  
    - You can simply google search images and use filters to make sure you aren't violating any copyright. You can also use a graphic and editor like photoshop and GIMP.
4. How do you create a String vs a Number in JavaScript?  
    - Numbers can just be input as simple number characters. They can not be spelled out with text. A string is created by enclosing text in single or double quotation marks.
5. What is a Variable and why are they important in JavaScript?  
    - Variables store values of different data types. They are important because we need values to write and run functions.

-----
## Introduction to HTML


1. What is an HTML attribute?  
    - An attribute contains information that won't appear in the content but is instead used to target the element with specific information. 


2. Describe the Anatomy of an HTMl element.  
    - an html element needs an opening tag which would attritbutes if any are assigned, content such as paragraph text, source links, etc, and a closing tag.  

3. What is the Difference between ```<article>``` and ```<section>``` element tags?  
    - The ```<section>``` tag is a generic standalone section of a document and should always have a heading. The ```<article>``` tag specifically references a standalone piece such as newpaper article.

4. What Elements does a “typical” website include?
    - header, nav bar, main content or body, side bar, and footer

5. How does metadata influence Search Engine Optimization?
    - Meta data usually contains decriptive information about the document, important keywords, author names etc. The information that is loaded first and used by seacrh engines.

6. How is the ```<meta>``` HTML tag used when specifying metadata?
    - The ```<meta>``` tag is used to describe the type of data is within the tag.

-----
## Miscellaneous
### How to start to design a Website

1. What is the first step to designing a Website?  
    - Pick a goal. Define a topic. You have to know what you want the website to do.
2. What is the most important question to answer when designing a Website?  
    -  "What exactly do I want to accomplish?"  
-----

### Semantics

1. Why should you use an ```<h1>``` element over a ```<span>``` element to display a top level heading?  
    - Because HTML should be coded to repesent the data that will be populated within the tags. Using a ```<span>``` tag to display top level heading inaccurately descibes the data within the tag. Search engines wouldn't pick up this heading as a heading.

2. What are the benefits of using semantic tags in our HTML?  
    -  Search engines consider important keywords to influence page search rankings, they can be used for accessibility purposes, makes it easier to navigate code blocks, etc.  
-----

### What is JavaScript?

1. Describe 2 things that require JavaScript in the Browser?  
    - Buttons, widgets, embedded data, etc
2. How can you add JavaScript to an HTML document?  
    - You can add JavaScript internally by enclosing the script in a ```<script>``` tag. Or you can add a ```.js``` file in the same directory and refernce the file using ```<script src="filename.js" defer></script>```

-----












## Things I want to know more about
- I want to know more about sourcing media for your website. What are the limits or restrictions on the type of media you can use and how it can be used.
