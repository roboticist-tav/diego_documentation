# Year (property)
A `year` is a property to represent at temporal (Earth) year.  It has a shortened syntax of `yr`.

<a name="get"></a>
## Getting
To get the year from the proceeding object, use the `year` posit (or shortened `yr`). The return will be a numeric values represent an temporal year aspect of the preceding *object*. For a return representing a specific year (rather than an amount of years) the default format if not `format` posit is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_year();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_yr();`

For an *object* with an array of years, use the `index` (or shortened, `i`) posit to determine which year in the array you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_year()_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_yr()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
As the `year` posit with a *`year_value`* parameter to set the temporal year as a child (and so property) of the preceding *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_year(`*`year_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_year(`*`year_value`*`);`

Some *objects* allow for an array of years. To set an array of years, use multiple `year` posits. Alternatively an array can be used to set years in one `year` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_year(`*`{year_value1}`*`)_yr(`*`{year_value2}`*`)_`*`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_year([`*`year_array_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_yr([`*`year_array_moniker`*`]);`

<a name="type"></a>
## Typing
There are two types of *types* use for the `year` *property*: the first is the format of the string `{str}` output; and, the format of the numeric output.

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
In a similar way to typing, the `year` *property* can also be cast or formatted as a unit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_`*`<posit>`*`(❬year❭,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_`*`<posit>`*`(❬yr❭,`*`...`*`);`

<a name="cast"></a>
## Casting
Casting an `year` *property*  requires the `toyear` posit (or shortened `toyr`), both a single year and an array of years.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_toyear(`*`year_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_toyear(`*`{year_value_cast_to1}`*`)_toyr(`*`{year_value_cast_to2}`*`)_`*`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_toyear([`*`year_array__cast_to_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_toyr([`*`year_array__cast_to_moniker`*`]);`

<a name= "object"></a>
## Objecting
Objecting for the `year` *property* are mostly confined to preceding temporal *objects*. However, immediate preceding lesser temporal *objects* ([`milliyears`](./μs.md), and [`microyears`](./ms.md) siblings), will be skipped until either an elder sibling ([`hour`](./hr.md), [`jour`](./jour.md), [`day`](./day.md), [`month`](./mth.md), [`year`](./yr.md)) or a parent ([`tempor`](../obj/tempor.md)) precedes.



