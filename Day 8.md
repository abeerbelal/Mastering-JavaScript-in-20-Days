# eighth Day 🚀

## Closure 🔥💫
**Q:**
is Closure means that a function returns a function?🤔🤔🤔

➡️➡️Yes, closure refers to a situation where a function "closes over" its surrounding lexical scope, retaining access to the variables and parameters of that outer scope even after the outer function has finished executing. This often results in the function returning from within another function.
In simpler terms, a closure occurs when a function is defined within another function and it captures the variables from the outer function's scope, allowing those variables to persist even after the outer function has completed execution
 ```javaScript
function createFunction() {
	 function multiplyBy2 (num){
		  return num*2;
	 }
	 return multiplyBy2;
}
const generatedFunc = createFunction();
const result = generatedFunc(3); // 6

```
### backpack 👏
The way I will always remember closures is through the backpack analogy. When a function gets created and passed around or returned from another function, it carries a backpack with it. And in the backpack are all the variables that were in scope when the function was declared.

> #### Note:🔍
> [this is a very good reference](https://medium.com/dailyjs/i-never-understood-javascript-closures-9663703368e8) 🚀🚀


### What can we call this ‘backpack’? 🧐
* Closed Over `Variable Environment` (C.O.V.E.)
* Persistent Lexical Scope Referenced Data (P.L.S.R.D.)
* `Backpack`
* `Closure`


> #### 💡 Note :
> * Closure gives our functions persistent memories and an entirely new toolkit for writing professional code
> * **reduceRight:** Make cumulative operations in reverse order


### Practical Applications:  🌟 

1. **Helper functions:** Everyday professional helper functions like ‘once’ and ‘memoize’
2. **Iterators and generators:** These use lexical scoping and closure to achieve the
most contemporary patterns for handling data in JavaScript
3. **Module pattern:** Preserve state for the life of an application without polluting the
global namespace
4. **Asynchronous JavaScript:** Callbacks and Promises rely on closure to persist state
in an asynchronous environment


## Asynchronous JavaScript 🎯🚀

