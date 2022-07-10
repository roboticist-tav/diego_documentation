# Lexicon

The lexicon of ***Diego*** is the full syntactical vocabulary of all statement compositions:

| lexicon | domain | type |description |
| --- | --- | --- | --- |
| <a name=";"></a> *`<comand>`*`;` | abstract | *statement-operator* | [Termination](../abstract/special/semicolon.md) of preceeding *statement* |
| <a name=":"></a> `: `*`<command>`* | abstract | *statement-operator* | Termination of preceeding *statement* and the [negative outcome](../abstract/special/elvish.md) beginning of proceeding *statement* |
| <a name="?"></a> `? `*`<command>`* | abstract | *statement-operator* | Termination of preceeding *statement* and the [positive outcome](../abstract/special/elvish.md) beginning of proceeding *statement* |
| <a name="(())"></a> `(`*`moniker`*`)`<br>`()`<br>`(())` | abstract<br>metaphysic<br>physic | *object* | Refer to *object* monikered *moniker*<br>Refer to last referenced youngest generation *object* or refer to youngest generation nested *object*<br>Refer to last referenced oldest generation *object* or refer to oldest generation nested *object* |
| <a name="([])"></a> `([`*`variablemoniker`*`])`<br>`({datatype},[`*`variablemoniker`*`])` | abstract<br>metaphysic<br>physic | *object* |  Refer to *variable* *object* of value of *variablemoniker*<br>Refere to *variable* *object* of value of *variablemoniker* to datatype *datatype* |
| <a name="[]"></a> `[`*`variablemoniker`*`]`<br>`[]`<br>`[`*`moniker`*`]` | abstract<br>metaphysic<br>physic | *object*<br>*variable* | Refer to *variable* *object* *variablemoniker*<br>Refere to last scoped *variable* or 'this' parent scoped *object*<br>Refer to object *moniker* |
| <a name="{}"></a> `{`*`datatype`*`}`<br>`{}` | abstract | *statement* | [Datatype](../abstract/statem/datatype.md) declaration, or, cast of datatype *datatype*<br>Declare variant, or, cast to variant datatype |
| <a name="❬❭"></a> `❬`*`unit`*`❭`<br>`❬`*`unitsystem`*`❭`<br>`❬❭` | metaphysic | *statement* | [Unit](../metaphysic/statem/unit.md) declaration, or, cast of object *object*<br>Declare variant, or, cast to variant unit |
| <a name="+_a"></a> `+`, `-`, `*`, `×`, `**`, `/`, `÷`, `%`, `𝐦`, `𝐦𝐨𝐝` | abstract | *operator* | Arithmetic operators |
| <a name="+_b"></a> `²`, `³`, `^`, `ⁱ`, `√`, `∛`, `∜` | abstract | *operator* | Exponent operators |
| <a name="+_c"></a> `++`, `∆`, `--`, `—`, `∇` | abstract | *operator* | Crement operators|
| <a name="+_d"></a> `=`, `+=`, `-=`, `*=`, `×=`, `^=`, `/=`, `÷=`, `%=`  | abstract | *operator* | Assignment operators |
| <a name="+_e"></a> `&`, `+`, `+=`, `&=`  | abstract | *operator* | String operators |
| <a name="+_f"></a> `==`, `===`, `≡`, `≢`, `≅`, `≈`, `≊`, `!=`, `<>`, `≠`, `<`<br>`≮`, `<=`, `≤`, `≨`, `>`, `≯`, `>=`, `≥`, `≩` | abstract | *operator* | Comparison operators |
| <a name="+_g"></a>  `?`*`...`*`:` | abstract | *operator* | Tenary Operator |
| <a name="+_h"></a>  `&&`, `∧`, `||`, `∨`, `!`, `¬`  | abstract | *operator* | Logical Operators |
| <a name="+_i"></a>  `&`, `⊼`, `|`, `~`, `≁`, `^`, `⊻`, `<<`, `␏`, `>>`, `␎`  | abstract | *operator* | Bitwise Operators |
| <a name="+_j"></a>  `∪`, `∩`, `⊆`, `⊄`, `⊂`, `⊃`, `⊇`, `∅`, `𝐏`, `⊅`, `=`, `∁`<br>`∆`, `∉`, `|`, `#`, `×`, `₀`, `₁`, `₂`, `𝐐`, `𝐙`, `𝐑`  | abstract | *operator* | Set Theory Operators |
| <a name="abs"></a> `_abs(`*`numeric`*`)`<br>`_`*`<expressionposit>`*`(|`*`numeric`*`|)` | abstract | *function* | Provides the [absolute value](../abstract/funct/abs.md) of *numeric*<br>Provides the [absolute value](../abstract/funct/abs.md) of *numeric* in an *expression* |
| <a name="acos"></a> `_acos(`*`numeric`*`)`<br>`_acos([`*`variablemoniker`*`])`<br>`_`*`<expressionposit>`*`(𝐜𝐨𝐬⁻¹(`*`numeric`*`))`<br>`_`*`<expressionposit>`*`(𝐜𝐨𝐬⁻¹([`*`variablemoniker`*`]))` | abstract | *function* | Provides the [arccosine](../abstract/funct/acos.md) of *numeric* |
| <a name="actuat"></a> `actuat(`*`moniker`*`)`<br>`actuator(`*`moniker`*`)` | physic | *object* | [actuat](/actuat.md) |
| <a name="add"></a> `add_`*`<object>`* | abstract<br>metaphysic<br>physic | *verb* | Declare *object* |
| <a name="adicity"></a> `_adicity()` | abstract | *property* | Provides the [information](../abstract/prop/adicity.md) of *elements* or *members* of the preceeding *object* |
| <a name="after"></a> `_after(`*`temporalexpression`*`)` | abstract | *condit* | Preceeding *object* [after](../abstract/condit/after.md) *temporalexpression* for the proceeding *object*, usually to do the proceeding *action* |
| <a name="ai"></a> `ai`<br>`bot` | metaphysic<br>obj | | A construct present in the metaphysical world only. (Artificial Intelligence)<br>Example: *cal*, *ChatBot* | [ai](/bot.md) |
| <a name="alert"></a> `alert_`*`<thingy>`*`(`*`moniker`*`)` | physic | *verb* | [alert](../physic/verb/alert.md) |
| <a name="applain"></a> `applian`<br>`applicance` |  physic<br>obj | | A smart mobot that can safetly be classified as a *household applicance*.<br>Examples: washing machine, dishwasher.<br>`with_applian(dishWasher)_start(normalWash);` | [applian](../physic/obj/applian.md) |
| <a name="apprat"></a> `apparat(`*`moniker`*`)`<br>`apparatus(`*`moniker`*`)` | physic | *object* | [apparat](../physic/obj/apparat.md) |
| <a name="arena"></a> `arena(`*`moniker`*`)` | metaphysic | *object* | [arena](../metaphysic/obj/arena.md) |
| <a name="arity"></a> `_arity()` | abstract | *property* | Provides the [entire count](../abstract/prop/arity.md) *members* of the preceeding *object* |
| <a name="array"></a> `array(`*`moniker`*`)`<br>`ary(`*`moniker`*`)` | abstract | *object* | A [collection](../abstract/obj/ary.md) of multiple elements under a single *object* called *moniker* |
| <a name="ask"></a> `ask_` | metaphysic | *verb* | Requests information, to be returned with `tell` *verb*<br/>`ask_drone(drone1)_stat(avg_altitude);`<br/>`tell_drone(drone1)_stat(avg_altitude)_value(22.893);` | [ask](/ask.md)<br />_see also:_ [tell](/end/md) |
| <a name="ask"></a> `ask_`*`<thingy>`* | physic | *verb* | *[Ask](../metaphysic/verb/ask.md)* proceeding *thingy* |
| <a name="at"></a> `_at(`*`date`*`)` | abstract | *condit* | Preceeding *object* [at](../abstract/condit/at.md) [date](../abstract/obj/tempor.md) for proceeding *object* to do proceeding *action* |
| <a name="attr"></a> `attr`<br>`attribute` | metaphysic | *object* | Example: <br>See also: [spec](#spec) | [attr](../metaphysic/obj/attr.md) |
| <a name="before"></a> `_before(`*`date`*`)` | abstract | *condit* | Preceeding *object* [before](../abstract/condit/before.md) [date](../abstract/obj/tempor.md) for proceeding *object* to do proceeding *action* |
| <a name="begin"></a> `begin_`*`<object\|action>`* | abstract<br>metaphysic | *verb* | [Begin](../metaphysic/verb/begin.md) *action* on proceeding *object* |
| <a name="border"></a> `border` | physic | *object* | Floor marking showing borders, created using paint, tape, or, decals.<br>Example:<br><img src="/_img/256px-Floor_marking_5S_safety_Scanfil_Sieradz.jpg" alt="wayfind markings" style="width:200px;"/><br><sub>"<a href="https://commons.wikimedia.org/wiki/File:Floor_marking_5S_safety_Scanfil_Sieradz.jpg">Floor marking at the Scanfil Poland factory in Sieradz</a>"<br>by <a href="https://commons.wikimedia.org/wiki/User:Boston9">Adrian Grycuk</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/3.0/pl/">CC BY 2.0 Poland</a> </sub> | [border](../physic/obj/border.md) |
| <a name="bot"></a> `bot`<br>`ai` | metaphysic<br>obj | | A construct present in the metaphysical world only. (Artificial Intelligence)<br>Example: *cal*, *ChatBot* | [bot](/bot.md) |
| <a name="box"></a> `box` | metaphysic | *object* | A representation of a meta-physical enclosed space. The thing / meta-physical version of a `room`.<br>Example: inside a pit<br>See also: [room](#room) | [box](/box.md) |
| <a name="calc"></a> `_calc(`*`expression`*`)` |  abstract | *method* | Use [calculation](../abstract/meth/calc.md) of *expression* for preceeding *object*, with proceeding *object* |
| <a name="calc"></a> `calc_`*`<object>`*`(`*`objmoniker`*`)`<br/>`calc_`*`<object>`*`(`*`ofmoniker`*`)` | abstract<br/>metaphysic | *verb* | [calc](../metaphysic/verb/calc.md) |
| <a name="call"></a> `call_`*`<object>`* | metaphysic | *verb* | [call](../metaphysic/verb/call.md) |
| <a name="canal"></a> `canal` | physic | *object* | [canal](../physic/obj/canal.md) |
| <a name="ceiling"></a> `ceiling` | physic | *object* | <a name="ceiling"></a>| An identified top _side_ of a representation space in the physical world | [ceiling](ceiling.md) |
| <a name="channel"></a> `channel(`*`moniker`*`)` | physic | *object* |An exclusive sub-section of a `workspace`, sometimes referred to as a _conversation_ | [channel](../metaphysic/obj/channel.md) |
| <a name="cloud"></a> `cloud(`*`moniker`*`)`   | physic | *object* | |
| <a name="clump"></a> `clump(`*`moniker`*`)` | abstract | *object* | A multi-dimesional  collection of [data](../abstract/obj/clump.md) storage *object* called *moniker* |
| <a name="computer"></a> `computer(`*`moniker`*`)`<br>`comput(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[computer](../metaphysic/obj/computer.md)* *moniker* |
| <a name="comrelay"></a> `commrelay(`*`moniker`*`)` | | | https://www.autonodyne.com/AUTO_behaviors2.html | [comrelay](#comrelay) |
| <a name="concat"></a> `_concat()`<br>`_concatenate()`<br>`_concat(`*`arymoniker`*`)`<br>`_concatenate(`*`arymoniker`*`)`<br>`_concat(`*`arymoniker1`*`,`*`arymoniker1`*`,`*`...`*`)`<br>`_concatenate(`*`arymoniker1`*`,`*`arymoniker1`*`,`*`...`*`)` | abstract | *object* | Concatenates proceeding *objects* (*arrays*) with proceeding *objects*<br>Concatenates array *arymoniker* with preceeding *objects*<br>Concatenates arrays *arymonikers* with preceeding *objects* |
| <a name="concord"></a> `concord(`*`settings`*`)` | abstract<br>metaphysic | *setter* |  |
| <a name="consens"></a> `consens(`*`settings`*`)`<br>`consensus(`*`settings`*`)` | abstract<br>metaphysic | *setter* | [consens](../metaphysic/setter/consens.md) |
| <a name="console"></a> `console` | metaphysic | *object* | A metaphysical presence used to only provide an interface to all other *thingies* | [console](../metaphysic/obj/console.md) |
| <a name="corridor"></a> `corridor` | metaphysic | *object* | <a name="corridor"></a> | A representation of a physically defined 3d space, designed for a human, to manoeuvre inside, predominately along a single plane.<br>There should be an attempt for physical (real-world) borders. | [corridor](../metaphysic/obj/corridor.md) |
| <a name="counter"></a> `counter(`*`variablemoniker`*`)` | abstract | *object* | [counter](../abstract/obj/counter.md) |
| <a name="counter"></a> `counter` | | [counter](../abstract/obj/counter.md)
| <a name="decisiven"></a> `decisiven(`*`settings`*`)`<br>`decisiveness(`*`settings`*`)` | metaphysic | *setter* |  |
| <a name="decpl"></a> `_decpl(`*`numeric`*`)`<br>`_decplaces(`*`numeric`*`)` | abstract | *setter* | Set the default number of decimal place to use in calcluations adn on display (as a setter) [decpl](../abstract/setter/decpl.md)<br/>See also [`fix`](../abstract/meth/fix.md) *method* |
| <a name="deed"></a> `deed(`*`moniker`*`)` | abstract | *object* | A basic one-dimensional [data](../abstract/obj/deed.md) data *object* called *moniker*, immutable except for *deed owner* |  [deed](./obj/deed.md) |
| <a name="dict"></a> `dict(`*`moniker`*`)`<br>`_dict(`*`moniker`*`)`<br>`dictionary(`*`moniker`*`)`<br>`_dictionary(`*`moniker`*`)` | abstract | *object* | A [keyed collection](../abstract/obj/dict.md), with key-value pairs, data storage *object* called *moniker* |
| <a name="distan"></a> `_distan(`*`distancevalue`*`)`<br>`_distance(`*`distancevalue`*`)`<br>`_distan({unit},`*`distancevalue`*`)`<br>`_distance({unit},`*`distancevalue`*`)`<br> | metaphysic | *posit*<br/>*property* | Preceeding *object* of [distance](../metaphysic/prop/distan.md) of proceeding *object* |
| <a name="distan"></a> `distan(`*`objectname`*`)`<br/>`distance(`*`objectname`*`)` | metaphysic | *object* | [distan](../metaphysic/obj/distan.md) |
| <a name="door"></a> `door` | metaphysic | *object* | <a name="door"></a> | A `thing` representation of a physical doorway / gate, designed for a human.<br>See also: [portal](#portal); [gate](#gate) | [door](#door)
| <a name="durat"></a> `_durat(`*`durationvalue`*`)`<br>`_duration(`*`durationvalue`*`)`<br>`_durat({unit},`*`durationvalue`*`)`<br>`_duration({unit},`*`durationvalue`*`)`<br> | metaphysic | *condit* | Preceeding *object* of [duration](../metaphysic/condit/durat.md) of proceeding *object* |
| <a name="during"></a> `_during(`*`date`*`)` | abstract | *condit* | Preceeding *object* [during](../abstract/condit/during.md) [date](../abstract/obj/tempor.md) for proceeding *object* to do proceeding *action* |
| <a name="e"></a> `_e()`<br>`_e(`*`decplaces`*`)` |  abstract | *constant* | Use [Euler's number](../abstract/const/e.md) for preceeding *object*, with proceeding *object* |
| <a name="equip"></a> `equip(`*`moniker`*`)`<br>`equipment(`*`moniker`*`)` | metaphysic | *object* | <br>See also: `apparatus`; `instru`*[ment]*; `peripheral`;  `sensor` | [equip](equip.md) |
| <a name="ergcon"></a> `_ergcon(`*`ergconvalue`*`)`<br>`_ergcon({unit},`*`ergconvalue`*`)` | metaphysic | *property* | Preceeding *object* of [energy consumption](../metaphysic/prop/ergcon.md) of proceeding *object* |
| <a name="firma"></a> `firma` | metaphysic | *object* | An identified down _side_ of a representation space in the physical world. | [firma](../physic/obj/firma.md) |
| <a name="fix"></a> `_fix(`*`decplaces`*`)`<br/>`_tofix(`*`decplaces`*`)` | abstract | *method* | Converts preceeding *object-value* in to *decplaces* number of [fixed decimal places](../abstract/meth/fix.md) |
| <a name="float"></a> `{float}` | abstract<br>datatype | | Float abstract datatype | [float](../abstract/obj/float.md) |
| <a name="floor"></a> `floor`<br>`level` | | [floor](#floor.md)<br>[level](#level) |
| <a name="fog"></a> `fog(`*`moniker`*`)` | metaphysic | *object* | A zone (`puff`) used for diego communication that relies on UDP [fog](../metaphysic/obj/fog.md) |
| <a name="follow"></a> `follow_`*`<object>`* | metaphysic | *verb* | *[Follow](../metaphysic/verb/follow.md)* proceeding *object* |
| <a name="for"></a> `_for([`*`loopername`*`])` | abstract | *flow* | [for](../abstract/flow/for.md) |
| <a name="for"></a> `_for(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` | abstract | *flow* | [for](../abstract/flow/for.md) |
| <a name="foreach"></a> `_foreach(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` | abstract | *flow* |  |
| <a name="foreign"></a> `foreign(`*`moniker`*`)`<br>`foreigner(`*`moniker`*`)` | [foreign](../metaphysic/obj/foreign.md) |
| <a name="forin"></a> `_forin(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` |abstract | *flow* |  |
| <a name="form"></a> `form`*[ation]* | |
| <a name="forof"></a> `_forof(`*`startexpression`*`,`*`condition`*`,`*`repeatexpression`*`)` |  abstract | *flow* |  |
| <a name="funct"></a> `funct(`*`moniker`*`)`<br>`_funct(`*`moniker`*`)`<br>`function(`*`moniker`*`)`<br>`_function(`*`moniker`*`)` | abstract | *action* | [funct](../abstract/obj/funct.md) |
| <a name="gait"></a> `gait(`*`moniker`*`)` | metaphysic | *object* | The thing version of `stride` [gait](../metaphysic/obj/gait.md)
| <a name="gate"></a> `gate` | metaphysic | *object* | [gate](../metaphysic/obj/gate.md) |
| <a name="geofence"></a> `geofence` <a name="fence"></a> | | [geofence](../metaphysic/obj/geofence.md) |
| <a name="ghost"></a> `ghost(`*`moniker`*`)` | metaphysic | *object* | [ghost](../metaphysic/obj/ghost.md) |
| <a name="gimbal"></a> `gimbal` | | |
| <a name="go"></a> `go_`*`<object>`* | physic | *verb* | Manouve Proceeding *object* to [go](../metaphysic/verb/go.md) proceeding *action* on *object* |
| <a name="goal"></a> `goal(`*`moniker`*`)`<br>`_goal(`*`moniker`*`)` | metaphysic | *posit-object* | *Action* on *[goal](../metaphysic/obj/goal.md)* *moniker*<br>Proceed with *[goal](../metaphysic/obj/goal.md)* *moniker* |
| <a name="goto"></a> `_goto()` | metaphysic | *verb* |  Preceeding *object(s)* [goto](../metaphysic/verb/goto.md) to proceeding *object(s)* |
| <a name="goto"></a> `goto_`*`<object>`* | physic | *verb* | Manouve Proceeding *object* to [goto](../metaphysic/verb/goto.md) proceeding *object* |
| <a name="guide"></a> `guide` | |
| <a name="handler"></a> `handler` | | |
| <a name="hash"></a> `hash(`*`moniker`*`)` | abstract | *object* | A two-dimensional [collection](../abstract/obj/hash.md) data storage *object* called *moniker*, with hashed keys |
| <a name="hold"></a> `hold`, `household` |||
| <a name="human"></a> `human(`*`moniker`*`)` | physic | *object* | Representation of a human being, present and alive in the physical *'real'* world. |
| <a name="if"></a> `_if_(`*`expression`*`)` | abstract | *operator* |  |
| <a name="indent"></a> `indent(`*`moniker`*`)`<br>`indenture(`*`moniker`*`)` | abstract | *object* | A basic one-dimensional [data](../abstract/obj/indent.md) storage *object* called *moniker*, immutable except for *indenture owners* |  [indent](./obj/indent.md) |
| <a name="instruct"></a> `instruct(`*`moniker`*`)`<br>`instruction(`*`moniker`*`)` | abstract<br>metaphysic | *action* | [instruct](../metaphysic/obj/instruct.md) |
| <a name="int"></a> `{int}` | abstract<br>datatype | | Integer abstract datatype | [int](../abstract/obj/int.md) |
| <a name="int32"></a> `{int32}` | abstract<br>datatype | | Integer abstract datatype | [int](../abstract/obj/int.md) |
| <a name="int64"></a> `{int64}` | abstract<br>datatype | | Integer abstract datatype | [int](../abstract/obj/int.md) |
| <a name="jagger"></a> `jagger(`*`moniker`*`)` | metaphysic | *object* | jagger](#jagger) | [jigger](/jigger.md) |
| <a name="ject"></a> `ject(`*`moniker`*`)` | metaphysic | *object* | A dumb physical [ject](../physic/obj/ject.md) |
| <a name="jigger"></a> `jigger(`*`moniker`*`)`| metaphysic | *object* | |
| <a name="kill"></a> `kill_`*`<human\|organic>`*<br>`kill_`*`<object>`* | physic | *verb* | [Kill](../metaphysic/verb/kill.md) proceeding *human*/*organic*<br>[De-commission](../metaphysic/verb/kill.md) proceeding *object* |
| <a name="kill"></a> `kill_`*`<variable>`* | abstract | *verb* | *[Kill](../abstract/verb/kill.md)* proceeding *variable* |
| <a name="label"></a> `label_`*`<object>`* | |
| <a name="lead"></a> `lead_`*`<object>`* | metaphysic | *verb* | *[lead](../metaphysic/verb/lead.md) proceeding *object* |
| <a name="lexi"></a> `lexi(`*`moniker`*`)`<br>`lexikon(`*`moniker`*`)` | abstract | *object* | A two-dimensional [collection](../abstract/obj/lexi.md) data storage *object* called *moniker*, with unique keys |
| <a name="lib"></a> `lib`, `library` | | |
| <a name="list"></a> `list(`*`moniker`*`)` | abstract | *object* | A database-assigned [collection](../abstract/obj/list.md) *object* called *moniker* |
| <a name="ln"></a> `_ln(`*`numeric`*`)`<br>`_log(`*`numeric`*`)`<br>`_ln([`*`numericvariablemoniker`*`])`<br>`_log([`*`numericvariablemoniker`*`])`  |  abstract | *function* | Use [natural logarithm](../abstract/funct/ln.md) (base [e](../abstract/const/e.md)) for preceeding *object*, with proceeding *object*<br>See also: [ln2](../abstract/const/ln2.md); [ln10](../abstract/const/ln10.md) |
| <a name="ln10"></a> `_ln10()`<br>`_ln10(`*`decplaces`*`)`<br>`_ln(10)`<br>`_ln(10)_decpl(`*`decplaces`*`)` |  abstract | *constant* | Use [natural logarithm of 10](../abstract/const/ln10.md) for preceeding *object*, with proceeding *object*<br>See also: [ln](../abstract/funct/ln.md) |
| <a name="ln2"></a> `_ln2()`<br>`_ln2(`*`decplaces`*`)`<br>`_ln(2)`<br>`_ln(2)_decpl(`*`decplaces`*`)` |  abstract | *constant* | Use [natural logarithm of 2](../abstract/const/ln2.md) for preceeding *expression*, with proceeding *object*<br>See also: [ln](../abstract/funct/ln.md) |
| <a name="load"></a> `load_`*`<object>`* | metaphysic | *verb* | *[load](../metaphysic/verb/load.md)* proceeding *object* |
| <a name="mach"></a> `mach(`*`moniker`*`)`<br>`machine(`*`moniker`*`)` | physic | *object* | [mach](../physic/obj/mach.md) |
| <a name="mach"></a> `mech(`*`moniker`*`)`<br> | physic | *object* | |
| <a name="map"></a> `map(`*`moniker`*`)` | metaphysic | *object* | |
| <a name="mapprovider"></a> `_mapprovider(`*`mapprovider`*`)` | metaphysic | *setter* | [mapprovider](../metaphysic/setter/mapprovider.md) |
| <a name="matrix"></a> `matrix(`*`moniker`*`)`` | abstract | *object* | A two-dimensional collection [data](../abstract/obj/matrix.md) storage *object* called *moniker* |
| <a name="me"></a> `me_`*`<object\|action>`* | abstract | *special* | *[Me](../abstract/special/me/md)* (or this) does *action* or my *object*...<br>Representation of self |
| <a name="metric"></a> `metric` | |
| <a name="misson"></a> `misssion(`*`moniker`*`)` | metaphysic | *object* | [mission](../metaphysic/obj/mission.md) |
| <a name="mist"></a> `mist(`*`moniker`*`)` | metaphysic | *object* | A connectivity zone (wired or wireless) with the distance range of < 10m.<br>For example: RFID | [mist](/mist.md) |
| <a name="mobot"></a> `mobot(`*`moniker`*`)`   | metaphysic | *object* | A conveyed *thingy* in the physical *'real'* world.<br>Examples: Samasung Galaxy watch, cellphone | [mobot](/mobot.md) |
| <a name="mode"></a> `mode` | |
| <a name="mover"></a> `mover(`*`moniker`*`)` | See: [jigger](#jigger) | |
| <a name="msg"></a> `_msg(`*`message`*`)`<br>`_message(`*`message`*`)` | metaphysic | *??* | Proceed with *[message](../metaphysic/obj/msg.md)* *moniker* |
| <a name="msg"></a> `msg_`*`<object>`* | metaphysic | *verb* | *[message](../metaphysic/verb/msg.md)* proceeding *object* |
| <a name="msg"></a> `msg(`*`moniker`*`)`<br>`message(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[message](../metaphysic/obj/msg.md)* *moniker* |
| <a name="namespace"></a> `namespace(`*`moniker`*`)`<br>`ns(`*`moniker`*`)` | abstract | *object* | [namespace](../abstract/obj/namespace.md) |
| <a name="neigh"></a> `neigh`, `neighbour` |||
| <a name="ob"></a> `ob`  | metaphysic | *object* | A civilian[^civilian] immobile ject in the  physical *'real'* world.<br>Examples: unidentified lampost (or thing pointing out of the ground), etc.<br>`call_robot(alif)_found()_ob()_photo()_blob(d3Mtd2l6EAMyCwguEBDIL`*`...`* | [obstacle](../metaphysic/onstacle.md) | [ob](ob.md) |
| <a name="object"></a> `object`  | metaphysic | *object* | A dumb immobile physical [object](../physic/obj/object.md) |
| <a name="obstacle"></a> `obstacle` | |
| <a name="organic"></a> `organic` | metaphysic | *object* | Representation of a non-human being, present and alive in the physical *'real'* world.<br>Example: cat, dog | [organic](/organic.md) |
| <a name="orientat"></a> `_orientat(`*`variablemoniker`*`)`<br>`_orientation(`*`variablemoniker`*`)` | metaphysic | *posit-variable* |  |
| <a name="orientat"></a> `_orientat(`*`x`*`,`*`y`*`,`*`j`*`,`*`k`*`)`<br>`_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)`<br>`_orientation(`*`x`*`,`*`y`*`,`*`j`*`,`*`k`*`)`<br>`_orientation(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)` | metaphysic | *posit-action* |  |
| <a name="orientat"></a> `_orientat(`*`x`*`,`*`y`*`,`*`z`*`)`<br>`_orientation(`*`x`*`,`*`y`*`,`*`z`*`)` | metaphysic | *posit-action* |  |
| <a name="package"></a> `package` | | |
| <a name="path"></a> `path(`*`moniker`*`)` | metaphysic | *object* | [path](../metaphysic/obj/path.md) |
| <a name="payload"></a> `payload(`*`moniker`*`)`<br>`pload(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[payload](../metaphysic/obj/payload.md)* *moniker* |
| <a name="pi"></a> `_pi()`<br>`_pi(`*`decplaces`*`)` |  abstract | *constant* |  |
| <a name="pipe"></a> `pipe(`*`moniker`*`)` | metaphysic | *object* | [duct](../metaphysic/obj/duct.md)  | [pipe](../metaphysic/obj/pipe.md) |
| <a name="plafond"></a> `plafond` | |
| <a name="poi"></a> `poi(`*`moniker`*`)` | metaphysic | *object* |
| <a name="point"></a> `point(`*`moniker`*`)` | abstract | *object* | [point](../abstract/obj/point.md) |
| <a name="poll"></a> `poll_`*`<object>`*`(`*`objmoniker`*`)`<br/>`poll_`*`<object>`*`(`*`ofmoniker`*`)` | metaphysic | *verb* | [poll](../metaphysic/verb/poll.md)  |
| <a name="pose"></a> `_pose(`*`moniker`*`)` | metaphysic | *posit-object* | Proceed with *[pose](../metaphysic/obj/pose.md)* *moniker* |
| <a name="printer"></a> `printer(`*`moniker`*`)`<br>`ptr(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[printer](../metaphysic/obj/printer.md)* *moniker* |
| <a name="proc"></a> `proc`, ``proced`, `procedure` | | |
| <a name="process"></a> `process(`*`moniker`*`)`<br>`process(`*`moniker`*`)` | metaphysic | *object* |  |
| <a name="prog"></a> `prog(`*`moniker`*`)`, `program(`*`moniker`*`)`, `programme(`*`moniker`*`)` | | |
| <a name="puff"></a> `puff(`*`moniker`*`)` |
| <a name="rail"></a> `rail(`*`moniker`*`)` | metaphysic | *object* | [rail](../physic/obj/rail.md) |
| <a name="ret"></a> `_ret()`<br>`_ret({`*`datatype`*`})` | abstract | *function* | [ret](../abstract/funct/ret.md)
| <a name="robot"></a> `robot(`*`moniker`*`)`<br>`_robot(`*`moniker`*`)` | physic | *object* | *Action* on *[robot](../physic/obj/robot.md)* *moniker* |
| <a name="roi"></a> `roi(`*`moniker`*`)`<br>`regionofinterest(`*`moniker`*`)` | metaphysic | *object* | [roi](../metaphysic/obj/roi.md) |
| <a name="room"></a> `room` | | | A representation of a single physical enclosed space for a `thingy` to move freely around inside. | [chamber](../metaphysic/chamber.md) | [room](../physic/obj/room.md) |
| <a name="route"></a> `route(`*`moniker`*`)`<br/>`_route(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[route](../metaphysic/obj/route.md)* *moniker*<br/>Proceed with *[route](../metaphysic/obj/route.md)* *moniker* |
| <a name="scalar"></a> `scalar(`*`moniker`*`)`<br>`_scalar(`*`moniker`*`)`<br>`_scalar({dt},`*`moniker`*`)`<br>`_scalar([`*`variablemoniker`*`])` | *metaphysic* | *object* | Proceed with *[scalar](../metaphysic/obj/scalar.md)* *variablemoniker* [scalar](../metaphysic/obj/scalar.md) |
| <a name="scan"></a> `scan` | |
| <a name="sensor"></a> `sensor(`*`moniker`*`)`<br>`_sensor(`*`moniker`*`)` | metaphysic | *object* | *Action* on *[sensor](../metaphysic/obj/sensor.md)* *moniker*<br>Proceed with *[sensor](../metaphysic/obj/sensor.md)* *moniker* |
| <a name="set"></a> `set_`*`<object>`*`(`*`moniker`*`,`*`settings...`*`)`<br>`_set(`*`settings...`*`)` | abstract | *verb*<br>*posit* | [Sets](../abstract/verb/set.md) the *object* of *moniker* with *settings...* settings |
| <a name="set"></a> `set_`*`<setter>`*`(`*`settings`*`)` | abstract<br>metaphysic | *verb* | [Sets](../metaphysic/verb/set.md) the *setter* to *settings* settings |
| <a name="shaft"></a> `shaft(`*`moniker`*`)` | physic | *object* | [shaft](../physic/obj/shaft.md) |
| <a name="side"></a> `side` | | |
| <a name="sobriquet"></a> `sobriquet` | |
| <a name="spec"></a> `spec`<br>`specification` | <br>See also: `attribute` | [spec](../physic/obj/spec.md) |
| <a name="spine"></a> `spine` | | [spine](../metaphysic/obj/spine.md) |
| <a name="sql"></a> `_sql(`*`sqlquery`*`)` | abstract | *function* | Provides *sqlquery* [outcome](../abstract/funct/sql.md) into preceeding *object* | 
| <a name="sqrt2"></a> `_sqrt2()`<br>`_sqrt2(`*`decplaces`*`)` |  abstract | *constant* |  |
| <a name="stacle"></a> ||| [stacle](../metaphysic/obj/stacle.md)
| <a name="stance"></a> `stance` |  |
| <a name="stealth"></a> `stealth` |
| <a name="stride"></a> `stride` | | | The human version of `gait` |
| <a name="study"></a> `study_`*`<object>`* | physic | *verb* | *[Study](../metaphysic/verb/study.md)* proceeding *object* |
| <a name="sub"></a> `sub` | physic | *object* | A unidentified mobile physical [ject](sub.md) |
| <a name="subject"></a> `subject` | physic | *object* | A dumb mobile physical [ject](subject.md) |
| <a name="substacle"></a> ||| ](../metaphysic/substacle.md) | [sub
| <a name="swarm"></a> `swarm` | |
| <a name="tail"></a> `tail_`*`<object>`* | metaphysic | *verb* | *[Tail](../metaphysic/verb/tail.md)* behind proceeding *object* |
| <a name="tempor"></a> `tempor(`*`moniker`*`)`<br>`temporal(`*`moniker`*`)`<br>`{tempor}`<br>`{temporal}` | abstract | *object* | A primitive data object representing a [date](../abstract/obj/tempor.md) off a calendar monikered *moniker* |
| <a name="thing"></a> `thing` | physic<br>obj | | An immobile *thingy* in the physical *'real'* world.<br>Example: fridge, television | [thing](/thing/md) |
| <a name="thingy"></a> `thingy({robot},`*`moniker`*`)`<br>`add_thingy(`*`moniker`*`)_type(robot)` | physic | *verb-object*<br>*datatype* | *Action* on *[thingy](../physic/obj/thingy.md)* *moniker* of datatype [robot](../physic/obj/robot.md) |
| <a name="to"></a> `_to()` | abstract | *operator* | Preceeding from *object(s)* [to](../abstract/condit/to.md) proceeding *object(s)* |
| <a name="to"></a> `_to()` | metaphysic | *operator* | Preceeding *object(s)* *action* [to](../metaphysic/condit/to.md) proceeding *object(s)* |
| <a name="to"></a> `to` | metaphysic<br>posit | | [to](../metaphysic/condit/to.md) |
| <a name="tour"></a> `_tour(`*`moniker`*`)` | metaphysic | *posit-object* | Proceed with *[tour](../metaphysic/obj/tour.md)* *moniker* |
| <a name="toward"></a> `toward`<br>`towards` | metaphysic<br>posit | | [toward](../metaphysic/condit/toward.md) |
| <a name="track"></a> `track(`*`moniker`*`)` | physic | *object* | Floor/ground marking the side borders of a lane.<br>Example:<br><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/All-weather_running_track.jpg/800px-All-weather_running_track.jpg?20170320005232" alt="track" style="width:200px;"/><br><sub>"<a href="https://commons.wikimedia.org/wiki/File:All-weather_running_track.jpg">An all-weather running track (photo taken at the Dalin Sports Park, Chiayi, Taiwan)</a>"<br>by <a href="https://commons.wikimedia.org/wiki/User:Mk2010">Mk2010</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0">CC BY 4.0 International</a> </sub> | [track](track.md) |
| <a name="tunnel"></a> `tunnel(`*`moniker`*`)` | physic | *object* | Physical bar or continuous line of bars construction used to physically guide object along a pre-defined route.<br>Example:<br><img src="" alt="tunnel" style="width:200px;"/><br><sub>"<a href=""></a>"<br>by <a href=""></a> is licensed under <a href="">CC BY </a></sub> | [tunnel](tunnel.md) |
| <a name="txt"></a> `_txt(`*`text`*`)`<br>`_text(`*`text`*`)` | abstract | *property* | Proceed with *test* of *[text](../abstract/prop/txt.md)* *moniker* |
| <a name="type"></a> `type(`*`moniker`*`)`<br>`_type(`*`moniker`*`)`<br>`{`*`moniker`*`}` | |
| <a name="unit"></a> `_unit(`*`unit`*`)` | metaphysic | *posit-datatype* |  |
| <a name="unload"></a> `unload_`*`<object>`* | metaphysic | *verb* | *[Unload](../metaphysic/verb/unload.md)* proceeding *object* |
| <a name="using"></a> `_using(`*`moniker`*`)`<br/>`_using([`*`variablemoniker`*`])` | metaphysic | *condit* | [using](../metaphysic/condit/using.md) |
| <a name="var"></a> `var(`*`moniker`*`)`<br>`variable(`*`moniker`*`)`  | abstract | *object* | A basic one-dimensional mutable [data](../abstract/obj/var.md) storage *object* called *moniker*  |
| <a name="vector"></a> `vector(`*`moniker`*`)`<br>`_vector(`*`moniker`*`)` | metaphysic | *object*<br>*posit-object* | *Action* on *[vector](../abstract/obj/vector.md)* *moniker*<br>Proceed with *[way](../metaphysic/obj/way.md)* *moniker* |
| <a name="vehicle"></a> `vehicle` | physic<br>obj | | A guided *thingy* transporting `human`/`organic` thingies and/or controlled by a `human`.<br>Examples: car, airplane, <abbr title="uncrewed ground vehicle">ugv</abbr>.<br>`with_vehicle(familyCar)_equip(frontLeftWheel)_metric()_tyrepress();` | [vehicle](vehicle.md) |
| <a name="verb"></a> `verb(`*`moniker`*`)` | meta-abstract | *object* | *Action* on *[verb](../abstract/meta/verb.md)* *moniker* |
| <a name="wall"></a> `wall(`*`moniker`*`)` | physic | *object* | [litsan](../metaphysic/obj/litsan.md) | [wall](../physic/obj/wall.md) |
| <a name="way"></a> `way(`*`moniker`*`)`<br>`_way(`*`moniker`*`)` | metaphysic | *object*<br>*posit-object* | *Action* on *[way](../metaphysic/obj/way.md)* *moniker*<br>Proceed with *[way](../metaphysic/obj/way.md)* *moniker* |
| <a name="wayfind"></a> `wayfind` | | | Wayfinding floor signature, created using paint, tape, or, decals.<br>Example:<br><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Long-distance_Bus_Navigation_in_Japan.jpg/800px-Long-distance_Bus_Navigation_in_Japan.jpg?20140622041451" alt="wayfind markings" style="width:200px;"/><br><sub>"<a href="https://commons.wikimedia.org/wiki/File:Long-distance_Bus_Navigation_in_Japan.jpg">Tokyo Station</a>" by <a href="https://www.flickr.com/people/36516818@N00">mrhayata</a> is licensed under <a href="https://creativecommons.org/licenses/by/2.0/">CC BY 2.0</a></sub> | [route](../metaphysic/route.md)  | [wayfind](../physic/obj/wayfind.md) |
| <a name="waypoint"></a> `waypoint(`*`moniker`*`)`<br>`wp(`*`moniker`*`)`<br>`_waypoint(`*`moniker`*`)`<br>`_wp(`*`moniker`*`)` | metaphysic | *object*<br>*posit-object* | *Action* on *[waypoint](../metaphysic/obj/waypoint.md)* *moniker*<br>Proceed with *[waypoint](../metaphysic/obj/waypoint.md)* *moniker* |
| <a name="with"></a> `with_`*`<object>`*`(`*`moniker`*`)` | abstract<br>metaphysic<br>physic | *verb* | Refer to *object* of *moniker* |
| <a name="workspace"></a> `workspace` | | | An exclusive section of a `puff`, sometimes called a _room_ |
| <a name="world"></a> `world(`*`verbmoniker`*`)` | physic | *special* | *Action* of *verbmoniker* on *[world](../physic/special/world.md)* |
| <a name="zone"></a> `zone` | metaphysic | *object* | The thing version of an `arena` [zone](../metaphysic/obj/zone.md) |



