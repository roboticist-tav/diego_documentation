# Unit (function)
The use of angle brackets (`❬❭`) in **Diego** represents the metaphysic unit of measure and/or unit system.

## Syntax
Angle brackets are used to define units in declarations, such as with a `scalar` or `vector`. They can be used alongside datatype without any issue.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_scalar(❬`*`unit`*`❭,`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_vector({`*`datatype`*`},❬`*`unit`*`❭,`*`moniker`*`)`<br>

When setting the unit or unit system of a container statement, the angle brackets can be used in place of the `_unit` posit, such as, for example the `instruct` object.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `begin_instruct(`*`moniker`*`)_unit(`*`unitsystem`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `begin_instruct(`*`moniker`*`)_❬`*`unitsystem`*`❭`<br>

When a unit declaration can be used in a `funct`ion to declare the unit of the return *objects*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_function({double},❬`*`unit`*`❭,`*`moniker`*`)`<br>

When setting the unit system, globally for a thingy, the angle brackets are not required.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `set_unitsystem(`*`unitsystem`*`)`<br>

For assignment, initialisation, and referencing, adding a unit will always cast the unit. The [`_unit`](../funct/unit.md) posit can be used, instead of angle brackets (`❬❭`). For an omitted unit at declaration the cast will be from the `{variant}` unit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_vector(❬`*`unit`*`❭,`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_vector(`*`moniker`*`)_unit(`*`unit`*`)`<br>

Angle brackets (`❬❭`) and the [`_unit`](./unit.md) posit can be used with shortened referencing, referenced variables, and, encapsulated variables.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(❬`*`unit`*`❭,`*`objmoniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`objmoniker`*`)_unit(`*`unit`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `[❬`*`unit`*`❭,`*`variablemoniker`*`]`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `[`*`variablemoniker`*`]_unit(`*`unit`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `([❬`*`unit`*`❭,`*`variablemoniker`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `([`*`variablemoniker`*`])_unit(`*`unit`*`)`<br>

Casts can be achieved inside *expressions*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_calc([❬`*`unit`*`❭,`*`variablemoniker`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_calc(❬`*`unit`*`❭)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_msg([❬`*`unit`*`❭,`*`variablemoniker`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_msg(❬`*`unit`*`❭)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_txt([❬`*`unit`*`❭,`*`variablemoniker`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_txt(❬`*`unit`*`❭)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_if([❬`*`unit`*`❭,`*`variablemoniker`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<…>`*`_if(❬`*`unit`*`❭)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *etc…*

---
## References

* Datatype posit [`_unit`](./unit.md)
* Unit statement in [Lexicon](../../lexicon/lexicon.md#❬❭)
* See also [Datatype](../../abstract/dt/dt.md) statement



