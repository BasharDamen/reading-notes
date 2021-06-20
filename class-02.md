# Basics of HTML, CSS & JS  

## HTML TEXT ##
While working on a web page using HTML language, tags (known as markup) are added to the content of the page in which these tags provide extra meaning and give the ability to browsers to show users the appropriate structure for the page.  
The two markup types we will explain them are:  
    1- Structural markup.  
    2- Semmantic markup.

### **Structural Markup** ###  
The elements that can be used to describe both *headings* and *paragraphs*.

- **HEADINGS:**
There are six types or levels of headings in HTML:
```
 <h1> is used for the main headings
 <h2> is used for subheadings
 <h3>, <h4>,<h5>, <h6> are used in case if there are a further subheadings
```  
Contents are being displayed by the browser at different sizes.   

![headings](https://www.digitaleagles.com.au/wp-content/uploads/2020/03/h-headings.png)  



- **PARAGRAPHS**
Paragrapgh tags is being surrounding the words that make up the paragrapgh. For example:

```
<p> This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh</p>
```

<p> This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh This is a paragrapgh </p>     






- **BOLD & *ITALIC*:**  
Texts can be styled in HTML using:  
    `<b>..</b>` ---> to make the characters appear **bold**.  
    `<i>..</i>` ---> to make the character appear *italic*.  

- **SUPERSCRIPT & SUBSCRIPT**  

    1- `<sup>`: an element used to contain character that should be superscript.  
    2- `<sub>`: an element used to contain character that should be subscript.  

    Example:   
    `<h2> this is an example for<sup>sup</sup> and<sub>sub</sub></h2>`  
    Result:  

    <h2> this is an example for<sup>sup</sup> and<sub>sub</sub></h2>  

- **WHITE SPACE**  
    This is a way where authors used to make it easier to read the code, and this can be done by adding extra spaces or starting some elements on new lines.
```
    <p> This is how to use WHITE SPACE</p>
    <p> This is how to use       WHITE SPACE</p>
    <p> This is how to use 
        WHITE SPACE</p>
    
```

<p> This is how to use WHITE SPACE</p>
    <p> This is how to use       WHITE SPACE</p>
    <p> This is how to use 
        WHITE SPACE</p>  

  <br />  

- **Line Breaks & Horizontal Rules**  
    `<br />`: is used to make add a line break in middle of paragrapg.  
    Example :  
    `<p>This is how to use <br /> LINE BREAK</p>`
    <p>This is how to use <br /> LINE BREAK</p>  

    `<hr />`: is used creat a break between themes.  
    Example:  
```
    <p> Theme 1 </p>
   <hr />
    <p> Theme 2 </p>
```  

<p> Theme 1 </p>
   <hr />
    <p> Theme 2 </p>

<br />
<hr />

## CSS intro ##

### WHAT IS CSS** ###  
CSS stands for *cascading style sheets*. In short, CSS is a design language that makes a website look more appealing than just plain or uninspiring pieces of text. Whereas HTML largely determines textual content, CSS determines visual structure, layout, and aesthetics. HTML is a markup language, and CSS is a style sheet language.  

### How Does CSS Work with HTML? ###  

CSS makes the front-end of a website shine and it creates a great user experience. Without CSS, websites would be less pleasing to the eye and likely much harder to navigate. In addition to layout and format, CSS is responsible for font color and more.  

![css and html](https://miro.medium.com/max/2688/1*Q8w9PI58DKjolhl5aDeiOQ.png)  



<hr />

## BASIC JS INSTRUCTIONS ##  

### Statement ##  
Statements are used in JavaScript to control its program flow. The following are statements that are included in JS:  
* comment  
  
    The `//` characters tell JavaScript that you want to include explanatory comments in your program.  
    ```
    // single-line comment
    
    /* 
    multible-lines 
    comment
    */
    ```
* break  

    The break statement tells JavaScript to exit a "controlled structure" and resume execution at a point after the structure.  
    The break statement is used with structures built using the following commands:  
        - while  
        - for  
        - for..in  

* function  
    The function statement lets you create your own user-defined functions. Functions are self-contained routines that can be "called" elsewhere within your JavaScript code.  

* if...else  
    Functions are self-contained routines that can be "called" elsewhere within your JavaScript code.  

### DECISIONS & LOOPS in JS ###  

There are situations when we want to run the code at different conditions, such as, if one condition applies run a particular code, if another condition applies another code is run. This is prioritized with "if" and "else if" conditionals as follows:
```
function getColor(phrase){
   if (phrase === "stop"){
       console.log("red");
   } else if (phrase === "slow"){
       console.log("yellow");
   } else if (phrase === "go"){
       console.log("green");
   } else {
       console.log("purple");
   }
}
```  

We can run codes in multiple loops if we want to with the help of loops. With loops, our code runs until a certain condition is satisfied such as:  
```
for (let i = 25; i >= 0; i-=5) {
    console.log(i)
}
```