# Lexicon


`shell_robot({moniker|uuid});`


## Verbs

| verb         | inverse        | notes |
| ------------ | -------------- | ----- |
| `add_`    | `dispose_`, `dump_`,  `minus_` | Construction of an object      |
| `ask_`    | `tell_` | Request for information      |
| `back_` | `fetch_` | |
| `begin_`| `end_` | |
| `call_`    | `here_` or `pong_` | [roll]call request of existence      |
| `declare_` |
| `dispose_`, `dump_`,  `minus_` | `add_` | |
| `dump_`, `dispose_`, `minus_` | `add_` | |
| `end_`| `begin_` | |
| `exec_`, `run_`| | |
| `fetch_`    | `back_` |       |
| `get_` | `set_` | Retrieve setting value |
| `go_`, `start_` | `stop_`, (`halt_`, `pause_`) |       |
| `halt_`, `pause_` | (`go_`, `start_`), (`stop_`) | |
| `hear_` | `listen_` | |
| `here_`    | `call_` |       |
| `hook_` | `unhook_` | |
| `inform_` |
| `kill_` | | |
| `listen_`    | `hear_` |       |
| `look_` | `see_` | |
| `minus_`, `dispose_`, `dump_` | `add_`| |
| `murder_` | | |
| `neigh_` | | |
| `pause_`, `halt_` | (`go_`, `start_`), (`stop_`) | |
| `pong_`    | `ping_` |       |
| `proclaim_` |
| `rem_`    | `recall_` |       |
| `see_`    | `look_` |       |
| `set_`    | `get_` |       |
| `start_`, `go_` | `stop_`, (`halt_`, `pause_`) |       |
| `stop_` | `go_`, `start_`, (`halt_`, `pause_`) | |
| `tell_`    | `ask_` |       |
| `with_`    |                |       |
| `loop_`    |                |       |
| `detect_`    |                |       |
| `learn_` | | |
| `study_` | | |
| `label_`| | |
| `keep_`| | |
| `join_`| | |
| `form_`  | | |
| `request_`| | |
| `deafon_`| | |
| `discover_` | | |
| `ident_`, `identify_` | | |
| `tail_`| | |
| | | |
| | | |
| | | |


## Objects

| object         | notes |
| ------------ | ----- |
| `actuat`*`(or)`*| |
| `ai`      | 'Artificial Intelligence' is one of ten genera. |
| `badge` | |
| `birth` | |
| `blob` | |
| `blob`| |
| `calendar`| |
| `cloud` | |
| `comm` | |
| `consensus` | |
| `console` |       |
| `coord`, `coordinates` | |
| `decisiveness` | |
| `fog` | |
| `gate` |       |
| `geometric` | |
| `gnps` | **G**obal **N**avigation and **P**ositioning **S**ystem |
| `human`   |       |
| `id` | |
| `instruct`| |
| `label` | A human-readable string appened for one/many genera. |
| `litsan` | '**L**ine **i**n **t**he **San**d' |
| `litsan`| |
| `lnps` | **L**ocal **N**avigation and **P**ositioning **S**ystem |
| `make` | |
| `manufact` | |
| `marker` |       |
| `me` | *self*, Thingy from its own perspective |
| `metric` |       |
| `mist` | |
| `mobot`   |       |
| `model` | |
| `modelnum` | |
| `name` | |
| `neigh` | Neighbour | 
| `object`  |       |
| `organic` |       |
| `path` |       |
| `point` |       |
| `poll`    |       |
| `pulse`          |       |
| `pulsepoint` |       |
| `punkt` |       |
| `ranking` | |
| `robot`   |       |
| `route` | |
| `sensor`| |
| `serialnum` | |
| `snapshot`| |
| `stat` | |
| `stat`| |
| `subject` |       |
| `tempus`| |
| `thing`   |       |
| `tracker`| |
| `trackpoint` |       |
| `trigger`| |
| `vidshot`| |
| `waypoint`| |
| `winner`| |
|  | |
|  | |
|  | |

## Positions

| Position                                                 | Notes                                                 |
| -------------------------------------------------------- | ----------------------------------------------------- |
| `_at({date|datetime|time})`                              |                                                       |
| `_au({x},{y},{z})`                                       |                                                       |
| `_between({parameter_1})_and({parameter_2})_exclusive()` |                                                       |
| `_between({parameter_1})_and({parameter_2})`             |                                                       |
| `_blob({blob_uuid})`                                     |                                                       |
| `_for({parameter_1}[,... {parameter_n}])`                | Provides focus on `{parameter_1}` ... `{parameter_n)` |
| `_fps({fps})`                                            |                                                       |
| `_from({date|datetime|time})_to({date|datetime|time})`   |                                                       |
| `_from({date|datetime|time})`                            |                                                       |
| `_in({duration})`                                        |                                                       |
| `_latency({latency})`                                    |                                                       |
| `_locus({x},{y},{name/uuid})`                            |                                                       |
| `_locus({x},{y},{r},{name/uuid})`                        |                                                       |
| `_locus({x1},{y1},{x2},{y2},{name/uuid})`                |                                                       |
| `_type({type})`                                          |                                                       |
| `_value({value}[, {unit}])`                              |                                                       |
| `_blob({moniker/filename/uuid})`                         |                                                       |
|                                                          |                                                       |
|                                                          |                                                       |
|                                                          |                                                       |

