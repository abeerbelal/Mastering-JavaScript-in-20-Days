# nineth Day ☄️



## Classes & Prototypes 🔥
Prototype chain: the feature behind-the-scenes that enables emulation of OOP but is a compelling tool in itself

###  __proto__ and prototype 📝
Proto and prototype both are objects that help in whether creating an array, object, or function and provide access to those specific methods or objects directly without taking memory and even it will give access to its constructor and all the array methods like push, pop, etc.

Proto: It is an actual object that provides a way to inherit properties from JavaScript with the help of an object which is created with new. Every object with behavior associated has internal property [[prototype]].

```javaScript

function Student(name,age) {
 this.name = name;
 this.age = age;
}
var stu1 = new Student("John", 50);
 
// Object have proto property
stu1
 
// Also if apply strict equal to check
// if both point at the same
// location then it will return true.
Student.prototype === stu1._proto_
```
Prototype: This unique object contains shared characteristics and actions of instances. Given that it can be found in every function declaration, it is a means to inherit properties from javascript.


#### Our code is getting repetitive, we're breaking our DRY principle. And suppose we have millions of users! 
What could we do?🤔🤔🤔🤔

### Solutions:🎤🎤


1. **Generate objects using a function**

**Problem**:  each time we create a new user we make space in our computer's
memory for all our data and functions. But our functions are just copies

2. **Using the prototype chain**
3. Introducing the keyword that automates the hard work:
 
   **NEW** (95% of developers have no idea how it works and therefore fail interviews)
4. **The class**


>   **Notes**:
>


> - All objects have a **proto** property by default which defaults to linking to a big
> object - Object.prototype full of (somewhat) useful functions
> - Arrow functions override the normal this rules


- Two kinds of properties
1. Own properties: are defined directly on the object instance itself.
2. prototype properties: are defined on the prototype.

```javaScript
function User(name) {
 this.name = name;  //own property
}
User.prototype.numLegs = 2; // prototype property
```
