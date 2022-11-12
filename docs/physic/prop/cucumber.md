# Cucumber (type)
`{cucumber}` is a type of the [`organic`](./organic.md) *object*, representing a cucumber, a long, green-skinned fruit with watery flesh, usually eaten raw in salads or pickled. The `{cucumber}` type is a sub-type of `{fruit}`. In expressions the unicode `1F952` character (`🥒`) is used.

<a name="declare"></a><a name="initial"></a>
## Declaration & Initialisation
The declaration of a `cucumber` is as a type of `organic`.  Monikerless declarations are permissable, the IDE will assign `cucumber_`*`<uuid>`*, where *`<uuid>`* is the first four characters of its uuid declaration. `{cucumber}` can be declared with other types, most usually [`{plant}`](./plant.md) when growing, or `{fruit}` when prepared for eating . Hierarchial, although optional, `{plant}` usually comes before `{cucumber}`; and, `{fruit}` usually comes before `{cucumber}`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic{cucumber};`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({cucumber});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({cucumber},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({plant},{cucumber},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({fruit},{cucumber},`*`moniker`*`);`

<a name="assign"></a>
## Assignment
An `organic` can be assigned a `{cucumber}` anytime after declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`organic_moniker`*`,{cucumber});`

<a name="reference"></a>
## Referencing
Referencing a `cucumber` organic *object* is achieved with the `with` verb (or shortened `>_` notation), or the shortened `(`*`moniker`*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`cucumber_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_organic(`*`cucumber_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`cucumber_moniker1`*`,`*`cucumber_moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`cucumber_moniker`*`);`

<a name="DDS"></a>
## Discernment, Discrimination, and, Swarming
For discernment of `{cucumber}`s, use `🥒` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`⟦`*`…`*`🥒`*`…`*`⟧;`

Discrimination of `{cucumber}`s is possible using the `_oftype` function posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`_oftype{cucumber};`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`_oftype({cucumber});`

Only collective swarming is available for `{cucumber}`.

<a name="expression"></a>
## Expressions
The unicode `1F952` character (`🥒`) is used for `cucumber` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*`⟦`*`…`*`🥒`*`…`*`⟧;`

<a name="example"></a>
## Examples