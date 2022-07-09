# Lexicon

The lexicon of ***Diego*** is the full syntactical vocabulary of all statement compositions:

| lexicon | domain | type |description |
| --- | --- | --- | --- |
| `_abs(`*`numeric`*`)`<br>`_calc(|`*`numeric`*`|)` | abstract | *function* | Returns the [absolute value](../abstract/funct/abs.md) of *numeric*<br>Returns the [absolute value](../abstract/funct/abs.md) of *numeric* in an *expression* |
| `_acos(`*`numeric`*`)` | abstract | *function* | Returns the [arccosine](../abstract/funct/acos.md) of *numeric* |
| `_after(`*`date\|datetime\|time`*`)` | abstract | *condit* | Preceeding *object* [after](../abstract/condit/after.md) [date](../abstract/dt/date.md) \| [datetime](../abstract/dt/datetime.md) \| [time](../abstract/dt/time.md) for proceeding *object* to do proceeding *action* |
| `_at(`*`date\|datetime\|time`*`)` | abstract | *condit* | Preceeding *object* [at](../abstract/condit/at.md) [date](../abstract/dt/date.md) \| [datetime](../abstract/dt/datetime.md) \| [time](../abstract/dt/time.md) for proceeding *object* to do proceeding *action* |
| `_before(`*`date\|datetime\|time`*`)` | abstract | *condit* | Preceeding *object* [before](../abstract/condit/before.md) [date](../abstract/dt/date.md) \| [datetime](../abstract/dt/datetime.md) \| [time](../abstract/dt/time.md) for proceeding *object* to do proceeding *action* |
| `_calc(`*`expression`*`)` |  abstract | *method* | Use [calculation](../abstract/meth/calc.md) of *expression* for preceeding *object*, with proceeding *object* |
| `_decpl(`*`numericvalue`*`)`<br>`_decplaces(`*`numericvalue`*`)` | abstract | *setter* | Set the default number of decimal place to use in calcluations adn on display (as a setter) [decpl](../abstract/setter/decpl.md)<br/>See also [`fix`](../abstract/meth/fix.md) *method* |
| `_distan(`*`distancevalue`*`)`<br>`_distance(`*`distancevalue`*`)`<br>`_distan({unit},`*`distancevalue`*`)`<br>`_distance({unit},`*`distancevalue`*`)`<br> | metaphysic | *posit*<br/>*property* | Preceeding *object* of [distance](../metaphysic/prop/distan.md) of proceeding *object* |
| `_durat(`*`durationvalue`*`)`<br>`_duration(`*`durationvalue`*`)`<br>`_durat({unit},`*`durationvalue`*`)`<br>`_duration({unit},`*`durationvalue`*`)`<br> | metaphysic | *condit* | Preceeding *object* of [duration](../metaphysic/condit/durat.md) of proceeding *object* |
| `_during(`*`date`*`)` | abstract | *condit* | Preceeding *object* [during](../abstract/condit/during.md) [date](../abstract/dt/date.md) for proceeding *object* to do proceeding *action* |
| `_e()`<br>`_e(`*`decplaces`*`)` |  abstract | *constant* | Use [Euler's number](../abstract/const/e.md) for preceeding *object*, with proceeding *object* |
| `_ergcon(`*`ergconvalue`*`)`<br>`_ergcon({unit},`*`ergconvalue`*`)` | metaphysic | *property* | Preceeding *object* of [energy consumption](../metaphysic/prop/ergcon.md) of proceeding *object* |
| `_fix(`*`decplaces`*`)`<br/>`_tofix(`*`decplaces`*`)` | abstract | *method* | Converts preceeding *object-value* in to *decplaces* number of [fixed decimal places](../abstract/meth/fix.md) |
| `_for([`*`loopername`*`])` | abstract | *looper* | [for](../abstract/looper/for.md) |
| `_for(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` | abstract | *looper* | [for](../abstract/looper/for.md) |
| `_foreach(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` | abstract | *looper* |  |
| `_forin(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` |abstract | *looper* |  |
| `_forof(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` |  abstract | *looper* |  |
| `_goto()` | metaphysic | *verb* |  Preceeding *object(s)* [goto](../metaphysic/verb/goto.md) to proceeding *object(s)* |
| `_if_(`*`expression`*`)` | abstract | *operator* |  |
| `_ln(`*`numericvalue`*`)`<br>`_log(`*`numericvalue`*`)`<br>`_ln([`*`numericvariablename`*`])`<br>`_log([`*`numericvariablename`*`])`  |  abstract | *function* | Use [natural logarithm](../abstract/funct/ln.md) (base [e](../abstract/const/e.md)) for preceeding *object*, with proceeding *object*<br>See also: [ln2](../abstract/const/ln2.md); [ln10](../abstract/const/ln10.md) |
| `_ln10()`<br>`_ln10(`*`decplaces`*`)`<br>`_ln(10)`<br>`_ln(10)_decpl(`*`decplaces`*`)` |  abstract | *constant* | Use [natural logarithm of 10](../abstract/const/ln10.md) for preceeding *object*, with proceeding *object*<br>See also: [ln](../abstract/funct/ln.md) |
| `_ln2()`<br>`_ln2(`*`decplaces`*`)`<br>`_ln(2)`<br>`_ln(2)_decpl(`*`decplaces`*`)` |  abstract | *constant* | Use [natural logarithm of 2](../abstract/const/ln2.md) for preceeding *expression*, with proceeding *object*<br>See also: [ln](../abstract/funct/ln.md) |
| `_mapprovider(`*`mapprovider`*`)` | metaphysic | *setter* | [mapprovider](../metaphysic/setter/mapprovider.md) |
| `_msg(`*`message`*`)`<br>`_message(`*`message`*`)` | metaphysic | *??* | Proceed with *[message](../metaphysic/obj/msg.md)* *moniker* |
| `_orientat(`*`variablename`*`)`<br>`_orientation(`*`variablename`*`)` | metaphysic | *posit-variable* |  |
| `_orientat(`*`x`*`,`*`y`*`,`*`j`*`,`*`k`*`)`<br>`_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)`<br>`_orientation(`*`x`*`,`*`y`*`,`*`j`*`,`*`k`*`)`<br>`_orientation(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)` | metaphysic | *posit-action* |  |
| `_orientat(`*`x`*`,`*`y`*`,`*`z`*`)`<br>`_orientation(`*`x`*`,`*`y`*`,`*`z`*`)` | metaphysic | *posit-action* |  |
| `_pi()`<br>`_pi(`*`decplaces`*`)` |  abstract | *constant* |  |
| `_pose(`*`moniker`*`)` | metaphysic | *posit-object* | Proceed with *[pose](../metaphysic/obj/pose.md)* *moniker* |
| `_ret()`<br>`_ret({`*`datatype`*`})` | abstract | *function* | [ret](../abstract/funct/ret.md)
| `_scalar(`*`variablename`*`)` | metaphysic | *posit-variable* | Proceed with *[scalar](../metaphysic/obj/scalar.md)* *variablename* |
| `_sqrt2()`<br>`_sqrt2(`*`decplaces`*`)` |  abstract | *constant* |  |
| `_to()` | abstract | *operator* | Preceeding from *object(s)* [to](../abstract/condit/to.md) proceeding *object(s)* |
| `_to()` | metaphysic | *operator* | Preceeding *object(s)* *action* [to](../metaphysic/condit/to.md) proceeding *object(s)* |
| `_tour(`*`moniker`*`)` | metaphysic | *posit-object* | Proceed with *[tour](../metaphysic/obj/tour.md)* *moniker* |
| `_txt(`*`text`*`)`<br>`_text(`*`text`*`)` | abstract | *property* | Proceed with *test* of *[text](../abstract/prop/txt.md)* *moniker* |
| `_unit(`*`unit`*`)` | metaphysic | *posit-datatype* |  |
| `_using(`*`moniker`*`)`<br/>`_using([`*`variablename`*`])` | metaphysic | *condit* | [using](../metaphysic/condit/using.md) |
| `;` | abstract | *statement-operator* | [Termination](../abstract/special/semicolon.md) of preceeding *statement* |
| `:` | abstract | *statement-operator* | Termination of preceeding *statement* and the negative outcome [beginning](../abstract/special/elvish.md) of proceeding *statement* |
| `?` | abstract | *statement-operator* | Termination of preceeding *statement* and the positive outcome [beginning](../abstract/special/elvish.md) of proceeding *statement* |
| `(())` | abstract<br>metaphysic<br>physic | *object*<br>*action* | Refer to last referenced oldest generation *object* or refer to oldest generation nested *object*|
| `()` | abstract<br>metaphysic<br>physic | *object*<br>*action* | Refer to last referenced youngest generation *object* or refer to youngest generation nested *object* |
| `([`*`robotvariablename`*`])` | abstract<br>metaphysic<br>physic | *object* |  Refer to *[robot](../physic/obj/robot.md)* of value of *robotvariablename* [variable](../abstract/obj/var.md) of datatype *[robot](../physic/obj/robot.md)* |
| `([`*`waypointvariablename`*`])` | physic | *object*<br>*variable* | Refer to *[waypoint](../metaphysic/obj/waypoint.md)* of value of *robotvariablename* [variable](../abstract/obj/var.md) of datatype *[waypoint](../metaphysic/obj/waypoint.md)* |
| `({robot},[`*`variablename`*`])` | physic | *object*<br>*datatype*<br>*variable* | Refer to [robot-type](../physic/obj/robot.md) [robot](../physic/obj/robot.md) of value *variablename* [variable](../abstract/obj/var.md) |
| `({waypoint},[`*`variablename`*`])` | metaphysic | *object*<br>*datatype*<br>*variable* | Refer to [waypoint-type](../metaphysic/obj/waypoint.md) [waypoint](../metaphysic/obj/waypoint.md) of value *variablename* variable |
| `(`*`moniker`*`)` | abstract<br>metaphysic<br>physic | *object*<br>*action* |  Refer to last referenced eldest generation *object* monikered *moniker* |
| `(`*`robotmoniker`*`)` | physic | *object* | Refer to [robot](../physic/obj/robot.md) *robotmoniker* |
| `(`*`waypointmoniker`*`)` | metaphysic | *object* | Refer to [waypoint](../metaphysic/obj/waypoint.md) *waypointmoniker* |
| `[]` | abstract<br>metaphysic<br>physic | *object*<br>*variable* | Refer to last referenced *object*/*variable* or 'this' parent scoped *object* |
| `[`*`moniker`*`]` | abstract<br>metaphysic<br>physic | *object*<br>*variable* | Refer to last referenced *object* |
| `[`*`variablename`*`]` | abstract<br>metaphysic<br>physic | *variable* | Refer to last referenced *[variable](../abstract/obj/var.md)* monikered *moniker* |
| `{}` | abstract | *datatype* | Declaration or convert / cast of a [variant](../abstract/dt/variant.md) datatype. |
| `{}` | abstract | *datatype* | Declaration or convert / cast of a [variant](../abstract/dt/variant.md) datatype. |
| `{`*`datatype`*`}` | abstract | *statement* | Declaration or convert / cast of a [datatype](../abstract/statem/declar.md) |
| `{`*`datatype`*`}` | abstract | *statement* | Declaration or convert / cast of a [datatype](../abstract/statem/declar.md) |
| `{`*`objtype`*`}` | abstract | *statement* | Declaration or convert / cast of an [object-type](../abstract/statem/declar.md) |
| `{`*`objtype`*`}` | abstract | *statement* | Declaration or convert / cast of an [object-type](../abstract/statem/declar.md) |
| `{float}` | abstract<br>datatype | | Float abstract datatype | [float](../abstract/dt/float.md) |
| `{int}` | abstract<br>datatype | | Integer abstract datatype | [int](../abstract/dt/int.md) |
| `{int32}` | abstract<br>datatype | | Integer abstract datatype | [int](../abstract/dt/int.md) |
| `{int64}` | abstract<br>datatype | | Integer abstract datatype | [int](../abstract/dt/int.md) |
| `+` | abstract | *operator* | |
| `++` | abstract | *operator* | |
| `+=` | abstract | *operator* | |
| `action` <a name="action"></a> | abstract<br>action | | [action](/action.md) |
| `actuat(`*`moniker`*`)`<br>`actuator(`*`moniker`*`)` <a  name="actuat"></a> | physic<br>obj | [actuat](/actuat.md) |
| `add_`*`<object\|action>`* | abstract<br>metaphysic<br>physic | *verb* | Declare *object* |
| `ai`<br>`bot` | metaphysic<br>obj | | A construct present in the metaphysical world only. (Artificial Intelligence)<br>Example: *cal*, *ChatBot* | [ai](/bot.md) |
| `alert_`*`<thingy>`*`(`*`moniker`*`)` | physic | *verb* | [alert](../physic/verb/alert.md) |
| `apparat(`*`moniker`*`)`<br>`apparatus(`*`moniker`*`)` | physic | *object* | [apparat](../physic/obj/apparat.md) |
| `applian`<br>`applicance` |  physic<br>obj | | A smart mobot that can safetly be classified as a *household applicance*.<br>Examples: washing machine, dishwasher.<br>`with_applian(dishWasher)_start(normalWash);` | [applian](applian.md) |
| `arena(`*`moniker`*`)` | metaphysic | *object* | [arena](../metaphysic/obj/arena.md) |
| `ask_` | metaphysic | *verb* | Requests information, to be returned with `tell` *verb*<br/>`ask_drone(drone1)_stat(avg_altitude);`<br/>`tell_drone(drone1)_stat(avg_altitude)_value(22.893);` | [ask](/ask.md)<br />_see also:_ [tell](/end/md) |
| `ask_`*`<thingy>`* | physic | *verb* | *[Ask](../metaphysic/verb/ask.md)* proceeding *thingy* |
| `attr`<br>`attribute` <a name="attr"></a> | abstract<br>obj | | Lorem ipsum, lorem ipsum, lorem ipsum.<br>Example: <br>See also: [spec](#spec) | [attr](/attr.md) |
| `begin_`*`<object\|action>`* | abstract<br>metaphysic | *verb* | [Begin](../metaphysic/verb/begin.md) *action* on proceeding *object* |
| `border` | physic<br>obj | | Floor marking showing borders, created using paint, tape, or, decals.<br>Example:<br><img src="/_img/256px-Floor_marking_5S_safety_Scanfil_Sieradz.jpg" alt="wayfind markings" style="width:200px;"/><br><sub>"<a href="https://commons.wikimedia.org/wiki/File:Floor_marking_5S_safety_Scanfil_Sieradz.jpg">Floor marking at the Scanfil Poland factory in Sieradz</a>"<br>by <a href="https://commons.wikimedia.org/wiki/User:Boston9">Adrian Grycuk</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/3.0/pl/">CC BY 2.0 Poland</a> </sub> | [border](border.md) |
| `bot`<br>`ai` | metaphysic<br>obj | | A construct present in the metaphysical world only. (Artificial Intelligence)<br>Example: *cal*, *ChatBot* | [bot](/bot.md) |
| `box` <a name="box"></a> | metaphysic<br>obj | | A representation of a meta-physical enclosed space. The thing / meta-physical version of a `room`.<br>Example: inside a pit<br>See also: [room](#room) | [box](/box.md) |
| `calc_`*`<object>`*`(`*`objmoniker`*`)`<br/>`calc_`*`<object>`*`(`*`ofmoniker`*`)` | abstract<br/>metaphysic | *verb* | [calc](../metaphysic/verb/calc.md) |
| `call_`*`<object>`* | metaphysic | *verb* | [call](../metaphysic/verb/call.md) |
| `canal` | physic | *object* | [canal](../physic/obj/canal.md) |
| `ceiling` | physic | *object* | <a name="ceiling"></a>| An identified top _side_ of a representation space in the physical world. | [ceiling](ceiling.md) |
| `channel(`*`moniker`*`)` | physic | *object* |An exclusive sub-section of a `workspace`, sometimes referred to as a _conversation_ | [channel](../metaphysic/obj/channel.md) |
| `cloud(`*`moniker`*`)`   | physic | *object* | |
| `commrelay(`*`moniker`*`)` | | | https://www.autonodyne.com/AUTO_behaviors2.html | [comrelay](#comrelay) |
| `computer(`*`moniker`*`)`<br>`comput(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[computer](../metaphysic/obj/computer.md)* *moniker* |
| `concord(`*`settings`*`)` | abstract<br>metaphysic | *setter* |  |
| `consens(`*`settings`*`)`<br>`consensus(`*`settings`*`)` | abstract<br>metaphysic | *setter* | [consens](../metaphysic/setter/consens.md) |
| `console` | metaphysic | *object* | A metaphysical presence used to only provide an interface to all other *thingies* | [console](../metaphysic/obj/console.md) |
| `corridor` | metaphysic | *object* | <a name="corridor"></a> | A representation of a physically defined 3d space, designed for a human, to manoeuvre inside, predominately along a single plane.<br>There should be an attempt for physical (real-world) borders. | [corridor](../metaphysic/obj/corridor.md) |
| `counter(`*`variablename`*`)` | abstract | *object* | [counter](../abstract/obj/counter.md) |
| `counter` | | [counter](../abstract/obj/counter.md)
| `decisiven(`*`settings`*`)`<br>`decisiveness(`*`settings`*`)` | metaphysic | *setter* |  |
| `distan(`*`objectname`*`)`<br/>`distance(`*`objectname`*`)` | metaphysic | *object* | [distan](../metaphysic/obj/distan.md) |
| `door` | metaphysic | *object* | <a name="door"></a> | A `thing` representation of a physical doorway / gate, designed for a human.<br>See also: [portal](#portal); [gate](#gate) | [door](#door)
| `equip(`*`moniker`*`)`<br>`equipment(`*`moniker`*`)` | metaphysic | *object* | <br>See also: `apparatus`; `instru`*[ment]*; `peripheral`;  `sensor` | [equip](equip.md) |
| `firma` | metaphysic | *object* | An identified down _side_ of a representation space in the physical world. | [firma](../physic/obj/firma.md) |
| `floor`<br>`level` | | [floor](#floor.md)<br>[level](#level) |
| `fog(`*`moniker`*`)` | metaphysic | *object* | A zone (`puff`) used for diego communication that relies on UDP [fog](../metaphysic/obj/fog.md) |
| `follow_`*`<object>`* | metaphysic | *verb* | *[Follow](../metaphysic/verb/follow.md)* proceeding *object* |
| `foreign(`*`moniker`*`)`<br>`foreigner(`*`moniker`*`)` | [foreign](../metaphysic/obj/foreign.md) |
| `form`*[ation]* | |
| `funct(`*`moniker`*`)`<br>`_funct(`*`moniker`*`)`<br>`function(`*`moniker`*`)`<br>`_function(`*`moniker`*`)` | abstract | *action* | [funct](../abstract/obj/funct.md) |
| `gait(`*`moniker`*`)` | metaphysic | *object* | The thing version of `stride` [gait](../metaphysic/obj/gait.md)
| `gate` | metaphysic | *object* | [gate](../metaphysic/obj/gate.md) |
| `geofence` <a name="fence"></a> | | [geofence](../metaphysic/obj/geofence.md) |
| `ghost(`*`moniker`*`)` | metaphysic | *object* | [ghost](../metaphysic/obj/ghost.md) |
| `gimbal` | | |
| `go_`*`<object>`* | physic | *verb* | Manouve Proceeding *object* to [go](../metaphysic/verb/go.md) proceeding *action* on *object* |
| `goal(`*`moniker`*`)`<br>`_goal(`*`moniker`*`)` | metaphysic | *posit-object* | *Action* on *[goal](../metaphysic/obj/goal.md)* *moniker*<br>Proceed with *[goal](../metaphysic/obj/goal.md)* *moniker* |
| `goto_`*`<object>`* | physic | *verb* | Manouve Proceeding *object* to [goto](../metaphysic/verb/goto.md) proceeding *object* |
| `guide` | |
| `handler` | | |
| `hold`, `household` |||
| `human(`*`moniker`*`)` | physic | *object* | Representation of a human being, present and alive in the physical *'real'* world. |
| `instruct(`*`moniker`*`)`<br>`instruction(`*`moniker`*`)` | abstract<br>metaphysic | *action* | [instruct](../metaphysic/obj/instruct.md) |
| `jagger(`*`moniker`*`)` | metaphysic | *object* | jagger](#jagger) | [jigger](/jigger.md) |
| `ject(`*`moniker`*`)` | metaphysic | *object* | A non-smart object in the physical *'real'* world.<br>Examples: a rock, a shopping trolley, a chair, etc.<br>`with_search(findTVRemote)_found()_object(TVRemote);` | [object](../physic/obj/object.md) |
| `jigger(`*`moniker`*`)`| metaphysic | *object* | |
| `kill_`*`<human\|organic>`*<br>`kill_`*`<object>`* | physic | *verb* | [Kill](../metaphysic/verb/kill.md) proceeding *human*/*organic*<br>[De-commission](../metaphysic/verb/kill.md) proceeding *object* |
| `kill_`*`<variable>`* | abstract | *verb* | *[Kill](../abstract/verb/kill.md)* proceeding *variable* |
| `label` | |
| `lead_`*`<object>`* | metaphysic | *verb* | *[lead](../metaphysic/verb/lead.md) proceeding *object* |
| `lib`, `library` | | |
| `load_`*`<object>`* | metaphysic | *verb* | *[load](../metaphysic/verb/load.md)* proceeding *object* |
| `mach(`*`moniker`*`)`<br>`machine(`*`moniker`*`)` | physic | *object* | [mach](../physic/obj/mach.md) |
| `map(`*`moniker`*`)` | metaphysic | *object* | |
| `me_`*`<object\|action>`* | abstract | *special* | *[Me](../abstract/special/me/md)* (or this) does *action* or my *object*...<br>Representation of self |
| `mech(`*`moniker`*`)`<br> | physic | *object* | |
| `metric` | |
| `mist(`*`moniker`*`)`    | metaphysic | *object* | A connectivity zone (wired or wireless) with the distance range of < 10m.<br>For example: RFID | [mist](/mist.md) |
| `mobot(`*`moniker`*`)`   | metaphysic | *object* | A conveyed *thingy* in the physical *'real'* world.<br>Examples: Samasung Galaxy watch, cellphone | [mobot](/mobot.md) |
| `mode` | |
| `mover(`*`moniker`*`)` | See: [jigger](#jigger) | |
| `msg_`*`<object>`* | metaphysic | *verb* | *[message](../metaphysic/verb/msg.md)* proceeding *object* |
| `msg(`*`moniker`*`)`<br>`message(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[message](../metaphysic/obj/msg.md)* *moniker* |
| `namespace(`*`moniker`*`)`<br>`ns(`*`moniker`*`)` | abstract | object | [namespace](../abstract/obj/namespace.md) |
| `neigh`, `neighbour` |||
| `ns[]` | abstract | object | [namespace](../abstract/obj/namespace.md) |
| `ob`  | metaphysic | *object* | A civilian[^civilian] immobile ject in the  physical *'real'* world.<br>Examples: unidentified lampost (or thing pointing out of the ground), etc.<br>`call_robot(alif)_found()_ob()_photo()_blob(d3Mtd2l6EAMyCwguEBDIL`*`...`* | [obstacle](../metaphysic/onstacle.md) | [ob](ob.md) |
| `object`  | metaphysic | *object* | A non-smart immobile ject in the physical *'real'* world.<br>Examples: a rock, a chair, etc.<br>`call_robot(alif)_found()_object(carKeys);` | [stacle](../metaphysic/obj/stacle.md) | [object](../physic/obj/object.md) |
| `obstacle` | |
| `organic` | metaphysic | *object* | Representation of a non-human being, present and alive in the physical *'real'* world.<br>Example: cat, dog | [organic](/organic.md) |
| `package` | | |
| `path(`*`moniker`*`)` | metaphysic | *object* | [path](../metaphysic/obj/path.md) |
| `payload(`*`moniker`*`)`<br>`pload(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[payload](../metaphysic/obj/payload.md)* *moniker* |
| `pipe(`*`moniker`*`)` | metaphysic | *object* | [duct](../metaphysic/obj/duct.md)  | [pipe](../metaphysic/obj/pipe.md) |
| `plafond` | |
| `poi(`*`moniker`*`)` | metaphysic | *object* |
| `point(`*`moniker`*`)` | abstract | *object* | [point](../abstract/obj/point.md) |
| `poll_`*`<object>`*`(`*`objmoniker`*`)`<br/>`poll_`*`<object>`*`(`*`ofmoniker`*`)` | metaphysic | *verb* | [poll](../metaphysic/verb/poll.md)  |
| `printer(`*`moniker`*`)`<br>`ptr(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[printer](../metaphysic/obj/printer.md)* *moniker* |
| `proc`, ``proced`, `procedure` | | |
| `process(`*`moniker`*`)`<br>`process(`*`moniker`*`)` | metaphysic | *object* |  |
| `prog(`*`moniker`*`)`, `program(`*`moniker`*`)`, `programme(`*`moniker`*`)` | | |
| `puff(`*`moniker`*`)` |
| `rail(`*`moniker`*`)` | metaphysic | *object* | [rail](../physic/obj/rail.md) |
| `robot(`*`moniker`*`)`<br>`_robot(`*`moniker`*`)` | physic | *object* | *Action* on *[robot](../physic/obj/robot.md)* *moniker* |
| `roi(`*`moniker`*`)`<br>`regionofinterest(`*`moniker`*`)` | metaphysic | *object* | [roi](../metaphysic/obj/roi.md) |
| `room` | | | A representation of a single physical enclosed space for a `thingy` to move freely around inside. | [chamber](../metaphysic/chamber.md) | [room](../physic/obj/room.md) |
| `route(`*`moniker`*`)`<br/>`_route(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[route](../metaphysic/obj/route.md)* *moniker*<br/>Proceed with *[route](../metaphysic/obj/route.md)* *moniker* |
| `route` | |
| `scalar` | metaphysic<br>obj | | [scalar](../metaphysic/obj/scalar.md) |
| `scan` | |
| `type(`*`moniker`*`)`<br>`_type(`*`moniker`*`)`<br>`{`*`moniker`*`}` | |
| `sensor(`*`moniker`*`)`<br>`_sensor(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[sensor](../metaphysic/obj/sensor.md)* *moniker*<br>Proceed with *[sensor](../metaphysic/obj/sensor.md)* *moniker* |
| `set_`*`<setter>`*`(`*`settings`*`)` | abstract<br>metaphysic | *verb* | [Set](../metaphysic/verb/set.md) the *setter* to *settings* settings |
| `shaft(`*`moniker`*`)` | physic | *object* | [shaft](../physic/obj/shaft.md) |
| `side` | | |
| `spec`<br>`specification` | <br>See also: `attribute` | [spec](../physic/obj/spec.md) |
| `spine` | | [spine](../metaphysic/obj/spine.md) |
| `stance` |  |
| `stealth` |
| `stride` | | | The human version of `gait` |
| `study_`*`<object>`* | physic | *verb* | *[Study](../metaphysic/verb/study.md)* proceeding *object* |
| `sub` | | | A civilian[^civilian] mobile ject in the  physical *'real'* world.<br>Exmaples: *unidentified moving animal*, *unidentified flying object*<br>`with_robot(tha)_follow()_sub(e32f0);` | [substacle](../metaphysic/substacle.md) | [sub](sub.md) |
| `subject` | | | A non-smart mobile ject in the  physical *'real'* world.<br>Examples: a shopping trolley object<br>`with_robot(sha)_follow()_subject(ball_ef42b);` | [hunderan](../metaphysic/obj/hinderan.md)<br>*[ghost](../metaphysic/obj/ghost.md)* | [subject](subject.md) |
| `swarm` | |
| `tail_`*`<object>`* | metaphysic | *verb* | *[Tail](../metaphysic/verb/tail.md)* behind proceeding *object* |
| `thing` <a name="thing"></a> | physic<br>obj | | An immobile *thingy* in the physical *'real'* world.<br>Example: fridge, television | [thing](/thing/md) |
| `thingy({robot},`*`moniker`*`)`<br>`add_thingy(`*`moniker`*`)_type(robot)` | physic | *verb-object*<br>*datatype* | *Action* on *[thingy](../physic/obj/thingy.md)* *moniker* of datatype [robot](../physic/obj/robot.md) |
| `to` <a name="to"></a> | metaphysic<br>posit | | [to](../metaphysic/condit/to.md) |
| `toward`<br>`towards` <a name="toward"></a> | metaphysic<br>posit | | [toward](../metaphysic/condit/toward.md) |
| `track` <a name="track"></a> | physic<br>obj | | Floor/ground marking the side borders of a lane.<br>Example:<br><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/All-weather_running_track.jpg/800px-All-weather_running_track.jpg?20170320005232" alt="track" style="width:200px;"/><br><sub>"<a href="https://commons.wikimedia.org/wiki/File:All-weather_running_track.jpg">An all-weather running track (photo taken at the Dalin Sports Park, Chiayi, Taiwan)</a>"<br>by <a href="https://commons.wikimedia.org/wiki/User:Mk2010">Mk2010</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0">CC BY 4.0 International</a> </sub> | [track](track.md) |
| `tunnel` | physic<br>obj | | Physical bar or continuous line of bars construction used to physically guide object along a pre-defined route.<br>Example:<br><img src="" alt="tunnel" style="width:200px;"/><br><sub>"<a href=""></a>"<br>by <a href=""></a> is licensed under <a href="">CC BY </a></sub> | [tunnel](tunnel.md) |
| `unload_`*`<object>`* | metaphysic | *verb* | *[Unload](../metaphysic/verb/unload.md)* proceeding *object* |
| `var`<br>`variable` | abstract<br>obj | | [var](../abstract/obj/var.md)
| `vector(`*`moniker`*`)`<br>`_vector(`*`moniker`*`)` | metaphysic | *object*<br>*posit-object* | *Action* on *[vector](../abstract/obj/vector.md)* *moniker*<br>Proceed with *[way](../metaphysic/obj/way.md)* *moniker* |
| `vehicle` | physic<br>obj | | A guided *thingy* transporting `human`/`organic` thingies and/or controlled by a `human`.<br>Examples: car, airplane, <abbr title="uncrewed ground vehicle">ugv</abbr>.<br>`with_vehicle(familyCar)_equip(frontLeftWheel)_metric()_tyrepress();` | [vehicle](vehicle.md) |
| `verb(`*`moniker`*`)` | meta-abstract | *object* | *Action* on *[verb](../abstract/meta/verb.md)* *moniker* |
| `wall(`*`moniker`*`)` | physic | *object* | [litsan](../metaphysic/obj/litsan.md) | [wall](../physic/obj/wall.md) |
| `way(`*`moniker`*`)`<br>`_way(`*`moniker`*`)` | metaphysic | *object*<br>*posit-object* | *Action* on *[way](../metaphysic/obj/way.md)* *moniker*<br>Proceed with *[way](../metaphysic/obj/way.md)* *moniker* |
| `wayfind` | | | Wayfinding floor signature, created using paint, tape, or, decals.<br>Example:<br><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Long-distance_Bus_Navigation_in_Japan.jpg/800px-Long-distance_Bus_Navigation_in_Japan.jpg?20140622041451" alt="wayfind markings" style="width:200px;"/><br><sub>"<a href="https://commons.wikimedia.org/wiki/File:Long-distance_Bus_Navigation_in_Japan.jpg">Tokyo Station</a>" by <a href="https://www.flickr.com/people/36516818@N00">mrhayata</a> is licensed under <a href="https://creativecommons.org/licenses/by/2.0/">CC BY 2.0</a></sub> | [route](../metaphysic/route.md)  | [wayfind](../physic/obj/wayfind.md) |
| `waypoint(`*`moniker`*`)`<br>`wp(`*`moniker`*`)`<br>`_waypoint(`*`moniker`*`)`<br>`_wp(`*`moniker`*`)` | metaphysic | *object*<br>*posit-object* | *Action* on *[waypoint](../metaphysic/obj/waypoint.md)* *moniker*<br>Proceed with *[waypoint](../metaphysic/obj/waypoint.md)* *moniker* |
| `with_`*`<object>`*`(`*`moniker`*`)` | abstract<br>metaphysic<br>physic | *verb* | Refer to *object* of *moniker* |
| `workspace` | | | An exclusive section of a `puff`, sometimes called a _room_ |
| `world(`*`verbmoniker`*`)` | physic | *special* | *Action* of *verbmoniker* on *[world](../physic/special/world.md)* |
| `zone` | metaphysic | *object* | The thing version of an `arena` [zone](../metaphysic/obj/zone.md) |



