# Temporal Frequency (property)
The `freq` *property* with the `{tempor}` *type* provides a temporal regulated rate of events for a proceeding *object* (temporal frequency). The lengthened terms `frequen`, `frequent`, and, `frequency` can be used freely and interchangeably. A frequency expression is available, using the mathematical italic f symbol and square brackets (`𝑓[]`).

<a name="declare"></a>
## Declaration
Although the most common use of the temporal `freq` (or lengthened `frequen`, `frequent`, `frequency`) *property* is via a posit with given unit and expression, the temporal `freq` *property* can be declared using the `add_` verb, the `{tempor}` *type*, and, a *moniker*. Multiple temporal `freq`s cannot be declared with a single temporal `freq` declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_freq({tempor},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_freq({tempor},`*`moniker`*`);`

It is common to declare the temporal `freq` *property* using its posit with a *`frequency_expression`* provided. If the frequency expression is assigned at declaration then the `❬`*`unit`*`❭` must be given, enclosed in angle brackets (`❬❭`). For temporal `freq`encies the `{tempor}` type must also be declared. The use of a *moniker*, is optional, but if used with a frequency expression it must be enclosed in moniker brackets (`⟦⟧`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_freq({tempor},❬`*`unit`*`❭,`*`frequency_expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_freq({tempor},❬`*`unit`*`❭,`*`frequency_expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_freq(⟦`*`moniker`*`⟧,{tempor},❬`*`unit`*`❭,`*`frequency_expression`*`);`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_freq(⟦`*`moniker`*`⟧,{tempor},❬`*`unit`*`❭,`*`frequency_expression`*`);`<br>

<a name="reference"></a>
## Referencing
Referencing a temporal `freq` *property* is achieved with the `with` verb, or the shortened `(`*`frequency_moniker`*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_freq(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`frequency_moniker`*`);`

<a name="assign"></a>
## Assignment
Assignments to the temporal `freq` *property* are achieved by using proceeding posits.


add_poll({track},charger_share)
	()_quest(energy_level)_gauge({nrg})_v(❬urgency❭);
	()_freq("quarter_hr",❬min❭,15);
;
7152273a91ae8a6be1e696d96c4104c2
7152273a91ae8a6be1e696d96c4104c2
with_poll(charger_share)_offreq(quarter_hr)_i()_quest(energy_level)_enum(nonurgent);

<a name="posit"></a>
## Posits

| `_posit` | description | API |
| --- | --- | --- |
| <a name="temporfrom"> `_temporfrom` | A `tempor` to start the preceding *object* with the proceeding *object* definitions. | [temporfrom](../condit/temporfrom.md#freq)


---

<a name="seealso"></a>
## See Also

* Statistical Frequency
* Spatial Frequency 



<a name="declare"></a>
## Declaration

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment

<a name="initial"></a>
## Initialisation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="assign"></a>
## Assignment

<a name="reference"></a>
## Referencing
Referencing a ` ` *object* is achieved with the `with` verb, or the shortened `(`*` `*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker1`*`,`*`moniker2`*`,`*`...`*`);`<br>
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