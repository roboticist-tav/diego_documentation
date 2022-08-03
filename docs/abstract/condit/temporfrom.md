# Temporal From (condition)
The `temporfrom` *conditional property* is used to determine a `tempor` for the preceding *object* to action from, optionally using definitions of the proceeding *object*.

<a name="declare"></a>
## Declaration
The `temporfrom` *conditional property* is only available via posit syntax. To declare a new `temporfrom` *conditional property*, provide a *[`from_tempor_expression`](../obj/tempor.md#express)* with one of eight formats.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_temporfrom(`*`from_tempor_expression`*`);`

There are eight syntaxes available for a *[`from_tempor_expression`](../obj/tempor.md#express)*.

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

<a name="assign"></a>
## Assignment

; providing the moniker of a pre-declared `tempor`


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_temporfrom([`*`tempor_variable_name`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_temporfrom(`*`from_tempor_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_temporfrom(⟦`*`from_tempor_moniker`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_temporfrom([[`*`from_tempor_moniker`*`]]);`<br>


apt_freq();


<a name="freq"></a>

express