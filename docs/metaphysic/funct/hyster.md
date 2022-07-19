# Hysteresis (function)

https://en.wikipedia.org/wiki/Hysteresis#:~:text=Hysteresis%20is%20the%20dependence%20of,field%20changed%20in%20the%20past. 

https://www.compart.com/en/unicode/U+238E





## Trip
```diego
log_console()_journ(journ1)_rosary(); // wp1→wp2→wp3
log_console()_journ(journ1)_distan(); // 9d5244,de1b07,48d89f,c2e18e

log_console([2]: [3])_journ(journ1)_trip(wp1→wp2)_distan(❬❭,9d5244);
// wp1→wp2: 6.013m,wp1→wp2: 5.936m

log_console([2]: [3])_journ(journ1)_trip(wp1→wp2)_hyster([📛]','{temporfrom}hh:mm' -> '{temporto}hh:mm' '{durat}hh:mm' '{distan}❬❭);
/* wp1→wp2: alif,T17:23 -> T17:52 0:29 6.013m
=> wp1→wp2: bah,T14:53 -> T15:18 0:25 5.936m
*/
```

| `hyster posit` | description | API |
| --- | --- | --- |
| `_temporfrom(`*`tempor`*`)` &nbsp; `_temporfrom()` &nbsp; `_temporfrom([`*`variable_moniker`*`])` | The tempor when the thingy departed the left-side goal | [temporfrom](../../abstract/condit/temporfrom.md) |
| `_temporto(`*`tempor`*`)` &nbsp; `_temporto()` &nbsp; `_temporto([`*`variable_moniker`*`])` | The tempor when the thingy arrived at the right-side goal | [temporto](../../abstract/condit/temporto.md) |
| `_distan()` &nbsp; `_distance()`<br>`_distan([`*`variable_moniker`*`])` &nbsp; `_distance([`*`variable_moniker`*`])` | The distance record by the thingy | [distan](../obj/distan.md) |
| `_displacem()` &nbsp; `_displacement()`<br> | The displacement record by the thingy | [displacem](../obj/displacem.md) |
| `_unit()` |  | [unit](./unit.md) |
| `_hour()` &nbsp; `_hr()`<br>`_hour(`*`hour_format`*`)` &nbsp; `_hr(`*`hr_format`*`)` | Temporal hours<br>Temporal hours in format *hour_format* | [Hour](../dt/hr.md) |
| `_min()` &nbsp; `_minute()`<br>`_min(`*`min_format`*`)` &nbsp; `_minute(`*`min_format`*`)` |  | Temporal minutes<br>Temporal minutes in format *min_format* | [Minute](../dt/min.md) |

| `hyster operator` | description | API |
| --- | --- | --- |
| `{thingy_name}` &nbsp; `{📛}` | name of thingy | [thingy]() |
| `{tempor_from}` | The tempor when the thingy departed the left-side goal |
| `{tempor_to}` | The tempor when the thingy arrived at the right-side goal |
| `{distan}` &nbsp; `{distance}` | The distance record by the thingy | [distan](../obj/distan.md) |
| `{displacem}` &nbsp; `{displacement}` | The displacement record by the thingy | [displacem](../obj/displacem.md) |
| `❬❭`<br>`❬`*`unit`*`❭` | Unit symbol(s) of proceeding operator<br>Cast to specified unit *unit* | [unit](./unit.md) |
| `h` &nbsp; `hh` &nbsp; `+h` | Temporal hours, in different formats | [Hour](../dt/hr.md) |
| `m` &nbsp; `mm` &nbsp; `+h` | Temporal minutes, in different formats | [Minute](../dt/min.md) |












