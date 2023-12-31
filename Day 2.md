# secound Day ✏️
<br>


## Values & datatypes 🗝️
<br>

### Values 👇
Are chunks of information we want to work with, that information (data) can be of different types:

### JS has two kinds of data:

-  ### Primitive types:
  
1. **string** :
   
   in double-quotes,single quotess,a  backticks. does not have to just include ASCIIletters also have emojis 
     (ex: “abeer”, ‘abeer’ , `abeer`, "23", "👉")
3. **number** :
   
    (ex: 9, 525600, 3.14. 1.2e9, Infinity)
5. **boolean**:
   
    (ex: true, false)
7. **undefined**:
   
   there was supposed to have value. but accidental nothing
9. **null**:
    
    deliberate nothing.
    
- ### Objects:
    
     (e.g. `document` & friends)
   <br>
   👉 typeof => tells you the type of a value.
```
typeof "42" // string
typeof 42 //number
typeof false //boolean
typeof null //object
typeof "some string".length //number
typeof "" //string
```
### String 🔻
are made of a sequence of characters`"super".length //4`are in a specific order, each gets a number, starting at 0 called "index".
index => a number given to a position

#### Examples:
```
"ALOHA"[0]      // “A”
"ALOHA".length  // 5

//What's the index of a specific character?if not exist will return -1
"ALOHA".indexOf("A")  //0
"ALOHA".indexOf("a")  //-1

//Does this string contain some other string?
"ALOHA".includes("LOL")//false
"ALOHA".includes("HA")  // true

//Does this string start with some other string?
"ALOHA".startsWith("AL") // true

// At what index does this substring begin?
"ALOHA".indexOf("HA") // 3

 // Connecting strings together
"ALOHA" + "!"

//we can make all character in string small or capital 
"ALOHA".toLowerCase() // "aloha"
"aloha".toUpperCase() //"ALOHA"
```

### Exercises in course: 🔥
```
// 1. Add your last name in the players listing
document.getElementById("p1-name").append(" hanaysheh")

// 2. Retrieve the first "T" in the page title
document.title.indexOf("T")

// 3. Answer whether the page title contains the string "JavaScript"
document.title.includes("JavaScript")

// 4. Capitalize the heading "Tic Tac Toe"
document.querySelector("header h1").textContent =  // to appear in the page
document.querySelector("h1").textContent.toUpperCase()
```
 <br>


 ## Operators ➗🤔 

### Arithmetic operators
-  '+' add
-  '-' subtract
-  '*' multiply
-  '/' divide

  
 ### ➕ operator:
   is an operator with several different uses:
  - when operating on strings => it concatenates the strings ` "abeer" + "belal" `.
  - it can operate on Numbers by adding them `1+1`.
  - it called an overloaded operator because it does different functions.

 
 
### typeof:
The typeof operator returns a string indicating the type of the operand's value.
```
console.log(typeof 42);
// Expected output: "number"

console.log(typeof 'blubber');
// Expected output: "string"
```

### Comparison operators  ⚡️
- '>' greater than
- '<' less than
- '>=' greater than or equal to
- '<=' less than or equal to

### Equality operators:
| strict     | loosey-    | meaning            |
|------------|------------|--------------------|
| ===        | ==         | equals             |
| !==        | !=         | does not equal     |

 ### ⏳✨⚡️
| strict        | loosey-goosey | meaning           | Do these differ? How?🤔            |
|---------------|---------------|-------------------|-----------------------------------|
| 1 === 1       | 1 == 1        | equals            | No difference. Both are true.     |
| "1" === "1"   | "1" == "1"    | equals            | No difference. Both are true.     |
| 1 === "1"     | 1 == "1"      | does not equal    | Yes, difference. Strict comparison checks both value and type, so 1 (number) is not equal to "1" (string). Loose comparison only checks the value, so it considers them equal. |


### Nullish coalescing operator (??):🚩
The nullish coalescing (??) operator is a logical operator that returns its right-hand side operand when its left-hand side operand is `null` or `undefined`, and otherwise returns its left-hand side operand.

```javaScript
const foo = null ?? 'default string';
console.log(foo);
// Expected output: "default string"

const baz = 0 ?? 42;
console.log(baz);
// Expected output: 0
```

## Expressions ☄️
an expression evaluates (aka resolves) to a value, more like content.
```
4 / 2 * 10
"Frontend" + "Masters"
5 > 4 !== 3 > 4
```

 ## Variables: 🎯🚀
 A variable is a named reference to a valu—thatt way an unpredictable value can be accessed through a predetermined name.
 - Variables let us remember values.
 - as pointer points to specific value. 

  ### Declaring a variable
  - via var keyword ` var name;` 🔓
  - via let keyword ` let name;`🔐
  - via const keyword ` const name;` => const declares & assigns a "constant", aka a variable that can't be changed 🙄 🔒.

    ### Variable names
   -  camelCase 👉❓ 'variables contain values? e.g: `let FirstName;`
   -  lso_valid_but_less_common
   -  ddbut_Technicallyfine2

### Assigning a variable🔒:
" = "  operator here means assign value to variable 
```
let myDeclaredVariable;
myDeclaredVariable = "so value, much wow";

let myAssignedVariable = "such efficient, amaze"; //Declaring & assigning at once

let x = null;// i want this variable to be empty
let variable; //this will take undefined "nothing"
```
    

 
 ## **Statements vs. Expressions** 👩🏻‍💻🤔
 ### An expression "asks" JS for a value


```
myAssignedVariable  // what is the value of my variable
6 + 4               // what is the value of this summation
document.getElementById("board")
```

A **statement**  "tells" JS to do something, actions we want JS to do it

```
// e.g: declare/assign a variable
let ten = 6 + 4;
myDeclaredVariable = "new value";
let board = document.getElementById("board");

function add(x, y) {
    return x + y;
}

let biggest;
if (5 > 4) {
    biggest = 5;
} else {
    biggest = 4;
}
for (let character of "string") {
    console.log(character);
}
```
 















