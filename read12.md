# The <canvas> element

`<canvas id="tutorial" width="150" height="150"></canvas>`

At first sight a `<canvas>` looks like the `<img>` element, with the only clear difference being that it doesn't have the `src` and `alt` attributes. Indeed, the `<canvas>` element has only two attributes, `width` and `height`. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be **300 pixels** wide and **150 pixels** high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.<br>

The `id` attribute isn't specific to the `<canvas>` element but is one of the global HTML attributes which can be applied to any HTML element (like `class` for instance). It is always a good idea to supply an `id` because this makes it much easier to identify it in a script.

The `<canvas>` element can be styled just like any normal image (`margin`, `border`, `background` …). These rules, however, don't affect the actual drawing on the canvas. 


### The rendering context:

The `<canvas>` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The `<canvas>` element has a method called `getContext()`, used to obtain the rendering context and its drawing functions. `getContext()` takes one parameter, the type of context.


# Drawing shapes with canvas

### Drawing rectangles:

First let's look at the rectangle. There are three functions that draw rectangles on the canvas:

`fillRect(x, y, width, height)`<br>
Draws a filled rectangle.
`strokeRect(x, y, width, height)`<br>
Draws a rectangular outline.
`clearRect(x, y, width, height)`<br>
Clears the specified rectangular area, making it fully transparent.<br>

Each of these three functions takes the same parameters. `x` and `y` specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. `width` and `height` provide the rectangle's size.<br>

Below is the `draw()` function from the previous page, but now it is making use of these three functions:

```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}
```

The `fillRect()` function draws a large black square 100 pixels on each side.<br>
The `clearRect()` function then erases a 60x60 pixel square from the center, and then `strokeRect()` is called to create a rectangular outline 50x50 pixels within the cleared square.


and so on we can crreat:
1. Drawing paths:
Here are the functions used to perform these steps:<br>

`beginPath()`<br>
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.<br>
`Path methods`<br>
Methods to set different paths for objects.<br>
`closePath()`<br>
Adds a straight line to the path, going to the start of the current sub-path.<br>
`stroke()`<br>
Draws the shape by stroking its outline.<br>
`fill()`<br>
Draws a solid shape by filling the path's content area.<br>

2. Lines:
For drawing straight lines, use the `lineTo()` method.<br>

`lineTo(x, y)`<br>
Draws a line from the current drawing position to the position specified by `x` and `y`.
This method takes two arguments, `x` and `y`, which are the coordinates of the line's end point. The starting point is dependent on previously drawn paths, where the end point of the previous path is the starting point for the following, etc. The starting point can also be changed by using the `moveTo()` method.

The example below draws two triangles, one filled and one outlined.

```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    // Filled triangle
    ctx.beginPath();
    ctx.moveTo(25, 25);
    ctx.lineTo(105, 25);
    ctx.lineTo(25, 105);
    ctx.fill();

    // Stroked triangle
    ctx.beginPath();
    ctx.moveTo(125, 125);
    ctx.lineTo(125, 45);
    ctx.lineTo(45, 125);
    ctx.closePath();
    ctx.stroke();
  }
}
```

This starts by calling `beginPath()` to start a new shape path. We then use the `moveTo()` method to move the starting point to the desired position. Below this, two lines are drawn which make up two sides of the triangle.


3. Rectangles:
In addition to the three methods we saw in Drawing rectangles, which draw rectangular shapes directly to the canvas, there's also the `rect()` method, which adds a rectangular path to a currently open path.<br>

`rect(x, y, width, height)`<br>
Draws a rectangle whose top-left corner is specified by (`x`, `y`) with the specified `width` and `height`.
Before this method is executed, the `moveTo()` method is automatically called with the parameters (x,y). In other words, the current pen position is automatically reset to the default coordinates.<br>

# Applying styles and colors

1. Color:
Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: `fillStyle` and `strokeStyle`.<br>

`fillStyle = color`<br>
Sets the style used when filling shapes.<br>
`strokeStyle = color`<br>
Sets the style for shapes' outlines.<br>

color is a string representing a CSS `<color>`, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).<br>

The valid strings you can enter should, according to the specification, be CSS `<color>` values. Each of the following examples describe the same color.<br>

```
// these all set the fillStyle to 'orange'

ctx.fillStyle = 'orange';
ctx.fillStyle = '#FFA500';
ctx.fillStyle = 'rgb(255, 165, 0)';
ctx.fillStyle = 'rgba(255, 165, 0, 1)';
```

2. Transparency:
In addition to drawing opaque shapes to the canvas, we can also draw semi-transparent (or translucent) shapes. This is done by either setting the `globalAlpha` property or by assigning a semi-transparent color to the stroke and/or fill style.<br>

`globalAlpha = transparencyValue`<br>
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.<br>

The `globalAlpha` property can be useful if you want to draw a lot of shapes on the canvas with similar transparency, but otherwise it's generally more useful to set the transparency on individual shapes when setting their colors.<br>

Because the `strokeStyle` and `fillStyle` properties accept CSS rgba color values, we can use the following notation to assign a transparent color to them.<br>

```
// Assigning transparent colors to stroke and fill style

ctx.strokeStyle = 'rgba(255, 0, 0, 0.5)';
ctx.fillStyle = 'rgba(255, 0, 0, 0.5)';
```

The `rgba()` function is similar to the `rgb()` function but it has one extra parameter. The last parameter sets the transparency value of this particular color. The valid range is again between 0.0 (fully transparent) and 1.0 (fully opaque).<br>

# Drawing text

The canvas rendering context provides two methods to render text:<br>

`fillText(text, x, y [, maxWidth])`<br>
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.<br>

```
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.fillText('Hello world', 10, 50);
}
```

`strokeText(text, x, y [, maxWidth])`<br>
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.<br>

```
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.strokeText('Hello world', 10, 50);
}
```

### Styling text

In the examples above we are already making use of the `font` property to make the text a bit larger than the default size. There are some more properties which let you adjust the way the text gets displayed on the canvas:<br>

`font = value`<br>
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.<br>

`textAlign = value`<br>
Text alignment setting. Possible values: `start`, `end`, `left`, `right` or `center`. The default value is `start`.<br>

`textBaseline = value`<br>
Baseline alignment setting. Possible values: `top`, `hanging`, `middle`, `alphabetic`, `ideographic`, `bottom`. The default value is `alphabetic`.<br>

`direction = value`<br>
Directionality. Possible values: `ltr`, `rtl`, `inherit`. The default value is `inherit`.<br>

These properties might be familiar to you, if you have worked with CSS before.<br>

The following diagram from the WHATWG demonstrates the various baselines supported by the `textBaseline` property.<br>

> A textBaseline example:

Edit the code below and see your changes update live in the canvas:<br>

```
ctx.font = '48px serif';
ctx.textBaseline = 'hanging';
ctx.strokeText('Hello world', 0, 100);
```