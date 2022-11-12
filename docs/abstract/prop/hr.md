# Hour (property)
A `hour` is a property to represent at temporal (Earth) hour.  It has a shortened syntax of `hr`.

<a name="get"></a>
## Getting
To get the hour from the proceeding object, use the `hour` posit (or shortened `hr`). The return will be a numeric values represent an temporal hour aspect of the preceding *object*. For a return representing a specific hours (rather than an amount of hours) the default format if not `format` posit is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hr();`

For an *object* with an array of hours, use the `index` (or shortened, `i`) posit to determine which hour in the array you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour()_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hr()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
As the `hour` posit with a *`hour_value`* paramter to set the temporal hour as a child (and so property) of the preceding *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour(`*`hour_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour(`*`hour_value`*`);`

Some *objects* allow for an array of hours. To set an array of hours, use multiple `hour` posits. Alternatively an array can be used to set hours in one `hour` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour(`*`{hour_value1}`*`)_hr(`*`{hour_value2}`*`)_`*`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour([`*`hour_array_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hr([`*`hour_array_moniker`*`]);`

<a name="type"></a>
## Typing
There are two types of *types* use for the `hour` *property*: the first is the format of the string `{str}` output; and, the format of the numeric output.

Format Output:

| `{type}` | Output Range | Description |
| --- | --- | --- |
| <a name="h"></a> `{h}` | `0,1,…12,1…11` | Hour integer without leading zero. |
| <a name="hh"></a> `{hh}` | `00,01,…12,01…11` | Hour integer with leading zero. |
| <a name="H"></a> `{H}` | `0,1,…12,13…23` | 24-Hour integer without leading zero. |
| <a name="HH"></a> `{HH}` | `00,01,…12,13…23` | 24-Hour integer with leading zero. |

Numeric Output:

| `{type}` | Description |
| --- | --- |
| <a name="dh"></a> `{dh}` | Decimal hour, up to default decimal places. The default precision is one second equals `0.016666667`. Precision can be changed using the `precision` *function*. |
| <a name="h:m"></a> `{h:m}`  | Hours as integers and the minutes as _'firsts'_ ($\frac{1}{60}$) of the hour, separated by commas (`:`). |
| <a name="h:m:s"></a> `{h:m:s}` | Hours as integers and the minutes as _'firsts'_ ($\frac{1}{60}$) of the hour, and seconds as _'seconds'_ ($\frac{1}{3600}$) of the hour, separated by commas (`:`). |

<a name="unit"></a>
## Uniting
In a similar way to typing, the `hour` *property* can also be cast or formatted as a unit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_`*`<posit>`*`(❬hour❭,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_`*`<posit>`*`(❬hr❭,`*`…`*`);`

<a name="cast"></a>
## Casting
Casting an `hour` *property*  requires the `tohour` posit (or shortened `tohr`), both a single hour and an array of hours.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tohour(`*`hour_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tohour(`*`{hour_value_cast_to1}`*`)_tohr(`*`{hour_value_cast_to2}`*`)_`*`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tohour([`*`hour_array__cast_to_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tohr([`*`hour_array__cast_to_moniker`*`]);`

<a name= "object"></a>
## Objecting
Objecting for the `hour` *property* are mostly confined to preceding temporal *objects*. However, immediate preceding lesser temporal *objects* ([`seconds`](./s.md), [`milliseconds`](./μs.md), and [`microseconds`](./ms.md) siblings), will be skipped until either an elder sibling ([`jour`](./jour.md), [`day`](./day.md), [`month`](./mth.md), [`year`](./yr.md)) or a parent ([`tempor`](../obj/tempor.md)) precedes.

<a name= "min"></a>
### Minute
With `minute` as the preceding *object* the `hour` posit will 
