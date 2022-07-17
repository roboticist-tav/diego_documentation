# Automatic Dependent Surveillance–Broadcast (object) 


`with_drone(`*`moniker`*`)_adsb();`

`with_drone(`*`moniker`*`)_adsb(`*`moniker`*`);`

*`<object>`*`_adsb(`*`moniker`*`)`;

## Properties

| `property` | `{datatype}` / `❬unit❭` | description |
| --- | --- | --- |
| `id`<br>`hex` | `{id}` / `❬id_3❭`[^3btyehex] | A 3 Byte hexidecimal unique idendifier used in adsb messaging |
| `squawk` | `{int}` / `❬4_int❭` | A four-digit code assigned to a flight by air traffic control to match the flight to its radar screens |
| `fir` | `{str}` / `❬4_str❭` | A four charatcher code representing the Flight Information Region (FIR) |
| `uir` | `{str}` / `❬4_str❭` | A four character code representing the Upper Information Region (UIR), if no UIR then FIR is used |
| `tailnum`<br>`reg` | `{str}` / `❬tailnum❭`[₁](#tne) | A unique code given to each aircraft |
| `airspeed` | `{double}` / `❬kt❭` | The true air speed of the aircraft in knots[^avionicmeasurements] |
| `speed` | `{double}` / `❬kt❭` | The ground speed of the aircraft in knots[^avionicmeasurements] |
| `alt`<br>`altitude` | `{double}` / `❬ft❭` | The altitude of the aircraft in feet {ft}[^avionicmeasurements] |
| `course`<br>`heading` | `{int}` / `❬deg❭` | The heading or course (from North) of the aircraft |
| `vrate` | `{double}` / `❬ft/min❭`




<a name="tne"></a>
## Tail Number Enumerator 

![Tail Number Example](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/JAL_B747-400%28JA8089%29_%285481514185%29.jpg/220px-JAL_B747-400%28JA8089%29_%285481514185%29.jpg "JA8089")

| `example` | description and example return |
| --- | --- |
| `_adsb()_tailnum()` | Returns the full tail number, e.g. `JA8089` |
| `_adsb()_tailnum({crp})` | Return the country registration prefix, e.g. `JA` |
| `_adsb()_tailnum({-})` | Return the full tail number with hyphen, e.g. `JA-8089` |




[^3btyehex]: `{id_3}` refers to a 3 Byte (24 Bit) hexidecimal.
[^avionicmeasurements]: The preferred avionic measurement units are used, irrespective of the thingies `set_unitsys` setting. The units can be cast, for example: `_adsb()_speed({ms})`