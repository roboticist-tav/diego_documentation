# Topological Object Index

An topological index of all objects (at `thing` / `thingy` / `thingette` levels) used by **diego** instruction programming language.

## <a name="genera"></a> Thingy Objects (Genera of Thingies)

| thingy genera | notes<br>examples | API |
| --------- | ----- | ----- |
| `bot`, `ai` | A construct present in the metaphysical world only. (Artificial Intelligence)<br>Example: *cal*, *ChatBot* | [bot](/bot.md) |
| `console` | A metaphysical presence used to only provide an interface to all other *thingies* | [console](/console.md) |
| `human`   | Representation of a human being, present and alive in the physical *'real'* world. The human version of a `thing` / `robot`.  The non-human version of an `organic`.<br>Example: *Fred Jones* | [human](/human.md) |
| `mobot`, `mech` _[`mechanical thing`]_ | A conveyed *thingy* in the physical *'real'* world.<br>Examples: Samasung Galaxy watch, cellphone | [mobot](/mobot.md) |
| `organic` | Representation of a non-human being, present and alive in the physical *'real'* world.<br>Example: cat, dog | [organic](/organic.md) |
| `robot` | A self-propelled *thingy* in the physical *'real'* world.<br>Examples: Boston Dynamics Spot, robot arm, drone<br>See also: `human`; `thing` | [robot](/robot.md)
| `thing`, `appliance`, `mach`, `machine` | An immobile *thingy* in the physical *'real'* world.<br>Example: fridge, television | [thing](/thing/md) |
| `vehicle` | A guided *thingy* transporting `human`/`organic` thingies and/or controlled by a `human`.<br>Examples: car, airplane, ugv, radio-controlled toy car | [vehicle](/vehicle.md) |

## Self

| thingy genera | notes<br>examples | API |
| --------- | ----- | ----- |
| `me`      | Representation of self | [me](/me/md) |
| `we` ||
| `us`||
| 'them' ||
| 'you' ||


## Scope

| scope     | notes<brexamples | API |
| --------- | ----- | ----- |
 `mission` |

## <a name="geospatial"></a> Geospatial

