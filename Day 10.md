# tenth Day 💻


## Introduction 

 Whenever there's a divergence
between what your brain thinks
is happening, and what the
computer does, that's where
bugs enter the code.



```javaScript
// ex

let x = 2;
++x;  // 3
// this means 
x = x +1

let x = "2"
++x; // should be 21
//But it's 3 because JS convert the sting into number so make it additional operation
```


## Types 

 "In JavaScript, everything 
is an object." 🤔
false
> 
>  Every thing can behave as an object



### Primitive Types ⚡️

- undefined
- string
- number
- boolean
- object
- symbol: in ES6 used for suto private keys
- bigInt (future): let x = 34n

function & arrays are a subtype of a object type

> - undefined • string • number • boolean • object • symbol • null • bigint (future)⇒Not
> - object • function • array ⇒ Objects

<br>

> ###  Note: 📌
> In JavaScript, variables
> don't have types,
> values do.

<br>

> ###  Notes: 💡📌
> 1. typeof: always return string
 > ```javaScript
>   typeof 5;          // "number"
>    typeof "hello";    // "string"
>    typeof true;       // "boolean"
>    typeof undefined;  // "undefined"
>    typeof null;       // "object" (a historical mistake in JavaScript)
>    typeof [];         // "object"
>    typeof {};         // "object"
>    typeof function() {// "function"
>   ```

> 2. function & arrays not types of the top level they are subtypes of object,
 but when using typeof array ⇒ object while function ⇒ function
> 3. type of null = object it is a bug in JS, if they try to correct it a lot of things will fail in the JS


### NaN: ✨ 
(Special Values)is the only value that is not equal to it self

#### Typy of NaN 🔥
NaN type is number (invalid number), because it cmoes from numeric operations


### is NaN method ✨☄️
```javaScript
isNan()
// evaluate any argument to number then check weather it's a Nan or not
Number.isNan()
// better than the previous

isNaN("Abeer")          // ✅ true
Number.isNaN("Abeer")   // ❌ false
```

### Object.is( , )
it’s a built-in checker

better way for checking equality (better than ===)


```javaScript
 /We might use -0 for directions in some applications in which the sign means direct.
-0 === 0                // ✅ true
Object.is(-0 ,0 )       // ❌ false
```

> ### Note: 📌
>  === failed in Nan & -0

### Excersie🔥💫

```javaScript
// TODO: define polyfill for `Object.is(..)`

if (!Object.is || true){   // to disaple the built in method & build my own
    Object.is = function ObjectIs(x,y){
        const xNegZero = isItNegZero(x)
        const yNegZero = isItNegZero(y)

        if (yNegZero || xNegZero ){
            return yNegZero && xNegZero
        }else if (isItNane(x) && isItNane(y)){
            return true
        }else {
            return x===y
        }

        function isItNegZero(v){
            return v===0 && (1/v)=== -Infinity
        }

        function isItNane(v){
            return v !==v
        }
    }
} 

// tests:
console.log(Object.is(42,42) === true);
console.log(Object.is("foo","foo") === true);
console.log(Object.is(false,false) === true);
console.log(Object.is(null,null) === true);
console.log(Object.is(undefined,undefined) === true);
console.log(Object.is(NaN,NaN) === true);
console.log(Object.is(-0,-0) === true);
console.log(Object.is(0,0) === true);

console.log(Object.is(-0,0) === false);
console.log(Object.is(0,-0) === false);
console.log(Object.is(0,NaN) === false);
console.log(Object.is(NaN,0) === false);
console.log(Object.is(42,"42") === false);
console.log(Object.is("42",42) === false);
console.log(Object.is("foo","bar") === false);
console.log(Object.is(false,true) === false);
console.log(Object.is(null,undefined) === false);
console.log(Object.is(undefined,null) === false);
```

<br>
<br>

## Coercion 🍃💡 
type conversion

### Abstract Operations: ToPrimitive🧐
#### .toString ()  🌟 

```javaScript
(null).toString()                  // "null"
undefined.toString()               // "undefined"
true.toString()                    // "true"
false.toString()                   // "false"
3.14159.toString()                 // "3.14159"
(0).toString()                     // "0"
(-0).toString()                    // "0"

([]).toString()                    // ""
[1, 2, 3].toString()               // "1,2,3"
[null, undefined].toString()       // ","
[[[], [], []], []].toString()      // ",,,"
([,,,,]).toString()                // ",,,"

{}      "[object Object]"
{a:2}   "[object Object]"
```


###  ToNumber 💎

```javaScript
// using Number(x)

""        // 0
"0"       // 0
"-0"      // -0
" 009 "   // 9
"3.14159" // 3.14159
"0."      // 0
".0"      // 0
"."       // NaN
"0xaf"    // 175 // consvert hexacecimal to decimal

false      // 0
true       // 1
null       // 0
undefined  // Nan

[""]        // 0
["0"]       // 0
["-0"]      // 0-
[null]      // 0
[undefined] // 0
[1,2,3]     // NaN
[[[[]]]]    // 0
{ .. }      // NaN
```

<br>

#### Why true & false shouldn’t convert to 1 & 0 

```javaScript
3 > 2 > 1
(true) > 1
1 > 1 // false !!!!
```

### ToBoolean()
```javaScript
// Falsy values:
“”
0, -0
null
NaN
false
undefined
//Anything eles will be truthy value
```


  
### Cases of coercion: 🌠

```javaScript
// coercions: 

// string concatenation calls toString method
"Sarah" + 15

` ${variable}`
// also use toString

`hh ${variable.toString()}
// implicit `coercion, primitive types don't have methods

//All of the above are implicit
// explicit 
String(variable)

```

