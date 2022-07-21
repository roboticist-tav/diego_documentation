# Type (property)
The `type` property exposes the type or first category of the preceding *object* in physical and metaphysical contexts. In an abstract context, the type becomes the [datatype](../../abstract/dt/datatype.md) of primitives.

## Retrieval
Retrieval of the `type` *property* requires an empty parameter set of the `_type` posit. This will retrieve the type of the preceding *object*. The default format of the output will be via a type moniker surrounded in curly brackets (`{}`). The use of the `_value` (or shortened `_v`) posit is automatically implied and is not necessary. For the type of a proceeding *object*, use `type`s '*sibling*' property, `_typeof`. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_type();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_typeof(`*`object_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_type()_value();`

The `type` *properties* can be passed to an abstract storage *object* using the `_to`*`<object>`* syntax.  For instance for a *variable* (`var`) or an *array* (`ary`), the `_tovar` and `_toary` posit are use, respectively.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_type()_tovar(`*`variable_name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_typeof(`*`obj_moniker`*`)_tovar(`*`variable_name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_type()_toary(`*`ary_name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_typeof(`*`obj_moniker`*`)_toary(`*`ary_name`*`);`<br>

## Operator
The *of*`type` and `typeof` properties also have the associated `⊖` operator for use in expressions. The `⊖` operator should be used in expressions. The `⊖` operator should not used for 'symmetric difference in set theory, which should only use delta (`Δ`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<expression_posit>(`*`...⊖...`*`);`

## Declaration
Declaration requires either, the use of: the `_type` posit; or, direct declaration (usually in the declaration of the *object*) using curly brackets (`{}`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_type(`*`type`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_`*`<object>`*`({`*`type`*`},`*`obj_moniker`*`);`

!!! Important
    Syntax can be switched from declaration to retrieval upon various *verbs* used, such as `tell_`.  This most often occurs with non-human communication.

## Objects
The `type` property is a base fundamental property, so there are many associated preceding *objects*.

| `object` | description | API |
| --- | --- | --- |
| <a name="cellphone"></a> `cellphone` | The operating system the `cellphone` is running on, is used as its type. | [cellphone](../../physic/obj/cellphone.md#types) |
| <a name="thingy"></a> `thingy` | There are four types of thingy: [`human`](../../physic/obj/human.md); [`organic`](../../physic/obj/organic.md); [`robot`](../../physic/obj/robot.md); and, [`thing`](../../physic/obj/thing.md). | [thingy](../../physic/obj/thingy.md#types) |
| <a name="organic"></a> `organic` | `organic` types are those objects derived from common objects used in machine-learning visacuity[^visacuity]. | [organic](../../physic/obj/organic.md#types) |
| <a name=""></a> `` |  | [](#type) |
| <a name=""></a> `` |  | [](#type) |
| <a name=""></a> `` |  | [](#type) |
| <a name=""></a> `` |  | [](#type) |
| <a name=""></a> `` |  | [](#type) |
| <a name=""></a> `` |  | [](#type) |
| <a name=""></a> `` |  | [](#type) |

<a name="computer"></a>
### Computer



![OS Market Share](/_img/StatCounter-os_combined-ww-monthly-202101-202112.png)

<sub>OS Market Share<br>Source: [StatCounter Global Stats](https://gs.statcounter.com/os-market-share/desktop/worldwide/2021)</sub>

| `{type}` | description | API |
| --- | --- | --- |
| <a name="win"></a>  `{win}` | Microsoft&reg; Windows&#8482;. | [win](#type) |
| <a name="android"></a> `{osx}` &nbsp; `{os_x}` | Apple&reg; OS X&#8482;. | [osx](#type) |
| <a name="linux"></a> `{linux}` | Linux.  | [linux](#type) |
| <a name=""></a> `{chrome}` &nbsp; `{chrome}` &nbsp; `{chrome_os}` | Google&reg; Chrome OS&#8482;. | [chrome](#type) |

[^visacuity]: A portmanteau of 'vision' and 'acuity', representing machine-learning of thingies to identify common object in context by graphic depiction.  Formally known as 'computer vision'.