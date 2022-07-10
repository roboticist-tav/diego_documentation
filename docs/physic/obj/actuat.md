# Actuator (object)

A `actuat`or, derived from a `compon`ent is of a machine that is responsible for moving and controlling a mechanism or system, for example by opening a valve. In simple terms, it is a "mover". An actuator requires a control device and a source of energy.

 ## Syntax
 The default declaration syntax is to provide, at least, the moniker.  Both the common syntax `actuat` and the extended version `actuator` can be used:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_actuat(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_actuator(`*`moniker`*`);`

There is not a specific *type* of actuator, however, they can, optionally, be classified with `motion` and `soe` (source of energy):

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_actuat(`*`moniker`*`)_motion(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_actuat(`*`moniker`*`)_soe(`*`source_of_energy`*`);`

| `motion` | Description |
| --- | --- |
| `linear` | |
| `rotary` | |

| `soe` | Description |
| --- | --- |
| `hydraulic` | |
| `pneumatic` | |
| `electromechanical` | |
| `electrohydraulic` | |
| `thermomagnetic` | |
| `mechanical` | |
| `supercolled polymer` | |
| `piezoelectric` | |

https://www.creativemotioncontrol.com/types-of-actuators/

| `actuat`, `actuator` <a  name="actuat"></a> | See: [jigger](#jigger) | [actuator](/actuat.md) |

| `jigger`<br>`actuat`<br>`actuator`<br>`mover` <a  name="actuat"></a> | A child *device*  `thingette` that causes its parent `thingy` and/or sibling `thingette` to operate, usually providing motion. A public interface with the _puff_ should be avoided or at least strictly limited. The thing version of a `jagger`.<br>Example: motor controller; gearbox; motor<br>See also: [jigger](#jigger), 


| actuators | notes | API<br/>_see also_ |
|--|:--|--|
| `jagger` | An actuator that follows am irrational motion. Derived from `acutator` of `_motion(jagger)`. | [jagger](/actuat.md#jagger)<br/>_see also:_ [actuat](#actuat) |
| `jigger` | An actuator that follows a _'to and fro'_ motion. Derived from `acutator` of `_motion(jigger)`. | [jigger](/actuat.md#jigger)<br/>_see also:_ [actuat](#actuat) |
| `periodicator` | An actuator that follows a periodic motion. Derived from `actuator` of `_motion(periodicator)`. | [periodicator](/actuat.md#preiodicator)<br/>_see also:_ [actuat](#actuat) |
| `rotator` | An actuator that follows a rotational motion. Derived from `acutator` of `_motion(rotator)`. | [rotator](/actuat.md#rotator)<br/>_see also:_ [actuat](#actuat) |


| `jigger`<br>`actuat`<br>`actuator`<br>`mover` <a  name="actuat"></a> | A child *device*  `thingette` that causes its parent `thingy` and/or sibling `thingette` to operate, usually providing motion. A public interface with the _puff_ should be avoided or at least strictly limited. The thing version of a `jagger`.<br>Example: motor controller; gearbox; motor<br>See also: [jigger](#jigger), [jagger](#jagger) | [jigger](/jigger.md) |

| `mover` <a  name="mover"></a> | See: [jigger](#jigger) | |