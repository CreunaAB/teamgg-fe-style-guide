# Comparison Operators & Equality

* Use `===` and `!==` over `==` and `!=`.
* Use shortcuts for booleans, but explicit comparisons for strings and numbers.
```
// Avoid
if (isValid === true) {...}

// OK
if (isValid) {...}

// Avoid
if (name) {...}

// OK
if (name !== '') {...}

// Avoid 
if (list.length) {...}

// OK
if (list.length > 0) {...}
```
* When mixing operators, enclose them in parentheses.
```
// Avoid
const foo = a && b < 0 || c > 0;

// OK
const foo = (a && b < 0) || c > 0; 
```
* For the ternary operator in a multi-line setting, place ? and : on their own lines.
```
// Avoid
const location = env.development ? 
    'localhost' : 
    'www.example.com'

// OK
const location = env.development ? 'localhost' : 'www.example.com'

const location = env.development 
    ? 'localhost' 
    : 'www.example.com'
```
