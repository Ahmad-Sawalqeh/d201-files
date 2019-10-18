# Chapter 9: Flash, Video & audio

Flash is a very popular technology used to add animations, video, and audio to websites. Since the late 1990s, Flash has been a very popular tool for creating animations, and later for playing audio and video in websites.<br>
Since 2005, a number of factors have meant that fewer websites are written in Flash or even use elements of Flash in their pages.<br>

> Adding a Flash moVie To Your web Page:

```
<!DOCTYPE html>
 <html>
  <head>
    <title>Adding a Flash Movie</title>  
    <script type="text/javascript"   src="http://ajax.googleapis.com/ajax/libs/   swfobject/2.2/swfobject.js"></script>
    <script type="text/javascript">
      swfobject.embedSWF("flash/bird.swf",   "bird", "400", "300", "8.0.0");
    </script> 
  </head> 
  <body>
    <div id="bird">
      <p>An animation of a bird taking a shower</p>
    </div>
  </body> 
</html>
```

1. The location of the .swf file: flash/bird.swf
2. The element that the Flash movie should replace, specified by the value of the id attribute on the `<div>` element: bird
3. The width of the Flash movie: 400 px
4. The height of the Flash movie: 300 px
5. The minimum version of the Flash player needed to view the movie: Flash Player 8


### hTml5: PreParing Video For Your Pages:

Despite the HTML5 `<video>` element being a very recent addition, it is enjoying widespread use.<br>

***`<video>`***<br>
The `<video>` element has a number of attributes which allow you to control video playback:<br>

`src`:<br>
This attribute specifies the path to the video.

`poster`<br>
This attribute allows you to specify an image to show while the video is downloading or until the user tells the video to play.<br>

`width,height`<br>
These attributes specify the size of the player in pixels. <br>

`controls`<br>
When used, this attribute indicates that the browser should supply its own controls for playback.<br>

`autoplay`<br>
When used, this attribute specifies that the file should play automatically.<br>

`loop`<br>
When used, this attribute indicates that the video should start playing again once it has ended.<br>

`preload`<br>
This attribute tells the browser what to do when the page loads. It can have one of three values:
+ `none` The browser should not load the video until the user presses play.<br>
+ `auto` The browser should download the video when the page loads. <br>
+ `metadata` The browser should just collect information such as the size, first frame, track list, and duration.

```
<!DOCTYPE html>
 <html>
  <head>
    <title>Adding HTML5 Video</title> 
  </head> 
  <body>
    <video src="video/puppy.mp4" poster="images/puppy.jpg" width="400" height="300" preload controls loop>
      <p>A video of a puppy playing in the snow</p>  
    </video> 
  </body> 
</html>
```

### hTml5: PreParing adding audio To web Pages:

By far the most popular format for putting audio on web pages is MP3.<br>

***`<audio>`***<br>
HTML5 introduced the `<audio>` element to include audio files in your pages. As with HTML5 video, browsers expect different formats for the audio.<br>
The `<audio>` element has a number of attributes which allow you to control audio playback:<br>

`src`<br>
This attribute specifies the path to the audio file.<br>

`controls`<br>
This attribute indicates whether the player should display controls. If you do not use this attribute, no controls will be shown by default. You can also specify your own controls using JavaScript.<br>

`autoplay`<br>
The presence of this attribute indicates that the audio should start playing automatically. (It is considered better practice to let visitors choose to play audio.)

`preload`<br>
This attribute indicates what the browser should do if the player is not set to autoplay. It can have the same values we saw on page 214 for the `<video>` element.<br>

`loop`<br>
This attribute specifies that the audio track should play again once it has finished.<br>



```
<!DOCTYPE html>
 <html>
  <head>
    <title>Adding HTML5 Audio</title> 
  </head> 
  <body>
    <audio src="audio/test-audio.ogg" controls autoplay>
       <p>This browser does not support our audio format.</p>
    </audio>
  </body>
</html>
```


# Chapter 16: “Images”

Controlling the size and alignment of your images using CSS keeps rules that affect the presentation of your page in the CSS and out of the HTML markup.<br>

You can control the size of an image using the width and height properties in CSS, just like you can for any other box.<br>

Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.<br>

> AlIgnIng Images UsIng css:

```
img.align-left {
   float: left; 
   margin-right: 10px;
} 
img.align-right {
  float: right;
  margin-left: 10px;
}
img.medium {
   width: 250px; 
   height: 250px;
}
```

> CenterIng Images UsIng css:

```
img.align-center {
    display: block;  
    margin: 0px auto;
}
img.medium {
    width: 250px;
    height: 250px;
}
```

### BackgroUnd Images:

* background-image:

```
body {
   background-image: url("images/pattern.gif");
}
```

### RepeatIng Images:

* background-repeat
* background-attachment

```
body {
   background-image: url("images/header.gif");
   background-repeat: repeat-x;
   background-attachment: fixed;
}
```

The background-repeat property can have four values:<br>
`repeat`<br>
The background image is repeated both horizontally and vertically (the default way it is shown if the backgroundrepeat property isn't used).<br>
`repeat-x`<br>
The image is repeated horizontally only (as shown in the first example on the left).<br>
`repeat-y`<br>
The image is repeated vertically only.<br>
`no-repeat`<br>
The image is only shown once.<br><br>

The background-attachment property specifies whether a background image should stay in one position or move as the user scrolls up and down the page. It can have one of two values:<br>
`fixed`<br>
The background image stays in the same position on the page.<br>
`scroll`<br>
The background image moves up and down as the user scrolls up and down the page.<br>

### BackgroUnd posItIon:

* background-position

This property usually has a pair of values. The first represents the horizontal position and the second represents the vertical. If you only specify one value, the second value will default to center.<br>

```
body {
   background-image: url("images/tulip.gif"); 
   background-repeat: no-repeat; 
   background-position: center top;
}
```

You can also use a pair of pixels or percentages. These represent the distance from the top left corner of the browser window (or containing box). The top left corner is equal to 0% 0%. The example shown, with values of 50% 50%, centers the image horizontally and vertically.<br>

```
body {
   background-image: url("images/tulip.gif"); 
   background-repeat: no-repeat; 
   background-position: 50% 50%;
}
```

# Chapter 19: “Practical Information”

**search engine oPtimization (seo)**:<br>

SEO is a huge topic and several books have been written on the subject. The following pages will help you understand the key concepts so you can improve your website's visibility on search engines.<br>

> on-Page seo:

In every page of your website there are seven key places where keywords (the words people might search on to find your site) can appear in order to improve its findability.<br>

1. Page title The page title appears at the top of the browser window or on the tab of a browser. It is specified in the `<title>` element which lives inside the `<head>` element.<br>

2. url / WeB address The name of the file is part of the URL. Where possible, use keywords in the file name.<br>

3. headings If the keywords are in a heading `<hn>` element then a search engine will know that this page is all about that subject and give it greater weight than other text.<br>

4. text Where possible, it helps to repeat the keywords in the main body of the text at least 2-3 times. Do not, however, over-use these terms, because the text must be easy for a human to read

5. link text Use keywords in the text that create links between pages.<br>

6. image alt text Search engines rely on you providing accurate descriptions of images in the alt text. This will also help your images show up in the results of image-based searches.<br>

7. Page descriPtions The description also lives inside the `<head>` element and is specified using a `<meta>` tag. It should be a sentence that describes the content of the page. (These are not shown in the browser window but they may be displayed in the results pages of search engines.)



