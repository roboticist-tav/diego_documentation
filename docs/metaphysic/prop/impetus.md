# Impetus (property)

<a name="impetus"></a>
### Impetus
The [*types*]( ./type.md#drone) of `drone` are divided by their configuration of mechanisms for 'lift' and 'propulsion' and 'steer' (*pitch*, *roll*, *yaw*).

| lift | propulsion | steer | `{type}` | operator | description | API |
| --- | --- | --- | --- | --- | --- | -- |
| <a name=""></a> rotor | tilt | transverse rotor | `{}` |  | []() |
| <a name=""></a> rotor | tiltrotor | transverse rotor | `{}` |  | []() |
| <a name=""></a> rotor | jet | transverse rotor | `{}` |  | []() |
| <a name=""></a> rotor-array | rotor-array | rotor-array | `{}` |  | [a]() |
| <a name=""></a> counterotor-array | counterotor-array | counterotor-array | `{}` |  | [a]() |
| <a name=""></a> rotor |  | `{}` |  | []() |
| <a name=""></a>  | | `{}` |  | []() |
| <a name=""></a>  | | `{}` |  | []() |
| <a name=""></a>  | | `{}` |  | []() |

| <a name=""></a> rotor | rotor array | `{}` |  | []() |
| <a name="_blackberry"></a> `{bb}` &nbsp; `{blackberry}` | :: | Cell phone running on Blackberry&reg; operating system. | [bb](../../physic/prop/bb.md#blackberry) |
| <a name="_iOS"></a> `{ios}` &nbsp; `{iphone}` &nbsp; `{apple}` | :: | Cell phone running on Apple&reg; iOS&#8482;. | [ios](../../physic/prop/ios.md#cellphone) |
| <a name="_windows"></a> `{win}` &nbsp; `{ms}` &nbsp; `{microsoft}` | :: | Cell phone running on Microsoft&reg; Windows Mobile&#8482;. | [win](../../physic/prop/win_mobile.md#cellphone) |

https://en.wikipedia.org/wiki/Tiltrotor
https://en.wikipedia.org/wiki/Counter-rotating_propellers

## Objects

<a name="drones"></a>
### Drones


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