# HTML Links, CSS Layout, JS Functions  


Topics:  

* HTML links  
    - Writing Links.
    - Link to other Sites
    - Link to Other Pages on The Same Site
* CSS Layout
    - Key Concepts in positioning Elements.  
        - Building Blocks.
        - Block-Level Elements.
        - Inline Elements.
        - Containing Elements.
        - Controlling The Position of Elements
* JS function

## HTML Links ##

Links are the the distinguishing feature of the web pages that allow us to navigat through different web pages.    

![links](https://www.internetingishard.com/html-and-css/links-and-images/links-and-images-6820c7.png)


### Writing Links ###  
In html, we use `<a>..</a>` element to creat links. in order for the user to move to any page he can on wahtever he want in these links. Specifying the page you want to link you can use the `href` attribute.  

 `<a href="websiteLINK"> Page's name </a>`  


![linkatt](https://www.internetingishard.com/html-and-css/links-and-images/html-attributes-6f5690.png)

### Link to other Sites ###   

> When you link to a different website, the value of the href attribute will be the full web address for the site, which is known as an absolute URL.  

  


### Link to Other Pages on The Same Site ###

Using this way, you do not need to specifiy the **DOMAIN** name in the URL. You will only need to use a ***relative*** URL.  


![relative](https://www.internetingishard.com/html-and-css/links-and-images/relative-links-e178d0.png)  


--- 


## CSS Layout ##  

In order to make your page looks attractive, you should learn how to control where to site the elements.  


### Key Concepts in positioning Elements ###  

**Building Blocks**  

> CSS treats each HTML element as if it is in its own box. This box will either be a *block-level* box or an *inline* box.   

Block-level boxes start on a new line and look like the main building blocks of any layout.

**Block-Level Elements**

a block-level element is any element that starts a new line (e.g., paragraph) and uses the full width of the page or container. A block-level element can take up one line or multiple lines and has a line break before and after the element.

**Inline Elements**  
Inline elements display in a line. They do not force the text after them to a new line.  

![boxes](https://monetate-media-screenshots.s3.us-east-2.amazonaws.com/commonly-used-html_3.png)


**Containing Elements**  

Containing elements mean creating a nested boxes. This is, a one block-level element sites inside another block-level element. The outer box called *Containing* and act as the parent for the inner box.

![cont](https://mattryall.net/image/css-normal-flow.png)  
   


**Controlling The Position of Elements**  
There are five *positioning Schemes* in CSS in order to control the layout of page:  

1. Normal Flow.  
    `position: static;`

    In this type, each block-level element sits top of the next one.

2. Relative Positioning.  
    `postion: relative;`  

    Using this way, elements moves in relation to where it would have been normal flow.

3. Absolute Positioning.  
    `position: absolute;`  

    “Absolute positioning” is just like relative positioning, but the offset is relative to the entire browser window instead of the original position of the element. Since there’s no longer any relationship with the static flow of the page, consider this the most manual way to lay out an element.  

4. Fixed Positioning.  
    `position: fixed;`  
    “Fixed positioning” has a lot in common with absolute positioning: it’s very manual, the element is removed from the normal flow of the page, and the coordinate system is relative to the entire browser window. The key difference is that fixed elements don’t scroll with the rest of the page.  

![types](https://www.internetingishard.com/html-and-css/advanced-positioning/css-positioning-schemes-790d5b.png)


5. Overlapping Elements.  
    `z-index;`
    The z-index property lets you control the depth of elements on the page. If you think of your screen as 3D space, negative z-index values go farther into the page, and positive ones come out of the page.

    ![zindex](https://www.internetingishard.com/html-and-css/advanced-positioning/css-z-index-c87ef0.png)


---

## Functions, Methods, & Objects in JS ##  

In order for programmers to organize their code ,that the complix scripts can run a huge amount of lines, they use *functions*, *methods*, and *objects*.  

### Functions ###  

Functions in JS used in order to group a series of statements together in purpose of performing a task.  

>* Using finctions is recommended way to organize your code.  
>
>* function offer a way to **store** the steps need to achieve a task. So, it becomes helpfull in the prioritizing the process of loading a page.  
  
  
**Declaring a Function**  
To create a function we can use a function declaration.

It looks like this:  

```
function showMessage() {

  alert( 'Hello everyone!' );
}
```

**Calling The Function**  
Our new function can be called by its name: showMessage().

For instance:

```
function showMessage() {
  alert( 'Hello everyone!' );
}

 showMessage();
 showMessage();

```
The call showMessage() executes the code of the function.  

