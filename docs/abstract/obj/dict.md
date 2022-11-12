# Dictionary (object)
The `dict`ionary object is an associative data type, which holds key-value pairs. Sometimes called *maps* in programming languages. The use of "map" was discouraged during the development of the **Diego** language because a `map` object is an metaphysic object representing a map of an spatial area, learnt by thingies at childhood.

<a name="declare"></a>
## Declaration
The default declaration of the `dict`ionary object is to at least provide a *moniker*. With no datatype for the keys and value the `{variant}` datatype is implied when key-value pairs are added.  The datatype of the keys or the keys-values can be declared at declaration.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dictionary(`*`moniker`*`,{`*`key_datatype`*`});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker`*`{`*`key_datatype`*`},{`*`value_datatype`*`});`

<a name="initial"></a>
## Initialisation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker`*`,⟦{`*`key_value`*`},`*`value_value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker1`*`,⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`moniker2`*`,⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`moniker…`*`,⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker`*`,{`*`key_datatype`*`},⟦{`*`key_value`*`},`*`value_value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker1`*`{`*`key_datatype`*`},⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`moniker2`*`,{`*`key_datatype`*`},⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`moniker…`*`,{`*`key_datatype`*`},⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker`*`,{`*`key_datatype`*`},{`*`value_datatype`*`},⟦{`*`key_value`*`},`*`value_value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_dict(`*`moniker1`*`,{`*`key_datatype`*`},{`*`value_datatype`*`},⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`moniker2`*`,{`*`key_datatype`*`},{`*`value_datatype`*`},⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`moniker…`*`,{`*`key_datatype`*`},{`*`value_datatype`*`},⟦{`*`key_value1`*`},`*`value_value1`*`,{`*`key_value2`*`},`*`value_value2`*`,{`*`key_value…`*`},`*`value_value…`*`⟧);`

<a name="assign"></a>
## Assignment
Assignment of keys or keys-values is allowed at declaration, initialisation, and post-declaration. The `_key`, `_value`, and, `_set` posits are used for assignment, their equivalent syntax, `_keys`, `_k`, `_values`, `_v` are identical and can be used freely and interchangeably. The `set_` verb can also be used to the same effect as the `_set` posit. Any value given with no value will return as `undefined` when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict(`*`moniker`*`)_key(`*`key`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dict(`*`moniker`*`)_keys(`*`key1`*`,`*`key2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dictionary(`*`moniker`*`)_keys(`*`key1`*`,`*`key2`*`,`*`…`*`)_values(`*`val1`*`,`*`val2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dict(`*`moniker`*`)_k(`*`key1`*`,`*`key2`*`,`*`…`*`)_v(`*`val1`*`,`*`val2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker`*`)_set(`*`key1`*`,`*`val1`*`,`*`key2`*`,`*`val2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `set_dict(`*`moniker`*`,`*`key1`*`,`*`val1`*`,`*`key2`*`,`*`val2`*`,`*`…`*`)`

## Referencing
To reference a `dict` the `_ofkey` posit is used.  Without the `_ofkey` posit, the complete `dict` is returned. The `_ofkey` posit can accept variables using the `[]` square brackets to escape variables.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dict(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_dict(`*`moniker`*`)_ofkey(`*`key`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`dictmoniker`*`)_ofkey(`*`key`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dictionary(`*`moniker`*`)_ofkey(`*`key`*`,`*`key`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_dict(`*`moniker`*`)_ofkey([`*`variablename`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dict(`*`moniker`*`)_ofkey([`*`variablename`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dictionary(`*`moniker`*`)_ofkey([`*`variablename`*`],[`*`variablename`*`],[`*`variablename`*`])`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`dictmoniker`*`)_ofkey([`*`arrayname`*`])`

## Examples
A simple example is as follows:
```diego
// dictionary
add_dict(tanzanianBanknoteWidths)_keys(500,1000,2000,5000,10000)_values(120,125,130,135,140);
```

Key or value datatype can be contructed `struct`ures, as in this example:
```diego
add_struct(vertex)_param({float64},lat,lng);
add_dict({str},{vertex},m);

with_me()
    (m)_key(Bell Labs)_value(40.68433,-74.39967);
    (m)_str(Bell Labs)_vertex(40.68433,-74.39967);
    (m)_keyval(Bell Labs,40.68433,-74.39967);
    log_console()_dict(m)_ofkey(Bell Labs)_me();
;
```
<sub>Translated from [Maps, A Tour of Go](https://go.dev/tour/moretypes/19)</sub>

---

## See Also

* Similar abstract objects: [`lexicon`](./lexi.md); [`hash`](./hash.md); [`ary`](./ary.md); [`yush`](./yush.md)
* Equivalent metaphysic objects: [`spec`](../../metaphysic/obj/spec.md)
* [`dict` on Rosetta Code](https://rosettacode.org/wiki/Associative_array/Creation#Diego)

