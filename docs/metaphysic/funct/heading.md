# Heading (function)
The `heading` function provides orientation in the frame of the `map` *object* being referenced.  It is irrespective of the momentum (i.e. 'line of travel') of the moving thingy, and only includes the 'right-hand-rule' pointing to the north pole on the referenced `map` from the centrepoint of the thingy, regardless of the orientation of the thingy to it momentum.

Only measurable values are provided for the `heading` function, for string values (e.g. Norht-West, SW, *etc…*) use [`bearing`](./bearing.md) function.

## Syntax
Declaration and assignment of *heading* is supplied using only one parameter, show here as *`heading`*. The function will use the provided *heading* for the preceeding object for all its applicable *objects*. The unit can be provided with the heading, using the angle brackets (`❬❭`), however, the units are usally declared with the `map` object. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_heading(❬`*`unit`*`❭,`*`heading`*`);`

<a name="unit"></a>
## Units
The unit can be provided with the heading, using the angle brackets (`❬❭`), however, the units are usally declared with the `map` object. Any units declared with the `heading` function are cast to the `map` units by the callee automatically.  Length or Earth coordinate units are used with `heading`.

| `❬unit❭` | description | API |
| --- | --- | --- |
| <a name="❬❭"></a> `❬❭` | Use the default units, either from setters or set on the map. This can easier to omit. | [unit](./unit.md) |
| <a name="❬num❭"></a> `❬num❭` | No unit used, uses only numeric values.<br>Numeric values can be provided as a three digit bearing values, e.g. "015", as 15°. | [num](../dt/num.md#num) |
| <a name="❬dd❭"></a> `❬dd❭` &nbsp; `❬deg❭` &nbsp; `❬dec_deg❭` | Using decimal degrees, usually to 6 decimal places, or set with `_precision` posit. | [dd](../dt/dd.md) |
| <a name="❬dm❭"></a> `❬dm❭` | Using degrees and decimal minutes. | [dm](../dt/dm.md) |
| <a name="❬dms❭"></a> `❬dms❭` | Using degrees, minutes, and, seconds. | [dms](../dt/dms.md) |
| <a name="❬rad❭"></a> `❬rad❭` | Using radians usually to 6 decimal places, or set with `_precision` posit. | [rad](../dt/rad.md) |
| <a name="❬si❭"></a> `❬μm❭` &nbsp; `❬mm❭` &nbsp; `❬cm❭` &nbsp; `❬dm❭`<br>`❬m❭`<br>`❬dam❭` &nbsp; `❬hm❭` &nbsp; `❬km❭` *etc…*  | Using SI length units. | [SI](../dt/si.md#length) |
| <a name="❬imp❭"></a> `❬thou❭` &nbsp; `❬inch❭` &nbsp; `❬"❭` &nbsp; `❬ft❭` &nbsp; `❬foot❭` &nbsp; `❬'❭` &nbsp; `❬yd❭` &nbsp; `❬yard❭` &nbsp; `❬mile❭` &nbsp; `❬league❭` | Using imperial length units. | [Imperial](../dt/imperial.md#length) |
| <a name="❬marine❭"></a> `❬fathom❭` &nbsp; `❬n_mile❭` | Using marine length units. | [Imperial](../dt/imperial.md#marine_length) |
| <a name="❬uss❭"></a> `❬chain❭` &nbsp; `❬rod❭` | Using US surveying length units. | [Imperial](../dt/imperial.md#us_survey_length) |

Other [coordinate units](http://epsg.io/?q=units%20kind%3ALENUNIT), like *[chains](http://epsg.io/?q=chain%20kind%3AUNIT)*, are available.  Also see the [`coords`](../obj/coords.md) *object* and the [`datum`](./datum.md) function.

## Objects
The *objects* that use the `heading` function are associated with mapping and routing.

| `object` | description | API |
| --- | --- | --- |
| <a name="pose"></a> `pose` |A representation of an orientation at a physical point. | [Pose](#pose) |
| <a name="way"></a> `way` | A pair of `pose` *objects*, representing their orientational and physical relationship. | [Way](#way) |
| <a name="❬dd❭"></a> `❬dd❭` &nbsp; `❬deg❭` &nbsp; `❬dec_deg❭` | Using decimal degrees, usually to 6 decimal places, or set with `_precision` posit. | [dd](../dt/dd.md) |
| <a name="❬dm❭"></a> `❬dm❭` | Using degrees and decimal minutes. | [dm](../dt/dm.md) |
| <a name="❬dms❭"></a> `❬dms❭` | Using degrees, minutes, and, seconds. | [dms](../dt/dms.md) |
| <a name="❬rad❭"></a> `❬rad❭` | Using radians usually to 6 decimal places, or set with `_precision` posit. | [rad](../dt/rad.md) |
| <a name="❬si❭"></a> `❬μm❭` &nbsp; `❬mm❭` &nbsp; `❬cm❭` &nbsp; `❬dm❭`<br>`❬m❭`<br>`❬dam❭` &nbsp; `❬hm❭` &nbsp; `❬km❭` *etc…*  | Using SI length units. | [SI](../dt/m.md) |
| <a name="❬imp❭"></a> `❬thou❭` &nbsp; `❬inch❭` &nbsp; `❬"❭` &nbsp; `❬ft❭` &nbsp; `❬foot❭` &nbsp; `❬'❭` &nbsp; `❬yd❭` &nbsp; `❬yard❭` &nbsp; `❬mile❭` &nbsp; `❬league❭` | Using imperial length units. | [Imperial](../dt/imperial.md#length) |
| <a name="❬marine❭"></a> `❬fathom❭` &nbsp; `❬n_mile❭` | Using marine length units. | [Imperial](../dt/imperial.md#marine_length) |
| <a name="❬uss❭"></a> `❬chain❭` &nbsp; `❬rod❭` | Using US surveying length units. | [Imperial](../dt/imperial.md#us_survey_length) |


<a name="pose"></a>
### Pose
The `pose` *object* is a representation of an orientation at a physical point. For time-frame reference a thingy will usually use the `_orientatat` function, however, navigation can be use `heading` values.  It is usual to provide `heading` as an additional resource for mapping rather than routing.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_pose(`*`moniker`*`)_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_pose(`*`moniker`*`)_heading(❬dec_deg❭,`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_pose(`*`moniker`*`)_heading(❬rad❭`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_pose(`*`moniker`*`)_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker`*`)_heading(`*`heading`*`);`

<a name="way"></a>
## Way
The `way` *object* is a pair of `pose` *objects*, representing their orientational and physical relationship. The `way` *object* needs two orientations to be effective, and the orientations, as headings, can be provided using the `_out`, `_in`, and, `_outin` posits.  The proceeding `_heading` posit provides the orientation in terms of heading to the preceeding out/in posits.  The heading relies on the maps being used, or to be used.  The `map` *object* should be know to the thingy beforehand.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_way(`*`moniker`*`)_out()_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_way(`*`moniker`*`)_in()_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_way(`*`moniker`*`)_out()_in()_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_way(`*`moniker`*`)_outin()_heading(`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`waymoniker`*`)_out()_heading(`*`heading`*`)_in()_heading(`*`heading`*`);`

The *`heading`* *parameter* should be supplied in the unit settings of the map, usually decimal degrees, however, the unit can be specified in the `heading` using the angle brackets (`❬❭`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_way(`*`moniker`*`)_out()_heading❬`*`unit`*`❭,`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_way(`*`moniker`*`)_in()_heading❬`*`unit`*`❭,`*`heading`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_way(`*`moniker`*`)_outin()_heading❬`*`unit`*`❭,`*`heading`*`);`

<a name="course"></a>
## Course

<a name="excurs"></a>
## Excurs

<a name="goal"></a>
## Goal

<a name="trip"></a>
## Trip

<a name="journ"></a>
## Journ

<a name="tour"></a>
## Tour

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