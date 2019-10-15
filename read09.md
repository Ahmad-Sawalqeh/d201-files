# Chapter 15: “Layout”:

1. Building Blocks:

CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.<br>

> containing Elements:<br>

If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.<br>

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

When you move any element from normal flow, boxes can overlap. The `z-index` property allows you to control which box appears on top.<br>


***Overlapping elements***:<br>

`z-index`<br>
When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page. 
If you want to control which element sits on top, you can use the `z-index` property. Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a `z-index` of 10 will appear over the top of one with a `z-index` of 5.


***Floating elements***:<br>
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
