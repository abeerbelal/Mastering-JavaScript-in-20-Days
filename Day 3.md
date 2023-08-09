# Third Day ✏️
<br>


## Arrays 🔥💫:
Arrays let us keep multiple values together in a single collection
` let synonyms = ["plethora", "array", "cornucopia"] `

- Arrays can be empty, or hold a single item
  ```
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
```
synonyms[1] = "variety";
let lastItem = synonyms.pop();
synonyms.push("multitude");
```
- Arrays can hold any type of items, or mix and match! `let mixedArray = ["pop", 6, "squish", false, document];`
- Arrays can do lots of useful tricks!
  ```
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
 ```
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
 ```
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
```
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

```
let letVariable = "original value";
letVariable = "new value";

const constVariable = "original value";
constVariable = "new Value";
```
<br>

### Immutable variable with mutable value 💡
What happens when we use const with a mutable value like an array?
```
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

```
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

```
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
```
const indecisive = {
    lunch: "sandwich"
};
indecisive.lunch = "tacos";
indecisive.snack = "chips";
```

### Feezing an object: 🥶❄️:
trick in JS, to essentially freeze an object in place and make it **immutable**,
and never be able to change from how it was when it was declared.

```
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
```
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
```
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







