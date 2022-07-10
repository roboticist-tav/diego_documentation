# Adicity (property)
The `adicity` property provides the information of *elements* or *members* of the preceeding *object*. There is no adicity *object*.

## <a name="arran"></a> Arrangement [`arran` `arn` `arrangem` `arrangement`]
When the `adicity` property is applied to a preceeding `arran`, the *element* information is provided as a comma-separated list (`,`), with the negative and positive ranges separated with a pipe (`|`). The default output of the `arran` *object* is also its `adicity` property, so the syntax is implied. There are no parameters.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<arran>`*`_adicity()`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<arran>`*

For example:
```diego
add_arran({int},arran1)_v(1,2,3,4,5,6,7,8);

(arran1)_pop()_pop()_pop();         // pop the last/end three elements

log_console()_(arran1)_adicity();   // 6,7,8|1,2,3,4,5
log_console()_(arran1);             // 6,7,8|1,2,3,4,5
```

## <a name="tempor"></a> Date [`tempor` `temporal`]
The `adicity` property is applied to the `tempor` *object* to provide details of *members* in the `tempor` *object* construction. The *member* information consists of the ISO 8601 / RFC 3339 implementation with Time Zone Extension and Calendar Extension. Any missing *members* are signified with a quesiton mark (`?`).

This property can be useful for testing: the extent of composition of the `tempor` construction; or, the understanding of a `tempor` as understood by a thingy. There are no parameters.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<tempor>`*`_adicity()`

Formating of the `adicity` property is achieved using the [`stringify`](../funct/stringify.md) *function*, for example:
```diego
// 4 December 1973	Pioneer 10 reaches Jupiter
// The convention for timezone in 'space' is UTC

add_tempor(pioneer💋Jupiter)_v(Dec 1973)_timezone(etc/utc);

log_console()_tempor(pioneer💋Jupiter)_adicity();  // 1973-12-??T??:??:??.????+??:??[Etc/UTC][u-ca=?]

with_tempor(pioneer💋Jupiter)_day(4);

log_console()_tempor(pioneer💋Jupiter)_adicity();  // 1973-12-04??:??:??.????+??:??[Etc/UTC][u-ca=?]

log_console()_tempor(pioneer💋Jupiter)_adicity()_stringify(JSON);
// =>
// {
//    "year":1973,
//    "month":12,
//    "day":4,
//    "dayofweek":2
// }
```
For a more detailed test of `date` composition, use the [`adicity`](./adicity.md) property.