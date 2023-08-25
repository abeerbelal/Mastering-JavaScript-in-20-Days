# Twelfth day 📝


## Advanced Scope 🎨:

### lexical scope 

The idea is that a compiler figures out all the scopes ahead of time before being executed 

lex → the first stage of parsing

- The scope of a variable is determined by its location in the source code where it's defined.
- The scope of a variable is fixed at the time of code compilation and remains the same throughout the program's execution

<br>

### lexical scope VS. dynamic scope  ⚡️

The scope of **dynamic scope** is determined based on a runtime condition (where this function has been called).


- Dynamic scope is determined by the flow of control during program execution.
- The scope of a variable is based on where a function is called, not where it's defined in the source code.
- The scope of a variable can change at runtime, depending on how functions are called

while **lexical scope** is determined at another time.

```javaScript
const n = "Abeer"

function f(){
    console.log(n)
}

function ff(){
    const n = " Hello"
    f()
}

ff()
// Abeer => lexical
// Hello => dynamic
```

<br>

## Function Scoping 🍄

> ### Principle of privilege:📌
> You  should default to keep everything private and only expose the minimal necessary

<br>

```javaScript
let x
try {
    x = funMayReturnError(1)
}
catch (error) {
    x = 5
}

// using anaymaous function 
let x = (function bringX() {
    try {
        return funMayReturnError(1)
    }
    catch (error) {
        return 5
    }
})
```

<br>

### IIFE (Immediately Invoked Function Expression) 💭
It's a design pattern in JavaScript that involves defining and executing a function expression immediately after its creation. The IIFE pattern is often used to create a private scope for variables and avoid polluting the global scope with unnecessary identifiers.

```javaScript
function f (){
    console.log("hello")
}
f()

// we can do
//Also it may not have a name
(function  ff (){    // not a function declaration
    console.log("hello")
})()
```

<br>

### Block Scoping 🧱


> ### Note:💡
> Block(curly braces) are not scope until they have let or const inside them

<br>

### Hoisting ✨⚡️
- **Hoisting** is the process of moving variable and function declarations to the top of their scope.
- Variable declarations are hoisted but not their assignments. They are accessible but have an initial value of `undefined`.
- Function declarations are also hoisted, allowing them to be called before they are defined.
- Hoisting does not apply to function expressions, arrow functions, or variables declared with `let` or `const`.

<br>


```javaScript
var t = "1"
o()

function o(){
    console.log(t)
    var t = "2"
}
o() //undefined
```

   <br>
   <br>
   
### let & hoisting ✨☄️ 
We can’t say that let doesn't have hoisting, instead it’s kind of uninitialized state

```javaScript
var t = "1"

{
    console.log(t)
    let t = "2"
}

// error
// but should print 1, because it's in the outer scope, 
```


