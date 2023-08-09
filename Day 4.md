# Forth Day ✨

## Functions 🔥:
 values are things, variables point to things, **functions** do things.

 ### declaring (creating) a function:
 ```
function half(x) {
    return x / 2;
}
```
### calling (using) a function: `const one = half(2);`
 ### Parameters & Arguments:
 Some functions need more than one value to work
 ```
function add(x, y) {
    return x + y;
}
add(2,3);
```
### Some functions don't even need any values :
called void functions
```
function getRandomNumber() {
    return Math.random();
}
getRandomNumber();
```
- parameters are the inputs a function expects,
- arguments are the actual values the function is called with,
- Parameters should be named like variables, and behave like variables within the function body
- JS is pretty "loosey-goosey" about missing/extra arguments`getRandomNumber("unexpected")`it will give result
```
function add3(x, y, z) {
    console.log("My parameters are named x, y, z");
    console.log("I received the arguments", x, y, z);
    return x + y + z;
}
const sum = add3(4,5,6);
```
