# Naming

* HTML elements should be in lowercase.
```
body,
div {
}
```
* Classes should be lowercase.
* Hyphenate class selector names; avoid underscores and camelCase.
* Use meaningful names; use structural or purposeful names over presentational.
```
// Avoid
// Avoid uppercase
.ClassName { }

// Avoid camel case
.commentForm { }

// What is a c1-xr? Use a more explicit name.
.c1-xr { }
```
* Avoid presentation- or location-specific words in names, as this will cause problems when you need to change the color, width, or feature later.
```
// Avoid
.blue
.text-gray
.100width-box

// OK
.warning
.primary
.lg-box
```
* Don’t abbreviate unless it’s a well-known abbreviation.
```
// Avoid
.bm-rd

// OK
.block--lg
```
* Name CSS components and modules with singular nouns.
```
.button {
}
```
