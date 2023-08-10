# Fifth Day 🔥

## Conditionals 👩🏻‍💻

If statment: ❓🌟
If it's given some other value, JS will convert it to a boolean and decide based on its "truthiness”
```
const you = {wannaBeMyLover: true};
if (you.wannaBeMyLover) {
    you.gottaGetWithMyFriends = true;
}
```
code in the if block only runs if the (condition) is true

- we can use else to run other code if (condition) is false
```
if (you.reallyBugMe) {
    console.log("Goodbye");
} else {
    console.log("Hello");
}
```
- We can chain else and if blocks to account for multiple conditions
  ```
  function compare(x, y) {
    if (x > y) {
        console.log(x, "is greater than", y);
    } else if (x < y) {
        console.log(x, "is less than", y);
    } else {
        console.log(x, "is equal to", y);
    }```


### The (condition) is usually an expression that evaluates to a boolean
```
if (forecast === "rain") {
    console.log("bring an umbrella");
}

```

- If it's given some other value, JS will convert it to a boolean and decide based on its "truthiness" `if ("nonempty strings are truthy") {
    console.log("this line will run");
### Conditional ternary operator `condition ? valueIfTrue : valueIfFalse; `



## Loops 💫

Loops let us run the same chunk of code multiple times => this is called iteration
```
for (let rep = 0; rep < 10; rep += 1) {
    console.log("now doing rep", rep);
}
console.log("do you even lift bro");
```
We can use for...of to iterate over characters in a string 
```
for (let char of "ALOHA") {
    console.log(char);
}
```
OR items in an array ,because strings & arrays are "iterables"
```
for (let item of ["pop", 6, "squish"]) {
    console.log(typeof item);
}
```

## map & filter 🌟 
The map & filter methods also let us process all the items in an array

### map : 🗺️
Calls a function on each item in an array to create a new array
```
const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];
const nicknames = spices.map(s => s.nickname + " Spice"); //Arrow functions are useful for this!
```

> note:📌
> String templates are useful too! Make them with backticks and ${}, e.g.
> s => `${s.nickname} Spice`; is equivalent to s => s.nickname + " Spice"


### filter 
calls a true/false function on each item, and creates a new array with only the items where the function returns true
```
const mels = spices.filter(s => s.name.includes("Mel"));
```

Examp;e 🔍:
```
/* From the spices array, use map and filter to:

create a new array names with only the name of each girl
create a new array endInY with just the girls whose nickname ends in "y" */

const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];

const names = spices.map(s=>s.name)
const endInY = spices.filter(s=>s.nickname.endsWith("y"))
```

## Spread (...): 💎
Is another neat trick for iterating over arrays,
It lets us take all the items in an array and spread 'em around


### Spread (...): 💎🔮
It lets us take all the items in an array and spread 'em around
```
const oldBurns = ["square", "wack"];
const newBurns = ["basic", "dusty", "sus"];

const burnBook = [...oldBurns, ...newBurns];
// equivalent to
const burnBook = oldBurns.concat(newBurns);
```
We can also use it to pass all the items from an array as arguments to a function or method
```
const skills = ["HTML", "CSS", "JS"];
const newSkills = ["React", "TypeScript", "Node"]
skills.push(...newSkills);
console.log(...skills);
```
