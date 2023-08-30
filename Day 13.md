# What is TypeScript?

TypeScript is an open source, typed syntactic superset of JavaScript
- Compiles to readable JS
- Three parts: Language, Language Server and Compiler
- Kind of like a fancy linter

#### Why developers want types
It allows you, as a code author, to leave more of your intent “on the page”

This kind of intent is often missing from JS code. For example:
```javaScript
function add(a, b) {
  return a + b
}
```

Is this meant to take numbers as args? strings? both?

What if someone who interpreted a and b as numbers made this “backwards-compatible change?”

```javaScript
function add(a, b, c = 0) {
  return a + b + c
}
```

We’re headed for trouble if we decided to pass strings in for `a` and `b`!

Types make the author’s intent more clear
```javaScript
function add(a: number, b: number): number {
  return a + b
}
add(3, "4")
Argument of type 'string' is not assignable to parameter of type 'number'.
```

It has the potential to move some kinds of errors from runtime to compile time 1

Examples:

- Values that are potentially absent (null or undefined)
- Incomplete refactoring
- Breakage around internal code contracts (e.g., an argument becomes required)

### Variables and Values


In JavaScript we declare variables all the time with let and const like this:
```
let age = 6
    
let age: number
```
As we can see, `TypeScript` is able to infer that age is a number, based on the fact that we’re initializing it with a value as we are declaring it.
If we try to give age a value that is incompatible with number, we get an error

```javaScript
let age = 6
age = "not a number"
//Type 'string' is not assignable to type 'number'.
```
**In TypeScript, variables are “born” with their types.** Although there are ways of making them more specific in certain branches of code, there’s no (safe) way of changing age’s type from number to string

### Literal Types

The type `6` is called **a literal type**. If our `let` declaration is a variable that can hold `any number`, the `const` declaration is one that can hold `only 6` — a specific number.

>  Theme: Inferring with safe specificity
>
> 
> There’s a common idea you’ll see again and again when working with TypeScript. Inference is not so specific as to get in the way of 
> common behavior.

> For example, the let variable declaration above could have assumed age to be of type 6, but this would have interfered with our ability 
> to set this re-assignable variable to 7 or 8.

#### Implicit any and type annotations
Sometimes, we need to declare a variable before it gets initialized, like endTime below:
```javaScript
// between 500 and 1000
const RANDOM_WAIT_TIME =
  Math.round(Math.random() * 500) + 500
 
let startTime = new Date()
let endTime
      
let endTime: any
 
setTimeout(() => {
  endTime = 0
  endTime = new Date()
}, RANDOM_WAIT_TIME)
```
`endTime` is “born” without a type, so it ends up being an implicit `any`.

TypeScript doesn’t have enough information around the declaration site to infer what endTime should be, so it gets **the most flexible type: any.**

Think of `any` as “the normal way JS variables work”, in that you could assign `endTime` to a `number`, then later a `function`, then a `string`.

If we wanted more safety here, we could add a type annotation:
```javaScript
// between 500 and 1000
const RANDOM_WAIT_TIME =
  Math.round(Math.random() * 500) + 500
 
let startTime = new Date()
let endTime: Date
      
//let endTime: Date
 
setTimeout(() => {
  endTime = 0
//Type 'number' is not assignable to type 'Date'.
  endTime = new Date()
}, RANDOM_WAIT_TIME)
```

### Function arguments and return values
The` : foo` syntax we’ve just seen for variable type annotations can also be used to describe function arguments and return values. In this example it’s not clear, even from the implementation of the function, whether add should accept numbers or strings.


```javaScript
function add(a, b) {
  return a + b // strings? numbers? a mix?
}
```

Here’s what your in-editor tooltip would look like if you were using this function:

```javaScript
const result = add(3, "4")
               
//function add(a: any, b: any): any
result
  
//const result: any
```

Without type annotations, “anything goes” for the arguments passed into add. Why is this a problem?
```javaScript
const result = add(3, "4")
const p = new Promise(result)
                        
//const result: any
```
If you’ve ever created a `Promise` using the promise constructor, you may see that we are using a `string` where we should use a two-argument function. This is the kind of thing we’d hope that TypeScript could catch for us.

Without type annotations, “anything goes” for the arguments passed into `add`. Why is this a problem?

Let’s add some type annotations to our function’s arguments
```javaScript
function add(a: number, b: number) {
  return a + b
}
const result = add(3, "4")
//Argument of type 'string' is not assignable to parameter of type 'number'.
```
Great, now we can enforce that only values of type number are passed into the function, and TS can now determine the return type automatically:
```javaScript
function add(a: number, b: number) {
  return a + b
}
const result = add(3, 4)
               
//function add(a: number, b: number): number
```
If we wanted to specifically state a return type, we could do so using the `:foo` syntax in one more place
```javaScript
function add(a: number, b: number): number {}
//A function whose declared type is neither 'void' nor 'any' must return a value.
```

This is a great way for code authors to state their intentions up-front. TypeScript will make sure that we live up to this intention, and errors will be surfaced at the location of the function declaration instead of where we use the value returned by the function.


### Objects

We can use this type with a variable using the same : foo notation we’ve already discussed!
```javaScript
let car: {
  make: string
  model: string
  year: number
}
```
We could create a function to print values of this type to the console:

```javaScript
function printCar(car: {
  make: string
  model: string
  year: number
}) {
  console.log(`${car.make} ${car.model} (${car.year})`)
}
```

