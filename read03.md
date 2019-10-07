# Chapter 3: “Lists”:

> Ordered lists

  are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.

> Unordered lists 

  - are lists that begin with a bullet point (rather than characters that indicate order).
Definition lists
  - are made up of a set of terms along with the definitions for each of those terms.

`<ol>` <br>
The ordered list is created with the `<ol>` element.<br>

`<li>` <br>
Each item in the list is placed between an opening `<li>` tag and a closing `</li>` tag. (The li stands for list item.)

#### index.html
```

<ol>
 <li>Chop potatoes into quarters</li>
 <li>Simmer in salted water for 15-20 minutes until tender</li>
 <li>Heat milk, butter and nutmeg</li>
 <li>Drain potatoes and mash</li>
 <li>Mix in the milk mixture</li>
</ol>

```

#### result
1. Chop potatoes into quarters
1. Simmer in salted water for 15-20 minutes until tender
1. Heat milk, butter and nutmeg
1. Drain potatoes and mash
1. Mix in the milk mixture


`<ul>` <br>
The ordered list is created with the `<ul>` element.<br>

`<li>` <br>
Each item in the list is placed between an opening `<li>` tag and a closing `</li>` tag. (The li stands for list item.)

#### index.html
```

<ul>
 <li>Chop potatoes into quarters</li>
 <li>Simmer in salted water for 15-20 minutes until tender</li>
 <li>Heat milk, butter and nutmeg</li>
 <li>Drain potatoes and mash</li>
 <li>Mix in the milk mixture</li>
</ul>

```

#### result
- Chop potatoes into quarters
+ Simmer in salted water for 15-20 minutes until tender
* Heat milk, butter and nutmeg
+ Drain potatoes and mash
- Mix in the milk mixture


### We can use nested list

You can put a second list inside an <li> element to create a sublist or nested list.<br>

#### index.html
```

<ul>
 <li>Mousses</li> 
 <li>Pastries
   <ul>
      <li>Croissant</li>   
      <li>Mille-feuille</li>   
      <li>Palmier</li>   
      <li>Profiterole</li>  
   </ul> 
 </li> 
 <li>Tarts</li> 
</ul

```

#### result
- Mousses
+ Pastries
    * Croissant
    + Mille-feuille
    * Palmier
    + Profiterole
- Tarts

# Chapter 13: “Boxes”:

### Border, margin & Padding

Every box has three available properties that can be adjusted to control its appearance:<br>

1. ***Border***:<br>
Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

- `border-width`: The border-width property is used to control the width of a border. The value of this property can either be given in pixels or using one of these values: thin, medium and thick.

- `border-style` : You can control the style of a border using the border-style property. This property can thses values:
solid, dotted, dashed and double.

- `border-color` : You can specify the color of a border using either RGB values, hex codes or CSS color names (as you saw on pages 251-252).
It is possible to individually control the colors of the borders on different sides of a box using:
border-top-color, border-right-color, border-bottom-color and border-left-color.

- `border-radius` : CSS3 introduces the ability to create rounded corners on any box, using a property called border-radius. The value indicates the size of the radius in pixels, You can specify individual values for each corner of a box using:
border-top-right-radius, border-bottom-right-radius, border-bottom-left-radius and border-top-left-radius.

1. ***Margin***:<br>
Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.


1. ***Padding***:<br>
Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.


# Chapter 4: “Decisions and Loops”:

> Evaluating conditions & conditional statements:

There are two components to a decision:
1. An expession is evaluated, which returns a value.
1. A conditional statement says what to do in a given situation.

* For example:
```

if(score > 50){
    document.write('you Passed');
} else {
    document.write('Try again...');
}

```

it says : if the condition return **true** execute the statements between the first set of curly brackets<br>
otherwise<br>
execute the statements between the second set of curly brackets<br>

> Comparison operators: evaluating conditions<br>

```

NAME                   - OPERATOR
is equal to            -    ==
is not equal to        -    !=
strict equal to        -    === 
strict not equal to    -    !==
grater then            -     >
less then              -     <
grater then or equal   -     >=
less then  or equal    -     <=

```

> Structuring comparison operators:

`(score >= pass)`

(score >= pass) : enclosing brackets<br>
*score* : operand<br>
*>=* : comparison operators<br>
*pass* : operand<br>

> Logical operatores:
`((5 < 2>) && (2 >= 3))`

*(5 < 2)* : expression 1<br>
*&&* : logical operator<br>
*(2 >= 3)* : expression 2<br>


+ Types of logical operatores:
```

NAME                   - OPERATOR
logical AND            -    &&
logical OR             -    ||
logical NOT            -    !

```

### USING IF STATEMENTS :
The if statement evaluates (or checks) a condition. if the condition evaluates to true, any statements in the subsequent code block are executed.

```

if(score >= 50){
    congratulation();
}

```

if : its a keyword<br> 
(score >= 50): condition<br>
congratulation(): code to execute if value is true<br>

* for example:
```

var score 75; // Score
var msg; // Message 
if (score>= 50) { // If score is 50 or higher 
    msg = 'Congratulations!'; 
    msg += ' Proceed to the next round. ' ;
}

```

#### another type of if statement:
```

if(score >= 50){
    congratulation();
}else{
    encourage();
}

```

if : its a keyword<br> 
(score >= 50): condition<br>
congratulation(): code to execute if value is true<br>
encourage(): code to execute if value is false<br>


