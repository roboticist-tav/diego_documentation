# Thingys / Thingies

## <a name="a"></a> A: [actuator](#actuator); [apparatus](#apparatus); [appliance](#appliance); [arena](#arena)
| a | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| actuator | `_actuat();`<br>`_actuator();`<br>`_compon()_type(actuator);`<br>`_mover();` | A component that is responsible for moving and controlling a mechanism or system. In simple terms, it is a "mover". An actuator requires a control device and a source of energy.<br>[jigger](#jigger) | [actuator](/actuator.md) |
| apparatus<a name="apparatus"></a> | `_ apparat();`<a name="apparat"></a><br>`_ apparatus();` | A technical *device* `thingy`, carried/worm by a human, for use for a particular purpose or activity. An `apparatus` should have access to the _puff_. The human version of a `sensor`.<br>Example: geiger counter, multi-meter; *a handheld device*<br>See also: [sensor](#sensor)| [apparat](/apparat.md) |
| appliance | `_applian()`<br>`_appliance()` <a name="appliance"></a>| A *device* or *piece of equipment* `thingy` designed to perform a specific task, that is **not** attached / carried / worm by a human. An `apparatus` can or cannot have access to the _puff_. The human version of a `mach`*[ine].*<br>Example: refrigerator, washing machine<br>See also: [mach](#mach) | [appliance](/applicance.md) |
| arena<a name="arena"></a> | `_arena();` | A representation of physically defined 3d space for a `thing`(s) to move freely around inside. There should be an attempt to represent physical (real-world) borders. The human version of a `zone`.<br>Example: atrium, open plan office floor<br>See also: [zone](#zone); [fence](#fence) | [arena](/arena.md) |
| attribute<a name="attribute"></a> |  `_attr()`<br>`_attribute()`  | Lorem ipsum, lorem ipsum, lorem ipsum.<br>Example: <br>See also: [spec](#spec) | [attr](/attr.md) |

## <a name="b"></a> B: [border](#border); [bot](#bot); [box](#box); [button](#button); 
| b | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| `border` <a name="border"></a> | .<br>Example: <br>See also: [wall](#wall) | [border](/border.md) |
| `box` <a name="box"></a> | A representation of a meta-physical enclosed space. The thing / meta-physical version of a `room`.<br>Example: inside a pit<br>See also: [room](#room) | [box](/box.md) |
| bot | `_bot();` | A construct present in the metaphysical world only. (Artificial Intelligence)<br>*cal*, *ChatBot* | [bot](/bot.md) |
| box    | `_object()_type(box);` | A  container used for the storage or transportation of its contents. |  [box](/box.md) |
| button | `_thing()_type(button);` | A remote device used to send simple remote procedure calls from human boolean interaction.<br>[Amazon Dash Button](https://en.wikipedia.org/wiki/Amazon_Dash) | [button](/button.md) |

## <a name="c"></a> C: [ceiling](#ceiling); [corridor](#corridor)
| c | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| cellphone, mobile phone | `_cellphone();`<br>`_mobot()_type(cellphone);` | A portable telephone that can make and receive calls over a radio frequency link while the user is moving within a telephone service area. | [cellphone](/cellphone.md) | 
| chair | `_object()_type(chair);` | One of the basic pieces of furniture, an actual representation of a seat. | [chair](/chair.md) |
| computer | `_comput();`<br>`_mobot()_type(computer);` | A digital electronic machine that can be programmed to carry out sequences of arithmetic or logical operations (computation) automatically. | [computer](/computer.md) |
| `ceiling` <a name="ceiling"></a>| An identified top _side_ of a representation space in the physical world. An undetermined human version of a `plafond`.<br>See also: [side](#side); [plafond](#plafond); [firma](#firma); [wall](#wall); [border](#border) | [ceiling](/ceiling.md) |
| `corridor` <a name="corridor"></a> | A `thing` representation of physically defined 3d space, designed for a human, to manoeuvre inside, predominately along a single plane. There should be an attempt for physical (real-world) borders. The human version of a `pipe`.<br>See also: `arena`; `fence`; `pipe`; `zone` | [corridor](/corridor.md) |

## <a name="d"></a>D: [door](#door)
| d | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| door<a name="door"></a> | `_object()_type(door);` | A `thing` representation of a physical doorway / gate, designed for a human.<br>See also: [portal](#portal); [gate](#gate) | [door](#door)
| doorbell | `_object()_type(doorbell);`| A doorbell is a signaling device typically placed near a door to a building's entrance. | [doorbell](/doorbell.md) |
| (smart doorbell) | `_doorbell();`<br>`_mobot()_type(doorbell);` | A smart doorbell is an internet-connected doorbell that notifies the smartphone or other electronic device of the home owner when a visitor arrives at the door.<br>[Google Next Hello](https://en.wikipedia.org/wiki/Google_Nest#Nest_Hello) | [doorbell](/doorbell.md) |

## <a name="e"></a>E: [equip](#equip)
| e | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| equipment<a name="equipment"></a> | `_equip()`<br>`_equipment()` | <br>See also: [`_apparat()`](#apparatus); [`_instru()`](#instrument); [`_peripher()`](#peripheral);  [`_sensor()`](#sensor) | [equipment](/equipment.md) |

## <a name="f"></a>F: [fence](#fence); [firma](#firma)
| f | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| freezer<br>fridge (refrigerator) | `_thing()_type(fridge);` | A commercial and home appliance consisting of a thermally insulated compartment and a heat pump (mechanical, electronic or chemical) that transfers heat from its inside to its external environment so that its inside is cooled to a temperature below the room temperature. | [fridge](/fridge.md) |
| *[geo-]*`fence` <a name="fence"></a> | |
| `firma` <a name="firma"></a> | An identified down _side_ of a representation space in the physical world. An undetermined human version of a `marack`.<br>See also: [side](#side); [marack](#marack); [ceiling](#ceiling); [wall](#wall); [border](#border); [ground](#ground); [track](#track) | [firma](/firma.md) |
| `floor` / `level` | |
| `foreign`*[er]* | |
| `form`*[ation]* | |

## <a name="g"></a>G: [gait](#gait); [gate](#gate)
| g | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| gait<a name="gait"></a> | `_gait()` | The thing version of `stride` | |
| gate | `_gate()` | | |
| ghost | `_ghost()` | | |
| guide | `_guide()` | | |

## <a name="h"></a>G: [human](#human)
| h | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| `human` | The human version of a `thing` / `robot`.  The non-human version of an `organic`.<br>See also: |

## <a name="i"></a>I: [instruct](#instruct); [label](#label)
| i | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| `instruct` | |

## <a name="j"></a>J: [jigger](#jigger); [jagger](#jagger)
| i | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| jagger |`instruct` | |
| `jigger`<br>`actuat`<br>`actuator`<br>`mover` <a  name="actuat"></a> | A child *device*  `thingette` that causes its parent `thingy` and/or sibling `thingette` to operate, usually providing motion. A public interface with the _puff_ should be avoided or at least strictly limited. The thing version of a `jagger`.<br>Example: motor controller; gearbox; motor<br>See also: [jigger](#jigger), [jagger](#jagger) | [jigger](/jigger.md) |


| l | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| lock | `_object()_type(lock);` | [lock](/lock.md) |
| (smart lock) | `_thing()_type(lock);` | An electromechanical lock which is designed to perform locking and unlocking operations on a door when it receives such instructions from an authorized device using a wireless protocol and a cryptographic key to execute the authorization process.<br>See [Smart lock](https://en.wikipedia.org/wiki/Smart_lock) | [lock](/lock.md) |
| lamp | `_object()_type(lamp);` | <br>See: [Light fixture](https://en.wikipedia.org/wiki/Light_fixture) | [lamp](/lamp.md) |
| `label` | |

| m | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| machine <a name="machine"></a> | `_mach();`<br>`_machin();`<br>`_machine();` | The stationary version of a `mech` | [machine](/machine.md) |
| mainpulator <a name="manipulator"> | ~~`_manip();`<br>`_manipulat();`<br>`_manipulator();`~~<br>`_equip()_type(mainpulator);` | | [manipulator](/manipulator.md) |
| map <a name="map"></a> | `_map()` | | [map](/map.md) |
| me | `me_`<br>`_me()` | |
| `mech`*[anical thing]* | The motion version of a `mach` |
| metric<a name="metric"></a> | `_metric()` |  |
| mode<a name="mode"></a> | `_mode()` | |
| mover | Use: `_actuat();` | A component that is responsible for moving and controlling a mechanism or system. In simple terms, it is a "mover". An actuator requires a control device and a source of energy.<br>See: [actuator](#actuator) | [mover](/actuator.md) |

| `obstacle` | |
| `organic` *[thing]* | |

| p | `{object}`<br>description | references |
|--|:--|---|
| personal robot | `{verb}_robot({moniker|uuid})_type(personal_robot);`<br>Kuni Mobile Robot | [personal_robot](/personal_robot.md) |
| printer | `{verb}_thing({moniker|uuid})_type(printer);`<br> | [printer](/printer.md) |
| `path` | |
| `payload` | |
| `pipe` | The thing version of a `corridor` |
| `plafond` | |
| `point` | <br>See also: `route`; `path` |
| `proc`*[edure]* | |
| `prog`*[ramme]* | |

| `robot` | <br>See also: `human`; `thing` |
| `room` | A representation of a physical enclosed space. The humnan / physical version of a `room`.  
| `route` | |

| s | `{object}`<br>description<br>examples | references |
|--|:--|---|
| Smart Speaker | `{verb}_thing({moniker|uuid})_type(smart_speaker);`<br>or `{verb}_thing({moniker|uuid})_type(voice_controller);`<br>Google Home Mini; Google Nest Mini; Amazon Echo | [smart_speaker](/smart_speaker.md) |
| switch | `{verb}_thing({moniker|uuid})_type(switch);` | |
| watch | `{verb}_mobot({moniker|uuid})_type(watch);` | |
| speaker | `{verb}_thing({moniker|uuid})_type(speaker);` | |
| `sensor` | The thing version of an `apparatus`.<br>See also: [apparat](#apparat) |
| `side` | | |
| `spec`*[ification]* | <br>See also: `attribute` |
| `stance` |  |
| `stride` | The human version of `gait` |
| `swarm` | |
| 

| `thing` | The thing version of a `human` |
| `track` | |

| `wall` | |
| `zone` | The thing version of an `arena` |


| `console` | A metaphysical presence used to only provide an interface to all other *thingies* | [console](/console.md) |
| `human`   | Representation of a human being, present and alive in the physical *'real'* world. The human version of a `thing` / `robot`.  The non-human version of an `organic`.<br>Example: *Fred Jones* | [human](/human.md) |
| `me`      | Representation of self | [me](/me/md) |
| `mobot`   | A conveyed *thingy* in the physical *'real'* world.<br>Examples: Samasung Galaxy watch, cellphone | [mobot](/mobot.md) |
| `organic` | Representation of a non-human being, present and alive in the physical *'real'* world.<br>Example: cat, dog | [organic](/organic.md) |
| `robot`   | A self-propelled *thingy* in the physical *'real'* world.<br>Examples: Boston Dynamics Spot, robot arm, drone<br>See also: `human`; `thing` | [robot](/robot.md)
| `thing`   | An immobile *thingy* in the physical *'real'* world.<br>Example: fridge, television | [thing](/thing/md) |
| `vehicle` | A guided *thingy* transporting `human`/`organic` thingies and/or controlled by a `human`.<br>Examples: car, airplane, ugv, radio-controlled toy car | [vehicle](/vehicle.md) |
| `thingy` | | [thingy](/thingy.md) |


_generat({generation});



_