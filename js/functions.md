# Functions

* Prefer the use of the spread `...` operator.
```
// Avoid
const x = [1, 2, 3, 4, 5];
console.log.apply(console, x);

// OK
const x = [1, 2, 3, 4, 5];
console.log(...x);

// Avoid
new (Function.prototype.bind.apply(Date, [null, 2016, 8, 5]));

// OK
new Date(...[2016, 8, 5]);
```

* If your function takes a single argument and doesn’t use braces, omit the parentheses. Less visual clutter.
```
// Avoid
[1, 2, 3].map((x) => x + x);

// OK
[1, 2, 3].map(x => x + x);
```

* Use arrow functions for all anonymous functions (eg a inline callback).
```
// Avoid
[1, 2, 3].forEach(function(x) {
    return x + 1;
});

// OK
[1, 2, 3].forEach(() => {
    return x + 1;
});

```