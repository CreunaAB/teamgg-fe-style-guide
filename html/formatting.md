# Formatting

* Ensure that you use valid HTML. Use tools such as the [W3C HTML validator](https://validator.w3.org/nu/) to test.
* Use soft tabs with four spaces indent
* Put each element on its own line and indent each element.
```
// Avoid
<div class="box"><div class="box__inner"></div></div>

<div class="box">
    <div class="box__inner"><span>Hello</span></div>
<div>

// OK
<div class="box">
    <div class="box__inner">
        <span>Hello</span>
    </div>
<div>
```
* All HTML code should be lowercase. This applies to HTML element names, attributes, attribute values, CSS selectors, properties and property values. The exception is strings.
```
// Avoid
<A HREF="#" CLASS="link">HOME</A>

// OK
<a href="#" class="link">HOME</a>
```
* Use optional open/close tags.
```
<h1>Welcome

```