| geospatial | notes<br>examples | API |
|--|:--|--|
| `arena` <a name="arena"></a> | A representation of physically defined 3d space for a `thing`(s) to move freely around inside. There should be an attempt to represent physical (real-world) borders. The human version of a `zone`.<br>Example: atrium, open plan office floor<br>See also: [zone](#zone); [fence](#fence) | [arena](/arena.md) |
| `border` <a name="border"></a> | .<br>Example: <br>See also: [wall](#wall) | [border](/border.md) |
| `box` <a name="box"></a> | A representation of a meta-physical enclosed space. The thing / meta-physical version of a `room`.<br>Example: inside a pit<br>See also: [room](#room) | [box](/box.md) |
| `ceiling` <a name="ceiling"></a>| An identified top _side_ of a representation space in the physical world. An undetermined human version of a `plafond`.<br>See also: [side](#side); [plafond](#plafond); [firma](#firma); [wall](#wall); [border](#border) | [ceiling](/ceiling.md) |
| `corridor` <a name="corridor"></a> | A `thing` representation of physically defined 3d space, designed for a human, to manoeuvre inside, predominately along a single plane. There should be an attempt for physical (real-world) borders. The human version of a `pipe`.<br>See also: `arena`; `fence`; `pipe`; `zone` | [corridor](/corridor.md) |
| `door` <a name="door"></a> | A `thing` representation of a physical doorway / gate, designed for a human.<br>See also: [portal](#portal); [gate](#gate) | [door](#door)
| `fence`, `geofence` | |
| `firma` | An identified down _side_ of a representation space in the physical world. An undetermined human version of a `marack`.<br>See also: [side](#side); [marack](#marack); [ceiling](#ceiling); [wall](#wall); [border](#border); [ground](#ground); [track](#track) | [firma](/firma.md) |
| `floor` / `level` | |
| `foreign`, `foreigner` | | [foreginer](/foreigner.md) |
| `litsan` |**L**ine **i**n **t**he **San**d is a 2d geo-spatial line. |
| `map` | A map |
| `marker` | | [marker](/marker.md) |
| `obstacle` | [obstacle](/obstacle.md) |
| `path` | | [path](/path.md) |
| `pipe` | The thing version of a `corridor` | [pipe](/pipe.md) |
| `plafond` | | [plafond](/plafond.md) |
| `point` | <br>See also: `route`; `path` | [path](/path.md) |
| `room` | A representation of a physical enclosed space. The humnan / physical version of a `room`.  | [room](/room.md) |
| `route` | | [route](/route.md) |
| `track` | | [track](/track.md) |
| `wall` | | [wall](/wall.md) |
| `zone` | The thing version of an `arena` |
| `rosary` |

## <a name="organs"></a> Thing Composition (Organ / Components / Devices)

| thing composition | notes | API |
|--|:--|--|
| `actuator', 'actuat', mover` | A device ('thingy') that causes a _'thingy'_ or other device to operate.<br/>derived objects:<br/>`jigger` ... ``actuat()_motion(jigger)`<br/>`rotator` ... `actuat()_motion(rotator)` | [actuat](actuat.md) |
| `apparatus`, `apparat`, `impedimentum`, `impedi` | A logical grouping of `instru`s, necessary for a particular purpose. | [apparat](apparat.md) |
| `device` | A genera agnostic 'thingy', used and carried/attached/worm by another 'thingy', for use for a particular activity or purpose.  | [device](/device.md)<br/>_see also:_ [peripheral](peripheral.md) |
| `equipment`, `equip` | A logical grouping of `peripheral`s, necessary for a particular purpose. | [equip](equip.md) |
| `instrument`, `instru`, `implement`, `imple` | A device ('thingy'), used and carried/worm by a human, for use for a particular activity or purpose.<br/>Example: geiger counter, multi-meter; *a handheld device* | [instru](/instru.md)<br/>_see also:_ [peripheral](peripheral.md) |
| `peripheral` | A device ('thingy'), used by a non-human, for use for a particular activity or purpose. but not an integral part (_i.e. carried / attached via a port_) of the non-human. | [peripheral]
| `sensor` | A device ('thingy') which detects and/or measures a physical property and records, indicates, or otherwise responds to it. | [sensor](sensor.md)<br/>_see also:_ [camera](camera.md) |
| `gimbal` |||
| `willis` | A logical grouping of `sensor`s, necessary for a particular purpose. | | 

## <a name="sensors"></a> Sensors

| sensors | notes | API<br/>_see also_ |
|--|:--|--|
| `camera` | A sensor for recording/streaming visual images. Derived from `sensor` of `_type(camera)`. | <br/>_see also:_ [lens](lens.md)) |








| `spec`, `specification` | <br>See also: `attribute` | [spec](/spec.md) |

| ~~`manip`*[ulator]*~~ | ~~Depreciated from version 1.1, use `equip` with type `manip`~~|


`stance` = URDF Model_State  joint_state array









| actuators | notes | API<br/>_see also_ |
|--|:--|--|
| `jagger` | An actuator that follows am irrational motion. Derived from `acutator` of `_motion(jagger)`. | [jagger](/actuat.md#jagger)<br/>_see also:_ [actuat](#actuat) |
| `jigger` | An actuator that follows a _'to and fro'_ motion. Derived from `acutator` of `_motion(jigger)`. | [jigger](/actuat.md#jigger)<br/>_see also:_ [actuat](#actuat) |
| `periodicator` | An actuator that follows a periodic motion. Derived from `actuator` of `_motion(periodicator)`. | [periodicator](/actuat.md#preiodicator)<br/>_see also:_ [actuat](#actuat) |
| `rotator` | An actuator that follows a rotational motion. Derived from `acutator` of `_motion(rotator)`. | [rotator](/actuat.md#rotator)<br/>_see also:_ [actuat](#actuat) |

## Thing External Anatomy

| thing anatomy | notes | API |
|--|:--|--|
| `head` | | |
| `torso` |||
| `limb` |||
| `manipulator` | `limb()_type(manipulator)` | | 
| `prolongation` | | |
`cavity`; `generator`, `body`, `leg`, `arm`

## Thing Internal Anatomy

| thing anatomy | notes | API |
|--|:--|--|
| `` | | |
| `` |||
| `` |||
| `` | `limb()_type(manipulator)` | | 
| `` | | |
``; `generator`

## Thing Descriptor (Universal Robotic Description Format - URDF)

| thing descriptor | notes | API |
|--|:--|--|
| `joint` | A structure that transforms spatial vectors between two or more `link`s.  Most usually a `joint`'s state is managed through an `actuat`or. |  [joint](joint.md)<br/>_see also:_ [link](link.md)<br/>[actuat](actuat.md) |
| `link` |||
| `transmiss`, `transmission` |||

## Joints (Universal Robotic Description Format - URDF)

| thing descriptor | notes | API |
|--|:--|--|
| `hip` | `joint()_ofsort(hip) |  [joint](joint.md)<br/>_see also:_ [link](link.md)<br/>[actuat](actuat.md) |
| `link` |||
| `transmiss`, `transmission` |||



## <a name="comm"></a> Commuincation

| comunication | notes<br>examples | API |
|--|:--|--|
| `email` | | |


## <a name="stats"></a> Statistics

| statistics | notes<br>examples | API |
|--|:--|--|
| `metric` | | [metric](/metric.md) |
| `payload` | | [payload](/payload.md) |

## <a name="proce"></a> Procedural Structuring

| procedural | notes<br>examples | API |
|--|:--|--|
| `instruct`, `instruction` |  | [instruct](/instruct.md) |
| `proc`, `procedure` | | [proc](/proc.md) |
| `prog`, `program`, `programme` | | [prog](/prog.md) |
| `action` | | [action](/action.md) |

## <a name="audit"></a> Auditing & Error Handling

| auditing | notes<br>examples | API |
|--|:--|--|
| `valid` | | [valid](/valid.md) |
| `err`, `error` | | [err](/err.md) |
| `refuse` |
| `wtf`


| `mode` | | [mode](/mode.md) |
| `gate` | | [gate](/gate.md) |
| `guide` | | [guide](/guide.md) |
| `side` | | [side](/side.md) |

## <a name="discriminat"></a> Discrimination

| discrimination | notes<br>examples | API |
|--|:--|--|
| `label` | | [label](/label.md) |



human - thing (mech, robot, obstacle, organic)

https://specializedstairs.com/anatomy-of-a-staircase/
_stringer(open, closed, mono


> Author: Tavis PItt
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjE0MTcxMDA2MSw0MTM1OTIzMDksMTI3OD
AwOTA5MywxMjkxNjAzMDk2LDQ0NDM5MzA3OCwxODg4Njc3MjIx
LC05MjUwNDE3OTYsMTQ5MTQ1NDM1MF19
-->