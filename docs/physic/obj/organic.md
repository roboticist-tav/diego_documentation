# Organic (object)
The `organic` *object* is a derivative of `thingy` and one of the four main hierarchical thingy types.  The `organic` *object* is a representation of a non-human being, present and alive in the physical 'real' world.

```mermaid
flowchart TD
    thingy((thingy)) --> human([human])
    thingy --> organic([organic])
    thingy --> robot([robot])
    thingy --> thing([thing])

    organic2([organic]) --> fauna{{fauna}}
    organic2([organic]) --> flora{{flora}}
```
<div style="text-align: right"><sub>Genera of Thingies</sub></div><br>

## Declaration
The default declaration of the `organic` *object* is to at least provide a *moniker*. A type can be provided at declaration using curly brackets (`{}`). All *types* of `organic` are not available to be declared by name.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({`*`type`*`},`*`moniker`*`);`

## Referencing
To reference the `organic`, use, either the `with` verb or the shortened syntax using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced. All *types* of `organic` are not available to be referenced by name.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic({`*`type`*`,`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`organic_moniker`*`);`

<a name="types"></a>
## Typing
The [*types*](../../metaphysic/prop/type.md#organic) of the `organic` *object* are those objects derived from common objects used in machine-learning visacuity.

| `type` &nbsp; `operator` | coco identifier |description | API |
| --- | --- | --- | -- |
| <a name="{bear}"></a> `{bear}` &nbsp; `{🐻}` | ![coco](https://cocodataset.org/images/cocoicons/23.jpg) | bear | [bear](#bear) |
| <a name="{bird}"></a> `{bird}` &nbsp; `{🐦}` | ![coco](https://cocodataset.org/images/cocoicons/16.jpg) | bird | [bird](#bird) |
| <a name="{cat}"></a> `{cat}` &nbsp; `{🐈}` | ![coco](https://cocodataset.org/images/cocoicons/17.jpg) | cat | [cat](./cat.md) |
| <a name="{cow}"></a> `{cow}` &nbsp; `{🐄}` &nbsp; `{🐮}` | ![coco](https://cocodataset.org/images/cocoicons/21.jpg) | cow | [cow](#cow) |
| <a name="{dog}"></a> `{dog}` &nbsp; `{🐕}` | ![coco](https://cocodataset.org/images/cocoicons/18.jpg) | dog | [dog](#dog) |
| <a name="{elephant}"></a> `{elephant}` &nbsp; `{🐘}` | ![coco](https://cocodataset.org/images/cocoicons/22.jpg) | elephant | [elephant](#elephant) |
| <a name="{giraffe}"></a> `{giraffe}` &nbsp; 🦒 | ![coco](https://cocodataset.org/images/cocoicons/25.jpg) | giraffe | [giraffe](#giraffe) |
| <a name="{horse}"></a> `{horse}` &nbsp; 🐎 &nbsp; 🐴 | ![coco](https://cocodataset.org/images/cocoicons/19.jpg) | horse | [horse](#horse) |
| <a name="{sheep}"></a> `{sheep}` &nbsp; 🐑 | ![coco](https://cocodataset.org/images/cocoicons/20.jpg) | sheep | [sheep](#sheep) |
| <a name="{zebra}"></a> `{zebra}` &nbsp; 🦓 | ![coco](https://cocodataset.org/images/cocoicons/24.jpg) | zebra | [zebra](#zebra) |

<a name="bear"></a>
## Bear (type)
`bear` is a *type* of the `organic` *object*, representing a physical living animal (bear).

### Declaration & Assignment
The `bear` *type* can only be declared, assigned and referenced through the `organic` *object*, defining the *type* by using curly brackets (`{}`), as such: `{bear}`.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic({bear},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_organic(`*`moniker`*`)_type(bear);`

### Referencing
To reference the `bear` *type*, use, either `with_organic` or shortened referencing using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_organic({bear},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`bear_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `({bear},`*`organic_moniker`*`);`<br>

### Expressions
There is an bear operator (🐻), to be used in expressions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<...>`*`_`*`<expression_posit>`*`(`*`...`*`🐻`*`...`*`);`

### Visacuity

![bear](../../_img/bear.png)<br><sub>Source: [#212688 Coco Explorer](https://cocodataset.org/#explore?id=212688)</sub>

<a name="bird"></a>
#### Bird (type)


<a name="cow"></a>
## Cow (type)

<a name="dog"></a>
## Dog (type)

<a name="elephant"></a>
## Elephant (type)

<a name="giraffe"></a>
## Giraffe (type)

<a name="horse"></a>
## Horse (type)

<a name="sheep"></a>
## Sheep (type)

<a name="zebra"></a>
## Zebra (type)