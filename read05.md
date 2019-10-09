# Chapter 5: “Images”

## Adding Images:

`<img>`<br>
To add an image into the page you need to use an `<img>` element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:<br>

- It must carry the following two attributes:<br>
1. `src`<br>
 This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site.
2. `alt`<br>
 This provides a text description of the image which describes the image if you cannot see it.

- `height`<br>
 This specifies the height of the image in pixels.
- `width`<br>
 This specifies the width of the image in pixels.
- `align` => `left` , `right` , `top` , `bottom` , `middle` <br>
 The align attribute was commonly used to indicate how the other parts of a page should flow around an image. It has been removed from HTML5 and new websites should use CSS to control the alignment of image.


 * For example:
 ```
<img src="images/quokka.jpg" alt="A family of quokka" width="600" height="450" align="left"/>
 ```

> Type of images: Image formats: jpeg, gif, png.


# Chapter 11: “Color”

1. rgb values:<br>
 These express colors in terms of how much red, green and blue are used to make it up.
2. hex Codes:<br>
 These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign.
3. Color names:<br>
 There are 147 predefined color names that are recognized by browsers.

+ For example:
```
/* color name */
h1 { 
   color: DarkCyan;
}
/* hex code */
h2 {
   color: #ee3e80;
}
/* rgb value */
p {
   color: rgb(100,100,90);
}
```

## Css3: opacity, rgba

```
p.one {
   background-color: rgb(0,0,0);
   opacity: 0.5;
} 
p.two {
   background-color: rgb(0,0,0); 
   background-color: rgba(0,0,0,0.5);
}
```

## Css3: hsl, hsla

```
body {
   background-color: #C8C8C8;
   background-color: hsl(0,0%,78%);
}
p {
   background-color: #ffffff;
   background-color: hsla(0,100%,100%,0.5);
}
```


# Chapter 12: “Text”


1. `weight` : <br>
`Light`, `Medium`, `Bold`, `Black`.

2. `style` : <br>
`Normal`, `Italic`, `Obliqu`.


## Specifying Typefaces

* `font-family`:<br>
The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.

```
body {
  font-family: Georgia, Times, serif;
}   
h1, h2 {
  font-family: Arial, Verdana, sans-serif;
}   
.credits {
  font-family: "Courier New", Courier, monospace;
}
```

## Size of Type

* `font-size`:<br>
The font-size property enables you to specify a size for the font. There are several ways to specify the size of a font. The most common are:<br>

**Pixels** are commonly used because they allow web designers very precise control over how much space their text takes up. The number of pixels is followed by the letters px.

**percentages** The default size of text in browsers is 16px. So a size of 75% would be the equivalent of 12px, and 200% would be 32px.

```
body {
   font-family: Arial, Verdana, sans-serif;
   font-size: 12px;
} 
h1 {
   font-size: 200%;
}
h2 {
   font-size: 1.3em;
}
```

## more font choice

+ `@font-face`:<br>
@font-face allows you to use a font, even if it is not installed on the computer of the person browsing, by allowing you to specify a path to a copy of the font, which will be downloaded if it is not on the user's machine.

***font-family*** This specifies the name of the font. This name can then be used as a value of the font-family property in the rest of the style sheet.

***format*** This specifies the format that the font is supplied in.

The various font formats should appear in your code in this order:
1. eot 
2. woff 
3. ttf/otf 
4. svg

```
@font-face {
   font-family: 'ChunkFiveRegular';
   src: url('fonts/chunkfive.eot');
} 
h1, h2 {
   font-family: ChunkFiveRegular, Georgia, serif;
}
```

## text-transform

The text-transform property is used to change the case of text giving it one of the following values:<br>

**uppercase** This causes the text to appear uppercase.
**lowercase** This causes the text to appear lowercase.
**capitalize** This causes the first letter of each word to appear capitalized.

```
h1 {
   text-transform: uppercase;
} 
h2 {
   text-transform: lowercase;
} .
credits {
   text-transform: capitalize;
}
```

## text-decoration

The text-decoration property allows you to specify the following values:<br>

**none** This removes any decoration already applied to the text.
**underline** This adds a line underneath the text.
**overline** This adds a line over the top of the text.
**line-through** This adds a line through words.

```
.credits {
   text-decoration: underline;
} 
a {
   text-decoration: none;
}
```

## letter-spacing, word-spacing

typographers use for the space between each letter. You can control the space between each letter with the letter-spacing property.<br>

```
h1, h2 {
   text-transform: uppercase;
   letter-spacing: 0.2em;
} 
.credits {
   font-weight: bold; 
   word-spacing: 1em;
}
```

## text-align

The text-align property allows you to control the alignment of text. The property can take one of four values:<br>

+ `left`: This indicates that the text should be left-aligned.
+ `right`: This indicates that the text should be right-aligned.
+ `center`: This allows you to center text.
+ `justify`: This indicates that every line in a paragraph, except the last line,  should be set to take up the full width of the containing box.

```
h1 {
   text-align: left;
} 
p {
   text-align: justify;
} 
.credits {
   text-align: right;
}
```
