# Chapter 7: “Forms”:

Traditionally, the term 'form' has referred to a printed document that contains spaces for you to fill in information.<br>

> Form Controls:

1. Adding Text:<br>
+ Input text(single line).
- Password input.
* Text Area(multi-line).

2. Making Choices:<br>
- Radio button.
+ checkbox.
* Drop-down boxs.

3. Submitting Forms:<be>
- Sumbit button.
- Image button.

4. Uploading files:<br>
- File upload.

### Form struCture:

`<form>`<br>
Form controls live inside a `<form>` element. This element should always carry the action attribute and will usually have a method and id attribute too.<br>

`action`<br>
Every `<form>` element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.<br>

`method`<br>
Forms can be sent using one of two methods: get or post.<br>

```
<form action="http://www.example.com/subscribe.php"  method="get">
 <p>This is where the form controls will appear.</p> 
</form>
```

**Text Input**:<br>

`<input>`<br>
The `<input>` element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.<br>

`type="text"` <br>
When the type attribute has a value of text, it creates a singleline text input.<br>

```
<form action="http://www.example.com/login.php">
 <p>Username:
   <input type="text" name="username" size="15"    maxlength="30" /> 
  </p> 
</form>
```

**Password Input**:<br>

`type="password"`<br>
 When the type attribute has a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked out. They are hidden in this way so that if someone is looking over the user's shoulder, they cannot see sensitive data such as passwords.<br>

`name`<br>
The name attribute indicates the name of the password input, which is sent to the server with the password the user enters.<br>

```
<form action="http://www.example.com/login.php">
 <p>Username:
   <input type="text" name="username" size="15"    maxlength="30" />
  </p>
  <p>Password:
    <input type="password" name="password" size="15"    maxlength="30" /> 
  </p> 
</form
```

**Text Area**:<br>

`<textarea>`<br>
The `<textarea>` element is used to create a mutli-line text input. Unlike other input elements this is not an empty element. It should therefore have an opening and a closing tag. <br>

Any text that appears between the opening `<textarea>` and closing `</textarea>` tags will appear in the text box when the page loads.<br>

```
<form action="http://www.example.com/comments.php">
 <p>What did you think of this gig?</p>  
 <textarea name="comments" cols="20" rows="4">
    Enter   your comments...
 </textarea>
</form>
```

**Radio button**:<br>

`<input>`
 `type="radio"` Radio buttons allow users to pick just one of a number of options.<br>

`name`<br>
The name attribute is sent to the server with the value of the option the user selects. When a question provides users with options for answers in the form of radio buttons, the value of the name attribute should be the same for all of the radio buttons used to answer that question.<br>

`value`<br>
The value attribute indicates the value that is sent to the server for the selected option. The value of each of the buttons in a group should be different (so that the server knows which option the user has selected).<br>

`checked`<br>
The checked attribute can be used to indicate which value (if any) should be selected when the page loads. The value of this attribute is checked. Only one radio button in a group should use this attribute.<br>

```
<form action="http://www.example.com/profile.php">
 <p>Please select your favorite genre:  <br />
    <input type="radio" name="genre" value="rock" checked="checked" /> Rock 
    <input type="radio" name="genre" value="pop" />     Pop   
    <input type="radio" name="genre" value="jazz" />     Jazz 
  </p> 
</form>
```

**Checkbox**:<br>

`<input>`<br>
`type="checkbox"` Checkboxes allow users to select (and unselect) one or more options in answer to a question.
name The name attribute is sent to the server with the value of the option(s) the user selects. When a question provides users with options for answers in the form of checkboxes, the value of the name attribute should be the same for all of the buttons that answer that question.<br>

`value`<br>
The value attribute indicates the value sent to the server if this checkbox is checked.<br>

`checked`<br>
he checked attribute indicates that this box should be checked when the page loads. If used, its value should be checked.<br>

```
<form action="http://www.example.com/profile.php">
 <p>Please select your favorite music service(s):  <br />
    <input type="checkbox" name="service"     value="itunes" checked="checked" /> iTunes
    <input type="checkbox" name="service"     value="lastfm" /> Last.fm   
    <input type="checkbox" name="service"     value="spotify" /> Spotify 
 </p> 
</form>
```

**Drop DoWn lIst boX**:<br>

