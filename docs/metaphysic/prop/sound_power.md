# Sound Power (type)
The `{sound_power}` type of `metric` (_single mutable_), or `meter` (_multiple mutable_), or `spec`ification (_single immutable_), represents sound power or acoustic power, the rate at which sound energy is emitted, reflected, transmitted or received, per unit time. Sound power is defined[^sound_power] as "through a surface, the product of the sound pressure, and the component of the particle velocity, at a point on the surface in the direction normal to the surface, integrated over that surface." 


<a name="declare"></a>
## Declaration
The declaration of `{sound_power}` is through typing `metric` or `meter` or `spec` *objects*, either moniker or monikerless.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric({sound_power});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric({sound_power},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_meter({sound_power});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_meter({sound_power},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_spec({sound_power});`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_spec({sound_power},`*`moniker`*`);`

<a name="initial"></a>
## Initialisation
The value of `{sound_power}` of a `metric` or `meter` or `spec` can be initialised at declaration or after.  The unit can be provided using the double angled brackets (`⟪⟫`).  Any unit not stated are implied to be the default (or first initialisation of unit). Multiple values can be assigned for mutable *objects*, `metric` and `meter`. Range of values can also be assigned directly inside the `add_` declaration or with the `_range` property.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric({sound_power},`*`moniker`*`,`*`value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_meter({sound_power},`*`moniker`*`,`*`value`*`⟪`*`unit`*`⟫);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_spec({sound_power},`*`moniker`*`,`*`value`*`,⟪`*`unit`*`⟫);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric({sound_power},`*`moniker`*`,`*`value1`*`,`*`value2`*`,`*`value…`*`,⟪`*`unit`*`⟫);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_meter({sound_power},`*`moniker`*`,`*`range_from`*`-`*`range_to`*`⟪`*`unit`*`⟫);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_spec({sound_power},`*`moniker`*`)_range(`*`range_from`*`,`*`range_to`*`,⟪`*`unit`*`⟫);`

<a name="assign"></a>
## Assignment

<a name="reference"></a>
## Referencing
Referencing a ` ` *object* is achieved with the `with` verb, or the shortened `(`*` `*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`_moniker`*`);`

<a name="type"></a>
## Typing

<a name="get"></a>
## Getting

<a name="set"></a>
## Setting

<a name="cast"></a>
## Casting

<a name="properties"></a>
## Properties

<a name="example"></a>
## Examples




[^sound_power]:  [ISO 80000-8(en) Quantities and Units - Acoustics.](https://www.iso.org/obp/ui/#iso:std:iso:80000-8:ed-3:v1:en) [ISO].