# Chapter 2: “Text”:

1. HTML has six "levels" of headings:
`<h1>` is used for main headings and its the largest content.
`<h2>` is used for subheadings.
`<h6>` is the smallest content.
If there are further sections under the subheadings then the <h3> element is used, and so on...

* For examples:
> index.html:
```
<h1>This is a Main Heading</h1>
<h2>This is a Level 2 Heading</h2>
.<br>
.<br>
<h6>This is a Level 6 Heading</h6>
````

> result:
# This is a Main Heading<br>
## This is a Level 2 Heading<br>
.<br>
.<br>
##### This is a Level 6 Heading<br>



2. `<p>` To create a paragraph, surround the words that make up the paragraph with an opening `<p>` tag and closing `</p>` tag.
* For exapmle:
> index.html:<br>
```
<p>
A paragraph consists of one or more sentences that form a self-contained unit of discourse.<br>
 The   start of a paragraph is indicated by a new   line.<br>
</p>
```

> result:

A paragraph consists of one or more sentences that form a self-contained unit of discourse.<br>
 The   start of a paragraph is indicated by a new   line.




3. `<b>`By enclosing words in the tags <b> and </b> we can make characters appear bold.
* For example:
> index.html:
```
<p>
This is how we make a word appear <b>bold.</b>
</p>
```

> result:

This is how we make a word appear **bold**.


4. `<i>` By enclosing words in the tags <i> and </i> we can make characters appear italic.
* For example:
> index.html:
```
<p>
This is how we make a word appear <i>italic</i>.
</p>
```

> result:

This is how we make a word appear *italic.*

5. `<br>` As you have already seen, the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag `<br/>`.
* For example:
> index.html:
```
<p>
The Earth<br/> gets one hundred tons heavier every day<br/> due to falling space dust.
</p>
```

> result:

The Earth<br/>
 gets one hundred tons heavier every day<br/> 
 due to falling space dust.

 6. `<hr>` To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections using the `<hr/>` tag.
 * For example:
> index.html:
```
<p>
Venus is the only planet that rotates clockwise.
</p> 
<hr /> 
<p>
Jupiter is bigger than all the other planets combined.
</p>
```

> result:

Venus is the only planet that rotates clockwise.
<hr />
Jupiter is bigger than all the other planets combined.

7. `<strong>` The use of the `<strong>` element indicates that its content has strong importance. For example, the words contained in this element might be said with strong emphasis.
 * For example:
> index.html:
```
<p>
<strong>Beware:</strong> Pickpockets operate in this area.
</p>
```

> result:

**Beware:** Pickpockets operate in this area.



# Chapter 10: Ch.10 “Introducing CSS”:

CSS allows you to create rules that specify how the content of an element should appear. For example, you can specify that the background of the page is cream, all paragraphs should appear in gray using the Arial typeface, or that all level one headings should be in a blue, italic, Times typeface.

CSS works by assoclating rule with HTML elements. These rule govern how the content of specified elements should be displayed. A CSS rule contains two parts: a **selector** and a **declaration**.

* For example:
```
p {
    font-family: Arial;
}
```
P:    selector<br>
{font-family: Arial;}:    declaration<br>
font-family:ProPerty<br>
Arial : value<br>

+  ***Selector***: indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with comma.
+ ***Declaration***: indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a property and a value), and are separated by a colon.
+ ***Properties*** indicate the aspects of the element you want to change. For example, color, font, width, height and border
+ ***Values*** specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be.

### Using External CSS

`<link>` <br>
The `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the `<head>` element.
<br>
It should use three attributes:<br>
**href**<br> This specifies the path to the CSS file (which is often placed in a folder called css or styles).<br>
**type**<br> This attribute specifies the type of document being linked to. The value should be text/css.<br>
**rel**<br> This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file

* For example:
> index.html:
```

<!DOCTYPE html>
 <html>
  <head>
    <title>Using External CSS</title>
    <link href="css/styles.css" type="text/css"    rel="stylesheet" /> 
  </head>
  <body>
    <h1>Potatoes</h1>  
    <p>There are dozens of different potato varieties. They are usually described as early, second early and maincrop.</p> 
  </body> 
 </html>

```

> style.css:
```

body {
      font-family: arial;
      background-color: rgb(185,179,175);
}
h1 {
      color: rgb(255,255,255);
}

```

### Using Internal CSS

You can also include CSS rules within an HTML page by placing them inside a `<style>` element, which usually sits inside the `<head>` element of the page. <br>
The `<style>` element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/css.

* For example:
> index.html:
```

<!DOCTYPE html>
 <html>
  <head>
    <title>Using Internal CSS</title>  
    <style type="text/css">
       body {
                font-family: arial;
                background-color: rgb(185,179,175);
        }   
        h1 {    color: rgb(255,255,255);
        }  
    </style>
  </head>
  <body>
    <h1>Potatoes</h1>  
    <p>There are dozens of different potato varieties. They are usually described as early, second early and maincrop.</p> 
  </body> 
 </html>

```

