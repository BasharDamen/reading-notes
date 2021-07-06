# CSS Transforms, Transitions, and Animations  

# CSS Transformation   

## **Introducing CSS Transformations**


**Transform property** in CSS is used to modify the appearance of an element in the browser through *transilation*, *rotation* , *other means*.   
Using transformation, you can size, position, and change elements.  
transform property has two options, 2D and 3D.


 When defined in a style sheet, transformations are applied as the page is rendered, so you don't actually see any animations taking place. Transforms can also be applied as a mouseover or similar effect.  

For example:   

> ```
> <style type="text/css">
> 
>   .showbox {
>     float: left;
>     margin: 4em 1em;
>     width: 100px;
>     height: 60px;
>     border: 2px solid green;
>     background-color: #fff;
>     line-height: 60px;
>     text-align: center;
>   }
> 
> </style>
> 
> <div class="showbox" style="transform: translate(3em,0);">box 1</div>
> <div class="showbox" style="transform: rotate(30deg); border-color: red;">box 2</div>
> <div class="showbox" style="transform: translate(-3em,1em);">box 3</div>
> <div class="showbox" style="transform: scale(2);">box 4</div>
> <div style="clear: left;"></div>
> ```
>
> <style type="text/css">
> 
>   .showbox {
>     float: left;
>     margin: 4em 1em;
>     width: 100px;
>     height: 60px;
>     border: 2px solid green;
>     background-color: #fff;
>     line-height: 60px;
>     text-align: center;
>   }
> 
> </style>
> 
> <div class="showbox" style="transform: translate(3em,0);">box 1</div>
> <div class="showbox" style="transform: rotate(30deg); border-color: red;">box 2</div>
> <div class="showbox" style="transform: translate(-3em,1em);">box 3</div>
> <div class="showbox" style="transform: scale(2);">box 4</div>
> <div style="clear: left;"></div>  


* Of note is the fact that the text is still selectable in transformed elements, even when rotated, and that scaling an element affects properties including border widths and font sizes and not just the box dimensions.  


## Transform Syntax  


The syntax of transform including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parantheses.  
> ```
> div {
>   -webkit-transform: scale(1.5);
>      -moz-transform: scale(1.5);
>        -o-transform: scale(1.5);
>           transform: scale(1.5);
> }
> ```  



## Scale  

The scale value allows you to control the size of an element.  
For example, the value 2 would transform the size to be 2 times its original size. The value 0.5 wpuld transform the size to be half its original size.

scale value conrtols the width(X-axis) and the height(Y-axis).
![scale](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/scale()/scale.png)


**Scale Syntax**  

> ```
> div:hover {
>   transform: scale(2);
> }
> ```

## Rotate  

Using rotate value, you can rotate the element either clockwise or counterclockwise by specifying a number of degree.   
Positive values will rotate the element clockwise.  
Negative values will rotate the element counterclockwise.  

**Rotate Syntax**  
> ```
> div:hover {
>   transform: rotate(1080deg);
> }
> ```  

--- 

# CSS Translate 

The translate value moves an element left/right and up/down.   

this movement is depending on the parameters givin for the X(horizintal), Y(vertical) axis.

* A positive X value moves the element to the right.
*  a negative X moves the element to the left
* A positive Y value moves the element downwards
* a negative Y value, upwards.  

![translate](https://i7x7p5b7.stackpathcdn.com/codrops/wp-content/uploads/2014/12/translate-example.png)  

**translate suntax**  
> ```
> div:hover {
>   transform: translate(20px, 20px);
> }
> ```

---

# Skew  

With the skew value, the element skews (or tilts) one direction or the other based on the values given for the X and Y axes.

![skew](https://www.sanjaywebdesigner.com/articles/wp-content/uploads/2019/07/transform-skew-html-css-in-delhi-india.jpg)  

**skew syntax**  
>```
>div {
>  transform: skewX(25deg);
>  transform: skewY(10deg);
>  transform: skew(25deg, 10deg);
>}
>```


![trans](https://www.htmldog.com/figures/transform.png)