### Geometric

```Diego
add_geometric({name/uuid})
with_geometric({name/uuid})
	_type({type})
	_value({linear_x},{linear_y},{linear_x},{angular_x},{angular_y},{angular_z})

```

Geometric Types

| type       | Type                                                         | Value                                                        |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `accel`    | Expresses acceleration in free space broken into its linear and angular parts. | `_value({linear_x},{linear_y},{linear_x},{angular_x},{angular_y},{angular_z})` |
| accelcovar | Expresses acceleration in free space with uncertainty.       | `_value({})                                                  |
|            |                                                              |                                                              |
|            |                                                              |                                                              |
|            |                                                              |                                                              |
|            |                                                              |                                                              |
|            |                                                              |                                                              |
|            |                                                              |                                                              |
|            |                                                              |                                                              |



```Diego
_for({parameter_1},... {parameter_n})					Provides focus on {parameter_1} ... {parameter_n)
_between({parameter_1})_and({parameter_2})				Provides focus from {parameter_1} to {parameter_2} inclusive
_between({parameter_1})_and({parameter_2})_exclusive()	Provides focus from {parameter_1} to {parameter_2} exclusive


label({label});					Caller assigns label {label} to the callee
label({label})
	_for({uuid/name}, ...);		Assigns a label {label} to {uuid/name_1} ... {uuid/name_n}
ping({uuid/name});				Tests of reachability between caller and {uuid/name} callee
pong({uuid/name}):				Return/result of a ping from caller
pong({uuid/name})
	_ttl({byte}					Time To Live or hop limit of the lifespan or lifetime of data in the Diego universe
	_time({millsecs});			The latency in milliseconds of the ping messeage transmitted and then received back again

ask();							Caller requests minimal (name and identification) data on the callee
ask({uuid/name});				Caller requests minimal (name and identification) data on {uuid/name};


add_stat({stat_name});			Caller adds stat {stat_name} to callee;
with_stat({stat_name});


add_stat()
add_poll();
poll();							
with_poll();

goto_point()
go_route()



tell()
	_uuid({uuid})
	_name({name})
	_manufact({manufacturer})
	_make({make/brand})
	_model({model_name})
	_badge({badge/series})
	_id()_serial_number({serial_number})
	_id()
	

ask_energy();
tell_energy({energy_value})_unit({unit_of_measure});


ask_energy({uuid/name});

ask()
	_for()						_for({uuid/name}, ...);	





TAE40116_DEL_AT1_TP_v1_.pdf






, where {paramter_1} is expected to respond or 

ask();			ask({uuid});					ask()_for({human_uuid});
ask_human();	call_human({human_uuid});		call_human()_for({human_uuid});
ask_ai();		ask_ai({ai_uuid});				ask_ai()_for({ai_uuid});



ask_ai();
ask();

ask_organic();
ask_label();
ask_human();
ask_ai();

ask_gps({uuid/name})_freq({frequency}[,{unit}])_stopat({datetime})_until()



call({uuid});
call_human({human_uuid});		call_human()_for({human_uuid});
call_ai({ai_uuid});				call_ai()_for({ai_uuid});
call_robot({robot_uuid});		call_robot()_for({robot_uuid});
call_organic({organic_uuid});	call_organic()_for({organic_uuid});
call_thing({thing_uuid});		call_thing()_for({thing_uuid});
call_console({console_uuid});	call_console()_for({console_uuid});

call({moniker});
call_human({human_moniker});		call_human()_for({human_moniker});
call_ai({ai_moniker});				call_ai()_for({ai_moniker});
call_robot({robot_moniker});		call_robot()_for({robot_moniker});
call_thing({thing_moniker});		call_thing()_for({thing_moniker});
call_console({console_moniker});	call_console()_for({console_moniker});

call()_as({label})


```

## Navigation & Positioning

```Deigo
add_stat({moniker/uuid})
with_stat({moniker/uuid})
	
begin_stat({moniker/uuid}) - end_stat()
end_stat({moniker/uuid}) - begin_stat()
exec_stat({moniker/uuid}) - bump
call_stat({moniker/uuid})	- here_stat
start_stat({moniker/uuid}) - stop_stat
stop_stat({moniker/uuid})	- go_stat
pause_stat({moniker/uuid})


```

## System Commands

|  system command | Notes  |
|---|---|
| `help()`  | Provides the online help utility menu on system command line |
| 'modules"

```Diego

## Informant, Informing, Proclaiming

`proclaim_`		By default a `proclaim_` will send out a proclamation without any delivery or receive receipt.
`declare_`		By default a `declare_` will send out a declaration expecting a delivery receipt.
`inform_`		By default a `inform_` will inform and except a delivery and receive receipt.