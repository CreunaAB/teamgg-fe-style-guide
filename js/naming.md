### Naming
* Use descriptive names. 
```
// Avoid
function fId() {

}

// OK
function findById() {

}
```
* Use camelCase.
```
// Avoid
const thisisavariable = 'foo';
const this_is_a_variable = 'foo';

// OK
const thisIsAVariable = 'foo';
```
* Use PascalCase when naming classes
```
// Avoid
class user {...}

// OK
class User {...}
```
* Don't save references to `this`. Use arrow functions or `bind`.
```
// Avoid
function foo() {
    const self = this;

    return function() {
        console.log(self);
    }
}

// OK
function foo() {
    return () => {
        console.log(this);
    }
}
```