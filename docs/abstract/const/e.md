# Euler's Constant (constant)
The `e` object represents Euler's constant, the base of natural logarithms, which is approximately 2.718. It follows formula: $e^{i\pi} + 1 = 0$.

## Syntax
To provide a Euler's constant, use the `e()` posit or `ℇ` in expressions. Optionally, the number of decimal places can be given, if omitted the default decimal places of the callee thingy is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_e()`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_e(`*`decimal_places`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<expression_posit>`*`(`*`…`*`ℇ`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_e([`*`variable_name`*`])`<br>

## Example
The following function returns e:
```diego
add_funct(getNapier)_param(dp)_ret()_e([dp]);

me_msg()_funct(getNapier)_param(15);
// 2.718281828459045
```
---
## References

