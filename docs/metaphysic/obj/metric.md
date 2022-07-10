# Metric (object)



add_metric({name/uuid})
	_scalar({scalar}[, {unit}])
	_unit({unit})
	_for({name/uuid_1}[, ...{name/uuid_n}])
	_pulse()
	_tracker()


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric(`*`moniker`*`)_set(...)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `set_metric(`*`moniker`*`,settings...)`<br>

## Properties

| property | datatype / unit | description |
| --- | --- | --- |
| `scalar` | {id} / {id_3}[^3btyehex] | A 3 Byte hexidecimal unique idendifier used in adsb messaging |

## Posits

| posit | datatype / unit | description |
| --- | --- | --- |
| `_scalar(`*`moniker`*`)`<br>`_scalar({dt},`*`moniker`*`)` | {id} / {id_3}[^3btyehex] | A 3 Byte hexidecimal unique idendifier used in adsb messaging |


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