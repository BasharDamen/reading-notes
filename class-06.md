# JS Object Literals; The DOM  

## **OBJECTS** ##  

An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method. In addition to objects that are predefined in the browser, you can define your own objects.  

### **JavaScript Object Literal** ###  

A JavaScript object literal is a comma-separated list of name-value pairs wrapped in curly braces. Object literals encapsulate data, enclosing it in a tidy package. This minimizes the use of global variables which can cause problems when combining code.  
The following demonstrates an example object literal:  
```
var myObject = {
    sProp: 'some string value',
    numProp: 2,
    bProp: false
};
```  
Object literal property values can be of any data type, including array literals, functions, and nested object literals. Here is another object literal example with these property types:

```
var Swapper = {
    // an array literal
    images: ["smile.gif", "grim.gif", "frown.gif", "bomb.gif"],
    pos: { // nested object literal
        x: 40,
        y: 300
    },
    onSwap: function() { // function
        // code here
    }
};

```

### **Object Literal Syntax** ###  

Object literals are defined using the following syntax rules:

* A colon separates property name from value.
* A comma separates each name-value pair from the next.
* A comma after the last name-value pair is optional.  

If any of the syntax rules are broken, such as a missing comma or colon or curly brace, a JavaScript error will be triggered. Browser error messages are helpful in pointing out the general location of object literal syntax errors, but they will not necessarily be completely accurate in pointing out the nature of the error.  


### **Why and How We Use Object Literals** ##  

Object literals enable us to write code that supports lots of features yet still provide a relatively straightforward process for implementers of our code. No need to invoke constructors directly or maintain the correct order of arguments passed to functions. Object literals are also useful for unobtrusive event handling; they can hold the data that would otherwise be passed in function calls from HTML event handler attributes.  

---

## **Document Object Model (DOM)** ##  

The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web  

### **What is the DOM?** ###  

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.  

A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.  

For example, the standard DOM specifies that the querySelectorAll method in the code below must return a list of all the `<p>` elements in the document:  
```
const paragraphs = document.querySelectorAll("p");
// paragraphs[0] is the first <p> element
// paragraphs[1] is the second <p> element, etc.
alert(paragraphs[0].nodeName);
```
