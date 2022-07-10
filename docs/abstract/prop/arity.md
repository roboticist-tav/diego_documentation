# Arity (property)
The `arity` property provides the entire count *members* of the preceeding *object*, as a integer (`{int}`). It is most commonly used in collection *objects*, but this property in also available as a posit for non-collection *objects*. There is no arity *object*.

## <a name="arran"></a> Arrangement [`arran` `arn` `arrangem` `arrangement`]
The common use of the `arity` property is as a posit applied to a preceeding `arran`.  This is used to provide the count of elements in the `arran` from **both** the negative range and the positive range. There are no parameters.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<arran>`*`_arity()`

The [`length`](./length.md) property of an `arran` can sometimes be confused with the `arity` property, but, the `length` (or `len`) property for `arran`s only provides the positive range. For example:
```diego
add_arran({int},arran1)_v(1,2,3,4,5,6,7,8);

(arran1)_pop()_pop()_pop();       // pop the last/end three elements

log_console()_(arran1);           // 6,7,8|1,2,3,4,5
log_console()_(arran1)_length();  // 5
log_console()_(arran1)_arity();   // 8
```

## <a name="array"></a> Array [`array` `ary`]
Due to the simularities of the `array` with the `arran` *object*, the `arity` property is provided for `array`s.  However, unlike `arran`s, `array`s are not allowed a negative range, so the `arity` property becomes a equivalent to the `_length` (also `_len`) property. There are no parameters.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<array>`*`_arity()`

...is identical to...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<array>`*`_length()`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<array>`*`_len()`

## <a name="date"></a> Date [`date`]
The `arity` property is applied to the `date` *object* to provide the count of elements in the `date` *object* construction. This can be useful for testing: the extent of composition of the `date` construction; or, the understanding of a `date` by a thingy. There are no parameters.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<date>`*`_arity()`

For example:
```diego
add_date(independenceDay)_v(04-Jul);

log_console()_date(independenceDay)_arity();  // 2

with_date(independenceDay)_year(1776);

log_console()_date(independenceDay)_arity();  // 3
```
For a more detailed test of `date` composition, use the [`adicity`](./adicity.md) property.


