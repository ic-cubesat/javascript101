class: middle, center

# Introduction to Javascript
Imperial Cubesat, Software Engineering

---

# Goals
- **Part 1**: Web development 101
  - How does a webpage work?
  - What is HTML, CSS and Javascript
- **Part 2**: Introduction to Javascript
  - Basic syntax, writing functions.
  - Drawing on the HTML5 Canvas element

---
class: center

# How does a webpage work?

.half-slide.lfl.centered[
**Amazon 1995**
![amazon-1995](images/amazon-1995.jpg)
]
--
.half-slide.rfl.centered[
**Amazon 2015**
![amazon-2015](images/amazon-2015.jpg)
]

---

# How did a webpage work in 1995?

- A webpage is just a **static document** containing
formatted text, images and links to other webpages.
The contents of a webpage and how it should appear on the screen are described
in *HTML* and *CSS*.
--

  - A *client* requests a webpage from a *server* and maybe passes along
  some extra data using his web browser.
  This is done over *HTTP* (Hypertext Transfer Protocol).
  - The server generates the page depending on what the client sent,
  or just reads the webpage from a file.
  Then it trasmits the webpage back to client.
  - The client's web browser renders the webpage on the screen.
--

- The webpage is **completely static** in the sense that it does not change
after it has been loaded, can not interact with the user
or with external services.
--

- To achieve any kind of interactivity a new webpage must be requested
from the server each time the user wants for something to happen.
--

## .center.red[**Boring, not very useful!**]
---

### .left[Today:]

.half-slide.lfl[![spotify](images/spotify.png)]
.half-slide.rfl[![webgl-example](images/webgl-example.jpg)]
--

## .clear.center[Webpages are complete applications]
--
class: center
--

*Thanks to...*
--

# Javascript .red[❤]!

---

# How does a 2015 webpage work?
- **HTML**, or Hypertext Markup Language defines the contents of the page.
- **CSS**, or Cascading Style Sheet defines how these contents are displayed,
i.e. how the webpage looks.
- **Javascript** is a programming language that defines how the page behaves.
It interacts with the user, sends and receives data from a webserver,
modifies the HTML and CSS of the webpage and can even do things like 3D graphics.

.center[HTML and CSS are **.red[not]** programming languages.]

--

```html
<span class='centered'>
  HTML and CSS are <em>not</em> programming languages.
</span>
```

```css
.centered {
  text-align: center;
}

em {
  font-weight: bold;
  color: red;
}
```

---

# What is HTML?
* The standard markup language to create webpages, initially released in 1993.
* Is a series of HTLM elements consisting of tags, for example:
  * `<h1>CubeSat</h1>` - Header (title)
  * `<img src='images/tesla.jpg' alt='Tesla Model S' />` - an image
  * `<a href='https://cubesat.ic.ac.uk'>Imperial Cubesat</a>` - a link
* Good HTML defines content and gives meaning, but does not describe
how the webpage will look.
--

```html
<!DOCTYPE html>
<html>
<head>
  <title>Example HTML Page</title>
</head>
<body>
  <header class='main'>
    <h1>This is an example HTML page</h1>
  </header>
    <span class='acronym'>HTML</span> is <em>wonderful</em>.
    Here's a link to <a href='https://google.com'>google</a>
  </section>
</body>
</html>
```
---
# What is CSS?
* A stylesheet language introduced in 1995, used to define how
a webpage should look.
* Can be included directly in HTML `<style>` tags or referenced from an
external .css file
* Is a series of rules of the type *All header elements should be bold and red"

--

```css
h1 {
  font-style: Sans-serif;
  color: red;
  font-weight: bold;
}

* em.somestyleclass {
  font-style: italic;
  color: blue;
}
```

--

* We can specify IDs and classes for HTML elements, that we can then use
in stylesheets to define how they'll look.

```html
<em class='somestyleclass'> This will be italic and blue </em>
```

---

# What is Javascript?

* Javascript is a programming language introduced in 1995,
intended to be included in webpages. Javascript **can run inside the browser**
and all modern browsers support javascript.
* Like CSS, it can be included directly in an HTML `<script>` tag,
or referenced from a .js file.
* Dynamic, duck typing. Not really objected oriented, but
similar to OOP languages.

--

```javascript
function isPrime(x) {
  for(var i=2;i<x;i++) {
    if(x % i == 0) return false;
  }
  return true;
}
console.log([1, 2, 3, 4, 5, 6, 7, 8, 9, 10].map(isPrime));
```
--

### What Javascript isn't:
* A client-only programming language.
* .red[**Java**]. Java and javascript are completely unrelated.

---

class: middle, center
# A few more things about javascript

