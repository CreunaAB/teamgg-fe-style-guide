# Formatting

* Use single quotes for values, not double quotes. 
```
// Avoid
const value = "hello";

// OK
const value = 'hello';
```
* Use braces with all multi-line blocks.
```
// Avoid
if (isValid)
    return true;

// OK
if (isValid) {
    return true;
}
```
* Use semiccolons. Always. (https://hackernoon.com/an-open-letter-to-javascript-leaders-regarding-no-semicolons-82cec422d67d)
* Don't use leading commas
```
// Avoid
const list = [
    one
   ,two
   ,three
]

// OK
const list = [
    one,
    two,
    three
]
```