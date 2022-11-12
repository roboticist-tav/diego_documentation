# Vegetable (type)
`{vegetable}` is a type of the [`organic`](./organic.md) *object*, representing a part of a plant than is consumed by humans or other animals for food.  The `vegetable` type also has a shortened syntax of `veg`.  In expressions the unicode `1F472` character (`🍲`) is used.

<a name="declare"></a><a name="initial"></a>
## Declaration & Initialisation
The declaration of a `vegetable` is as a type of `organic`.  It can be declared with other types, most usually [`plant`](./plant.md). Hierarchial, although optional, `{plant}` usually comes before `{vegetable}`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({vegetable},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({plant},{vegetable},`*`moniker`*`);`<br>

<a name="assign"></a>
## Assignment
An `organic` can be assigned a `{vegetable}` anytime after declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`organic_moniker`*`,{vegetable});`

<a name="reference"></a>
## Referencing
Referencing a `vegetable` organic *object* is achieved with the `with` verb (or shortened `>_` notation), or the shortened `(`*`moniker`*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`vegetable_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_organic(`*`vegetable_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`vegetable_moniker1`*`,`*`vegetable_moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`vegetable_moniker`*`);`

<a name="DDS"></a>
## Discernment, Discrimination, and, Swarming

<a name="expression"></a>
## Expressions
The unicode `1F372` character (`🍲`) is used for `vegetable` in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `⟦`*`…`*`🍲`*`…`*`⟧`

<a name="example"></a>
## Examples

