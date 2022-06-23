# Lexicon

## Genera

| Genus     | Notes |
| --------- | ----- |
| `human`   |       |
| `ai`      |       |
| `robot`   |       |
| `mobot`   |       |
| `organic` |       |
| `thing`   |       |
| `console` |       |
| `object`  |       |
| `subject` |       |

## Verbs

| Verb         | Inverse        | Notes |
| ------------ | -------------- | ----- |
| `add_`    | `minus_` |       |
| `ask_`    | `tell_` |       |
| `back_` | `fetch_` | |
| `call_`    | `here_` or `pong_` |       |
| `fetch_`    | `back_` |       |
| `get_` | `set_` | |
| `go_` | `stop_` and `pause_` |       |
| `hear_` | `listen_` | |
| `here_`    | `call_` |       |
| `listen_`    | `hear_` |       |
| `look_` | `see_` | |
| `minus_`    | `add_` |       |
| `pause_` | see `go_` and `stop_` | |
| `pong_`    | `ping_` |       |
| `rem_`    | `recall_` |       |
| `see_`    | `look_` |       |
| `set_`    | `get_` |       |
| `stop_` | `go_` and `pause_` | |
| `tell_`    | `ask_` |       |
| `with_`    |                |       |
| `kill_` | | |
| `murder_` | | |
| `neigh_` | | |
| `hook_` | `unhook_` | |
|  | | |
|  | | |
|  | | |

## Nouns

| Noun      | Notes |
| --------- | ----- |
| `ai`      | 'Artificial Intelligence' is one of ten genera. |
| `badge` | |
| `birth` | |
| `cloud` | |
| `comm` | |
| `console` |       |
| `coord` | |
| `fog` | |
| `gate` |       |
| `gnps` | **G**obal **N**avigation and **P**ositioning **S**ystem |
| `human`   |       |
| `id` | |
| `label` | A human-readable string appened for one/many genera. |
| `litsan` | '**L**ine **i**n **t**he **San**d' |
| `lnps` | **L**ocal **N**avigation and **P**ositioning **S**ystem |
| `make` | |
| `manufact` | |
| `marker` |       |
| `metric` |       |
| `mist` | |
| `mobot`   |       |
| `model` | |
| `modelnum` | |
| `name` | |
| `object`  |       |
| `organic` |       |
| `path` |       |
| `point` |       |
| `poll`    |       |
| `pulse`          |       |
| `pulsepoint` |       |
| `punkt` |       |
| `robot`   |       |
| `route` |       |
| `serialnum` | |
| `stat` | |
| `subject` |       |
| `tempus` |       |
| `thing`   |       |
| `tracker` |       |
| `trackpoint` |       |
| `geometric` | |
| `blob` | |
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

