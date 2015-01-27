% Web Development 101

# The Basics

## Actors

1. A _browser_ (on behalf of a user)
    * Requests data and must figure out how to render it and how to
      allow the user to interact with it
2. A server _hosting_ a website, to which the user wants to connect
    * Must understand _requests_ from the user and provide a _reply_
3. A Domain Name Server (DNS) which knows about machines on the Internet

## Life of a request

1. User types in browser address
     * `http://wwww.Google.com`
2. The browser requests the IP\footnote{Internet Protocol} from the DNS:
     * `http://wwww.google.com` --> `92.4.96.944`
3. The IP address identifies the host server and can be used to find a
   _path_ from the user's machine to it through the network
4. The user browser then sends a request to the host
     * `Hey, give me (some page of) your website`
5. The host server responds with the requested data

# Text Structure and Looks

## Without HTML

* The host server's response contains:
    * _Status_ -- encodes whether the request was successful
    * _Headers_ -- e.g. to identify the content as text/html, audio, video etc.
    * _Body_ -- Webpage

This is what the text would look like without HTML:

```
Gmail Images Google UK Google Search I'M Feeling Lucky ...
```

Text alone is not enough - _what does it mean_?

## Hypertext Markup Language (HTML)

* HTML  is used to specify _meaning_:
     * `<tag> some text here </tag>`
     * `<tag ... />`

* Many tags, for example:
    * `<title>Google</title> -- the title`
    * `<h1>Google</h1>       -- very important`
    * `<h5>Google Search</h5>       -- not so important`

* We can also use HTML to add other _elements_:
    * `<img src='...'/> - an image`
    * `<a href='...'/>  - link to another page`
    * `<button ... />   - button`
    * `<text   ... />   - text input`
    * `<canvas .../>    - drawing area`


## HTML Example

```html
<html>
<head>
  <title>Awesome News Corp</title>
</head>
<body>
  <h1>Breaking News</h1>
  <h2>CubeSat Success</h2>
  <p>Imperial College successfully launched a CubeSat.
  Where it is, nobody knows...</p>
</body>
</html>
```

## HTML Example

TODO Screenshot of webpage

* HTML - _What does the text mean_?
* But, _what should it look like_?


## Cascading Style Sheets

### Cascading Style Sheets
We use Cascading Style Sheets (CSS) to tell
the user's browser what the page must look like.


## HTML Example Revisited

```html
<h1>Breaking News</h1>
<h2>CubeSat Success</h2>
<p>Imperial College successfully launched a CubeSat.</p>
<div class="branding"> News brought by ic-spy. </div>
```

CSS defines styling for pre-defined tags or for custom classes.

```css
h1 {
    color: orange;
    text-align: center;
}

.branding {
    font-family: "Times New Roman";
    font-size: 0.5em;
    color: gray;
}
```

## HTML Example Revisited

TODO Screenshot

* HTML - _What does the text mean_?
* CSS  - _what should it look like_?
* But, _how should the text behave_?

### JavaScript

We use JavaScript to tell the browser what the page should behave
like.


# JavaScript 101

## JavaScript Example

```html
<body onload="myfunction()">
<h1> Drawing example </h1>
<canvas id="myCanvas" width="200" height="100"> </canvas>

<script>
  function myfunction () {
    var canvas = document.getElementById("myCanvas");
    // Do something with the canvas
    alert("Hello!");
  }
</script>
</body>
```

## JavaScript Example
```html
<canvas id="myCanvas" width="200" height="100"> </canvas>
```

* JavaScript can be used to interact with the HTML _document_:

```JavaScript
var canvas = document.getElementById("myCanvas");
```

* `var` - defines a variable (something that changes)
* `canvas` - is the name of the variable
* `document` - refers to the HTML document containing the JS code
* `getElementById` - is a function (method) of the document; it
  returns the HTML element with the provided id


# Over to You

## Resources

* Very good collection of online tutorials for HTML, CSS, JS
     * `http://www.w3schools.com/`

* About the `canvas` object:
     * `http://www.w3schools.com/canvas/`
