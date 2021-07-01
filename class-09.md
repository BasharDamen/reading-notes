# Forms and Events

# HTML Forms #  
The `<form>` HTML element represents a document section containing interactive controls for submitting information.  

HTML Forms are required, when you want to collect some data from the site visitor. For example, during user registration you would like to collect information such as name, email address, credit card, etc.  

![form](https://www.htmlgoodies.com/wp-content/uploads/2021/04/HTML-Form.png)  

## Form Attributes ##  

Apart from common attributes, following is a list of the most frequently used form attributes −

1. **action**  
    Backend script ready to process your passed data.  

2. **method**  
    Method to be used to upload data. The most frequently used are GET and POST methods.

3. **target**  
    Specify the target window or frame where the result of the script will be displayed. It takes values like _blank, _self, _parent etc.

4. **enctype**  
    You can use the enctype attribute to specify how the browser encodes the data before it sends it to the server. Possible values are −  

    application/x-www-form-urlencoded − This is the standard method most forms use in simple scenarios.  

    mutlipart/form-data − This is used when you want to upload binary data in the form of files like image, word file etc.  

## HTML Form Controls ##  

There are different types of form controls that you can use to collect data using HTML form −  

* Text Input Controls   
* Checkboxes Controls  
* Radio Box Controls  
* Select Box Controls  
* File Select boxes  
* Hidden Controls  
* Clickable Buttons  
* Submit and Reset Button  

![htmlformcontrol](https://cdn.educba.com/academy/wp-content/uploads/2019/07/HTML-Form-Controls.png)  

---

# Lists, Tables & Forms #

## list-style ##  

The CSS list-style property defines the appearance, position, and image for list item elements. It is a shorthand property for setting the list-style-type, list-style-position, and list-style-image CSS properties.

The list-style CSS shorthand property allows you to set all the list style properties at once.    

## Syntax ##  

The syntax for the list-style CSS property is:

>`list-style: list-style-type list-style-position list-style-image;
`  


## Parameters or Arguments ##   

|   Value   |  Description
|-----------|------------
|   disc    |Filled circle. This is the default. `ul { list-style: disc; }`
|   circle  |Hollow circle  `ul { list-style: circle; }`
|   square  |Filled square `ul { list-style: square; }`
|   decimal |Decimal numbers starting with 1. `ol { list-style: decimal; }`
|   decimal-leading-zero | Decimal numbers starting with 1, padded with 0 at the front for numbers less than 10. `ol { list-style: decimal-leading-zero; }`
| lower-roman  |Lowercase roman numerals. `ol { list-style: lower-roman; }`
|upper-roman| Uppercase roman numerals. `ol { list-style: upper-roman; }`  


![lists](https://i.ytimg.com/vi/CeJmtFatBuY/maxresdefault.jpg)



**Note**  

* The list-style property can be applied to `<ol>`, `<ul>` or `<li>` tags.  

* The list-style applies to elements with display: list-item.

* When using the list-style property, you can provide one or all of the values (list-style-type, list-style-position and list-style-image values) and they can be provided in any order.

* See also the list-style-image, list-style-position, and list-style-type properties.