`<select>`<br>
A drop down list box (also known as a select box) allows users to select one option from a drop down list. 
The `<select>` element is used to create a drop down list box. It contains two or more `<option>` elements. <br>

`name`<br>
 The name attribute indicates the name of the form control being sent to the server, along with the value the user selected.<br>

 `<option>`
The `<option>` element is used to specify the options that the user can select from. The words between the opening `<option>` and closing `</option> `tags will be shown to the user in the drop down box.<br>

`value`<br>
 The `<option>` element uses the value attribute to indicate the value that is sent to the server along with the name of the control if this option is selected.<br>

 `selected`<br>
  The selected attribute can be used to indicate the option that should be selected when the page loads. The value of this attribute should be selected.<br>

```
<form action="http://www.example.com/profile.php"> 
  <p>What device do you listen to music on?</p> 
  <select name="devices">
      <option value="ipod">iPod</option>
      <option value="radio">Radio</option>
      <option value="computer">Computer</option>  
  </select>
</form>
```


  **File Input box**:<br>

`<input>`<br>
If you want to allow users to upload a file (for example an image, video, mp3, or a PDF), you will need to use a file input box.<br>

`type="file"`<br>
 This type of input creates a box that looks like a text input followed by a ***browse*** button. When the user clicks on the ***browse*** button, a window opens up that allows them to select a file from their computer to be uploaded to the website.


```
<form action="http://www.example.com/upload.php" method="post">
  <p>Upload your song in MP3 format:</p> 
  <input type="file" name="user-song" /><br /> 
  <input type="submit" value="Upload" /> 
</form>
```

**SubmIt button**:<br>

`<input>`<br>
`type="submit"` The submit button is used to send a form to the server.<br>

`name`<br>
It can use a name attribute but it does not need to have one.<br>

`value`<br>
 The value attribute is used to control the text that appears on a button. It is a good idea to specify the words you want to appear on a button because the default value of buttons on some browsers is ‘Submit query’ and this might not be appropriate for all kinds of form.<br>

 ```
 <form action="http://www.example.com/subscribe.php">
  <p>Subscribe to our email list:</p>
  <input type="text" name="email" /> 
  <input type="submit" name="subscribe"   value="Subscribe" /> 
 </form>
 ```

 **Labelling Form Controls**:<br>

 `<label>`<br>
When introducing form controls, the code was kept simple by indicating the purpose of each one in text next to it. However, each form control should have its own `<label>` element as this makes the form accessible to vision-impaired users.<br>

`for`<br>
 The for attribute states which form control the label belongs to.  Note how the radio buttons use the id attribute. The value of the id attribute uniquely identifies an element from all other elements on a page

```
<label>Age: <input type="text" name="age" /> </label> <br/ >
Gender: 
<input id="female" type="radio" name="gender" value="f">
<label for="female">Female</label> 
<input id="male" type="radio" name="gender"  value="m"> 
<label for="male">Male</label>
```

# Chapter 14: “Lists, Tables & Forms”:

+ list-style-type:

The list-style-type property allows you to control the shape or style of a bullet point (also known as a **marker**). 
It can be used on rules that apply to the `<ol>`, `<ul>`, and `<li>` elements

1. Unordered Lists.
1. ordered Lists.

```
<h1>The Complete Poems</h1>
<h2>Emily Dickinson</h2> 
<ol>
 <li>Life</li> 
 <li>Nature</li> 
 <li>Love</li> 
 <li>Time and Eternity</li> 
 <li>The Single Hound</li> 
</ol>
```
**Tables**:<br>

A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.<br>

> Basic Table structure:

`<table>`<br>
The `<table>` element is used to create a table. The contents of the table are written out row by row.<br>
`<tr>`<br>
You indicate the start of each row using the opening `<tr>` tag. (The tr stands for table row.) 
It is followed by one or more `<td>` elements (one for each cell in that row). 
At the end of the row you use a  closing `</tr>` tag.<br>
`<td>`<br>
Each cell of a table is represented using a `<td>` element. (The td stands for table data.)
At the end of each cell you use a closing `</td>` tag.<br>

> index.html
```
<table>
  <tr>
      <td>15</td>    
      <td>15</td>
      <td>30</td>
  </tr>  
  <tr>
      <td>45</td>    
      <td>60</td>    
      <td>45</td>  
  </tr>  
  <tr>
      <td>60</td>    
      <td>90</td>    
      <td>90</td>  
  </tr> 
</table>
```
> browser

