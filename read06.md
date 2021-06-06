# Design web pages with CSS

## CSS ##
**CSS** which stands for **_Cascading Style Sheets_**, is a language made in order to allow you to give a style to your _HTML_ page. that is, how it will look like to the users of the page.  
CSS can be used in coloring the page, changing text style, controlling images' places and size, and so on.

## CSS syntax ##
CSS is a rule-based language, this means that CSS is working depinding on your rules or ordars such as making a rule in order to change your HTML page's header or changing the color of text.
Rule written after another, will result in a complete CSS stylesheet.

## Applying CSS to HTML ##

There are three ways to aply CSS to HTML: Inline, Internally, and Externally.

### External stylesheet ###
This is the most common and useful method to apply your CSS to HTML. That can be done by adding the link of the CSS file to the HTML document in the `<link>` element:
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

### Internal stylesheet ###
Using this method, a stylesheet will be resided inside the HTML doc. To create an internal stylesheet, you place CSS inside a `<style>` element contained inside the HTML `<head>`.
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

### Inline stylesheet ###
By using this method, each HTML element will be affected by a CSS decleration which being written within style attribute. Using this method will look like this:
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
  </head>
  <body>
    <h1 style="color: blue;background-color: yellow;border: 1px solid black;">Hello World!</h1>
    <p style="color:red;">This is my first CSS example</p>
  </body>
</html>
```    
