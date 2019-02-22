# General

* Use vanilla Javascript whenever possible. Avoid using frameworks such as jQuery.
* Strive for readability and maintainability over writing less code. 

### References

* Use `const` for all of your references. Avoid using `var`. 
* Don't create global variables.
```
// Avoid
var a = 1;
var b = 2;

// OK
const a = 1;
const b = 2;
```
* If you must reassign references, use `let` instead of `var` since `let` is block scoped (not accessible outside the block) rather than function scoped like `var`.
```
// Avoid
var count = 1;
if (true) {
  count += 1;
}

// OK
let count = 1;
if (true) {
  count += 1;
}
```

### Strings

* Prefer template literals over string concatenation.
```
// Avoid
function sayHello(name) {
    return 'Hello ' + name + '!';
}

// OK
function sayHello(name) {
    return `Hello ${name}!`;
}

```

### Imports
* Always use modules (`import`/`export`) over a non-standard module system, such as `require`. 
* In modules with a single export, prefer default export over named export.
* Put all `imports` above non-import statements. 
```
// Avoid
import foo from './foo';
foo.init();

import bar from './bar';

// OK
import foo from './foo';
import bar from './bar';

foo.init();
```
* Multiline imports should be indented just like multiline array and object literals.
```
// Avoid
import { classOne, classTwo, classThree, classFour }

// OK
import {
    classOne, 
    classTwo, 
    classThree, 
    classFour
}
```
