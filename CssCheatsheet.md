# Css Cheatsheet

## Property Shorthands:
Almost all Css properties have shorthands for the four directions... It can accept 4, 3, 2 or 1 parameters.
The directions are changind clockwise. Example:

```
  4 params = top right bottom left
  3 params = top (right left) bottom
  2 params = (top bottom) (right left)
  1 params = (top right bottom left)
```

## Auto Margin property:

By setting the property margin to auto, the browser will center the element inside it's container, by all the directions.

## Margin Collapse:

Top and Bottom margins are merged into a single one, equal to the largest of the both.
Example: 
```
  <h1 style="margin-bottom: 50px;"> MyElm </h1>
  <h1 style="margin-top: 20px;"> AnotherElm </h1>
```  
   The margin between the elements will be equal to 50px, because of the collapse.

## Padding:

Padding stands for an element internal margin, or between it's border. However, if you set a padding on an element who has a defined size, the padding will add up on it's size (width or height). Example:

```  
  elm {
    width: 300px;
    padding: 25px;
  }
  Total width = 325px.
```  

To solve this problem, we can use box-sizing property:

```  
  box-sizing: border-box;
```  

## Fonts:
 Always set Fallback generic fonts, as the example:
```   
 "Lucida Sans Unicode", "Lucida Grande", sans-serif
```   
 It's not a good practice to set the size with Pixels, cause it will be fixed no matter what's the font size configured with the browser. It can be tricky for users with visual disabilites to read then. If you want it to be resizable, use EM units. The default font size for browsers are 16px, and 1em = fontSize in pixels. So, 1em = 16pixels by default. To calculate the appropriate size, just use the formula:
 ```  
  Size(em) = Size(px) / 16
 ```  
 Another trick is to use VW units, which stands for "Viewport Width". With that, the font size will be resized with the size of the window. Example:
 ```
  font-size:10vw
  ```
It means to use 10% of the viewport width
