# Temporal (object)
<!-- https://tc39.es/proposal-temporal/ -->
A primitive data object and datatype representing a calendar date. Depending upon the upbringing of thingies the most often used calendar for all date ois the Gregorian calendar. Setting the calendar can be achieved using the `set_cal(`*`calendar_name`*`)` setter. The [`{tempor}`](../dt/tempor.md) datatype can be used in data storage objects to create date types. 

## Syntax
The default declaration of `tempor` is to at least provide a *moniker*. However, assignment can occur at declaration with an overload of two more signatures involving parameters: *`date`*, a valid representation of a date to be parsed into its component parts; *`year`*, a numeric value for a year; *`month`*, a numeric or alphanumeric value for a month; and, *`day`*, a numeric or alphanumeric value for a day-of-month. The extended syntax, `temporal` can be used freely and interchangeably with `tempor`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_tempor(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_temporal(`*`moniker`*`,`*`date`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_tempor(`*`moniker`*`,`*`year`*`,`*`month`*`,`*`day`*`);`

The *`date`* parameter can be passed through the `_value` (including `_v`) posit. The other component parts can be added separately with their own posits.  Assignment can occur at declaration, initialisation, and post-declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_tempor(`*`moniker`*`)_value(`*`date`*`)``<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_value(`*`date`*`)``<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_year(`*`year`*`)_month(`*`month`*`)_day(`*`day`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_year(`*`year`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_month(`*`month`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_day(`*`day`*`);`

The `dag` (Afrikaans for "day") or `dow` posit is used to differentiate day from day-of-week. For example, for the date 1776-Jul-14, the `day` was 14, whereas, the `dag` / `dow` was `Thursday`, or `4`. The `dag` and `dow` posits are identical, only syntactically different, they can be used freely and interchangeably.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_dag(`*`dag`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_tempor(`*`moniker`*`)_dow(`*`dow`*`)`

## Posits

| method | description | API |
| --- | -------- | --- |
| <a name="arity"></a> `_arity()` | Provides the named elements in the *object* | [arity](../prop/arity.md) |
| <a name="year"></a> `_year(`*`index`*`)`<br>`_at()` | Provides the element at index *index* |
| <a name="now"></a> `_now()`<br>`_now(`*`dateformat`*`)` | Provides the exact datetime<br>Provides the exact datetime in format dateformat | [now](../prop/now.md) |
| <a name="instant"></a> `_instant()` | Provides the current exact system time, without regard to calendar or time zone | [instant](../prop/instant.md) |
| <a name="year"></a> `_year()`<br>`_year(`*`year`*`)` | Provides the element at index *index* |
| <a name="instant"></a> `_instant()` | Provides the 'exact time' as a fixed point in time without regard to calendar or location |
| <a name="zdt_a"></a> `_zdt()`<br>`_zone_datetime()` | Provides the timezone-aware and calendar-aware (of the thingy caller) of the thingies *now* | [zdt](../funct/zdt.md) |
| <a name="zdt_b"></a> `_zdt(`*`epoch_nanoseconds`*`,`*`timezone`*`)` | Accepts the timezone-aware and 
calendar-presumed (usually Georgian), of the thingy caller | [zdt](../funct/zdt.md) |
| <a name="zdt_c"></a> `_zdt(`*`epoch_nanoseconds`*`,`*`timezone`*`,`*`calendar`*`)` | Accepts the timezone-aware and calendar-aware of the thingy caller | [zdt](../funct/zdt.md) |
| <a name="zdt_d"></a> `_fromzdt(`*`date`*`)` | Provides the timezone-aware and calendar-aware date #date* | [zdt](../funct/zdt.md) |
| <a name="zdt_e"></a> `_tozdt(`*`date`*`)` | Provides the timezone-aware and calendar-aware date #date* | [zdt](../funct/zdt.md) |

---
## See also

* [`{tempor}`](../dt/tempor.md);
* [`tempor`](../obj/tempor.md);




# Temporal (datatype)
The `{tempor}` datatype is of the primative data object [`tempor`](../obj/tempor.md), representing a calendar date. Depending upon the upbringing of thingies the most often used calendar for all dates is the Gregorian calendar. Setting the calendar can be achieved using the `set_cal(`*`calendarname`*`)` setter. 

## Syntax
Since the `tempor` object is a deriviative of the basic data storage *objects*, the datatype `{tempor}` can be used, when declaring the data storage object. The commonly used basic data storage *object* is var.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({tempor},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({tempor},`*`moniker`*`)_value(`*`date`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({tempor},`*`moniker`*`)_year(`*`year`*`)_month(`*`month`*`)_dag(`*`dag`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({tempor},`*`moniker`*`)_year(`*`year`*`)_month(`*`month`*`)_dag(`*`dag`*`)_day(`*`day`*`);`

## Gotchas
The data storage *object* is implied, however, when used, the specific *data storage *object* will applied its own adaptations of the data, for example:
```diego
add_var({tempor},independenceDay)_v(04-Jul-1776);

log_console()_var(independenceDay);  // 04-Jul-1776
log_console()_date(independenceDay);  // 1776-07-04T??:??:??.????Z[?][u-ca=?]4
```

---
## See also




<a name="express"></a>
## Expressions
There are several syntaxes to express a `tempor`.  All date expressions must conform to the ISO 8601 / RFC 3339 format.

| `expression syntax` | description | `example` |
| --- | --- | --- |
| <a name="plainmonthday"></a> `P`*`MM`*`-`*`DD`* | Plain month-day, known as 'PlainMonthDay'. | `P08-05` |
| <a name="plainyearmonth"></a> `P`*`YYYY`*`-`*`MM`* | Plain year-month, known as 'PlainYearMonth'. | `P2020-08` |
| <a name="plaindate"></a> `P`*`YYYY`*`-`*`MM`*`-`*`DD`* | Plain date, known as 'PlainDate'. | `P2020-08-05` |
| <a name="plaintime"></a> `T`*`HH`*`:`*`mm`*`:`*`ss`* | Plain time, known as 'PlainTime'. | `T20:06:13` |
| <a name="plaindatetime"></a> `P`*`YYYY`*`-`*`MM`*`-`*`DD`*`T`*`HH`*`:`*`mm`*`:`*`ss`* | Plain datetime, known as 'PlainDateTime'. | `P2020-08-05T20:06:13` |
| <a name="instant"></a> `P`*`YYYY`*`-`*`MM`*`-`*`DD`*`T`*`HH`*`:`*`mm`*`:`*`ss`*`+`*`offset`*<br>`P`*`YYYY`*`-`*`MM`*`-`*`DD`*`T`*`HH`*`:`*`mm`*`:`*`ss`*`Z` | Instant datetime, known just as 'Instant'. | `P2020-08-05T20:06:13+09:00`<br>`P2020-08-05T11:06:13Z` |
| <a name="zoneddatetime"></a> `P`*`YYYY`*`-`*`MM`*`-`*`DD`*`T`*`HH`*`:`*`mm`*`:`*`ss`*`+`*`offset`*`[`*`time_zone_extension`*`]` | Zoned datetime, known as 'ZonedDateTime'.| `P2020-08-05T20:06:13+09:00[Asia/Tokyo][u-ca-japanese]` |
| <a name="zoneddatetime_full"></a> `P`*`YYYY`*`-`*`MM`*`-`*`DD`*`T`*`HH`*`:`*`mm`*`:`*`ss`*`+`*`offset`*`[`*`time_zone_extension`*`][`*`calendar_extension`*`]` | Full zoned datetime, known as 'FullZonedDateTime'. | `P2020-08-05T20:06:13+09:00[Asia/Tokyo][u-ca-japanese]` |

![Temporal Expressions](https://tc39.es/proposal-temporal/docs/persistence-model.svg)

