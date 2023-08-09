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

