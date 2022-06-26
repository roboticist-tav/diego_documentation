# Commands

## <a name="a"></a> A: [add_count](#add_counter); [add_funct](#add_function);
| `cmd` | description<hr>`example` | API |
|--|:--|---|
| `add_count()` <a name="add_counter"></a> <br> `add_counter()` <br> `add_var()_counter()` | Declaration of a counter variable.<hr>`add_count(patrol complete)_start(0.0)_inc(0.5);`<br>`[patrol complete];` | [`count`](/counter.md) |
| `add_funct()` <a name="add_function"></a><br>`add_function()` | Delcaration of a funcion, or simultaneous declatation and assignment of a function.<br>See also: [`begin_funct`](#begin_funct)<hr>`add_funct({{int},add)_arg(a,b)`<br>&nbsp;&nbsp;&nbsp;&nbsp;`[]_ret()_calc([a]+[b]);`<br>`;`<br>`add_funct(multiply);` | [`funct`](/function.md) |
| `add_instruct()` <a name="add_instruct"></a><br>`add_instruction()`<br>`add_instructor()` | Delcaration of a funcion, or simultaneous declatation and assignment of an instruction.<br>See also: [`begin_instruct`](#begin_instruct)<hr>`add_instruct(move robot forward)`<br>&nbsp;&nbsp;&nbsp;&nbsp;`...`<br>`;`<br>`add_instruct(come back to later);` | [`instruct`](/instruction.md) |
| `add_var()` <a name="add_var"></a> <br>`add_variable()` | Declatation of a variable.<br>`add_var(x);`<br>`add_var({int},a);` | [`var`](/variable.md) |

## <a name="b"></a> B: [begin_funct](#begin_funct); [begin_instruct](#begin_instruct);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `begin_funct()` <a name="begin_funct"></a><br>`begin_function()` | Marks the start of a function and monikers it for reference.<br>See also: [`with_funct`](#with_funct)<hr>`begin_funct({{int},add)_arg(a,b);`<br>&nbsp;&nbsp;&nbsp;&nbsp;`[]_ret()_calc([a]+[b]);`<br>`end_funct[];` | [`funct`](/function.md) |
| `begin_instruct()` <a name="begin_instruct"></a><br>`begin_instruction()`<br>`begin_instructor()` | Marks the start of an instruction and monikers it for reference.<br>See also: [`with_instruct`](#with_instruct)<hr>`begin_instruct(move robot forward);`<br>&nbsp;&nbsp;&nbsp;&nbsp;`...`<br>`end_instruct[];` | [`instruct`](/instruction.md) |

## <a name="d"></a> D: [detect_human](#detect_human);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `detect_human()` | | |
| `discover_human()` | | |
| `discover_gait()` | | |
| `discover_behav()` | | |
| `drop_breadcrumbs()` | | |

## <a name="e"></a> E: [end_funct](#end_funct); [end_instruct](#end_instruct);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `end_funct()`<a name="end_funct"></a><br>`end_funct[]`<br>`end_function()`<br>`end_function[]` | Marks the end of a function.<br>See also: [`with_funct`](#with_funct)<hr>`begin_funct({{int},add)_arg(a,b);`<br>&nbsp;&nbsp;&nbsp;&nbsp;`[]_ret()_calc([a]+[b]);`<br>`end_funct[];` | [`funct`](/function.md) |
| `end_instruct()`<a name="end_instruct"></a><br>`end_instruct[]`<br>`end_instruction()`<br>`end_instruction[]`<br>`end_instructor()`<br>`end_instructor[]` | Marks the end of an instruction.<br>See also: [`with_instruct`](#with_instruct)<hr>`begin_instruct(move robot forward);`<br>&nbsp;&nbsp;&nbsp;&nbsp;`...`<br>`end_instruct[];` | [`instruct`](/instruction.md) |

## <a name="f"></a> F: [form_swarm](#form_swarm);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `form_swarm()` |  | |

## <a name="g"></a> G: [go_diego](#go_diego);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `go_diego()` | ~~Depreciated in version 1.1~~ | |

## <a name="j"></a> J: [join_swarm](#join_swarm);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `join_swarm()` |  | |

## <a name="k"></a> K: [kill_human](#kill_human);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `kill_human()` |  | |

## <a name="l"></a> L: [listen_human](#listen_human);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `listen_human()` |  | |
| `label_human()` |  | |
| `learn_object()` |  | |
| `learn_animate()` |  | |
| `learn_inanimate()` |  | |
| `learn_organic()` |  | |
| `learn_human()` |  | |
| `learn_mech()` |  | |
| `learn_robot()` |  | |
| `identify_human()` | | |

## <a name="m"></a> M: [murder_human](#murder_human);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `murder_human()` |  | |

## <a name="s"></a> S: [set_concor](#set_concord); [set_consens](#set_consensus); [set_decisiv](#set_decisiveness); [set_thread](#set_thread);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `set_concor()`<br>`set_concord()`<br>`set_consensus()` | Sets the consensus to be used in polls.<br>See also: [`set_consensus`](#set_consensus) | [`concord`](/concord.md) |
| `set_consens()`<br>`set_consensus()`<br>`set_concord()` | Sets the consensus to be used in polls.<br>See also: [`set_concord`](#set_concord.md) | [`consensus`](../actions/concord.md) |
| `set_decisiv()`<br>`set_decisiveness()` | Sets the level of decisiveness to be used in decisions. | [`decision`](../actions/decision.md) |
| `set_distancecalc()` | | |
| `set_rank()` | Sets the rank to be used in following instructions and commands. | [`rank`](/rank.md) |
| `set_thread()` | Sets the thread level to be used in following instructions. | [`thread`](/thread.md) |
| `set_unitsystem()` | Sets the unit system level to be used. | [`unit`](/unit.md) |
| `study_human()` | | |

## <a name="t"></a> T: [tail_robot](#tail_robot);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
## tail_robot(*robot_moniker*)
#### tail_robot(*robot_moniker*)
#### tail_robot(*robot_moniker*)_on(*route moniker*)
#### tail_robot(*robot_moniker*)_by(*trail_type*)
|```trail_type```|Description  |
|--|--|
| ```follow``` |  |
| ```trail``` | |
| ```snake``` | |
| ```leapfrog``` | |

## <a name="w"></a> W: [with_funct](#with_funct); [with_instruct](#with_instruct);
| `cmd` | description<hr>`examples` | API |
|--|:--|---|
| `with_funct()`<a name="with_funct"></a><br>`[]`<br>`with_function()` | Assignment of a `funct`.<br>See also: [`begin_funct`](#begin_funct)<hr>`with_funct({{int},add)_arg(a,b)`<br>&nbsp;&nbsp;&nbsp;&nbsp;`[]_ret()_calc([a]+[b]);`<br>`;` | [`funct`](/function.md) |
| `with_instruct` <a name="with_instruct"></a><br>`with_instruction`<br>`witn_instructor` | Assignment of an `instruct`.<br>See also: [`begin_instruct`](#begin_instruct)<hr>`with_instruct(move robot forward)`<br>&nbsp;&nbsp;&nbsp;&nbsp;`...`<br>`;` | [`instruct`](/instruction.md) |










## drop_breadcrumbs(*route_moniker*)
#### drop_breadcrumbs(*route_moniker*)


# Goes
## go_point
## go_route
#### go_route(*route_moniker*)
#### go_route(*route_moniker*)_until(
#### goback_route(*route_moniker*)
#### go_route(*route_moniker*)_goback()
## go_detect
## goto_charge
## gointo_hiding
# Elections

# Pollsters
## poll_distance(*moniker*)
#### poll_distance(*point_moniker*)
#### poll_distance(*point_moniker*)*[...]*_by(*distance_metric*)
A robot will poll all robots for their distance to *point_moniker* from their current position.  The additional *distance_metric* sub command determines the calculation used in the return poll. *distance_metric* is a enumerator:
|```distance_metric```| Description |
|--|--|
| ```direct``` | Calculates the distance based on 'euclidean distance' calculation on the ```local``` map and ```local``` map types.  For the ```global``` map and ```global``` map types the ‘haversine’ formula is used to calculate the great-circle distance.<br> Distance is returned in metres.   |
| ```cityblock``` | Calculates the distance based on 'manhattan distance' calculation on a  ```local``` map and ```local``` map types.  For the ```global``` map and ```global``` map types the ‘haversine’ formula is used to calculate the great-circle distance between each _nth_ axis..<br>Distance is returned in metres.   
| ```learned``` | Calculates the distance using averaged odometric past knowledge (if any).  Where the robot has no past knowledge, direct distance is used.<br>Distance in returned in metres with an additional percentage of _calculated_ distances (against direct distances) used.<br>**Note: By using the ```_under(```*```condition_moniker```*```)``` sub command the ```calc``` distance calculation will only use past knowledge matching the *```condition moniker```*.** |
<sub>For a simplified explanation of 'euclidean' and 'manhattan' distance calculations see:  https://www.analyticsvidhya.com/blog/2020/02/4-types-of-distance-metrics-in-machine-learning/</sub>

#### poll_distance(*route_moniker*)
#### poll_distance(*route_moniker*)_at(*start_point*, *end_point*)
#### poll_distance(*start_point*, *end_point*)

### poll_distance(*point_moniker*)_in(*distance*)

## poll_energy(*moniker*)
#### poll_energy(*point_moniker*)
#### poll_energy(*route_moniker*)
#### poll_energy(*route_moniker*)_at(*start_point*, *end_point*)


, unanimous__by(direct)
Each robot will send a 'poll' as: ```poll_distance(rallying point, unanimous__by(direct)```, and, in turn, each robot will return their results as ```poll_distance(rallying point)_in(```*```metres```*```)```.

Each will robot will wait for a unanimous consensus and the winner will run ```call_point(sentry point)``` with it's current position.  The loser(s) will run ```listen_point(sentry point)```.
# Messengers
## msg_robot(*msg*)
## msg_human(*msg*)


## alert_human(*alert_moniker*)
## alert_world
#### alert_world(*alert_moniker*)




## call_counter(*call*)

## ask_distance(*route_moniker*)

## study_route(*route_moniker*)
#### study_route(*route_moniker*)_
## study_point(*point_moniker*)
####

# Inquirers
## error_human(*error*)
## ask_human(*ask*)
### ask_human(*ask*)

# Payloaders

## load_payload(*payload_moniker*)
## unload_payload(*payload_moniker*)


## call_payload(*payload_moniker*)

## call_sensor(*sensor_moniker*)


# Finders
## find_route
#### find_route(*route_moniker*, *startpoint*, *endpoint*)
#### find_route(*route_moniker*, *startpoint*, *endpoint*)_using(*map_provider*)
#### set_mapprovider(*map_provider*)
#### 
