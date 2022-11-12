# Datatype (statement)
The use of curly brackets (`{}`) in **Diego** represents the datatype of the object.

## Syntax
Curly brackets are used to define datatype in declarations, such as with a `var`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({`*`datatype`*`},`*`moniker`*`)`

All primative objects have their datatype counterpart.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({str},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({int},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({double},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({float},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({real},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({bool},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({tempor},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; etc…

In declarations, omitting the datatype will imply the [`{variant}`](../dt/variant.md) datatype is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_array(`*`moniker`*`)`

For assignment, initialisation, and referencing, adding a datatype will always cast the datatype. The [`_dt`](../funct/dt.md) posit can be used, instead of curly brackets (`{}`). For an omitted datatype at declaration the cast will be from the `{variant}` datatype.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_ary({`*`datatype`*`},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_ary(`*`moniker`*`)_dt(`*`datatype`*`)`<br>

 Curly brackets (`{}`) and the [`_dt`](../funct/dt.md) posit can be used with shortened referencing, referenced variables, and, encapsulated variables.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `({`*`datatype`*`},`*`objmoniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`objmoniker`*`)_dt(`*`datatype`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `[{`*`datatype`*`},`*`variablemoniker`*`]`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `[`*`variablemoniker`*`]_dt(`*`datatype`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `([{`*`datatype`*`},`*`variablemoniker`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `([`*`variablemoniker`*`])_dt(`*`datatype`*`)`<br>

Casts can be achieved inside *expressions*, such as, for example, the `calc` function.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_calc⟦[{`*`datatype`*`},`*`variablemoniker`*`])`<br>

---
## References

* Datatype posit [`_dt`](../funct/dt.md)
* Datatype statement in [Lexicon](../../lexicon/lexicon.md#{})
* See also [Unit]() statement



