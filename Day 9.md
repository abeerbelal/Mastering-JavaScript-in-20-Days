# nineth Day ☄️


## Classes & Prototypes 🔥
Prototype chain: the feature behind-the-scenes that enables emulation of OOP but is a compelling tool in itself

###  __proto__ and prototype 📝


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
