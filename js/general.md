# General

* Use vanilla Javascript whenever possible. Avoid using frameworks such as jQuery.
* Strive for readability and maintainability over writing less code. 

### Formatting
* Use single quotes for values, not double quotes. This is for consistency across the codebase. 
```
// Bad
const value = "hello";

// Good
const value = 'hello';
```

### Spacing

* Use soft-tabs with four space indent.

### References

* Use `const` for all of your references. Avoid using `var`. 
```
// Bad
var a = 1;
var b = 2;

// Good
const a = 1;
const b = 2;
```
* If you must reassign references, use `let` instead of `var` since `let` is block scoped (not accessible outside the block) rather than function scoped like `var`.
```
// Bad
var count = 1;
if (true) {
  count += 1;
}

// Good
let count = 1;
if (true) {
  count += 1;
}
```

### Strings

* Prefer template literals over string concatenation.
```
// Bad
function sayHello(name) {
    return 'Hello ' + name + '!';
}

// Good
function sayHello(name) {
    return `Hello ${name}!`;
}

```

### Functions

* Prefer the use of the spread `...` operator.
```
// bad
const x = [1, 2, 3, 4, 5];
console.log.apply(console, x);

// good
const x = [1, 2, 3, 4, 5];
console.log(...x);

// bad
new (Function.prototype.bind.apply(Date, [null, 2016, 8, 5]));

// good
new Date(...[2016, 8, 5]);
```

* If your function takes a single argument and doesn’t use braces, omit the parentheses. Less visual clutter.
```
// Bad
[1, 2, 3].map((x) => x + x);

// Good
[1, 2, 3].map(x => x + x);
```

* Use arrow functions for all anonymous functions (eg a inline callback).
```
// Bad
[1, 2, 3].forEach(function(x) {
    return x + 1;
});

// Good
[1, 2, 3].forEach(() => {
    return x + 1;
});

```

### Classes & Constructors

* Always use `class`. Avoid using `prototype`, `module` and other design patterns.
```
// Bad
function Person(name, age) {
    this.name = name;
    this.age = age;
}

Person.prototype.sayHello = function() {
    console.log(`Hi! My name is ${this.name}`);
}

// Good
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
// Bad
class Person {
  constructor() {}

  getName() {
    return this.name;
  }
}

// Also bad
class John extends Person {
  constructor(...args) {
    super(...args);
  }
}

// Good
class John extends Person {
  constructor(...args) {
    super(...args);
    this.name = 'Rey';
  }
}
```

### Imports
* Always use modules (`import`/`export`) over a non-standard module system, such as `require`. 
