# Classes & Constructors

* Always use `class`. Avoid using `prototype`, `module` and other design patterns.
```
// Avoid
function Person(name, age) {
    this.name = name;
    this.age = age;
}

Person.prototype.sayHello = function() {
    console.log(`Hi! My name is ${this.name}`);
}

// OK
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    sayHello {
        console.log(`Hi! My name is ${this.name}`);
    }
}
```

* Classes have a default constructor if one is not specified. An empty constructor function or one that just delegates to a parent class is unnecessary. 
```
// Avoid
class Person {
  constructor() {}

  getName() {
    return this.name;
  }
}

// Also Avoid
class John extends Person {
  constructor(...args) {
    super(...args);
  }
}

// OK
class John extends Person {
  constructor(...args) {
    super(...args);
    this.name = 'Rey';
  }
}
```
* Constructors of derived classes must call super.
```
// Avoid
class Dog {
    constructor() {
        super();
    }
}

// OK
class Dog extends Animal {
    constructor() {
        super();
    }
}
```