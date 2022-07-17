# Equals (function)
A logical open gate function for boolean or twinned expressions. The `equals` function is the transverse of `not` function.

## Syntax
`euals` can be used as its own expression posit (`_equals`) or as an operator inside another expression posit, using the equals symbol (`=`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_equals(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_`*`<expression_posit>`*`(`*`...`*`=`*`...`*`);`

The is operator (`=`), can be used inside its posit `equals`, but this counter-productive to the function of the logical open gate, however, it can be achieved.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_equals(`*`...`*`=`*`...`*`);`

## Example
```diego
add_bool(bool1);
log_console()_valueof()_equals([bool1]);             // undefined

with_bool(bool1)_v(false);

log_console()_valueof()_equals()_bool(bool1);        // true
log_console()_valueof()_equals([bool1]);             // true
log_console()_valueof()_calc(=[bool1]);              // true
```
