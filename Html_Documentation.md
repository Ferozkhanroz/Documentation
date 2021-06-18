# HTML BASICS
_Hello Legends! Before we start off with anything in-depth lets look into some basics of **HTML5**_
<br>

# CONTENTS
- [What is HTML?](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#what-is-html)
- [What is an HTML ELEMENT?](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#what-is-an-html-element)
- [Html Attributes](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-attributes--)
- [Html Headings & Paragraphs](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-headings--paragraphs--)
- [Html Formatting](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-formatting--) 
- [Html Forms and Input Controls](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-forms--input-controls--)
- [Html Links](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-links--)
- [Html Lists](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-lists--)
- [Html Iframe](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-iframe--)
- [Html Tables](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-tables--)
- [Html Styles](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-styles--)
- [Html Multimedia](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-multimedia--)
- [Html JavaScript](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-javascript--)
- [Html Browser Support](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-browser-support)
- [Html Attributes](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-attributes---1)
- [Html Global Attributes](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-global-attributes--)
- [Html Events](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-events--)
- [Html Canvas](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-canvas--)
- [HtmlAudio & Video](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-audio--video--)
- [Html Character sets and Encodings](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-character-sets-and-encodings--)
- [Html Language code](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-language-code--)
- [Html Country Code](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#html-country-code--)
- [Http Messages](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#http-messages--)
- [Http Methods](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#http-methods--)
- [Acknowledgements](https://github.com/Ferozkhanroz/HTML/blob/main/HTML%20DOCUMENTATION.md#acknowledgements--)

## What is HTML?
    
HTML stands for Hyper Text Markup Language used for creating Web Pages which describes the
structure of the web page consisting a series of elements.
    
pretty simple right?

---
## What is an HTML ELEMENT?  
   An HTML element is defined by a start tag, some content, and an end tag:
>SYNTAX : `<tagname>` content `</tagname>`

some basic tags are :-
-  `<html></html>`
-  `<head></head>`
-  `<title></title>`
-  `<h1></h1>`
-  `<p></p>`<br>

_NOTE :_ Not all elements should have a closing tag, there are certain tags like `<br>` which do not have a closing tag. we'll see more in future examples.

---
## HTML ATTRIBUTES :-
HTML attributes provide additional information about HTML elements.  
- `href`
- `src`
- `width`
- `height`
- `alt`
### Examples using attributes :-
    <a href="https://www.halleyx.com">Visit Halleyx</a>
    
    <img src="link_to_image.jpg">
    
    <img src="link_to_image.jpg" width="500" height="600">
    
    <img src="img.jpg" alt="image to show alt attribute in html">
    
- <small> _`<a>`_ tag is used to define hyperlink. _href_ attribute specifies the URL of the page the link goes to..</small>
    
- <small>_`<img>`_ tag is used to embed an image in an HTML page. The _src_ attribute specifies the path to the image to be displayed..</small>

- <small>_`<img>`_ tag should also contain the _width_ and _height_ attributes, which specifies the width and height of the image (in pixels)</small>

- <small>_`<img>`_ tag with an _alt_ attribute specifies an alternate text for an image, if the image cannot be displayed for any reason, the alternative text will be displayed</small>

---
## HTML HEADINGS & PARAGRAPHS :-   
HTML headings are titles or subtitles that you want to display on a webpage.
There are 6 different sizes each heading can be defined starting with  `<h1>` which is the most important and
biggest heading to `<h6>` which is the smallest heading.

### Examples for Headings :
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
    <h3>Heading 3</h3>
    <h4>Heading 4</h4>
    <h5>Heading 5</h5>
    <h6>Heading 6</h6>

A paragraph always starts on a new line, and is usually a block of text.
### Examples for Paragraphs :
    <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
        incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud 
        exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat </p>

---
    
## Example for a simple HTML Doc  :-
     <!DOCTYPE html>
     
     <html>
         <head>
             <title> This is a Title </title>
         </head>
     
         <body>
               
             <h1> This is a Heading </h1>
             <p> This is a paragraph. </p>

         </body>
     </html>

### Explanation for the above example :-
- `<!DOCTYPE html>` : This declaration defines that this document is an HTML5 document.
- `<html>` : This element is the root element of an HTML page.
- `<head>` :  This element contains meta information about the HTML page.
- `<title>` :  This element specifies a title for the HTML page.
- `<body>` : This element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
- `<h1>` :  This element defines a large heading.
- `<p>` : This element defines a paragraph.
---
## HTML FORMATTING :-
HTML formatting elements are used to display special types of text.
>SYNTAX :  `<tagname>` text `</tagname>`

### A few examples of basic formatting elements :-
- `<b>` Bold text `</b>` = <b> Bold text </b>
- `<strong>` Important text `</strong>` = <strong> Important text </strong>
- `<i>` Italic text `</i>` = <i>  Italic text </i>
- `<em>` Emphasized text `</em>`= <em> Emphasized text </em>
- <`mark>` Marked text `</mark>` = <mark> Marked text </mark>
- `<small>` Smaller text `</small>` = <small> Smaller text </small>
- `<del>` Deleted text `</del>` = <del> Deleted text </del>
- `<ins>` Inserted text `</ins>` = <ins> Inserted text </ins>
- `<sub>` Subscript text `</sub>` = Normal Text<sub> Subscript text </sub>
- `<sup>` Superscript text `</sup>` = Normal Text <sup> Superscript text </sup>

---

Now that we have done with the boring basic stuff..Lets get started with something interesting.
## HTML FORMS & INPUT CONTROLS :- 
 The HTML `<form>` is simply used to create a form from user inputs.
 > SYNTAX :  
 > `<form>` <br>
 >            . <br>
 >            form elements <br>
 >            . <br>
 > `</form>`
 
A form element contains different types of input elements like text field, check box, submit buttons. <br>
The most basic form element we'll be using is `<input>` and `<label>` elements. <br>
An `<input>` element can be displayed in many ways, depending on the _type_ attribute. <br>

### A few examples for `<input>` element :- 
- `<input type="text">` =	Displays a single-line text input field
- `<input type="radio">`	= Displays a radio button (for selecting one of many choices)
- `<input type="checkbox">`	= Displays a checkbox (for selecting zero or more of many choices)
- `<input type="submit">`	= Displays a submit button (for submitting the form)
- `<input type="button">`	= Displays a clickable button.
 
The `<label>` tag defines a label for many form elements. <br>
The `<label>` element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focus on the input element. <br>
The _for_ attribute of the `<label>` tag should be equal to the _id_ attribute of the `<input>` element to bind them together. <br>
 
### A few examples for `<label>` element :- 
    <form>
      <label for="fname">First name:</label><br>
      <input type="text" id="fname" name="fname"><br>
      <label for="lname">Last name:</label><br>
      <input type="text" id="lname" name="lname">
    </form>
---
## HTML LINKS :- 
As we saw earlier in the html attributes _href_  attribute is used to specify 
the destination address of the link used. The _`<a>`_ tag is used to link the _source_ anchor to the _destination_ anchor which may be any Web resource such as an image, a video clip, a program, an HTML document or an element within an HTML document.

### Examples for using Link :- 
    <a href = "https://www.halleyx.com">Welcome to Halleyx</a>
 
 "Welcome to Halleyx" is the text display which on clicked will take the user to the destination page.
 
---
## HTML LISTS :-
As we all know what is a list, html offers 3  different types of list on how things can be arranged.
 - ul : An unordered list. This will list items using plain bullets.
 - ol : An ordered list. This will use different schemes of numbers to list your items.
 - dl : A definition list. This arranges your items in the same way as they are arranged in a dictionary.
### Ordered List :- 
    <ol>
       <li>Wraith</li>
       <li>Octane</li>
       <li>Pathfinder</li>
       <li>Mirage</li>
    </ol> 
### Unordered List :- 
    <ul>
       <li>Wraith</li>
       <li>Octane</li>
       <li>Pathfinder</li>
       <li>Mirage</li>
    </ul> 
### Description List :-
A description list is a list of terms, with a description of each term.
The `<dl>` tag defines the description list, the `<dt>` tag defines the term name, and the `<dd>` tag describes each term.
    
    <dl>
      <dt>Coffee</dt>
      <dd>- 500 gms</dd>
      <dt>Milk</dt>
      <dd>- 1 ltr</dd>
    </dl> 

 ---
 ## HTML IFRAME :-
 The iframe in HTML stands for _Inline Frame_. An inline frame is used to embed another document within the current HTML document.
 > SYNTAX : `<iframe src="URL"></iframe>`
 ### A simple Iframe example :-
     
      <!DOCTYPE html>
      <html>
  
      <body>
         <p> Any content can be displayed</p>
         <iframe src="https://www.halleyx.com" 
                 height="300" width="400">
         </iframe>
  
      </body>
  
      </html>
Running this block of code will open the desired link inside a frame with the specified dimensions.
 
---

## HTML TABLES :-
A table is an arrangement of data in rows and columns, or possibly in a more complex structure. <br>
An HTML table is defined with the `<table>` tag. Each table row is defined with the `<tr>` tag. A table header is defined with the `<th>` tag. By default, table headings are bold and centered. A table data/cell is defined with the `<t>` tag.

### Example to create a simple table :- 
      <table>
        <tr>
            <th>NAME</th>
            <th>D.O.B</th>
            <th>MOBILE</th>
        </tr>
        <tr>
            <td>Nayanthara</td>
            <td>18.11.2000</td>
            <td>951XXX5914</td>
        </tr>
        <tr>
            <td>Samantha</td>
            <td>26.01.1999</td>
            <td>904XXX2435</td>
        </tr>
        <tr>
            <td>Anushka</td>
            <td>05.11.2000</td>
            <td>638XXX7595</td>
        </tr>
      </table>
 
---
## HTML STYLES :- 
The HTML _style_ attribute is used to add styles to an element, such as color, font, size, and more.
 > SYNTAX : `<tagname style="property:value;">` <br>

The property is a **CSS** property. The value is a **CSS** value.
### Some cool examples you can try out with styles :
#### Background : 
Set the background color for a page: 
      
      <body style="background-color:powderblue;">

         <h1>This is a heading</h1>
         <p>This is a paragraph.</p>

      </body>

 Set background color for two different elements:
      
      <body>

         <h1 style="background-color:powderblue;">This is a heading</h1>
         <p style="background-color:tomato;">This is a paragraph.</p>

      </body>
 
#### Text Color :<br>
The CSS color property defines the text color for an HTML element:
      
      <h1 style="color:blue;">This is a heading</h1>
      <p style="color:red;">This is a paragraph.</p>

#### Fonts :- 
The CSS font-family property defines the font to be used for an HTML element:

      <h1 style="font-family:verdana;">This is a heading</h1>
      <p style="font-family:courier;">This is a paragraph.</p>
 
#### Text Size :- 
The CSS font-size property defines the text size for an HTML element:

      <h1 style="font-size:300%;">This is a heading</h1>
      <p style="font-size:160%;">This is a paragraph.</p>
 
#### Text Alignment :- 
The CSS text-align property defines the horizontal text alignment for an HTML element:

      <h1 style="text-align:center;">Centered Heading</h1>
      <p style="text-align:center;">Centered paragraph.</p>
 
 There are a lot more fonts and colors are  available for you to explore...play with them!
 
---
## HTML MULTIMEDIA :- 
Multimedia comes in many different formats. It can be almost anything you can hear or see, like images, music, sound, videos, records, films, animations, and more. Multimedia elements (like audio or video) are stored in media file. There are so many types of video and audio formats available but only a few of them are supported in HTML.

### VIDEO :- 
`<video>` element is used to embed the video in our html.
	
	<video controls>
  		<source src="link_to_video.mp4" type="video/mp4">
	</video>

### AUDIO :- 
To play an audio file in HTML, use the `<audio>` element
	
	<audio controls>
  		<source src="link_to_audio.mp3" type="audio/mpeg">
	</audio>


The _controls_ attribute adds video/audio controls, like play, pause, and volume.
There are also few other attributes like _autoplay_ & _autoplay muted_ .

---
## HTML JAVASCRIPT :- 
JavaScript makes HTML pages more dynamic and interactive. <br>
The HTML `<script>` tag is used to define a client-side script (JavaScript).
The `<script>` element either contains script statements, or it points to an external script file through the src attribute.
	
### Example :- 
	
	<button type="button" onclick="myFunction()">Click Me!</button>

	<p id="demo">This is a demonstration.</p>

	<script>
	function myFunction() { 
  	document.getElementById("demo").innerHTML = "Hello JavaScript!";
	}
	</script> 
	
Execute this cool example. Basically what we have done here is using javascript we made the html content change by clicking a button. <br>
This will be much more easier when we are familiar with JavaScript.

---
## HTML BROWSER SUPPORT
Actually you need not be worried about this section as it just lists all HTML elements that are supported by different browsers like Chrome, Edge, Firefox, Safari and Opera.<br>
The latest version of any of those browsers should do good on-the-go.
You can go <a href="https://www.w3schools.com/tags/ref_html_browsersupport.asp">HERE</a> to see all the supported elements from different browsers.

---
## HTML ATTRIBUTES :- 
Some of the HTML attributes and elements that can be used within is listed below..

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Attribute**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Belongs to**
<pre>
accept		      	       &lt;input&gt;
action	                       &lt;form&gt;
alt 		               &lt;area&gt;, &lt;img&gt;, &lt;input&gt;
autocomplete	               &lt;form&gt;, &lt;input&gt;
autoplay 	               &lt;audio&gt;, &lt;video&gt;
</pre>

There are a lot more <a href="https://www.w3schools.com/tags/ref_attributes.asp">HERE</a>. Check them out!.

---
## HTML GLOBAL ATTRIBUTES :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Attribute**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description** <br>
<pre>
accesskey	              Specifies a shortcut key to activate/focus an element
class	                      Specifies one or more classnames for an element (refers to a class in a style sheet)
contenteditable	              Specifies whether the content of an element is editable or not
data-*	                      Used to store custom data private to the page or application
dir	                      Specifies the text direction for the content in an element
draggable	              Specifies whether an element is draggable or not
hidden	                      Specifies that an element is not yet, or is no longer, relevant
id	                      Specifies a unique id for an element
lang	                      Specifies the language of the element's content
spellcheck	              Specifies whether the element is to have its spelling and grammar checked or not
style	                      Specifies an inline CSS style for an element
tabindex	              Specifies the tabbing order of an element
title	                      Specifies extra information about an element
translate	              Specifies whether the content of an element should be translated or not
</pre>

---
## HTML EVENTS :- 
HTML has the ability to let events trigger actions in a browser, like starting a JavaScript when a user clicks on an element. <br>
Below are few examples of the global event attributes that can be added to HTML elements to define event actions.

### Form Event Examples :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Attribute**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description** <br>
<pre>
onblur			      Fires the moment that the element loses focus
onchange		      Fires the moment when the value of the element is changed
oncontextmenu		      Script to be run when a context menu is triggered
onfocus			      Fires the moment when the element gets focus
oninput			      Script to be run when an element gets user input
oninvalid		      Script to be run when an element is invalid
onreset			      Fires when the Reset button in a form is clicked
onsearch		      Fires when the user writes something in a search field (for <input="search">)
onselect		      Fires after some text has been selected in an element
onsubmit		      Fires when a form is submitted
</pre>
	
### Keyboard Event Examples :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Attribute**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description**
<pre>
onkeydown		      Fires when a user is pressing a key
onkeypress	              Fires when a user presses a key
onkeyup	 		      Fires when a user releases a key
</pre>

### Mouse Event Examples :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Attribute**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description**
<pre>
onclick			      Fires on a mouse click on the element
ondblclick	 	      Fires on a mouse double-click on the element
onmousedown	 	      Fires when a mouse button is pressed down on an element
onmousemove	 	      Fires when the mouse pointer is moving while it is over an element
onmouseout	 	      Fires when the mouse pointer moves out of an element
onmouseover	 	      Fires when the mouse pointer moves over an element
onmouseup		      Fires when a mouse button is released over an element
onmousewheel	 	      Deprecated. Use the onwheel attribute instead
onwheel	 		      Fires when the mouse wheel rolls up or down over an element
</pre>

---
## HTML CANVAS :- 
The HTML <canvas> tag is used to draw graphics, on the fly, via scripting (usually JavaScript).<br>

### Colors, Styles & Shadows :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Property**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description**
<pre>
fillStyle		      Sets or returns the color, gradient, or pattern used to fill the drawing
strokeStyle		      Sets or returns the color, gradient, or pattern used for strokes
shadowColor		      Sets or returns the color to use for shadows
shadowBlur		      Sets or returns the blur level for shadows
shadowOffsetX		      Sets or returns the horizontal distance of the shadow from the shape
shadowOffsetY		      Sets or returns the vertical distance of the shadow from the shape
</pre>

---
## HTML AUDIO & VIDEO :- 
The HTML5 DOM(Document Object Model) has methods, properties, and events for the <audio> and <video> elements.

### HTML Audio/Video Methods :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Method**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description**
<pre>
addTextTrack()		      Adds a new text track to the audio/video
canPlayType()		      Checks if the browser can play the specified audio/video type
load()		              Re-loads the audio/video element
play()			      Starts playing the audio/video
pause()			      Pauses the currently playing audio/video
</pre>

### HTML Audio/Video Properties :- 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Properties**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description**
<pre>
audioTracks		      Returns an AudioTrackList object representing available audio tracks
autoplay		      Sets or returns whether the audio/video should start playing as soon as it is loaded
controller		      Returns the MediaController object representing the current media controller of the audio/video
controls		      Sets or returns whether the audio/video should display controls (like play/pause etc.)
currentSrc		      Returns the URL of the current audio/video
currentTime		      Sets or returns the current playback position in the audio/video (in seconds)
defaultMuted		      Sets or returns whether the audio/video should be muted by default
defaultPlaybackRate	      Sets or returns the default speed of the audio/video playback
duration		      Returns the length of the current audio/video (in seconds)
videoTracks		      Returns a VideoTrackList object representing the available video tracks
volume		              Sets or returns the volume of the audio/video
</pre>
	
### HTML Audio/Video Events :- 
	
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Events**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Description**
<pre>
abort			      Fires when the loading of an audio/video is aborted
canplay			      Fires when the browser can start playing the audio/video
ended			      Fires when the current playlist is ended
error		 	      Fires when an error occurred during the loading of an audio/video
pause			      Fires when the audio/video has been paused
play		              Fires when the audio/video has been started or is no longer paused
suspend		     	      Fires when the browser is intentionally not getting media data
timeupdate		      Fires when the current playback position has changed
volumechange		      Fires when the volume has been changed
</pre>
	
---
## HTML CHARACTER SETS AND ENCODINGS :- 
To display an HTML page correctly, the browser must know what character set (encoding) to use:

> `<meta charset="UTF-8">`
	
Whenever we write a html code we'll be using the above encoding.
<a href="https://www.w3schools.com/tags/ref_charactersets.asp">HERE's</a> where you can see the entire character sets encoding.

---
## HTML LANGUAGE CODE :- 
You should always include the lang attribute inside the <html> tag, to declare the language of the Web page. This is meant to assist search engines and browsers.
	
	<html lang="en">
	...
	</html>
	
List of all <a href="https://www.w3schools.com/tags/ref_language_codes.asp">Language Codes</a>

## HTML COUNTRY CODE :-  
In HTML, country codes can be used as an addition to the language code in the _lang_ attribute.
First Two characters defines the language code and Last Two characters defines the country code.
	
	<html lang="en-US">
	...
	</html>
	
List of all <a href="https://www.w3schools.com/tags/ref_country_codes.asp">Country Codes</a>

---
## HTTP MESSAGES :- 
When a browser requests a service from a web server, an error might occur, and the server might return an error code called **status messages**
- Messages that start with **1** hundred are **informative messages**.
- Messages that start with **2** hundres are **successful messages**.
- Messages that start with **3** hundred are **Redirection messages**.
- Messages that start with **4** hundres are **Client-error messages**.	
- Messages that start with **5** hundres are **Server-error messages**.	

---
## HTTP METHODS :- 
The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients and servers.<br>
Some of the commonly used http methods are :<br>
- GET
- POST
- PUT
- HEAD
- DELETE
- PATCH
- OPTIONS

The two most common HTTP methods are: GET and POST.
#### GET :
GET is used to request data from a specified resource.
#### POST :
POST is used to send data to a server to create/update a resource.

---
Most of the basic and important topics from HTML has been covered.<br>
.<br>
.<br>
.<br>
.<br>
.<br>
.<br>
## Acknowledgements :- 
- Shout out to <a href="https://www.youtube.com/watch?v=vQWlgd7hV4A">@Dev Ed</a> for his easy to learn crash course on HTML.
- Also to <a href="https://www.w3schools.com/html/default.asp">W3Schools</a> which hugely helped in drafting the documentation.
