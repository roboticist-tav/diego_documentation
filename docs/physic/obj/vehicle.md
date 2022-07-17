# Vehicle (object)
The `vehicle` *object* is a derived `human`, representing a propelled thingy that transports the human who is controlling it.  Similarly a thingy that was originally designed to transport the human who is controlling it, but then later modified to be self-controlled and not carry the human who is controlling it, is still a `vehicle` but an unmanned one.

```mermaid
    flowchart LR
    thingy((thingy)) --> human([human])
    human --> vehicle
```
<div style="text-align: right"><sub>Vehicle Hierarchy</sub></div>

<a name="declaration"></a>
## Declaration
The default declaration of the `vehicle` *object* is to at least provide a *moniker*. A type can be provided at declaration using curly brackets (`{}`). The derived *objects* can be declared by name. The `vehicle` object can also be declared by casting `robot`. However, this will imply that the `vehicle` is a child of the `human`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_vehicle(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_vehicle({`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_`*`<type>`*`(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_human({vehicle},`*`moniker`*`);`

<a name="referencing"></a>
## Referencing
To reference `vehicle`, use, either the `with` verb or the shortened syntax using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_vehicle(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_vehicle({`*`type`*`,`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`vehicle_moniker`*`);`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`vehicle_type_moniker`*`);`

## Posits

| `posit` | operator | description | API |
| --- | --- | --- | --- |
| <a name="_car"></a> `_car()`<br>`_car(`*`moniker`*`)` &nbsp; `_vehicle({`*`car`*`},`*`moniker`*`)` | 🚗 |  A wheeled motor vehicle that is used for transportation of mainly people instead of goods. | [car](#car) |
| <a name="_truck"></a>  `_truck()` &nbsp; `_lorry()` &nbsp; `_van()`<br>`_truck(`*`moniker`*`)` &nbsp; `_lorry(`*`moniker`*`)` &nbsp; `_van(`*`moniker`*`)`<br>`_vehicle({`*`truck`*`},`*`moniker`*`)` | 🚚 | A motor vehicle designed to transport cargo, carry specialized payloads, or perform other utilitarian work. | [truck](#truck) |
| <a name="_airplane"></a> `_airplane()` <br> `_airplane(`*`moniker`*`)` &nbsp; `_vehicle({`*`airplane`*`},`*`moniker`*`)` | ✈ &nbsp; 🛩 | A fixed-wing aircraft that is propelled forward by thrust from a jet engine, propeller, or rocket engine.  | [airplane](#airplane) |
| <a name="_bus"></a> `_bus()` <br> `_bus(`*`moniker`*`)` &nbsp; `_bus({`*`airplane`*`},`*`moniker`*`)` | 🚌 | A road vehicle that carries significantly more passengers than an average car or van.  | [bus](#bus) |
| <a name="_copter"></a> `_plane()` <br> `_(`*`moniker`*`)` &nbsp; `_({`*`unit`*`},`*`moniker`*`)` | |  | [](#) |
| <a name="_hovercraft"></a> `_hovercraft()` <br> `_hovercraft(`*`moniker`*`)` &nbsp; `_({`*`unit`*`},`*`moniker`*`)` | |  | [](#) |
| <a name="_spacecraft"></a> `_spacecraft()` <br> `_spacecraft(`*`moniker`*`)` &nbsp; `_({`*`unit`*`},`*`moniker`*`)` | |  | [](#) |
| <a name="_ship"></a> `_ship()` <br> `_boat(`*`moniker`*`)` &nbsp; `_vehicle({`*`ship`*`},`*`moniker`*`)` | ⛵ &nbsp; 🛥 |  | [](#) |
| <a name="_sub"></a> `_submarine()` <br> `_submarine(`*`moniker`*`)` &nbsp; `_vehicle({`*`submarine`*`},`*`moniker`*`)` | |  | [](#) |
| <a name="_blimp"></a> `_blimp()` <br> `_blimp(`*`moniker`*`)` &nbsp; `_({`*`unit`*`},`*`moniker`*`)`  | | . | [](#) |
| <a name="_cycle"></a> `_cycle()` &nbsp; `_bicycle()`<br>`_cycle(`*`moniker`*`)` &nbsp; `_vehicle({`*`cycle`*`},`*`moniker`*`)`<br> `_bicycle(`*`moniker`*`)` | 🚲 |A representation of a human-powered or motor-powered assisted, pedal-driven, single-track vehicle, wheels attached to a frame. | [cycle](#cycle) |
| <a name="_mcycle"></a> `_mcycle()` &nbsp; `_motorcycle()` &nbsp; `_motorbike()`<br>`(`*`moniker`*`)` &nbsp; `_({`*`unit`*`},`*`moniker`*`)` | 🏍 |  | [](#) |
| <a name="_train"></a> `_train()` <br> `_train(`*`moniker`*`)` &nbsp; `_vehicle({`*`train`*`},`*`moniker`*`)` | 🚆 |  | [](#) |
| <a name="_tram"></a> `_tram()` <br> `_(`*`moniker`*`)` &nbsp; `_({`*`unit`*`},`*`moniker`*`)` | |  | [](#) |

aircraft - airplane, seaplane, airboat, blimp
watercraft - ship, boat, submarine
cycle - bicycle, unicycle, tandem
https://cocodataset.org/#home

<a name="car"></a>
### Cars



