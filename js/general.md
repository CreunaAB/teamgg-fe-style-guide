# General

* Use vanilla Javascript whenever possible. Avoid using frameworks such as jQuery.


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
