# Css Cheatsheet

## Property Shorthands:
Almost all Css properties have shorthands for the four directions... It can accept 4, 3, 2 or 1 parameters.
The directions are changind clockwise. Example:
4 params = top right bottom left
3 params = top (right left) bottom
2 params = (top bottom) (right left)
1 params = (top right bottom left)

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