15 15 30<br>
45 60 54<br>
60 90 90<br>

### spanning columns:

The colspan attribute can be used on a `<th>` or `<td>` element and indicates how many **columns** that cell should run across.<br>

### spanning roWs:

The rowspan attribute can be used on a `<th>` or `<td>` element to indicate how many **rows** a cell should span down the 
table.<br>

### WidTh & spacing:

The opening `<table>` tag could also use the **cellpadding** attribute to add space inside each cell of the table, and the **cellspacing** attribute to create space between each cell of the table. The values for these attributes were given in pixels.<br>

### border & background:

The **border** attribute was used on both the `<table>` and `<td>` elements to indicate the width of the border in pixels.
The **bgcolor** attribute was used to indicate background colors of either the entire table or individual table cells. The value is usually a hex code.<br>


# Chapter 6: “Events”:

> HOW EVENTS TRIGGER JAVASCRIPT CODE:

When the user interacts with the HTML on a web page, there are three steps involved in getting it to trigger some JavaScript code. Together these steps are known as event handling.<br>

1. Select the element node(s) you want the script to respond to.
1. Indicate which event on the selected node(s) will trigger the response. 
1. State the code you want to run when the event occurs. 


> TRADITIONAL DOM EVENT HANDLERS:

All modern browsers understand this way of creating an event handler, but you can only attach one function to each event handler.<br>

`element.onevent = functionName ;`

* element : element.
* onevent : event.
* functionName : code.

> EVENT LISTENERS:

Event listeners are a more recent approach to handling events. They can deal with more than one function at a time but they are not supported in older browsers. <br>

`element .addEventlistener('event', functionName [, Boolean]) ; `

+ addEventlistener('event', functionName [, Boolean]) : Method.


> FOCUS & BLUR EVENTS:

The HTML elements you can interact with, such as links and form elements, can gain focus. These events fire when they gain or lose focus. <br>


**Event** |**Trigger** 
--- | ---
|`focus `| When an element gains focus, the focus event fires for that DOM node..
|`blur`|When an element loses focus, the b 1 ur event fires for that DOM node.
|`focusin`|Same as focus (see above but not supported in Firefox at time of writing).
|`focusout`|Same as b 1 ur (see above but not supported in Firefox at time of writing) .

  > MOUSE EVENTS :

  The mouse events are fired when the mouse is moved and also when its buttons are clicked.<br>

**Event** |**Trigger** 
--- | ---
|`click `| The click. event will fire for the element that the mouse is currently over..
|`dbclick`|Fires when the user clicks the primary mouse button twice in quick succession.
|`mousedown `| Fires when the user clicks down on any mouse button. 
|`mouseup `| Fires when the user releases a mouse button.
|`mouseover `| Fires when the cursor was outside an element and is then.
|`mouseout  `| Fires when the cursor is over an element, and then moves onto another element - outside of the current element or a child of it. 
|`mousemove  `| Fires when the cursor is moved around an element. This event is repeatedly fired..


> KEYBOARD EVENTS:

**Event** |**Trigger** 
--- | ---
|`input  `| Fires when the value of an `<input>` or `<textarea>` element changes.
|`keydown `|Fires when the user presses any key on the keyboard. If the user holds down a key, the event continues to fire repeatedly. This is important because it mimics what would happen in a text input if the user holds down a key (the same character would be added repeatedly while the key is held down)..
|`keypress  `| Fires when the user presses a key that would result in a character being shown on the screen. For example, this event would not fire when the user presses the arrow keys, whereas the keydown event would. If the user holds down a key, the event continues to fire repeatedly. 
|`keyup  `| Fires when the user releases a key on the keyboard. The keydown and keypress events fire before a character shows on screen, whereas keyup fires after it appears.


> FORM EVENTS:


**Event** |**Trigger** 
--- | ---
|`submit  `|  When a form is submitted, the submit event fires on the node representing the `<form>` element. It is most commonly used when checking the values a user has entered into a form before sending it to the server.
|`change `|Fires when the status of several form elements change.
|`input `| The i nput event. which you saw on the previous page is commonly used with `<input>` and `<textarea>` elements. 




