# Lexikon (object)
The `lexikon` object is an associative data type, which holds key-value pairs like a [`dict`](./dict.md) object, however, the keys are uuids and managed. `lexikon` is named form Swedish for dictionary, it can be shortened to `lexi`.

## Sytnax
The default declaration of the `lexikon` object is to at least provide a *moniker*. `lexikon` can be shortened to `lexi`. With no datatype for values declared they will  be implied as `{variant}`, the keys are always uuid version 4 (`{uuid_4}`). However, the datatype of the values can be declared at declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_lexi(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_lexikon_(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_lexi({`*`valdt`*`},`*`moniker`*`)`

Assignment of values is allowed at both declaration, initialisation, and post-declaration. The `_value` posits are used for assignment, their equivalent syntax, `_values`, `_v` are identical and can be used freely and interchangeably.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_lexi(`*`moniker`*`)_value(`*`key`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_lexikon(`*`moniker`*`)_values(`*`val1`*`,`*`val2`*`,`*`…`*`)`

To reference a `lecikon` is, effectively, the reverse of a `dict` object, by using the `_ofval` posit. Without the `_ofval` posit, the complete `lexikon` is returned. The `_ofval` posit can accept variables using the `[]` square brackets to escape variables.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_lexi(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_lexi(`*`moniker`*`)_ofval(`*`val`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`leximoniker`*`)_ofval(`*`val`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_lexikon(`*`moniker`*`)_ofval(`*`val`*`,`*`key`*`,`*`…`*`)`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_lexi(`*`moniker`*`)_ofval([`*`variablename`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_lexikon(`*`moniker`*`)_ofval([`*`variablename`*`],[`*`variablename`*`],[`*`variablename`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`leximoniker`*`)_ofval([`*`arrayname`*`])`

However, the real strength of the `lexikon` object is for use in comparison conditions, for exmaple:
```diego
add_lexi(droneStockRotarBlades)_v(  ???? )

```
TODO: think of something that is special enough the be id'ed but common enough to be shared and swapped between robots

Arrays can be converted (cast) to lexikons.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_ary(`*`moniker`*`)_tolexi()`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `lexi_ary(`*`moniker`*`)`<br>

The most common use of a lexikon is the [`liken`](../../metaphysic/obj/liken.md) object.
---
## See Also

* Similar abstract objects: [`dict`](./dict.md); [`hash`](./hash.md); [`ary`](./ary.md); [`yush`](./yush.md)
* Equivalent metaphysic objects: [`liken`](../../metaphysic/obj/liken.md)
* [`lexikon` on Rosetta Code](https://rosettacode.org/wiki/Associative_array/Creation#Diego)






