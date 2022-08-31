# Is (function)
A logical open gate function for expressions other than boolean or twinned expressions. The `is` function is the sibling functionality of `equals` function.

## Syntax
`is` can be used as its own expression posit (`_is`) or as an operator inside another expression posit, using either: the exclamation mark (`!`); or, the 'not tilde' symbol (`≁`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_is(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_equals(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_`*`<expression_posit>`*`(`*`...`*`=`*`...`*`);`

The is operator (`=`), can be used inside its posit `not`, but this counter-productive to the function of the logical NOT gate, however, it can be achieved.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_is(`*`...`*`=`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_equals(`*`...`*`=`*`...`*`);`

## Example
```diego
add_bool(bool1);
log_console()_valueof()_not([bool1]);             // undefined

with_bool(bool1)_v(false);

log_console()_valueof()_not()_bool(bool1);        // true
log_console()_valueof()_not([bool1]);             // true
log_console()_valueof()_calc(![bool1]);           // true
log_console()_valueof()_calc(≁[bool1]);           // true
```
