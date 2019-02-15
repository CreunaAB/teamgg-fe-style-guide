# Variables

* Create new variables in the following instances
    * The value is of a type that is generic and used repeatedly (eg colors, sizes, breakpoints, z-index)
    * The value is likely to be updated
* Variables across the whole scss codebase should be placed in their own file.
* Set all breakpoints to variables.
* Set all z-indexes to variables.
* Set all colors to variables.
```
//-- Example variables --//

// Breakpoints
$s: 767px;
$m: 968px;
$l: 1240px;

// Z-indexes
$z-below: -1;
$z-neutral: 0;
$z-promoted: 1;
$z-modal: 100;

// Colors
$color-white: #fff;
$color-black: #000;
$color-dark: #1a1a1a;
$color-red: #E5243B;
$color-green: #56C02B;
```
