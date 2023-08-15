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

JavaScript is:

- Single-threaded (one command runs at a time)
- Synchronously executed (each line is run in order the code appears)

<br>


```javaScript
function printHello() { console.log("Hello"); }
function blockFor1Sec() {
    setTimeout(()=>{console.log("1 sec");},1000) //3
    //blocks in the JavaScript thread for 1 sec
}

setTimeout(printHello, 0);//2
blockFor1Sec()
console.log("Me first!"); //1

```
> ### Note: 💡
> setTimeOut doesn't do anything in JS it has consequences in the web browser

#### JavaScript is not enough We need new pieces (some of which aren’t JavaScript at all) 💫

### Our core JavaScript engine has 3 main parts: 🔥

- Thread of execution
- Memory/variable environment
- Call stack

<br>

### We need to add some new components:  ⚡️🔥

- Browser APIs/Node background APIs
- Promises
- Event loop, Callback/Task queue and micro task queue

```javaScript
setTimeout(()=>console.log("Hello"), 0);

for (let i=0; i<100; i++)
    console.log("Me first!");

//for loop makes block for the execution, when finish the loop will print Hello
```



```javaScript
function setTime() {
    setTimeout(()=>{console.log("Hello")},4000)}

for (let i=0; i<5; i++)
    setTime()

console.log("Finally");

// Finally then Hello 
```

### Event Loop ➰🔥🔥
have asynchronous capabilities. It's responsible for handling and managing asynchronous operations in a non-blocking manner, allowing programs to perform tasks like responding to user input, fetching data from servers, and more, without freezing up the entire application.
```javaScript
console.log('Start');

setTimeout(() => {
    console.log('Timeout 1');
}, 0);

Promise.resolve().then(() => {
    console.log('Promise 1');
});

console.log('End');

 /* the output:=>
Start
End
Promise 1
Timeout 1
*/

```
## Promises ☄️🌘

Special objects built into JavaScript that get returned immediately when we make 
a call to a web browser API/feature (e.g. fetch) that’s set up to return promises 
(not all are)
Promises act as a placeholder for the data we expect to get back from the web 
browser feature’s background work.

#### A Promise is in one of these states:

- *pending*: initial state, neither fulfilled nor rejected.
- *fulfilled:* meaning that the operation was completed successfully.
- *rejected:* meaning that the operation failed.

#### promises object contains
 1. value 
 2. fulfilled: Array
 Any function I want to apply after fetching the data should be in the
 fulfilled array, but I don't have access to it, so .then do that
 In other words a function that automatically run when the data comes.


 **then** method and functionality to call on completion 💻🔥

```javaScript
- Any code we want to run on the returned data must also be saved on the promise
object
- Added using .then method to the hidden property ‘onFulfilment’
- Promise objects will automatically trigger the attached function to run (with its
input being the returned data
```

###  Order of execution: 👩🏻‍💻
We have three things to organize the execution:

1. **call stack**
2. **callback queue**
3. **micro queue**
 
> ### Note: ⏳
> When all the global code finished running and thers is nothing in the call stack 
> the queues is going to be checked (micro queue is the first)



```javaScript
function display(data){console.log(data)}
function printHello(){console.log("Hello");}
function blockFor300ms(){/* blocks js thread for 300ms */ }


const futureData = fetch('https://twitter.com/will/tweets/1')
futureData.then(display)
setTimeout(printHello, 0); 
// when the time finish the callback will be sent to callback queue
blockFor300ms()
console.log("Me first!");

// micro queu: display
// callback queue: printHello

/*
	Me first!
  Hello
  Response {type: 'cors', url: 'https://dummyjson.com/quotes', ...}
*/
```
