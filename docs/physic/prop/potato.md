# Potato (type)
`{potato}` (or `{🥔}`) is a type of the [`organic`](./organic.md) *object*, representing a potato, a starchy plant tuber which is one of the most important food crops, cooked and eaten as a vegetable. The `{potato}` type is a sub-type of `{vegetable}`. In expressions the unicode `1F954` character (`🥔`) is used.

<a name="declare"></a><a name="initial"></a>
## Declaration & Initialisation
The declaration of a `potato` is as a type of `organic`.  Monikerless declarations are permissable, the IDE will assign `potato_`*`<uuid>`*, where *`<uuid>`* is the first four characters of its uuid declaration. `{potato}` can be declared with other types, most usually [`{plant}`](./plant.md) when growing, or `{vegetable}` when prepared for eating . Hierarchial, although optional, `{plant}` usually comes before `{potato}`; and, `{vegetable}` usually comes before `{potato}`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic{potato};`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({potato});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({potato},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({plant},{potato},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({vegetable},{potato},`*`moniker`*`);`

<a name="assign"></a>
## Assignment
An `organic` can be assigned a `{potato}` anytime after declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`organic_moniker`*`,{potato});`

<a name="reference"></a>
## Referencing
Referencing a `potato` organic *object* is achieved with the `with` verb (or shortened `>_` notation), or the shortened `(`*`moniker`*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`potato_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_organic(`*`potato_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`potato_moniker1`*`,`*`potato_moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`potato_moniker`*`);`

<a name="DDS"></a>
## Discernment, Discrimination, and, Swarming
For discernment of `{potato}`s, use `🥔` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`⟦`*`…`*`🥔`*`…`*`⟧;`

Discrimination of `{potato}`s is possible using the `_oftype` function posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`_oftype{potato};`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`_oftype({potato});`

Only collective swarming is available for `{potato}`.

<a name="expression"></a>
## Expressions
The unicode `1F954` character (`🥔`) is used for `potato` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`⟦`*`…`*`🥔`*`…`*`⟧;`

<a name="example"></a>
## Examples