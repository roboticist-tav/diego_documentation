# Temporal (object)
<!-- https://tc39.es/proposal-temporal/ -->
A primative data object and datatype representing a calendar date. Depending upon the upbringing of thingies the most often used calendar for all datae ois the Gregorian calendar. Setting the calendar can be achieved using the `set_cal(`*`calendarname`*`)` setter. The [`{tempor}`](../dt/tempor.md) datatype can be used in data storage objects to create date types. 

## Syntax
The default declaration of `tempor` is to at least provide a *moniker*. However, assignment can occur at declaration with an overload of two more signatues involving parameters: *`date`*, a valid represenation of a date to be parsed into its component parts; *`year`*, a numeric value for a year; *`month`*, a numeric or alphanumeric value for a month; and, *`day`*, a numeric or alphanumeric value for a day-of-month. The extended syntax, `temporal` can be used freely and interchangably with `tempor`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_tempor(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_temporal(`*`moniker`*`,`*`date`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_tempor(`*`moniker`*`,`*`year`*`,`*`month`*`,`*`day`*`);`<br>

The *`date`* parameter can be passed through the `_value` (including `_v`) posit. The other component parts can be added separately with their own posits.  Assignement can occur at declaration, insitialisation, and post-declaration.

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
| <a name="instant"></a> `_instant()` | Provides the 'exact time' as a fixed point in time without regard to calendar or location |
| <a name="zdt_a"></a> `_zdt()`<br>`_zoneddatetime()` | Provides the timezone-aware and calendar-aware (of the thingy caller) of the thingies *now* | [zdt](../funct/zdt.md) |
| <a name="zdt_b"></a> `_zdt(`*`epochnanoseconds`*`,`*`timezone`*`)` | Accepts the timezone-aware and 
calendar-presumed (usually Georgian), of the thingy caller | [zdt](../funct/zdt.md) |
| <a name="zdt_c"></a> `_zdt(`*`epochnanoseconds`*`,`*`timezone`*`,`*`calendar`*`)` | Accepts the timezone-aware and calendar-aware of the thingy caller | [zdt](../funct/zdt.md) |
| <a name="zdt_d"></a> `_fromzdt(`*`date`*`)` | Provides the timezone-aware and calendar-aware date #date* | [zdt](../funct/zdt.md) |
| <a name="zdt_e"></a> `_tozdt(`*`date`*`)` | Provides the timezone-aware and calendar-aware date #date* | [zdt](../funct/zdt.md) |

---
## See also

* [`{date}`](../dt/date.md); [`{datetime}`](../dt/datetime.md); [`{time}`](../dt/datetime.md); 
* [`datetime`](../obj/datetime.md); [`time`](../obj/time.md);
