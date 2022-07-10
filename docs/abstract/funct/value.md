# Value

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