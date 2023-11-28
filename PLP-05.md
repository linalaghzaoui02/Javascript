# JavaScript Classes and Inheritance Project

## Introduction
This project demonstrates the use of classes and inheritance in JavaScript, a crucial aspect of object-oriented programming. We'll create a simple `Person` class, enhance it with attributes and methods, and then create a `Student` class that inherits from `Person`.

## 1. Creating a Simple Object: `Person`
The `Person` class represents a basic object with attributes like name and age.

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
}
```

## 2. Adding Class Attributes and Functions
We enhance the `Person` class by adding additional attributes and functions.

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
    }
}
```

## 3. Inheritance Example: `Student`
The `Student` class inherits from `Person` and includes student-specific attributes like `studentId`.

```javascript
class Student extends Person {
    constructor(name, age, studentId) {
        super(name, age);
        this.studentId = studentId;
    }

    study() {
        console.log(`${this.name} is studying.`);
    }
}
```

## 4. Testing the Classes
Instantiate and test the `Person` and `Student` objects.

```javascript
let alice = new Person('Alice', 30);
alice.greet();

let bob = new Student('Bob', 20, 'S1234567');
bob.greet();
bob.study();
```

## 5. Discussion
- **Naming Conventions**: JavaScript uses camelCase for naming variables and functions. Classes are typically named in PascalCase.
- **Standard Methods**: The `constructor` method is a standard method in JavaScript for initializing class objects.
- **Inheritance Mechanisms**: JavaScript supports inheritance through the `extends` keyword. Child classes can access parent class methods through `super`.
- **Method Overloading**: JavaScript does not support method overloading in the traditional sense as seen in languages like Java.

## Conclusion
This project showcases basic implementation of classes and inheritance in JavaScript. Understanding these concepts is fundamental for effective object-oriented programming in JavaScript.
