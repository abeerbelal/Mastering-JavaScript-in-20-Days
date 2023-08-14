#  seventh Day 💎


## JavaScript Principles  🎯🚀 
When JavaScript code runs, it:

1. Goes through the code line-by-line and runs/ ’executes’ each line - known as the **thread of execution**
2. Saves ‘data’ like strings and arrays so we can use that data later - in its memory. We can even save code (‘functions’)

**Execution context:**
Created to run the code of a 
function - has 2 parts (we’ve 
already seen them!)
- Thread of execution
- Memory

Call stack: 🔅
  is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function
**JavaScript keeps track of what function is currently running (where’s the thread of execution)**

e.g:
When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.


Run a function - add to call stack
Finish running the function - JS removes it from call stack
Whatever is top of the call stack - that’s the function we’re currently running

## Generalizing functions ✨🪀
In our code we it is more readable and usable to make it follow the DRY "don't repeat yourself" concept, and avoid repetition
We can generalize the function to make it reusable, we use parameters to apply this principle
‘Parameters’ (placeholders) mean we don’t need to decide what data to run our 
functionality on until we run the function 
- Then provide an actual value (‘argument’) when we run the function

## First class objects🤔

Functions in javascript = first-class objects
They can co-exist with and can be treated like any other javascript object
1. Assigned to variables and properties of other objects
2. Passed as arguments into functions
3. Returned as values from functions


### Higher Order Function VS callback function✨☄️:

| Term                   | Explanation                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Callback Function      | The function we insert and pass as an argument. It's the function that will be called later when certain conditions are met. |
| Higher-Order Function  | The outer function that accepts another function as an argument. It's a function that can manipulate or use the passed callback function. |



