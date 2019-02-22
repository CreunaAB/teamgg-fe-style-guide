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
* Use semiccolons. (https://hackernoon.com/an-open-letter-to-javascript-leaders-regarding-no-semicolons-82cec422d67d)
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

### Spacing

* Use soft-tabs with four space indent.
* Put one space before the leading brace.
```
// Avoid
function foo(){

}

// OK
function foo() {

}
```
* Put one space before opening parenthesis in control statements (`if`, `for` etc)
```
// Avoid
if(isValid) {
    return true;
}
 
// OK
if (isValid) {
    return true;
}
```
* Separate operators with spaces.
```
// Avoid
const x=y+10;


// OK
const x = y + 10;
```