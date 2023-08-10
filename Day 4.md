# Forth Day ✨

## Functions 🔥:
 values are things, variables point to things, **functions** do things.

 ### declaring (creating) a function:
 ```javaScript
function half(x) {
    return x / 2;
}
```
### calling (using) a function: `const one = half(2);`
 ### Parameters & Arguments:
 Some functions need more than one value to work
 ```javaScript
function add(x, y) {
    return x + y;
}
add(2,3);
```
### Some functions don't even need any values :📌
called void functions
```javaScript
function getRandomNumber() {
    return Math.random();
}
getRandomNumber();
```
- parameters are the inputs a function expects,
- arguments are the actual values the function is called with,
- Parameters should be named like variables, and behave like variables within the function body
- JS is pretty "loosey-goosey" about missing/extra arguments`getRandomNumber("unexpected")`it will give result
```javaScript
function add3(x, y, z) {
    console.log("My parameters are named x, y, z");
    console.log("I received the arguments", x, y, z);
    return x + y + z;
}
const sum = add3(4,5,6);
```
### Arrow functions:➡️
The => "fat arrow" lets us create an unnamed function without much code aka an arrow function `(x, y) => x + y`

### setAttribute() & removeAttribute() methods 📋✏️📌
`setAttribute :` Sets the value of an attribute on the specified element. If the attribute already exists, the value is updated; otherwise a new attribute is added with the specified name and value.

```


setAttribute(name, value)
```
 `removeAttribute:` removes the attribute with the specified name from the element.
 ```
removeAttribute(attrName)
```

### Scope:
In JS it doesn't just matter what variables we declare, It also matters where we declare them, Scope determines where variables are "in play".

```javaScript
function declareBankruptcy() {
    let bankruptcy = true;
}
declareBankruptcy();
console.log(bankruptcy);
```

- Scopes are nested within the program
- The widest scope is the global scope
- Each function gets its own new scope within the scope where it was declared
- Within each scope, you can access variables declared in a wider scope (e.g. global scope)
   But not those declared in a narrower scope (e.g. function scope)
```javaScript
let globalVariable = "I live in global scope"; 
function narrowerScope() {
    console.log(globalVariable);
    let localVariable = "I live in the function scope";
}
narrowerScope();
console.log(localVariable);
```
> Variables declared with let can be modified from within a narrower scope
> This can be useful, but also dangerous!
 ```javaScript
 let feeling = "free";
function trap() {
    feeling = "boxedIn";
}
trap();
console.log(feeling); //boxedIn
 ```

## Events & Handlers:
- The web browser fires events when certain things happen on the page
For example, when the user clicks somewhere on the page, a click event is fired
- We can detect events with JS using an event listener
The `.addEventListener()` method lets us listen for events on a DOM element

```javaScript
 .addEventListener() takes 2 parameters:
- The name of the event to listen to (e.g. "click")
- A handler function that JS calls when that event is fired on this element

document.addEventListener("click", () => {
    console.log("clicked")
});
```
JS passes an event object to the handler function with information about the event
If we accept this as a parameter, we can use it to get details
```
document.addEventListener("click", (event) => {
    console.log(event);
});
```

### event.target: ✨⚡️
Is the element the event fired on (in this case, which element was clicked)
```javaScript
document.addEventListener("click", (event) => {
    console.log(event.target);
});
```
<br>

### Some events: 💻🔥
1. **["click"](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)**
2. **["dblclick"](https://developer.mozilla.org/en-US/docs/Web/API/Element/dblclick_event)** 
3. [**"mouseover"**](https://developer.mozilla.org/en-US/docs/Web/API/Element/mouseover_event)
4. [**"mouseout"**](https://developer.mozilla.org/en-US/docs/Web/API/Element/mouseout_event)


```javaScript
let b = document.getElementsByName("true")[0]
b.addEventListener("mouseover", () => {
    console.log("The carser is in the button")
});

b.addEventListener("mouseout", () => {
    console.log("The carser is out the button")
});
```


