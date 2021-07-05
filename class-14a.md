# CSS Transforms, Transitions, and Animations  

# CSS Transformation   

## **Introducing CSS Transformations**

The effect of a CSS Transform is to modify the appearance of an element in the browser by translation, rotation or other means. When defined in a style sheet, transformations are applied as the page is rendered, so you don't actually see any animations taking place. Transforms can also be applied as a mouseover or similar effect.  

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

## **Animating your Transforms**  

While CSS Transformation in itself is a powerful tool for developers (though I shudder to think what will happen as it becomes more widely used), the ability to animate the same effects using -webkit-transition is far more exciting. Move your mouse over the following boxe for a demonstration:  

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
>     -webkit-transition: 1s ease-in-out;
>     -moz-transition: 1s ease-in-out;
>     -o-transition: 1s ease-in-out;
>     transition: 1s ease-in-out;
>   }
>   .showbox.slideright:hover {
>     -webkit-transform: translate(3em,0);
>     -moz-transform: translate(3em,0);
>     -o-transform: translate(3em,0);
>     -ms-transform: translate(3em,0);
>     transform: translate(3em,0);
>   }
> 
> </style>
> 
> <div class="showbox slideright">box 1</div>
> 
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
>     -webkit-transition: 1s ease-in-out;
>     -moz-transition: 1s ease-in-out;
>     -o-transition: 1s ease-in-out;
>     transition: 1s ease-in-out;
>   }
>   .showbox.slideright:hover {
>     -webkit-transform: translate(3em,0);
>     -moz-transform: translate(3em,0);
>     -o-transform: translate(3em,0);
>     -ms-transform: translate(3em,0);
>     transform: translate(3em,0);
>   }
> 
> </style>
> 
> <div class="showbox slideright">box 1</div>    
>```


What you see above is a box from the four boxes from the previous section, in their default states. When you mouseover any of the boxes, however, the CSS transformation is applied as a one second animation. When the mouse moves away the animation is reversed, taking each box back to its original state.

And we can do this without using JavaScript - only HTML and CSS!   

If you think that's cool, realise that CSS Animation can be applied not just to the transforms, but also to other CSS properties including: opacity, colour and a bunch of others.  




