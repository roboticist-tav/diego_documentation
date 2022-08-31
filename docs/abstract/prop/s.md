# Second (property)
A `second` is a property to represent at temporal (Earth) second or $\frac{1}{3600}$ of a hour.  It has a shortened syntax of `sec`.

<a name="get"></a>
## Getting
To get the second from the proceeding object, use the `second` posit (or shortened `sec`). The return will be a numeric values represent an temporal second aspect of the preceding *object*. For a return representing a specific second (rather than an amount of seconds) the default format is used, if not `format` posit is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_second();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sec();`

For an *object* with an array of seconds, use the `index` (or shortened, `i`) posit to determine which second in the array you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_second()_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sec()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
As the `second` posit with a *`second_value`* parameter to set the temporal second as a child (and so property) of the preceding *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_second(`*`second_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sec(`*`second_value`*`);`

Some *objects* allow for an array of seconds. To set an array of seconds, use multiple `second` posits. Alternatively an array can be used to set seconds in one `second` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_second(`*`{second_value1}`*`)_sec(`*`{second_value2}`*`)_`*`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_second([`*`second_array_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sec([`*`second_array_moniker`*`]);`

<a name="type"></a>
## Typing
There are two types of *types* use for the `second` *property*: the first is the format of the string `{str}` output; and, the format of the numeric output.

Format Output:

| `{type}` | Output Range | Description |
| --- | --- | --- |
| <a name=""></a> `{}` | ` ` | . |

Numeric Output:

| `{type}` | Description |
| --- | --- |
| <a name=""></a> `{}` | ` ` | . |

<a name="unit"></a>
## Uniting
In a similar way to typing, the `second` *property* can also be cast or formatted as a unit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_`*`<posit>`*`(❬second❭,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_`*`<posit>`*`(❬sec❭,`*`...`*`);`

<a name="cast"></a>
## Casting
Casting an `second` *property*  requires the `tosecond` posit (or shortened `tosec`), both a single second and an array of seconds.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tosecond(`*`second_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tosecond(`*`{second_value_cast_to1}`*`)_tosec(`*`{second_value_cast_to2}`*`)_`*`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tosecond([`*`second_array__cast_to_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_tosec([`*`second_array__cast_to_moniker`*`]);`

<a name= "object"></a>
## Objecting
Objecting for the `second` *property* are mostly confined to preceding temporal *objects*. However, immediate preceding lesser temporal *objects* ([`milliseconds`](./μs.md), and [`microseconds`](./ms.md) siblings), will be skipped until either an elder sibling ([`hour`](./hr.md), [`jour`](./jour.md), [`day`](./day.md), [`month`](./mth.md), [`year`](./yr.md)) or a parent ([`tempor`](../obj/tempor.md)) precedes.



