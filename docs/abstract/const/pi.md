# Pi (constant)
The `pi` *constant* represents pi ($\pi$), the ratio of the circumference of a circle to its diameter, which is approximately 3.14159.

## Syntax
To provide a pi, use the `pi()` posit or (`π` or `𝛑` or `𝜋` or `𝝅` or `𝝿`) in expressions. Optionally, the number of decimal places can be given, if omitted the default decimal places of the callee thingy is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_pi()`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_pi(`*`decimal_places`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<expression_posit>`*`(`*`...`*`π`*`...`*`);`

## Example
The following function returns e:
```diego
add_funct(calcCircumference)_param(radius)
    ()_ret()_calc⟦[radius]×(π+π)⟧;
;

me_msg()_funct(calcCircumference)_param(1);
// 6.283185307179586
```
---
## References

* Mathematical constants: [`e`](./e.md); [`ln2`](./ln2.md); [`ln10`](./ln10.md); [`ln10e`](./ln10e.md); 