### What is type checking?

Type-checking can be thought of as a task that attempts to evaluate the question of compatibility or type equivalence:
```javaScript
function foo(x) {
  // ... mystery code ...
}
//
// TYPE CHECKING
// -------------
// Is `myValue` type-equivalent to
//     what `foo` whats to receive?
foo(myValue)
```
This question can be asked at a function call - such as foo(myValue) in the above example - as an assignment,
```
// is the value y holds type-equivalent to what `x` allows?
x = y
```

### Static vs dynamic
Sorting type systems as either [static](https://www.typescriptlang.org/docs/handbook/2/basic-types.html#static-type-checking) or dynamic has to do with whether type-checking is performed **at compile time or runtime.**

> ***TypeScript’s type system is static.**

Java, C#, C++ all fit into this category. Keep in mind that inferrence can still occur in static type systems — TypeScript, Scala, and Haskell all have some form of static type checking.

**Dynamic type systems perform their “type equivalence” evaluation at runtime.** JavaScript, Python, Ruby, Perl and PHP fall into this category.

### Nominal vs structural

**Nominal type systems are all about NAMES**. Let’s take a look at a simple Java
ex:all that matters is whether myCar is an instance of the class named Car.


> TypeScript type system is structural

**Structural type systems are all about STRUCTURE or SHAPE.** Let’s look at a TypeScript example:
```javaScript
class Car {
  make: string
  model: string
  year: number
  isElectric: boolean
}
 
class Truck {
  make: string
  model: string
  year: number
  towingCapacity: number
}
 
const vehicle = {
  make: "Honda",
  model: "Accord",
  year: 2017,
}
 
function printCar(car: {
  make: string
  model: string
  year: number
}) {
  console.log(`${car.make} ${car.model} (${car.year})`)
}
 
printCar(new Car()) // Fine
printCar(new Truck()) // Fine
printCar(vehicle) // Fine
```


The function printCar doesn’t care about which constructor its argument came from, it only cares about whether it has:

- A `make` property that’s of type `string`
- A `model` property that’s of type `string`
- A `year` property that’s of type `number`
If the argument passed to it meets these requirements, printCar is happy.

### Duck typing

“Duck typing” gets its name from the “duck test”.

> “If it looks like a duck, swims like a duck, and quack like a duck, then it probably is a duck”.

In practice, this is very similar to structural typing, but “Duck typing” is usually used to describe dynamic type systems.

### “Strong” vs. “Weak” types
These terms, while used frequently, have no agreed-upon technical definition. In the context of TypeScript it’s common for those who say “strong” to really mean “static”.
