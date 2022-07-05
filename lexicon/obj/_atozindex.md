# A to Z Objects Index

An A to Z index of all objects used by **diego** instruction programming language.

## <a name="a"></a> A: [actuat](#actuat); [apparat](#apparat); [appliance](#appliance); [arena](#arena)

| A | Description | API |
|--|:--|---|
| `action` <a name="action"></a> | | [action](/action.md) |
| `actuat`, `actuator` <a  name="actuat"></a> | See: [jigger](#jigger) | [actuator](/actuat.md) |
| `apparat`, `apparatus` <a name="apparat"></a>| A technical *device* (`thingy`), carried/worm by a human, for use for a particular purpose or activity. The human version of a `sensor`.<br>Example: geiger counter, multi-meter; *a handheld device*<br>See also: [sensor](#sensor)| [apparat](/apparat.md) |
| `appliance` <a name="appliance"></a>| A *device* or *piece of equipment* `thingy` designed to perform a specific task, that is **not** attached / carried / worm by a human. An `apparatus` can or cannot have access to the _puff_. The human version of a `mach`*[ine].*<br>Example: refrigerator, washing machine<br>See also: [mach](#mach) | [appliance](/applicance.md)
| `arena` <a name="arena"></a> | A representation of physically defined 3d space for a `thing`(s) to move freely around inside. There should be an attempt to represent physical (real-world) borders. The human version of a `zone`.<br>Example: atrium, open plan office floor<br>See also: [zone](#zone); [fence](#fence) | [arena](/arena.md) |
| `attr`, `attribute` <a name="attr"></a> | Lorem ipsum, lorem ipsum, lorem ipsum.<br>Example: <br>See also: [spec](#spec) | [attr](/attr.md) |

## <a name="b"></a> B: [border](#border); [box](#box)

| B | Description | API |
|--|:--|--|
| `border` <a name="border"></a> | .<br>Example: <br>See also: [wall](#wall) | [border](/border.md) |
| `box` <a name="box"></a> | A representation of a meta-physical enclosed space. The thing / meta-physical version of a `room`.<br>Example: inside a pit<br>See also: [room](#room) | [box](/box.md) |
| `bot`, `ai` | A construct present in the metaphysical world only. (Artificial Intelligence)<br>Example: *cal*, *ChatBot* | [bot](/bot.md) |

## <a name="c"></a> C: [ceiling](#ceiling); [corridor](#corridor)

| C | Description | API |
|--|:--|--|
| `ceiling` <a name="ceiling"></a>| An identified top _side_ of a representation space in the physical world. An undetermined human version of a `plafond`.<br>See also: [side](#side); [plafond](#plafond); [firma](#firma); [wall](#wall); [border](#border) | [ceiling](/ceiling.md) |
| `channel` | | An exclusive sub-section of a `workspace`, sometimes referred to as a _conversation_ |
| `cloud`   | A zone (`puff`) used for diego communication that utilises a cloud based platform like twitter, discord, slack, _etc._ |
| `console` | A metaphysical presence used to only provide an interface to all other *thingies* | [console](/console.md) |
| `corridor` <a name="corridor"></a> | A `thing` representation of physically defined 3d space, designed for a human, to manoeuvre inside, predominately along a single plane. There should be an attempt for physical (real-world) borders. The human version of a `pipe`.<br>See also: `arena`; `fence`; `pipe`; `zone` | [corridor](/corridor.md) |
 | `commrelay_` | | https://www.autonodyne.com/AUTO_behaviors2.html |

## <a name="d"></a>D: [door](#door)
| D | Description | API |
|--|:--|--|
| `door` <a name="door"></a> | A `thing` representation of a physical doorway / gate, designed for a human.<br>See also: [portal](#portal); [gate](#gate) | [door](#door)

## <a name="e"></a>E: [equip](#equip)
| E | Description | API |
|--|:--|--|
| `equip`*[ment]* | <br>See also: `apparatus`; `instru`*[ment]*; `peripheral`;  `sensor` | [equip](equip.md) |

## <a name="f"></a>F: [fence](#fence); [firma](#firma)
| F | Description | API |
|--|:--|--|
| *[geo-]*`fence` <a name="fence"></a> | |
| `firma` <a name="firma"></a> | An identified down _side_ of a representation space in the physical world. An undetermined human version of a `marack`.<br>See also: [side](#side); [marack](#marack); [ceiling](#ceiling); [wall](#wall); [border](#border); [ground](#ground); [track](#track) | [firma](/firma.md) |
| `floor` / `level` | |
| `fog`     | A zone (`puff`) used for diego communication that relies on UDP | |
| `foreign`*[er]* | |
| `form`*[ation]* | |

## <a name="g"></a>G: [gait](#gait); [gate](#gate)

| G | Description | API |
|--|:--|--|
| `gait` | The thing version of `stride` |
| `gate` | |
| `ghost` |  |
| `guide` | |
| `gimbal` | | |

## <a name="h"></a>H: [human](#human)

| H | Description | API |
|--|:--|--|
| `human` | The human version of a `thing` / `robot`.  The non-human version of an `organic`.<br>See also: |
| `human`   | Representation of a human being, present and alive in the physical *'real'* world. The human version of a `thing` / `robot`.  The non-human version of an `organic`.<br>Example: *Fred Jones* | [human](/human.md) |
| `hold`, `household` |||
| `handler` | | |

## <a name="i"></a>I: [instruct](#instruct); [label](#label)

| I | Description | API |
|--|:--|--|
| `instruct` | |
| `inanimate` | |

## <a name="j"></a>J: [instruct](#instruct); [label](#label)

| I | Description | API |
|--|:--|--|
| `jagger` | jagger](#jagger) | [jigger](/jigger.md) |
| `jigger`<br>`actuat`<br>`actuator`<br>`mover` <a  name="actuat"></a> | A child *device*  `thingette` that causes its parent `thingy` and/or sibling `thingette` to operate, usually providing motion. A public interface with the _puff_ should be avoided or at least strictly limited. The thing version of a `jagger`.<br>Example: motor controller; gearbox; motor<br>See also: [jigger](#jigger), 

## <a name="k"></a>K:

| K | Description | API |
|--|:--|--|

## <a name="l"></a>L:

| L | Description | API |
|--|:--|--|
| `label` | |
| `lib`, `library` | | |

## <a name="m"></a>M:

| m | Description | API |
|--|:--|--|
| `mach`*[ine]* | The stationary version of a `mech` |
| ~~`manip`*[ulator]*~~ | ~~Depreciated from version 1.1, use `equip` with type `manip`~~|
| `map` | |
| `me`      | Representation of self | [me](/me/md) |
| `mech`*[anical thing]* | The motion version of a `mach` |
| `metric` | |
| `mode` | |
| `mover` <a  name="mover"></a> | See: [jigger](#jigger) | |
| `mobot`   | A conveyed *thingy* in the physical *'real'* world.<br>Examples: Samasung Galaxy watch, cellphone | [mobot](/mobot.md) |
| `mist`    | A connectivity zone (wired or wireless) with the distance range of < 10m.<br>For example: RFID | [mist](/mist.md) |

## <a name="n"></a>N:

| n | description | API |
|--|:--|--|
| `neigh`, `neighbour` |||

## <a name="o"></a>O:

| o | description | API |
|--|:--|--|
| `obstacle` | |
| `object`  | A civilian^1^ immobile *thingy* in the  physical *'real'* world       | lampost, bush, chair |
| `organic` | Representation of a non-human being, present and alive in the physical *'real'* world.<br>Example: cat, dog | [organic](/organic.md) |

## <a name="p"></a>P:

| p | description | API |
|--|:--|--|
| `path` | |
| `payload` | |
| `pipe` | The thing version of a `corridor` |
| `plafond` | |
| `point` | <br>See also: `route`; `path` |
| `proc`, ``proced`, `procedure` | | |
| `prog`, `program`, `programme` | | |
| `package` | | |
| `puff` | | |
| `poi` | | |

## <a name="q"></a>Q:

| q | description | API |
|--|:--|--|

## <a name="r"></a>R:

| r | description | API |
|--|:--|--|
| `robot`   | A self-propelled *thingy* in the physical *'real'* world.<br>Examples: Boston Dynamics Spot, robot arm, drone<br>See also: `human`; `thing` | [robot](/robot.md)
| `room` | A representation of a physical enclosed space. The humnan / physical version of a `room`.  
| `route` | |
| `regin`, `roi`, `regionofinterest` | | |


## <a name="s"></a>S:

| s | description | API |
|--|:--|--|
| `sensor` | The thing version of an `apparatus`.<br>See also: [apparat](#apparat) |
| `side` | | |
| `spec`*[ification]* | <br>See also: `attribute` |
| `stance` |  |
| `stride` | The human version of `gait` |
| `swarm` | |
| `subject` | A civilian^1^ movable *thingy* in the  physical *'real'* world       | *unidentified moving animal*, *unidentified flying object*  |
| `scan` | |
| `stealth` |

^1^: A civilian is a *thingy* with (or presumed to be with) no Diego interface

## <a name="t"></a>T:

| t | description | API |
|--|:--|--|
| `thing` | The thing version of a `human` |
| `thing`   | An immobile *thingy* in the physical *'real'* world.<br>Example: fridge, television | [thing](/thing/md) |
| `track` | |

## <a name="u"></a>U:

| u | description | API |
|--|:--|--|

## <a name="v"></a>V:

| v | description | API |
|--|:--|--|
| `vehicle` | A guided *thingy* transporting `human`/`organic` thingies and/or controlled by a `human`.<br>Examples: car, airplane, ugv, radio-controlled toy car | [vehicle](/vehicle.md) |

## <a name="w"></a>W:

| w | description | API |
|--|:--|--|
| `wall` | |
| `workspace` | An exclusive section of a `puff`, sometimes called a _room_ |

## <a name="xnz></a>XYZ:

| xyz | description | API |
|--|:--|--|
| `zone` | The thing version of an `arena` |

human - thing (mech, robot, obstacle, organic)

https://specializedstairs.com/anatomy-of-a-staircase/
_stringer(open, closed, mono


> Author: Tavis PItt<br>
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI5MDg2NDU1OSwxNjkyMTEyOTk3LDIxND
E3MTAwNjFdfQ==
-->


`puff`, `cloud`, `fog`, `mist`































