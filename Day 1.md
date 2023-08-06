# first day 💎🔥
 <br>
  
## Intoduction 💻 📋 📓

js is a programming language, lang of web, it helps websites to do things, modify and interact with HTML. It makes browser live.
- Created in 1995(Brendan Eich)
- we can run js in:
   - the browser
   - the server
   - embedded devices
 
We write JavaScript in:
1. The browser's js  console
2. local text editor e.g Vs code
3. online playground e.g codepen 
<br>

## DOM (Document Object Model) ✨
It's the tree of HTML document, structure of the page.

- document: represent the entire HTML document
- document.title: represent the page (document) title
- document.body: represent the body element

### Finding elements in web page:
here's a summary of some  different ways to find elements in the (DOM) using JavaScript
- `document.body.children`: all the elements within the body
- getElementById(): Finds an element by its unique ID attribute
  `
  document.getElementById("board");
  `
- querySelector(): Selects the first element that matches a CSS selector
  `
  document.querySelector("#board")
  `
- querySelectorAll(): Returns a NodeList containing all elements that match a CSS selector
   `
  document.querySelectorAll("h1")
  `
- getElementsByClassName(): Retrieves a collection of elements with the specified class name.
`
document.getElementsByClassName("player")
`
- `document.getElementsByClassName("player").length` the number of elements with class="player".
- ` document.getElementById("p1-name").textContent ` the text inside the element with id="p1-name".



### Editing the DOM with js:
these changes not persistent, because if i reload the page it's going to be different.

- ` document.title = "My Page"` change the page title, note the double-quotes.
- ` document.getElementById("p1-name").textContent = "Sofia" ` replace the text of the #p1-name element
- ` document.getElementById("p1-name").append(" & friends") ` add to the end of the element's current text.
  





