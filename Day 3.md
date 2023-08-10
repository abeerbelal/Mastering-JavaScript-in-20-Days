# Third Day ✏️
<br>


## Arrays 🔥💫:
Arrays let us keep multiple values together in a single collection
` let synonyms = ["plethora", "array", "cornucopia"] `

- Arrays can be empty, or hold a single item
  ```javaScript
  let emptyArray = [];
  let oneItemArray = ["lonely"];
  ```

- Like strings, arrays have a length `synonyms.length`
- And each value has an index
   `synonyms[1]
synonyms.indexOf("cornucopia")`

- Also like strings, we can check if an array contains a certain value
  `synonyms.includes("plethora")
synonyms.includes("variety")`

- Unlike strings, we can modify arrays
```javaScript
synonyms[1] = "variety";
let lastItem = synonyms.pop();
synonyms.push("multitude");
```
- Arrays can hold any type of items, or mix and match! `let mixedArray = ["pop", 6, "squish", false, document];`
- Arrays can do lots of useful tricks!
  ```javaScript
  "Abeer" == ["Abeer"]      // ✅
  "Abeer" === ["Abeer"]     // ❌
  "Sarah" === ["Abeer"][0]  // ✅

  ["c", "a", "d", "b"].sort() // ['a', 'b', 'c']
  [100, 2,50].sort()   // [100, 2,50].sort()  //It converts the elements into strings and then sort them
 
  ["lions", "tigers", "bears oh!"].join(" & ") // 'lions & tigers & bears oh!' // convert it to a string
  [1 , 2].join("@")  // '1@2'

  [1, 2, 3].concat([4, 5, 6]) // [1, 2, 3, 4, 5, 6] 
  ```

 ###  Array.prototype.join()
 The join() method creates and returns a new string by concatenating all of the elements in this array, separated by commas or a 
 specified separator string. If the array has only one item, then that item will be returned without using the separator.
 ```javaScript
const elements = ['Fire', 'Air', 'Water'];

console.log(elements.join());
// Expected output: "Fire,Air,Water"

console.log(elements.join(''));
// Expected output: "FireAirWater"

console.log(elements.join('-'));
// Expected output: "Fire-Air-Water"
```

  ## Mutating data:
  In JS certian values behave differently than certian other values that we might think are similar
 ```javaScript
let abcArray = ["a", "b", "c"];
abcArray[1] = "d";
abcArray;  // ['a', 'd', 'c']

let abcString = "abc";
abcString[1] = "d";
abcString; // 'abc'
  ```

### mutable vs. immutable🍀:
*"Mutable"* data can be edited (e.g. Arrays)

*"Immutable"* data always stays the same (e.g. strings & other primitives)

Do these do the same thing?❓
```javaScript
let numbers1 = [1, 2, 3];
let result1 = numbers1.push(4); 
numbers1;  // [1, 2, 3, 4]
 
let numbers2 = [1, 2, 3];
let result2 = numbers2.concat([4]);
numbers2; // [1, 2, 3]
```
<br>

> ###  **See this** 💥
> Some actions "**mutate**" an array (e.g. `oldArray.push(newValue)`)
> aka(called) change the array ***in-place***
> Other actions **do** ***not* mutate** the original array, but instead create a new copy (e.g. `oldArray.concat(otherArray)`)


   <br>

### Variables themselves can also be (im)mutable 🌟 

```javaScript
let letVariable = "original value";
letVariable = "new value";

const constVariable = "original value";
constVariable = "new Value";
```
<br>

### Immutable variable with mutable value 💡
What happens when we use const with a mutable value like an array?
```javaScript
const operands = [4, 6];
const sum = operands[0] + operands[1]; //  10

operands[0] = 5;
const newSum = operands[0] + operands[1]; // 11
```

<br>
<br>

> ###  Advises:📌
> 1.  If you have the choice keep thing immutable
> 2.  The default for array is const unlees you have a good reson to use let      

<br>

### Copying an array: ✏️

```javaScript
let array1 = [1,2,3,4]
let array2= array1
array1[0]=5

array1 // [5,2,3,4]
array2 // [5,2,3,4]

// Even if I used const >> the same result
```

   <br>
   <br>

## **Objects:** 🌞
- Objects collect multiple values together to describe more complex data
- Similar to how we can point at different values using variables in our code,
- objects let us point at related values using properties in the object.
- We can access edit and add any property using "."
- everything in javascript not a primitive type it is an object e.g array is a special kind of object

```javaScript
const js = {
    name: "JavaScript",
    abbreviation: "JS",
    isAwesome: true,
    officialSpec: "ECMAScript",
    birthYear: 1995,
    learn:false
    creator: "Brendan Eich"
};
```
Getting property values:`js.name`

Edit  property `js.learn = true`

Using property values `js.name.startsWith("Java")  ,  let age = 2022 - js.birthYear;`

Setting property values
```javaScript
const indecisive = {
    lunch: "sandwich"
};
indecisive.lunch = "tacos";
indecisive.snack = "chips";
```

