#  challenges 🔥🚀
<br>

##  Before I got access to FrontendMasters courses, I started my journey 💻📚🔍
<br>

## Coding Exercises for 3 challenges 🔥💻🚀
1. [Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)

   My Solution💻:
```javaScript
let a = 25;
let b = 36;
let c = 46;

a *= 5;
b *= 3;
c *= 10;
console.log(a,b,c);

```


2. [Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

      My Solution💻:
```javaScript
let myStr = "This is the first sentence. ";
myStr +="This is the second sentence.";

console.log(myStr);

```

3. [Use Bracket Notation to Find the Nth-to-Last Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)

      My Solution💻:
```javaScript
const lastName = "Lovelace";

const secondToLastLetterOfLastName = lastName[lastName.length - 2];

console.log(secondToLastLetterOfLastName);

```

<br>
<br>
<br>

4. [qustions about what is the output and why](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week1%20-%20javascript-from-first-steps-to-professional/day%202/tasks.md)
   

  My Solution💻 1:
```javaScript
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b); // the output => true, because  the == operator for comparison, type coercion can occur.
console.log(b === c);// the output => false, because the === operator performs a strict equality comparison without type coercio
console.log(!!d);// the output => true, because (double negation) operator is used to convert a value to its boolean representation
```

  My Solution💻 2:
 ```javaScript
  console.log(4 + 5 * "7"); the output =>39

```
5 * "7" evaluates to 35 because the string "7" is coerced to the number 7.
4 + 35 evaluates to 39

  My Solution💻 3:
```javaScript
let result = 5 + 2 * 3 - 1;the output =>10 
```
JavaScript follows a specific order of operations, (*) has higher precedence than addition (+) and subtraction (-). So, the multiplication operation is performed first.then addition then subtraction.

  My Solution💻 4:
```javaScript
let x = 10;
let y = '10';
console.log(x == y); Output: true,
console.log(x === y);Output: false,
```
The == operator performs type coercion before making the comparison.
The === operator performs a strict equality comparison without type coercion.
variable x has the value 10 (a number), and the variable y has the value '10' (a string).

 My Solution💻 5:
 ```javaScript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result); //true
```
 The expression num > 10 compares the value of num with 10. Since num is a string ("15"), JavaScript will perform a lexicographic (string) comparison.Both operands are true, so the logical AND operation results in true.The string "15" is not lexicographically less than the number 0, so this comparison is false.One operand is true, so the logical OR operation results in true.

 
<br>
<br>
<br>

5. [Copy Array Items Using slice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)

      My Solution💻:
```javaScript
function forecast(arr) {
  return arr.slice(2,4);
}
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));

```
6. [Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)

      My Solution💻:
```

```

7. [Write Reusable JavaScript with Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)


      My Solution💻:
```javaScript
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ["learning",...fragment, "is", "fun"]
  return sentence;
}

console.log(spreadOut());

```
8. [Understanding Undefined Value returned from a Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-undefined-value-returned-from-a-function)


      My Solution💻:
```javaScript
// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}
function addFive() {
  sum = sum + 5;
}

addThree();
addFive();

```

9. [Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)


      My Solution💻:
```javaScript
function timesFive(num) {
  return num *5;
}

const answer = timesFive(5);
console.log(answer)


```

10. [Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions).

      My Solution💻:
```javaScript
let myGlobal = 10;

function fun1() {
 oopsGlobal = 5;

}

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}

```
11. [Local Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions).

      My Solution💻:
```javaScript
function myLocalScope() {
 let myVar = "foo";
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);

```
12. [Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions).

      My Solution💻:
```javaScript
const outerWear = "T-Shirt";

function myOutfit() {
const outerWear = "sweater";
  return outerWear;
}

console.log(myOutfit());//sweater
console.log(outerWear);//T-Shirt

```
13. [Stand in Line](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/stand-in-line)

      My Solution💻:
```javaScript
function nextInLine(arr, item) {
  arr.push(item);
  
  return arr.shift();
  
}

let testArr = [1, 2, 3, 4, 5];

console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));

```
14. [Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)

      My Solution💻:
```javaScript
function checkSign(num) {
  return (num > 0) ? "positive" : (num < 0) ? "negative " : "zero";

}

console.log(checkSign(10));
console.log(checkSign(0));
console.log(checkSign(-2));

```
15. [Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)

      My Solution💻:
```javaScript
function checkSign(num) {
  return (num > 0) ? "positive" : (num < 0) ? "negative" : "zero";
}

console.log(checkSign(10));
console.log(checkSign(0));
console.log(checkSign(-2));

```
16. [Use the filter Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array)

      My Solution💻:
```javaScript
const filteredList = watchList
  .filter(movie => parseFloat(movie.imdbRating) > 8.0)
  .map(movie => {
    return {
      title: movie.Title,
      rating: movie.imdbRating
    };
  });

console.log(filteredList);


```
17. [Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)

      My Solution💻:
    
```javaScript
function golfScore(par, strokes) {
  const names  = [
    "Hole-in-one!",
    "Eagle",
    "Birdie",
    "Par",
    "Bogey",
    "Double Bogey",
    "Go Home!"
  ];

  if (strokes === 1) {
    return names [0];
  } else if (strokes <= par - 2) {
    return names [1];
  } else if (strokes === par - 1) {
    return names [2];
  } else if (strokes === par) {
    return names [3];
  } else if (strokes === par + 1) {
    return names [4];
  } else if (strokes === par + 2) {
    return names [5];
  } else {
    return names [6];
  }
}

// Test cases
console.log(golfScore(4, 1)); // Output: "Hole-in-one!"
console.log(golfScore(4, 2)); // Output: "Eagle"

```

18. [ricky&mortyTask](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week1%20-%20javascript-from-first-steps-to-professional/day%206/task.md)

      My Solution💻:
```javaScript

```
19. [Use Higher-Order Functions map, filter, or reduce to Solve a Complex Proble](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)

      My Solution💻:
```javaScript
const squareList = arr => {
   return arr
    .filter(num => Number.isInteger(num) && num > 0)
    .map(num => num * num);

};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);

```
20. [Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)

      My Solution💻:
```javaScript

function urlSlug(title) {
 return title.toLowerCase().split(' ').filter(word => word !== '').join("-");

}

 console.log(urlSlug(" Winter Is  Coming"));

```
21. [Functions and Callbacks](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%201/tasks.md)

      My Solution💻:
```javaScript

const mapAsync = async (arr, callback) => {
  const result = [];

  for (const item of arr) {
    const newVal = await callback(item);
    result.push(newVal);
  }

  return result;
};


const arr = [1, 2, 3, 4, 5];
const callback = async (x) => {
  return x * 2;
};

mapAsync(arr, callback)
  .then(newArr => {
    console.log(newArr); 
  })
  .catch(error => {
    console.error(error);
  });


```
22. [Call Stack and Recursion](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%201/tasks.md)

      My Solution💻:
```javaScript

```
23. [Exercises for closures](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%202/tasks.md)

23.1 
      My Solution💻:
```javaScript

```

23.2
      My Solution💻:
```javaScript

```
23.3
      My Solution💻:
```javaScript

```
23.4
      My Solution💻:
```javaScript

```
24. [Exercises for Async JS & Promises](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%203/tasks.md)

24.1 
      My Solution💻:
```javaScript
const task1 = () => new Promise((resolve) => {
    setTimeout(() => {
      const message = "Task 1 has executed successfully!";
      resolve(message);
    }, 3000);
  });

  const task2 = () => new Promise((resolve) => {
    setTimeout(() => {
      const message = "Task 2 has executed successfully!";
      resolve(message);
    }, 0);
  });

  const task3 = () => new Promise((resolve) => {
    setTimeout(() => {
      const message = "Task 3 has executed successfully!";
      resolve(message);
    }, 1000);
  });

  const task4 = () => new Promise((resolve) => {
    setTimeout(() => {
      const message = "Task 4 has executed successfully!";
      resolve(message);
    }, 2000);
  });

  const task5 = () => new Promise((resolve) => {
    setTimeout(() => {
      const message = "Task 5 has executed successfully!";
      resolve(message);
    }, 4000);
  });

  const asyncTasks = [task1, task2, task3, task4, task5];

  const executeInSequenceWithCBs = async (tasks, callback) => {
    const promises = tasks.map((task) => task());
    const results = await Promise.all(promises);
    callback(results);
    return results;
  };

  executeInSequenceWithCBs(asyncTasks, (messages) => {
    console.log(messages);
  });


```
24.2
      My Solution💻:
```javaScript
const apis = [
    {
        apiName: "products",
        apiUrl: "https://dummyjson.com/products",
    },
    {
        apiName: "users",
        apiUrl: "https://dummyjson.com/users",
    },
    {
        apiName: "posts",
        apiUrl: "https://dummyjson.com/posts",
    },
    {
        apiName: "comments",
        apiUrl: "https://dummyjson.com/comments",
    }
]


const executeInParallelWithPromises = (apis) => {
    const promises = apis.map(api => {
        return fetch(api.apiUrl)
            .then(response => { response.json() })
            .then(data => {
                return {
                    apiName: api.apiName,
                    apiUrl: api.apiUrl,
                    apiData: data
                }
            })
    })

    return Promise.all(promises)
}

executeInParallelWithPromises(apis)
    .then(data=>console.log(data))
    .catch(error => console.log(error))




```
24.3 
      My Solution💻:
```javaScript

const apis = [
    {
        apiName: "products",
        apiUrl: "https://dummyjson.com/products",
    },
    {
        apiName: "users",
        apiUrl: "https://dummyjson.com/users",
    },
    {
        apiName: "posts",
        apiUrl: "https://dummyjson.com/posts",
    },
    {
        apiName: "comments",
        apiUrl: "https://dummyjson.com/comments",
    }
]

const executeInSequenceWithPromises = async (apis) => {
    const results = []
    for (let api of apis){
        const respose = await fetch(api.apiUrl)
        const data = await respose.json()
        results.push({
            apiName: api.apiName,
            apiUrl: api.apiUrl,
            apiData: data
        })
    }
    return results
}

executeInSequenceWithPromises(apis)
    .then(results=>{console.log(results)})
    .catch(error =>console.log(error))


```
25.[Object Oriented Programming](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%204/task.md).

[My Solution💻](https://www.freecodecamp.org/fcc11472c2d-4ae0-4251-ad2d-40c5ee0c2238).

   

