# Chapter 4: Ch.4 “Links”:


Links are created using the `<a>` element. Users can click on anything between the opening `<a>` tag and the closing `</a>` tag. You specify which page you want to link to using the href attribute.<br>

```
<a href="http://www.imdb.com">IMDB</a>
```

- `<a href="http://www.imdb.com">` : it's an opening link tag.
- `href="http://www.imdb.com"` : this is the page the ***link*** takes you to.
- `IMDB` : this is the ***text*** the user clicks on.
- `</a>` : closing link tag.

Links are created using the `<a>` element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click on the link.<br>

Users can click on anything that appears between the opening `<a>` tag and the closing `</a>` tag and will be taken to the page specified in the href attribute.<br>


### Linking to other sites:

When you link to a different website, the value of the href attribute will be the full web address for the site, which is known as an absolute URL.<br>

> index.html

```
<p>Movie Reviews:
 <ul>
   <li><a href="http://www.empireonline.com">Empire</a></li>  
   <li><a href="http://www.metacritic.com">Metacritic</a></li>
   <li><a href="http://www.rottentomatoes.com">Rotten Tomatoes</a></li>
   <li><a href="http://www.variety.com">Variety</a></li>
 </ul> 
</p>
```

> result

Movies Reviews:
- Empire
+ Metacritic
* Rotten Tomatoes
- Variety

### relative urls:

Relative URLs can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files.<br>

could be:<br>
- same folder.
- child folder.
- grandchild folder.
- parent folder.
- grandparent folder.


### emaiL Links:


To create a link that starts up the user's email program and addresses an email to a specified email address, you use the <a> element. However, this time the value of the href attribute starts with mailto: and is followed by the email address you want the email to be sent to.<br>

`a href="mailto:jon@example.org">Email Jon</a>`

### OPening Links in A neW WinDoW:

> target:


If you want a link to open in a new window, you can use the target attribute on the opening `<a>` tag. The value of this attribute should be _blank.<br>

`<a href="http://www.imdb.com" target="_blank">Internet Movies Database</a>` <br>
thats will opens in window.<br>


# Chapter 15: “Layout”:

1. Building Blocks:

CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.<br>

+ Block-level elements start on a new line Examples include: 
`<h1> <p> <ul> <li>`<br>

* inline elements flow in Between surrounding text Examples include:
` <img> <b> <i> `<br>

2. ControLLing the position of eLement:

+ CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.<br>

1. ***normal flow***:<br>
 Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-byside, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).<br>

`position: static;`<br>


 2. ***relative position***:<br>
 This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.<br>

 `position: relative;`<br>

 3. ***Absolute Positioning***:<br>
  This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.<br>

 `position: Absolute;`<br>

4. ***Fixed Positioning***:<br>
 This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.

 `position: fixed;`<br>

 5. ***Floating elements***:<br>
 Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

`float `<br> 
as a property and using either `left;` or ` right;` as a value.

> we can clear the float using:
`clear` <br> 
as a property and using either `left;`, ` right;`, `both;` or `none` as a value.

 ## screen sizes:

 Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.<br>

 ## page sizes:

 Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).<br>

 - ***fixed width Layouts:***<br>
 Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.<br>

 - ***Liquid Layouts:***<br>
 Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.<br>

 - ***Layout grids:***<br>
 Composition in any visual art (such as design, painting, or photography) is the placement or arrangement of visual elements — how they are organized on a page. Many designers use a grid structure to help them position items on a page, and the same is true for web designers.<br>


## Css frameworKs:

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.<br>

*For example*: <br>
A Grid-based layout using the 960.gs grid.<br>


### Muliple style sheets:

***Using***:<br>

1. `@import`<br>
Some web page authors split up their CSS style rules into separate style sheets. For example, they might use one style sheet to control the layout and another to control fonts, colors and so on.<br>

> style.css

```
@import url("tables.css"); 
@import url("typography.css"); 
body {  
  color: #666666; 
  background-color: #f8f8f8; 
  text-align: center;
} 
#page {  
  width: 600px;  
  text-align: left;  
  margin-left: auto;  
  margin-right: auto;  
  border: 1px solid #d6d6d6;  
  padding: 20px;
} 
h3 {  
  color: #547ca0;
}

```

2. `link`:<br>
On this page you can see the other technique for including multiple style sheets. Inside the `<head>` element is a separate `<link>` element for each style sheet.<br>

> index.html

```

<!DOCTYPE html>
 <html>
   <head>
      <title>Multiple Style Sheets - Link</title>
      <link rel="stylesheet" type="text/css"    href="css/site.css" />  
      <link rel="stylesheet" type="text/css"    href="css/tables.css" />  
      <link rel="stylesheet" type="text/css"        href="css/typography.css" />
   </head> 
   <body>  
   <!-- HTML page content here --> 
   </body> 
 </html>

```

## Chapter 3 (first part): “Functions, Methods, and Objects”:

+ WHAT IS A FUNCTION?

Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements).<br>

* For example:
> JavaScript file

```
var msg = 'Sign up to receive our newsletter for 10% off!'; 
function updateMessage() {
   var el = document.getElementByld('message'}; 
   el .textContent = msg; 
} 
updateMessage(}; 
```

## Declaring a function:

to creat a function you give it a name and then statments needed to achieve its task inside the curly braces. This is known as a **function declaration**.<br>

```
function sayHello(){
  document.writr('Hello!');
}
```
`function` : function keyword.
`sayHello` : function name.
`{document.writr('Hello!');}` : code block (in curly braces).


## Calling a function:

Having declared the function, you can then execute all of the statements between its curly braces with just one line of code. This is known as **calling the function**.<br>

```
sayHello();
```

## Declarig functios that need information:

sometime a function need specific information to perform its task. In such case, when you declare the function you give it **parameters**. inside the function, the parameters act like variables.<br>

```
function getArea(width, height){
  return width * height;
}
```
`(width, height` : parameters.
`width` and `height` : the parameters are used like variables within the function.<br>