### Feezing an object: 🥶❄️:
trick in JS, to essentially freeze an object in place and make it **immutable**,
and never be able to change from how it was when it was declared.

```javaScript
const obj = {
  prop: 42,
};

Object.freeze(obj);

obj.prop = 33;
// Throws an error in strict mode

console.log(obj.prop);
// Expected output: 42
```

### Methods🌌✨:
Properties can point to functions too. We call function-properties "methods" on objectsCopy
```javaScript
const dog = {
    name: "Ein",
    breed: "Corgi",
    speak: function () {
        console.log("woof woof");
    }
}
dog.speak();
```
> ###  This:⚠️⚠️⚠️
> Its behavior is complicated & can be tricky
> A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between > strict mode and non-strict mode.
> In most cases, the value of this is determined by how a function is called (runtime binding). It can't be set by assignment during  
> execution, and it may be different each time the function is called. The bind() method can set the value of a function's this 
> regardless of how it's called, and arrow functions don't provide their own this binding (it retains the this value of the enclosing 
> lexical context).
```javaScript
const test = {
  prop: 42,
  func: function () {
    return this.prop;
  },
};

console.log(test.func());
// Expected output: 42
```

### Built in objects:🗝️
1. document
2. array
3. console : has methods : log, error 
4. Math
5. Function

   <br>
   <br>

   # Quiz solution:
 ```html
   <!DOCTYPE html>

<html lang="en-US"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    
    <title>Quiz.js</title>
    <style>
        body {
            margin: 1rem auto;
            padding: 3rem;
            font-family: sans-serif;
        }
        header {
            width: 50%;
            margin: 1em auto;
        }
        main {
            min-width: 25rem;
            max-width: 50%;
            margin: 0px auto;
            display:flex; 
            flex-direction: column;
        }
        #statement {
            border: 1px solid black;
            border-radius: 0.5rem;
            box-shadow: 5px 5px 5px gray;
            padding: 1rem;
            font-size: x-large;
            text-align: center;
            margin: 1rem 0px;
            min-height: 2em;
        }
        #explanation {
            padding: 1rem;
            text-align: center;
        }
        #options {
            width: 100%;
            display: flex;
            flex-direction: column;
        }
        button {
            padding: 0.5rem;
            font-size: medium;
            border-radius: 5px;
        }
        .correct {
            background-color: lightgreen;
        }
        .incorrect {
            background-color: lightpink;
        }
    </style>
  </head>
  <body>
    <header>
    <h1>Quiz.js</h1>
    <p>Do you know JS? Find out!</p>
    </header>

    <main>
    <div id="statement">
        
    </div>

    <div id="options">
        <button name="true" value="true">true</button>
        <button name="false" value="false">false</button>
    </div>

    <div id="explanation">

    </div>

    </main>

  

  <script type="text/javascript">


    // TODO 1: Declare & assign variables pointing to the corresponding element(s)
    // statement should be the "statement" div
    // optionButtons should be all the elements within the "options" div
    // explanation should be the "explanation" div

    const statement = document.getElementById("statement")
    const optionButtons = document.querySelector("#options").children
    const explanation = document.getElementById("explanation")


    // TODO 2: Declare & assign a variable called fact
    // Its value should be an object with a statement, true/false answer, and explanation 
    
    let fact = {
        statement : " 1 + 1 === 2",
        answer : true,
        explanation :  " the plus operation gives the sum of two numbers."
    }

    
    // TODO 3: Set the text of the statement element to the fact's statement

    statement.textContent= fact.statement

    // TODO 4: Declare disable & enable functions to set or remove the "disabled" attribute from a given button element
    // disable(button) should set the button element's attribute "disabled" to the value ""
    // enable(button) should remove the attribute "disabled" from the button element

    const disable = button =>{
        button.setAttribute("disabled","")
    }

    const enable = button =>{
         button.removeAttribute("disabled")
    }


    // TODO 5: Declare an isCorrect function that compares a guess to the right answer
    // isCorrect(guess) should return true if the guess matches the fact's answer
    
    const isCorrect = guess =>{ return guess === fact.answer.toString()}


    // TODO 6A: Use a for loop to add a click event listener to each of the optionButtons
    for (let b of optionButtons){
        b.addEventListener("click", event =>{
            
        
    
            // TODO 6B: Within the event handler function, display the fact's explanation by setting the text of the explanation element
            
            explanation.textContent = fact.explanation

            // TODO 7: Within the event handler function, 
            // Use a for loop to disable all the option buttons

            for (let allB of optionButtons)
                disable(allB)
        

            // TODO 8: Within the event handler function,
            // Get the guessed value from the clicked button
            // Use a conditional to compare the guess to the fact's answer
            // and add the "correct"/"incorrect" class as appropriate

            if (isCorrect(b.value)){
                b.classList.add("correct")
            }else{
                b.classList.add("incorrect")
            }

        })
    }
    

  </script>

</body></html>
 ```







