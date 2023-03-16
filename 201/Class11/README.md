# Audio, Video, Images

-----

## Video and Audio Content

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.
    - In the early 2000s you had to use a plug in. Now we just have the element tags.

2. Describe the use of the ```src``` and ```controls``` attributes in the ```<video>``` element.
    - ```src``` is used in the same way it its used for ```<img>``` elements. The attribute contains a path to the video you want to embed.
    - the ```controls``` attribute is used to include the brower's native control interface. 

3. Why is it important to have fallback content inside the ```<video>``` element?
    - if the browser accessing your web page doesn't support the ```<video>``` element. It's like the ```alt``` attribute for ```<img>``` elements

4. Write a very short story where ```<audio>``` and ```<video>``` are characters.
    - 

-----

## A Complete Guide To Grid

1. How does Grid layout differ from Flex?
    - flex is one-dimensional while grid is two-dimensional

2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.
    - grid container is the element on whcih grid is applied. it is the direc parent of all the grid items.
    - grid items are the direct children of the element on which grid is applied.
    - grid lines are dividing lines that make up the structure of the grid. They can be vertical or horizontal.

-----

## Responsive Images

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?
    - it makes your code cleaner

2. Define the following ```<img>``` attributes ```srcset``` and ```sizes```. Write an example of how they are used.
    - ```srcset``` defines the set of images we want to display and the size of each image. 
    - ```sizes``` defines a set of media conditions and indicates what image size would be best to choose when certain media conditions are true

3. How is ```srcset``` more helpful for responsive images than CSS or JavaScript?
    - makes your code more resiliant. if a browser has javaScript disabled your image will still render accordingly