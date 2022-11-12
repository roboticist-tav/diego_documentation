# Hash (object)
The `hash` table object is an associative data type, which holds key-value pairs like [`dict`](./dict.md) and [`lexikon`](./lexi.md) objects, however, the keys managed using a .

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_hash(`*`moniker`*`)`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_ary(`*`moniker`*`)_tohash()`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `hash_ary(`*`moniker`*`)`<br>




## Sytnax
The default declaration of the `dict`ionary object is to at least provide a *moniker*. With no datatype for the keys and value the `{variant}` datatype is implied when key-value pairs are added.  The datatype of the keys or the keys-values can be declared at declaration.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dictionary(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict({`*`keydt`*`},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict({`*`keydt`*`},{`*`valdt`*`},`*`moniker`*`)`<br>

Assignment of keys or keys-values is allowed at both declaration, initialisation, and post-declaration. The `_key` and `_value` posits are used for assignment, their equivalent syntax, `_keys`, `_k`, `_values`, `_v` are identical and can be used freely and interchangeably. Any key given with no value will return as `undefined` when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dict(`*`moniker`*`)_key(`*`key`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dict(`*`moniker`*`)_keys(`*`key1`*`,`*`key2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_dictionary(`*`moniker`*`)_keys(`*`key1`*`,`*`key2`*`,`*`…`*`)_values(`*`val1`*`,`*`val2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_dict(`*`moniker`*`)_k(`*`key1`*`,`*`key2`*`,`*`…`*`)_v(`*`val1`*`,`*`val2`*`,`*`…`*`)`<br>