# Millisecond (property)
A `millisecond` is a property to represent at temporal (Earth) millisecond or $\frac{1}{1000}$ of a [second](./s.md).  It has a shortened syntax of `ms`.

<a name="get"></a>
## Getting
To get the millisecond from the proceeding object, use the `millisecond` posit (or shortened `ms`). The return will be a numeric values represent an temporal millisecond aspect of the preceding *object*. For a return representing a specific millisecond (rather than an amount of millisecond) the default format is used, if not `format` posit is used.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_millisecond();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ms();`

For an *object* with an array of seconds, use the `index` (or shortened, `i`) posit to determine which second in the array you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_millisecond()_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ms_()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
As the `millisecond` posit with a *`millisecond_value`* parameter to set the temporal millisecond as a child (and so property) of the preceding *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_millisecond(`*`millisecond_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ms(`*`millisecond_value`*`);`

Some *objects* allow for an array of milliseconds. To set an array of milliseconds, use multiple `millisecond` posits. Alternatively an array can be used to set seconds in one `millisecond` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_millisecond(`*`{millisecond_value1}`*`)_ms(`*`{millisecond_value2}`*`)_`*`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_millisecond([`*`millisecond_array_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ms([`*`millisecond_array_moniker`*`]);`