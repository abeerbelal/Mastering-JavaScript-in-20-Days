# sixth Day ✨

## Data Fetching & Promises 🎯✨🎀

**APIs** "applications programming interface" provide URLs that point at data we care about
```javaScript
https://dog.ceo/api/breed/hound/list
  {
    "message": [
      "afghan",
      "basset",
      "blood",
      "english",
      "ibizan",
      "plott",
      "walker"
    ],
    "status": "success"
  }
```
**fetch()** lets us use JS to load data from APIs ` fetch("https://dog.ceo/api/breed/hound/list")`
>  ### JSON 📎🧷
> is a standard text-based format for representing structured data based on JavaScript object syntax.
>  It is commonly used for transmitting data in web applications


## Promises:💣

It takes time to fetch data from the network, So JS writes us an "IOU" for the data value it doesn't have yet aka a **Promise** of a value
```javaScript
>> fetch("https://dog.ceo/api/breed/hound/list")
Promise { <state>: "pending" }
```

Promises can be in 3 possible **states**:
- **pending**: still waiting for the value, hang tight
- **fulfilled** (aka "resolved"): finally got the value, all done
- **rejected**: sorry couldn't get the value, all done, It takes time for Promises to resolve, so they are "asynchronous"

### await
**await** lets us tell JS to stop and wait for an asynchronous operation to finish

> In the case of a Promise, it waits for it to resolve before continuing with our code
> ```javaScript
> let response = await fetch("https://dog.ceo/api/breed/hound/list");
>   console.log(response);
> ```
 The Promise we get from fetch() resolves to a Response object
 It's body contains the data we care about

 Calling the **.json()** method on the response parses its body as a JSON object `response.json()`
  awaiting the JSON Promise too, because .json()returnspromises
  ```javaScript
let response = await fetch("https://dog.ceo/api/breed/hound/list");
let body = await response.json();
```

## Destructuring 🦄 ⏳
is a fancy way of declaring multiple variables at once
By "extracting" values from an object with their property names `let {name, nickname} = spices[0];`
- If we only care about some of the properties, we can omit the others`let {nickname} = spices[2];`
- We can also destructure Arrays, assigning variables for their items`const [baby, ginger, scary, sporty, posh] = spices;`
- We can ignore the values in the array we don't need use commas to "skip" values`const [,,melB] = spices;`
- use ... to collect remaining values`const [babySpice, ...adultSpices] = spices;`
### Exercise: 👩🏻‍💻
```javaScript
let a, b, rest;
[a, b] = [10, 20];
console.log(a);
// Expected output: 10
console.log(b);
// Expected output: 20
[a, b, ...rest] = [10, 20, 30, 40, 50];
console.log(rest);
// Expected output: Array [30, 40, 50]
```
## async functions 🔥🔥💪

If we try to await something in a regular function...
```javaScript
⭕⭕⭕⭕⭕⭕XX JS doesn't allow it
function fetchResponse(url) {
    const response = await fetch(url);
    return response;
}
```
We need to make it an async function. This tells JS to expect to await async operations inside the function
```javaScript
async function fetchResponse(url) {
    const response = await fetch(url);
    return response;
}
```

### Modules🍃🔥
 let us split big codebases across multiple files


 ```javaScript
<script type="module">
    //...
</script>
```
 JS modules work **differently** from JS scripts
1. One difference is that we can't use await outside of a function in a script
```javaScript
<script>
    await fetch("https://dog.ceo/api/breed/hound/list");
</script>
```
2. Module scope
modules create their own scope, Try loading the page and accessing the BREEDS variable we declare in the module

### import && export
- **export** lets us expose variables from our module's scope to the outside world
- **import** lets us use an exposed variable from another module

## Debugging: ✏️📋
We can console.log() (or .warn() or .error()) is one way to understand what's happening when your program runs

```javaScript
function whyIsntThisWorking(input) {
    console.log("Well at least we got this far");
    console.log(input);
    return thingThatDoesntWork(input);
}
```

You can also use the browser's debugger to pause JS and inspect what's happening

```javaScript
function whyIsntThisWorking(input) {
    debugger;
    return thingThatDoesntWork(input);
}
```
The debugger statement creates a breakpoint where JS will pause and let you look around

## Error handling 🔥🌠
Once we've discovered where in our program an error is likely, we can do something about it!
Usually errors will cause JS to stop running our code
  
**try** lets us "watch out" for potential errors
its friend **catch** lets us manage errors when they occur
```javaScript
try {
    thisMightThrowAnError();
} catch (error) {
    console.error("As if! Error:", error); 
    console.log("Whatever, let's press on anyway");
}
console.log("still rollin' with the homies");
```
