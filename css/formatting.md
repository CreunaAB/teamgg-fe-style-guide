# Formatting

### General

At Creuna we aim for our code to be readable, modular and easily maintained. To help us achieve this we utilize the [BEM](https://en.bem.info/methodology/) methodology. You can read more about BEM in the previous link or in this [article](https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/).

### Specificity

* Always use the minimum specificty required to achieve the desired style. 
* Avoid nesting selectors as much as possible. Modifiers, pseudo-states/elements & media queries are the exceptions.
* Don't use ID's for styling.
* Minimize the use of !important. This should be reserved for helper classes and print css.
* Don't use @extend as this can have unexpected side effects.
```md
// Avoid
.block {
    display: block;

    &__element {
        margin: 10px 0;
    }

    img {
        display: block;
    }
}

// OK
.block {
    display: block;
}

.block__element {
    margin: 10px 0;

    &--modifier {
        margin: 20px 0;
    }
}

.block__image {
    display: block;
}
```

### Spacing

* Use soft-tabs with four space indent.
* Put one space after : in property declarations.
* Put spaces before { in rule declarations.
* Put a blank line between each selector block.
* To close a selector block, put an unindented closing curly brace on a separate line.
* Each declaration should appear on its own line for more accurate error reporting.
```
// Avoid
.rule{
    margin:10px;text-align:center;}
    
// OK
.rule {
    margin: 10px;
    text-align: center;
}

.another-rule {
    margin: 10px;
}
```

### Property-value pairs

* Put each pair on its own line.
* Indent each pair one level.
* End in a semicolon.
```
selector {
    name: value;
    name: value;
}
```
Spaces should separate values and operators in Sass expressions
```
// Avoid
selector {
  font-size: ($font-size+2em);
  font-size: ($font-size +2em);
}
// OK
selector {
  font-size: ($font-size + 2em);
}
```
Single-quote URLs and string values.
```
background-image: url('/images/banana.jpg');
font-family: 'Helvetica', sans-serif;
font-family: 'Lucida Grande', 'Helvetica', sans-serif;
```

### Order

* Use the following ordering
    * Declaration list (eg property: value;)
    * Media queries
    * Pseudo states (:checked, :blur) and pseudo-elements (:before, :after)
    * Nested elements
    * Nested classes
```
// OK
.module {
    @media (max-width: $s) { ... }

    &:before { ... }

    &--modifier {
        margin-top: 10px;
    }
}
```
