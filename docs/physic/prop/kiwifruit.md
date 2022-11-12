# Kiwifruit (type)
`{kiwifruit}` is a type of the [`organic`](./organic.md) *object*, representing a kiwifruit, a type of fruit with a thin hairy skin, green flesh, and black seeds. The syntax `{chinese_gooseberry}` can also be used. The `{kiwifruit}` type is a sub-type of `{fruit}`. In expressions the unicode `1F95D` character (`🥝`) is used.

<a name="declare"></a><a name="initial"></a>
## Declaration & Initialisation
The declaration of a `kiwifruit` is as a type of `organic`.  Monikerless declarations are permissable, the IDE will assign `kiwifruit_`*`<uuid>`*, where *`<uuid>`* is the first four characters of its uuid declaration. `{kiwifruit}` can be declared with other types, most usually [`{plant}`](./plant.md) and/or `{vine}` when growing, or `{fruit}` when prepared for eating . Hierarchial, although optional, `{plant}` usually comes before `{vine}` before `{kiwifruit}`; and, `{fruit}` usually comes before `{kiwifruit}`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic{kiwifruit};`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({kiwifruit});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({kiwifruit},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({plant},{kiwifruit},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({vine},{kiwifruit},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({plant},{vine},{kiwifruit},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({fruit},{kiwifruit},`*`moniker`*`);`

<a name="assign"></a>
## Assignment
An `organic` can be assigned a `{kiwifruit}` anytime after declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`organic_moniker`*`,{kiwifruit});`

<a name="reference"></a>
## Referencing
Referencing a `kiwifruit` organic *object* is achieved with the `with` verb (or shortened `>_` notation), or the shortened `(`*`moniker`*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`kiwifruit_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_organic(`*`kiwifruit_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`kiwifruit_moniker1`*`,`*`kiwifruit_moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`kiwifruit_moniker`*`);`

<a name="DDS"></a>
## Discernment, Discrimination, and, Swarming
For discernment of `{kiwifruit}`s, use `🥝` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`⟦`*`…`*`🥝`*`…`*`⟧;`

Discrimination of `{kiwifruit}`s is possible using the `_oftype` function posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`_oftype{kiwifruit};`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`_oftype({kiwifruit});`

Only collective swarming is available for `{kiwifruit}`.

<a name="expression"></a>
## Expressions
The unicode `1F95D` character (`🥝`) is used for `kiwifruit` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`⟦`*`…`*`🥝`*`…`*`⟧;`

<a name="example"></a>
## Examples