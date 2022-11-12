# Duration (function)
A 

<!-- https://tc39.es/proposal-temporal/docs/duration.html -->
<!-- https://en.wikipedia.org/wiki/ISO_8601#Durations -->

The capital letters P, Y, M, W, D, T, H, M, and S are designators for each of the date and time elements and are not replaced.



&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_durat(`*`period`*`);`<br>


| *`period`* | description |
| --- | --- |
| *`P…`* | `P` is the duration designator (for period) placed at the start of the duration representation |
| *`P…<year>Y…`* | `Y` i is the year designator that follows the value for the number of calendar years |
| *`P…<quarter>Q…`* | `Q` i is the year designator that follows the value for the number of quarter years |
| *`P…<fiscal_quarter>$…`* | `$` i is the year designator that follows the value for the number of fiscal quarter years |
| *`P…<month>M…`* | `M` is the month designator that follows the value for the number of calendar months |
| *`P…<week>W…`* | `W` is the week designator that follows the value for the number of weeks |
| *`P…<fortnight>F…`* | `F` is the fortnight designator that follows the value for the number of fortnights |
| *`P…<day>D…`* | `D` is the day designator that follows the value for the number of calendar days |
| *`P…<jour>J…`* | `J` is the day designator that follows the value for the number of jour days |
| *`PT…`* | `T` is the time designator that precedes the time components of the representation |
| *`PT…<hour>H…`* | `H` is the hour designator that follows the value for the number of hours |
*`PT…<minute>M…`* | `M` is the minute designator that follows the value for the number of minutes |
*`PT…<second.millisecondsmicroseconds>S…`* | `S` is the second designator that follows the value for the number of seconds |

https://en.wikipedia.org/wiki/Battle_of_Hastings#:~:text=The%20only%20undisputed%20facts%20are,the%20battle%20lasted%20until%20dusk.

Battle of Hastings
```diego
// Battle of Hastings
add_bout(battleOfHastings)
    ()_fromat(1066-10-14T09:00:00[Europe/London][u-ca=julian]);
    ()_fromto(1066-10-14T17:54:00[Europe/London][u-ca=julian]);
    ()_fromto()_time(17:54);
;
https://en.wikipedia.org/wiki/Luna_9
```diego
// Luna 9 mission
add_bout(luna9Mission)
    ()_fromat(1966-01-31T11:45:00[Europe/London][u-ca=julian]);
    // ()_fromto(1066-10-14T17:54:00[Europe/London][u-ca=julian]); // lengthy syntax
    ()_toat()_time(17:54);
;
3 February 1966 at 18:45:30 GMT

myDate)_bout(P)
B1066Y9M14D9+


## Posits

| method | description | API |
| --- | -------- | --- |
| <a name="year"></a> `_year()`<br>`_year(`*`yearnumeric`*`)` | References the temporal year of the preceeding *object*<br>Sets the temporal year of *yearnumeric* | [year](../dt/yr.md) |

<a name="declare"></a>
## Declaration

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment

<a name="initial"></a>
## Initialisation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="assign"></a>
## Assignment

<a name="reference"></a>
## Referencing
Referencing a ` ` *object* is achieved with the `with` verb, or the shortened `(`*` `*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`_moniker`*`);`

<a name="type"></a>
## Typing

<a name="get"></a>
## Getting

<a name="set"></a>
## Setting

<a name="cast"></a>
## Casting

<a name="properties"></a>
## Properties

<a name="example"></a>
## Examples