# More CSS Layout  


![img](https://cdn.educba.com/academy/wp-content/uploads/2019/12/CSS-Position.jpg)


## position ##  

The position CSS property sets how an element is positioned in a document. The top, right, bottom, and left properties determine the final location of positioned elements.  

**Syntax**  

position: static;
position: relative;
position: absolute;
position: fixed;
position: sticky;

**/* Global values */**  

position: inherit;
position: initial;
position: revert;
position: unset;  

### Values ###  
#### static ####  

The element is positioned according to the normal flow of the document. The top, right, bottom, left, and z-index properties have no effect. This is the default value

#### relative ####  

The element is positioned according to the normal flow of the document, and then offset relative to itself based on the values of top, right, bottom, and left. The offset does not affect the position of any other elements; thus, the space given for the element in the page layout is the same as if position were static.  
#### absolute ####  

The element is removed from the normal document flow, and no space is created for the element in the page layout. It is positioned relative to its closest positioned ancestor, if any; otherwise, it is placed relative to the initial containing block. Its final position is determined by the values of top, right, bottom, and left.   

#### fixed ####  

The element is removed from the normal document flow, and no space is created for the element in the page layout. It is positioned relative to the initial containing block established by the viewport, except when one of its ancestors has a transform, perspective, or filter property set to something other than none (see the CSS Transforms Spec), in which case that ancestor behaves as the containing block. (Note that there are browser inconsistencies with perspective and filter contributing to containing block formation.) Its final position is determined by the values of top, right, bottom, and left.
This value always creates a new stacking context. In printed documents, the element is placed in the same position on every page.  

#### sticky ####  

The element is positioned according to the normal flow of the document, and then offset relative to its nearest scrolling ancestor and containing block (nearest block-level ancestor), including table-related elements, based on the values of top, right, bottom, and left. The offset does not affect the position of any other elements.
This value always creates a new stacking context. Note that a sticky element "sticks" to its nearest ancestor that has a "scrolling mechanism" (created when overflow is hidden, scroll, auto, or overlay), even if that ancestor isn't the nearest actually scrolling ancestor. This effectively inhibits any "sticky" behavior (see the GitHub issue on W3C CSSWG).  

##### Types of positioning ####  

**A positioned element** is an element whose computed position value is either relative, absolute, fixed, or sticky. (In other words, it's anything except static.)  

**A relatively positioned element** is an element whose computed position value is relative. The top and bottom properties specify the vertical offset from its normal position; the left and right properties specify the horizontal offset.  

**An absolutely positioned element** is an element whose computed position value is absolute or fixed. The top, right, bottom, and left properties specify offsets from the edges of the element's containing block. (The containing block is the ancestor relative to which the element is positioned.) If the element has margins, they are added to the offset. The element establishes a new block formatting context (BFC) for its contents.  

**A stickily positioned element** is an element whose computed position value is sticky. It's treated as relatively positioned until its containing block crosses a specified threshold (such as setting top to value other than auto) within its flow root (or the container it scrolls within), at which point it is treated as "stuck" until meeting the opposite edge of its containing block.
Most of the time, **bsolutely positioned elements** that have height and width set to auto are sized so as to fit their contents. However, non-replaced, absolutely positioned elements can be made to fill the available vertical space by specifying both top and bottom and leaving height unspecified (that is, auto). They can likewise be made to fill the available horizontal space by specifying both left and right and leaving width as auto.
Except for the case just described (of absolutely positioned elements filling the available space):
If both top and bottom are specified (technically, not auto), top wins.
If both left and right are specified, left wins when direction is ltr (English, horizontal Japanese, etc.) and right wins when direction is rtl (Persian, Arabic, Hebrew, etc.).  

**Key Concepts in Positioning Elements**
##### Building Blocks ####
CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
##### Block-level elements ####
start on a new line
Examples include:
`< h1 >  < p > < ul > < li >`
#####  Inline elements ####
flow in between surrounding text
Examples include:
`< img > < b > < i >`
#### Website Layout ####

A website is often divided into headers, menus, content and a footer:

#### Parents of Floated Elements: Problem ####  

If a containing element only contains floated elements, some browsers will treat it as if it is zero pixels tall.

#### Parents of Floated Elements: Solution ####  

Although elements like <div>s normally grow to fit their contents, using the float property can cause a startling problem for CSS newbies: If floated elements have non-floated parent elements, the parent will collapse.
For example:
< div >
  < div style="float: left;">Div 1</div >
  < div style="float: left;">Div 2</div >
< /div >
The parent div in this example will not expand to contain its floated children - it will appear to have height: 0.
**How do you solve this problem?**
I would like to create an exhaustive list of solutions here. If you're aware of cross-browser compatibility issues, please point them out.
**Solution 1**
Float the parent.
< div style="float: left;" >
  < div style="float: left;">Div 1</div >
  < div style="float: left;">Div 2</div >
< /div >
**Pros: Semantic code.**
Cons: You may not always want the parent to float. Even if you do, do you float the parents' parents, and so on? Must you float every ancestor element?
**Solution 2**
Give the parent an explicit height.
```
< div style="height: 300px;" >
  < div style="float: left;">Div 1</div >
  < div style="float: left;">Div 2</div >
< /div >
```
**Pros: Semantic code.**
Cons: Not flexible - if the content changes or the browser is resized, the layout will break.
**Solution 3**
Append a "spacer" element inside the parent element, like this:
```
< div >
  < div style="float: left;" >Div 1< /div >
  < div style="float: left;" >Div 2< /div >
  < div class="spacer" style="clear: both;" >< /div >
< /div >
```
**Pros: Straightforward to code.**
Cons: Not semantic; the spacer div exists only as a layout hack.
**Solution 4**
Set parent to overflow: auto.
```
< div style="overflow: auto;" >
  < div style="float: left;" >Div 1< /div >
  < div style="float: left;" >Div 2< /div >
< /div >
```