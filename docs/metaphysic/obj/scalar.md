# Scalar (object)

## <a name="datamgt"></a> Data Management

| data management | notes<br>examples | API |
|--|:--|--|
| `attr`, `attribute` <a name="arena"></a> | Each `attr` is a immutable name-value pair (`{monniker|uuid}` as the name, `_value({value})` as the value). All data held in an `attr` should be immutable and have a one-to-one relationship (one name for one value).<br>Example: `add_attr(last_name)_value(Jones);` <br>See also: [spec](#spec) | [attr](/attr.md) |
| `blob` <a name="blob"></a> | **B**inary **L**arge **OB**ject |
| `var`, `variable` | | [var](/var.md) |
| `dict`, `dictionary` | | |
| `metric` | | [metric](/metric.md) |
| `scalar`
| `array`
| 

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