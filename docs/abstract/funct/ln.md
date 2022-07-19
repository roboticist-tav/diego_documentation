# Natural logarithm (function)
Provides the natural logarithm (in base [e](../const/e.md)) of a number.

## Syntax
To provide a the natural logarithm of a number use the `ln` posit or `㏒` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_ln(`*`numeric`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<expression_posit>`*`(`*`...`*`㏒(`*`numeric`*`)`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_ln([`*`variable_name`*`])`

## Example
The following function returns e:
```diego
add_funct(getNapier)_arg(dp)_ret()_e([dp]);

me_msg()_funct(getNapier)_arg(15);
// 2.718281828459045
```
---
## References

