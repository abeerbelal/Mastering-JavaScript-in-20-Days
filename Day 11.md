# Eleventh day Day 💡💖

## Equality == / === ⚓⚖️
== and === are used as comparison operators to check for equality between two values. However, they behave differently based on the context and type of values being compared.


### == (Equality Operator):📢
 is used to compare values for equality. It performs type coercion, which means it attempts to convert the values to a common type before comparing. This can lead to unexpected results when comparing values of different types.

```javaScript
'5' == 5;      // true, because the string '5' is coerced to the number 5
false == 0;     // true, because both are coerced to the same falsy value
null == undefined; // true, because they are both considered equal in loose comparison

```
### === (Strict Equality Operator):🌺
 is used to compare values for equality without performing type coercion. It checks not only the values but also the types of the values being compared. This is often referred to as "strict equality" or "identity equality." If the types of the operands are different, the comparison immediately returns false.

 ```javaScript
'5' === 5;     // false, because the types are different (string vs. number)
false === 0;    // false, because the types are different (boolean vs. number)
null === undefined; // false, because they have different types

```

<br>

## Static Typing 🎯⌨️


###  Benefits: 💫

1. Catch type-related mistakes
2. Communicate type intent
3. Provide IDE feedback
4. validating operand types to avoid errors



####  TypeScript and Flow:


are indeed similar in many ways because they both address the same general problem: adding static type checking to JavaScript to catch type-related errors early in the development process
### **[TypeScript vs Flow](https://github.com/niieani/typescript-vs-flowtype)** 


##  Scope ☄️🌌

JavaScript organizes scopes with functions and blocks

<br>

> ###  Note: 📌
>  Having two varibles with same name in different scopes called shadowing
>  **"shadowing"** refers to a situation where a variable declared in an inner scope has the same name as a variable declared in an  
>   outer scope. This can lead to unexpected behavior and bugs, as the inner variable "shadows" or takes
>  precedence over the outer variable within that inner scope.

<br>

### **Befor executing the code :** 💻🔥

1. scope maneger detrmine the scope
2. then bring data or store it in the variable

<br>



###  dynamic global variables: 🌍

If I try to use varible in current scope without declaring it, it will be declared in the global scope

```javaScript
function foo (){
    x = "abeer"
    console.log(x)
}
foo() //Outputs: abeer
```
   

### Disable it 🔥

```javaScript
"use strict" 
function foo (){
    x = "abeer"
    console.log(x)
}
foo() //Outputs:  referance error
```



## Scope & Function Expressions 🌊

### Function expression 
```javaScript
const add = function(x, y) {
  return x + y;
};

console.log(add(3, 5)); // Outputs: 8

```

### Named Function Expressions:

####  Benefits 💭

1. Reliable function self-reference (recursion, etc)
2. More debuggable stack traces
3. More self-documenting code


```javaScript
let fun1 = function fun2(){
    console.log("abeer")
}

fun1() // Outputs:abeer
fun2() Outputs: //ReferenceError
```

### Exercises🍃

```javaScript
/*
You are provided three functions stubs -- `printRecords(..)`, `paidStudentsToEnroll()`, and `remindUnpaid(..)` -- which you must define.

At the bottom of the file you will see these functions called, and a code comment indicating what the console output should be.

1. `printRecords(..)` should:
	- take a list of student Ids
	- retrieve each student record by its student Id (hint: array `find(..)`)
	- sort by student name, ascending (hint: array `sort(..)`)
	- print each record to the console, including `name`, `id`, and `"Paid"` or `"Not Paid"` based on their paid status

2. `paidStudentsToEnroll()` should:
	- look through all the student records, checking to see which ones are paid but **not yet enrolled**
	- collect these student Ids
	- return a new array including the previously enrolled student Ids as well as the to-be-enrolled student Ids (hint: spread `...`)

3. `remindUnpaid(..)` should:
	- take a list of student Ids
	- filter this list of student Ids to only those whose records are in unpaid status
	- pass the filtered list to `printRecords(..)` to print the unpaid reminders
*/

function printRecords(studentId) {
    return studentRecords.find(function getById(student) {
        return student.id === studentId
    })
}


function paidStudentsToEnroll() {
    const studentsToEnroll = studentRecords.filter(function needToEnroll(student) {
        return (student.paid && !student.currentEnrollment.includes(record.id))
        // checks if the id of the current record is not already present in the currentEnrollment array
    })

    return [...currentEnrollment, ...studentsToEnroll.map(function getIId(student) {
        return student.id
    })]
}

function remindUnpaid(recordIds) {
	const unpaidIds = recordIds.filter(function notPaidYet(studentId){
		const record = getStudentFromId(studentId);
		return !record.paid;
	});

	printRecords(unpaidIds);
}
```



   
## Functional Programming🔥
<br>

> ### Note:📝
>  Functional programming is a good habit. It keeps your code easy to manage and saves you from sneaky bugs. 


