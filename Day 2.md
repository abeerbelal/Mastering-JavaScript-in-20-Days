# secound Day ✏️
<br>


## Values & datatypes 🔑
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






