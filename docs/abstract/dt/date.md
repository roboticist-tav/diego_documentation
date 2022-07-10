# Date (datatype)
The `{date}` datatype is of the primative data object [`date`](../obj/date.md), representing a calendar date. Depending upon the upbringing of thingies the most often used calendar for all dates is the Gregorian calendar. Setting the calendar can be achieved using the `set_cal(`*`calendarname`*`)` setter. 

## Syntax
Since the `date` object is a deriviative of the basic data storage *objects*, the datatype `{date}` can be used, when declaring the data storage object. The commonly used basic data storage *object* is var.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({date},`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({date},`*`moniker`*`)_value(`*`date`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({date},`*`moniker`*`)_year(`*`year`*`)_month(`*`month`*`)_dag(`*`dag`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({date},`*`moniker`*`)_year(`*`year`*`)_month(`*`month`*`)_dag(`*`dag`*`)_day(`*`day`*`);`

## Gotchas
The data storage *object* is implied, however, when used, the specific *data storage *object* will applied its own adaptations of the data, for example:
```diego
add_var({date},independenceDay)_v(04-Jul-1776);

log_console()_var(independenceDay);  // 04-Jul-1776
log_console()_date(independenceDay);  // 1776-07-04 00:00:00 Thursday
```

---
## See also

* [`{datetime}`](./datetime.md); [`{time}`](./datetime.md); 
* [`date`](../obj/date.md); [`datetime`](../obj/datetime.md); [`time`](../obj/time.md);






