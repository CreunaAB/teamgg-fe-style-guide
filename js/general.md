# General

* Use vanilla Javascript whenever possible. Avoid using frameworks such as jQuery.
* Strive for readability and maintainability over writing less code. 

### Formatting
* Use single quotes for values, not double quotes. 
```
// Bad
const value = "hello";

// Good
const value = 'hello';
```
* Use braces with all multi-line blocks.
```
// Bad
if (isValid)
    return true;

// Good
if (isValid) {
    return true;
}
```
* Use semiccolons. Always. (https://hackernoon.com/an-open-letter-to-javascript-leaders-regarding-no-semicolons-82cec422d67d)
* Don't use leading commas
const list = [
    one
   ,two
   ,three
]

const list = [
    one,
    two,
    three
]

### Spacing

* Use soft-tabs with four space indent.
* Put one space before the leading brace.
```
// Bad
function foo(){

}

// Good
function foo() {

}
```
* Put one space before opening parenthesis in control statements (`if`, `for` etc)
```
// Bad
if(isValid) {
    return true;
}
 
// Good
if (isValid) {
    return true;
}
```
* Separate operators with spaces.
```
// Bad
const x=y+10;


// Good
const x = y + 10;
```

### References

* Use `const` for all of your references. Avoid using `var`. 
* Don't create global variables.
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
* In modules with a single export, prefer default export over named export.
* Put all `imports` above non-import statements. 
```
// Bad
import foo from './foo';
foo.init();

import bar from './bar';

// Good
import foo from './foo';
import bar from './bar';

foo.init();
```
* Multiline imports should be indented just like multiline array and object literals.
```
// Bad
import { classOne, classTwo, classThree, classFour }

// Good
import {
    classOne, 
    classTwo, 
    classThree, 
    classFour
}
```

### Comparison Operators & Equality
* Use `===` and `!==` over `==` and `!=`.
* Use shortcuts for booleans, but explicit comparisons for strings and numbers.
```
// Bad
if (isValid === true) {...}

// Good
if (isValid) {...}

// Bad
if (name) {...}

// Good
if (name !== '') {...}

// Bad 
if (list.length) {...}

// Good
if (list.length > 0) {...}
```
* When mixing operators, enclose them in parentheses.
```
// Bad
const foo = a && b < 0 || c > 0;

// Good
const foo = (a && b < 0) || c > 0; 
```