# Chapter 2: “Basic JavaScript Instructions”:

1. COMMENTS:<br>
 comments help us to explain what our code does. They help make your code easier to read and understand. This can help you and others who read your code.<br>

```

// Display the appropriate greeting based on the current time 

```
<br>
2. VARIABLE:<br>
A script will have to temporarily store the bits of information it needs to do its job. It can store this data in variables. A variable is a good name for this concept because the data stored in a variable can change (or vary) each time a script runs.

```
var quantity;

```
var : its a variable keyword<br>
quantity : its a variable name<br>
<br>
```
quantity = 3;

```
quantity : its a variable name<br>
= : assignment operator<br>
3 : variable value<br>
<br>
#### SHORTHAND FOR CREATING VARIABLES:
1.
```

var price = 5; 
var quantity = 14; 
var total = price * quantity;

```
2.
```

var price, quantity, total ;
price = 5; quantity = 14;
total = price * quantity;

```
3.
```

var price = 5, quantity = 14;
var total = price * quantity; 

```
4.
```

// Write total into the element with id of cost 
var el = document.getElementByld( 'cost'); 
el .textContent = '$' +total;

```


3. DATA TYPES:<br>
JavaScript distinguishes between numbers, strings, and true or false values known as Booleans.<br>

- **NUMERIC DATA TYPE** : The numeric data type handles numbers => 0.75
- **STRING DATA TYPE** : The strings data type consists of letters and other characters => 'H. am Ahmad Sawalqeh'
- **BOOLEAN DATA TYPE** : Boolean data types can have one of two values: true or false => true

* For example:
```
quantity = 3; // numeric data
text = 'hello JB'; // string data
status = false; // boolean data

```

### RULES FOR NAMING VARIABLES:
1. The name must begin with a letter, dollar sign ($),or an underscore (_). It must not start with a number.
1. The name can contain letters, numbers, dollar sign ($), or an underscore (_). Note that you must not use a dash(-) or a period (.) in a variable name.
1. You cannot use keywords or reserved words.
1. All variables are case sensitive, so score and Score would be different variable names, but it is bad practice to create two variables that have the same name using different cases. 
1. Use a name that describes the kind of information that the variable stores. For example, fi rstName might be used to store a person's first name, l astNarne for their last name, and age for their age.
1.If your variable name is made up of more than one word, use a capital letter for the first letter of every word after the first word. For example, f i rstName rather than fi rstnarne (this is referred to as camel case). You can also use an underscore between each word (you cannot use a dash). 


4. ARRAYS:<br>
An array is a special type of variable. It doesn't just store one value; it stores a list of values.

* For example:
```

var colors; 
colors ['white', 'black', 'custom'];

```

> VALUES IN ARRAYS :

Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one).<br>
```

INDEX - VALUE
  o   - 'white'
  1   - 'black'
  2   - 'custom' 

```

5. OPERATORS:<br>
Expressions rely on things called operators; they allow programmers to create a single value from one or more values.<br>

- ASSIGNMENT OPERATORS:<br>
`color = 'beige';`
- COMPARISON OPERATORS:<br>
`buy = 3 > 5;`
- ARITHMETIC OPERATORS:<br>
`area = 3 * 2;`
- LOGICAL OPERATORS:<br>
`buy= (5 > 3) && (2 < 4);`
- STRING OPERATORS:<br>
`greeting= 'Hi 1 + 'Molly';`

6. ARITHMETIC OPERATORS:<br>
JavaScript contains the following mathematical operators, which you can use with numbers. You may remember some from math class. <br>

```

NAME            - OPERATOR
ADDITION        -    +
SUBTRACTION     -    -
DIVISION        -    / 
MULTIPLICATION  -    *
INCREMENT       -   ++
DECREMENT       -   --
MODULUS         -    %

```

* For example:
```

var subtotal (13 + 1) * 5; // Subtotal is 70 
var shipping 0.5 * (13 + 1) ; // Shipping is 7 
var total subtotal + shipping; // Total is 77 

```

**STRING OPERATOR**: There is just one string operator: the+ symbol. It is used to join the strings on either side of it.<br>

* For example:
```

var greeting= 'Howdy '; var name= 'Mol ly' ; 
var welcomeMessage = greeting + name+ '!';

```

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


### switch statements:

A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.<br>

```

switch (level){
    case 'one':
    title = 'level 1';
    break;

    case 'two':
    title = 'level 2';
    break;

    case 'three':
    title = 'level 3';
    break;

    defult:
    title = 'test';
    break;
}

```

* For example:
```

var msg; 
var level = 2; 
// Message 11 Level 
// Determine message based on level 
switch (level) { 
    case 1: msg = 'Good luck on the first test' ; 
    break; 

    case 2: msg = 'Second of three - keep going!'; 
    break; 

    case 3: msg = 'Final round, al most there!'; 
    break; 

    default: msg = 'Good luck!'; 
    break;
}


```

