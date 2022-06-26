# Thingys / Thingies

| a | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| actuator | `_actuat({moniker\|uuid});`<br>`_compon({moniker\|uuid})_type(actuator);` | A component that is responsible for moving and controlling a mechanism or system. In simple terms, it is a "mover". An actuator requires a control device and a source of energy. | [actuator](/actuator.md) |


| b | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| bot | `_bot({moniker\|uuid});` | A construct present in the metaphysical world only. (Artificial Intelligence)<br>*cal*, *ChatBot* | [bot](/bot.md) |
| box    | `_object({moniker\|uuid})_type(box);` | A  container used for the storage or transportation of its contents. |  [box](/box.md) |
| button | `_thing({moniker\|uuid})_type(button);` | A remote device used to send simple remote procedure calls from human boolean interaction.<br>[Amazon Dash Button](https://en.wikipedia.org/wiki/Amazon_Dash) | [button](/button.md) |


| c | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| cellphone, mobile phone | `_cellphone({moniker\|uuid});`<br>`_mobot({moniker\|uuid})_type(cellphone);` | A portable telephone that can make and receive calls over a radio frequency link while the user is moving within a telephone service area. | [cellphone](/cellphone.md) | 
| chair | `_object({moniker\|uuid})_type(chair);` | One of the basic pieces of furniture, an actual representation of a seat. | [chair](/chair.md) |
| computer | `_comput({moniker\|uuid});`<br>`_mobot({moniker\|uuid})_type(computer);` | A digital electronic machine that can be programmed to carry out sequences of arithmetic or logical operations (computation) automatically. | [computer](/computer.md) |

| d | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| doorbell | `_object({moniker\|uuid})_type(doorbell);`| A doorbell is a signaling device typically placed near a door to a building's entrance. | [doorbell](/doorbell.md) |
| (smart doorbell) | `_doorbell({moniker\|uuid});`<br>`_mobot({moniker\|uuid})_type(doorbell);` | A smart doorbell is an internet-connected doorbell that notifies the smartphone or other electronic device of the home owner when a visitor arrives at the door.<br>[Google Next Hello](https://en.wikipedia.org/wiki/Google_Nest#Nest_Hello) | [doorbell](/doorbell.md) |

| e | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|


| l | `{object}` | description<br>_examples_ | API |
|--|:--|---|---|
| lock | `_object({moniker\|uuid})_type(lock);` | [lock](/lock.md) |
| (smart lock) | `_thing({moniker\|uuid})_type(lock);` | An electromechanical lock which is designed to perform locking and unlocking operations on a door when it receives such instructions from an authorized device using a wireless protocol and a cryptographic key to execute the authorization process.<br>See [Smart lock](https://en.wikipedia.org/wiki/Smart_lock) | [lock](/lock.md) |
| lamp | `_object({moniker\|uuid})_type(lamp);`<br>See: [Light fixture](https://en.wikipedia.org/wiki/Light_fixture) | [lamp](/lamp.md) |


| p | `{object}`<br>description | references |
|--|:--|---|
| personal robot | `{verb}_robot({moniker|uuid})_type(personal_robot);`<br>Kuni Mobile Robot | [personal_robot](/personal_robot.md) |
| printer | `{verb}_thing({moniker|uuid})_type(printer);`<br> | [printer](/printer.md) |




| s | `{object}`<br>description<br>examples | references |
|--|:--|---|
| Smart Speaker | `{verb}_thing({moniker|uuid})_type(smart_speaker);`<br>or `{verb}_thing({moniker|uuid})_type(voice_controller);`<br>Google Home Mini; Google Nest Mini; Amazon Echo | [smart_speaker](/smart_speaker.md) |
| switch | `{verb}_thing({moniker|uuid})_type(switch);` | |
| watch | `{verb}_mobot({moniker|uuid})_type(watch);` | |
| speaker | `{verb}_thing({moniker|uuid})_type(speaker);` | |

| 


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