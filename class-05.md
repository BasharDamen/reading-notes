# HTML Images; CSS Color & Text  




## Images In HTML ##  


### Adding img ###  



**Basic tag**  
In order to put a simple image on a webpage, we use the `<img>` element. This is an empty element (meaning that it has no text content or closing tag) that requires a minimum of one attribute to be useful — src (sometimes spoken as its full title, source). The src attribute contains a path pointing to the image you want to embed in the page, which can be a relative or absolute URL, in the same way as href attribute values in `<a>` elements.   

For example:  

>`<img src = https://www.edarabia.com/ar/wp-content/uploads/2021/01/html-definition-12-advantages-1.jpg>`  
>
>> ![html](https://www.edarabia.com/ar/wp-content/uploads/2021/01/html-definition-12-advantages-1.jpg)


**Alternative text**  

The next attribute we'll look at is `alt`. Its value is supposed to be a textual description of the image, for use in situations where the image cannot be seen/displayed or takes a long time to render because of a slow internet connection. For example, our above code could be modified like so:  

> `<img src = "https://www.i_broke_the_ling.jpg" alt = "this is an HTML img" >`  
>
>
>> ![this is an HTML img](https://www.i_broke_the_ling.jpg)

### Width and height ###    

You can use the `width` and `height` attributes to specify the width and height of your image.  

> ` <img src = Link alt = "dsicription" width= "200" height="150" > `  

---  


## Color in CSS ##  

### Foreground Color ###
`color`  


The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:
* rgb values
* Hex codes
* Color names  

### Background Color ###  

The `background-color` CSS property sets the background color of an element.
For example :  

> background-color: brown;   ===> This is a 'color name' type
>
>background-color: #74992e;   ===> This is a 'HEX code' type
>
>background-color: rgb(255, 255, 128);   ===> This is 'rgb' value  

### Contrast ###

The contrast() CSS function adjusts the contrast of the background color. Exaples:
> filter: contrast(1);
> 
> filter: contrast(50%);
> 
> filter: contrast(0);
>
> ![contrast](https://static-cse.canva.com/blob/140968/contrast-1.png)  



### opacity ###  

The opacity CSS property sets the opacity of an element. Opacity is the degree to which content behind an element is hidden, and is the opposite of transparency.  

![opasity](https://precisecontinental.com/wp-content/uploads/2016/05/opacity.jpg)

