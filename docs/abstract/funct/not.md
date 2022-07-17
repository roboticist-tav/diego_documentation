# Not (function)
A logical NOT gate function for boolean or twinned expressions. `not` is the transverse of `equals` function.

## Syntax
`not` can be used as its own expression posit (`_not`) or as an operator inside another expression posit, using either: the exclamation mark (`!`); or, the 'not tilde' symbol (`≁`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_not(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_`*`<expression_posit>`*`(`*`...`*`!`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_`*`<expression_posit>`*`(`*`...`*`≁`*`...`*`);`

The not operator (`!` or `≁`), can be used inside its posit `not`, but this counter-productive to the function of the logical NOT gate, however, it can be achieved.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_not(`*`...`*`!`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_not(`*`...`*`≁`*`...`*`);`

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
