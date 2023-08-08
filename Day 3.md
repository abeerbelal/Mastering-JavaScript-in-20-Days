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

  ## Mutating data:
  





