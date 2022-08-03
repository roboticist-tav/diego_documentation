# Deed (object)
The `deed` *object* is a inheritied variable (`var`), a basic one-dimensional data storage object, immutable except for *deed owner*.

<a name="declare"></a>
## Declaration
Although the most common use of the `deed` expression is via a posit, the `calc` *expressive object* can be declared.  The use of a *moniker*, is optional, but if used it must be enclosed in moniker brackets (`⟦⟧`) or double square brackets (`[[]]`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_deed(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_deed(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_deed(⟦`*`moniker`*`⟧,{`*`datatype`*`},`*`expression`*`);`



&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(⟦`*`moniker`*`⟧,`*`expression`*`);`<br>


`add_deed(`*`moniker`*`);`



```diego

// robot alif...
add_deed({int},deedIntegerA)_v(32);

// robot bah...
log_console()_deed(deedIntegerA); // 32
with_deed(deedIntegerA)_inc(1);
with_deed(deedIntegerA)_err(d3fe,deed `deedIntegerA` only mutable by `{robot}` `alif`);

// robot alif...
with_deed(deedIntegerA)_inc(1);

// robot bah...
log_console()_deed(deedIntegerA); // 33
```