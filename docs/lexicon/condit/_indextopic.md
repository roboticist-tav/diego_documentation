# Conditions
Conditions or `condit`s are used throughout ***Diego*** language to condtion preceeding *object* for proceeding *object*, usually to do a proceeding (or sometime preceeding) *action*.

Condits can be categorised into several categories: (Temporal Conditions)(#temp); 

<a name="temp"></a>
## Temporal Conditions
All temporal `condit`*ions* are determined at the callee's datetime system.  Dates are defaulted to `set_calendar(gregorian)`, but can be changed by the caller.

### `_at`
The `_at` condit*ion* determines that the preceeding command(s) are executed when a date|datetime|time matching the given *`date|datetime|time`* or *`date_var|datetime_var|time_var`*` of the callee.

The default syntax is `_at(`*`date|datetime|time`*`)`, for example:
```diego
// Robot 'alif' must maneuver to 'waypoint1' as soon as 'alif's date matches the date|datetime|time set:
go_robot(alif)_to(waypoint1)_at(12-Jun-2022);
go_robot(alif)_to(waypoint1)_at(12-Jun-2022 11:00);
go_robot(alif)_to(waypoint1)_at(11:00);
```
Variables can be used with `_at`, for example:
```diego
// Robot 'beh' must maneuver to 'waypoint1' as soon as 'beh's date matches the date|datetime|time variable 'pit':
go_robot(beh)_to(waypoint1)_at[pit];
go_robot(beh)_to(waypoint1)_at([pit]);  // same effect


// The variable 'pit' can be converted inside the _at condit:
go_robot(beh)_to(waypoint1)_at({time},[pit]);
```

The `_at` condit can be converted to a concomit*ant*, for example:
```diego
// Transfer _at to _concomit:
go_robot(teh)_to(waypoint1)_at(11:00)_concomit(dailyRoutine);

// Concomitant 'dailyRoutine' will continue indefinitely until:
stop_concomit(dailyRoutine);
start_concomit(dailyRoutine);
pause_concomit(dailyRoutine);
resume_concomit(dailyRoutine);  // (or start_…)
end_concomit(dailyRoutine);
```
…for more information on concomits see [concomit](/concomit.md).

### `_after`
The `_after` condit*ion* determines that the preceeding command(s) are executed after (and including) the date|datetime|time matching the given date|datetime|time or date_var|datetime_var|time_var` of the callee.

 The default syntax is `_after(`*`date|datetime|time`*`)`, for example:
```diego
// Robot 'alif' must maneuver to 'waypoint1' any time after 'alif's date matches the  date|datetime|time set:
go_robot(alif)_to(waypoint1)_after(12-Jun-2022);
go_robot(alif)_to(waypoint1)_after(12-Jun-2022 11:00);
go_robot(alif)_to(waypoint1)_after(11:00);
```
Variables can be used with `_after`, for example:
```diego
// Robot 'beh' must maneuver to 'waypoint1' anytime after 'beh's date matches the date|datetime|time variable 'pit':
go_robot(beh)_to(waypoint1)_after[pit];
go_robot(beh)_to(waypoint1)_after([pit]);        // same effect

// The variable 'pit' can be converted inside the _after condit:
go_robot(beh)_to(waypoint1)_after({time},[pit]);
```

The `_after` condit can be converted to a concomit*ant*, for example:
```diego
// Transfer _after to _concomit:
go_robot(teh)_to(waypoint1)_after(11:00)_concomit(dailyRoutine);

// Concomitant 'dailyRoutine' will continue indefinitely until:
stop_concomit(dailyRoutine);
start_concomit(dailyRoutine);
pause_concomit(dailyRoutine);
resume_concomit(dailyRoutine);  // (or start_…)
end_concomit(dailyRoutine);
```
…for more information on concomits see [concomit](/concomit.md).
### `_during`
### `_before`
The `_before` condit*ion* determines that the preceeding command(s) are executed only before (and including) the date|datetime|time matching the given date|datetime|time or date_var|datetime_var|time_var` of the callee.

To determine the extent of the 'before' logic, the callee will use the default `set_start({`*`date_datatype|time_datatype`*`,`*`setting`*`)` command, that the callee has learnt.  The caller can (if granted), set and reset the start dates and start times.  For example:
```diego
set_start({date},01-Jan);
set_start({time},00:00);

reset_start[];  // reset start settings back to how they were before set
reset_start();  // reset start settings to default
reset_
```

 The default syntax is `_before(`*`date|datetime|time`*`)`, for example:
```diego
// Robot 'alif' must maneuver to 'waypoint1' any time before 'alif's date matches the  date|datetime|time set:
go_robot(alif)_to(waypoint1)_before(12-Jun-2022);
go_robot(alif)_to(waypoint1)_before(12-Jun-2022 11:00);
go_robot(alif)_to(waypoint1)_before(11:00);
```
Variables can be used with `_before`, for example:
```diego
// Robot 'beh' must maneuver to 'waypoint1' anytime before 'beh's date matches the date|datetime|time variable 'pit':
go_robot(beh)_to(waypoint1)_before[pit];
go_robot(beh)_to(waypoint1)_before([pit]);        // same effect

// The variable 'pit' can be converted inside the _before condit:
go_robot(beh)_to(waypoint1)_before({time},[pit]);
```

The `_before` condit can be converted to a concomit*ant*, for example:
```diego
// Transfer _before to _concomit:
go_robot(teh)_to(waypoint1)_before(11:00)_concomit(dailyRoutine);

// Concomitant 'dailyRoutine' will continue indefinitely until:
stop_concomit(dailyRoutine);
start_concomit(dailyRoutine);
pause_concomit(dailyRoutine);
resume_concomit(dailyRoutine);  // (or start_…)
end_concomit(dailyRoutine);
```
…for more information on concomits see [concomit](/concomit.md).








| Sytnax | Notes<br />`example` |
| ---- | ---- |
| <br>`_at[`*`date_var\|datetime_var\|time_var`*`]`<br>`_at({`*`date_dt\|datetime_dt\|time_dt`*`}, [`*`date_var\|datetime_var\|time_var`*`])` | Condition that preceeding command(s) have a date\|datetime\|time matching the given *`date\|datetime\|time`* |
| `_from(`*`date|datetime|time`*`)_to(`*`date|datetime|time`*`)` | |
| `_after(`*`date|datetime|time`*`)` | |
| `_before(`*`date|datetime|time`*`)` | |
| `_ago(`*`value`*`, `*`unit`*`)` &nbsp; or…<br />`_ago(`*`value`*`)_unit(`*`unit`*`)` | |





## Spatial / Geo-spatial Conditions

There are sevaral spatial/geo-spatal postposits available.

| Sytnax | Notes<br />`example` |
| ---- | ---- |
| 





## Positions

| Position                                                 | Notes                                                 |
| -------------------------------------------------------- | ----------------------------------------------------- |
| `_at({date|datetime|time})`                              |                                                       |
| `_au({x},{y},{z})`                                       |                                                       |
| `_between({parameter_1})_and({parameter_2})_inclusive_()`
or _range({parameter_1})_and({parameter_2}) |                                                       |
| `_between({parameter_1})_and({parameter_2})`             |                                                       |
| `_blob({blob_uuid})`                                     |                                                       |
| `_for({parameter_1}[,… {parameter_n}])`                | Provides focus on `{parameter_1}` … `{parameter_n)` |
| `_fps({fps})`                                            |                                                       |
| `_from({date|datetime|time})_to({date|datetime|time})`   |                                                       |
| `_from({date|datetime|time})`
`_upto({date|datetime|time})`                         |                                                       |
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
_for({parameter_1},… {parameter_n})					Provides focus on {parameter_1} … {parameter_n)
_between({parameter_1})_and({parameter_2})				Provides focus from {parameter_1} to {parameter_2} inclusive
_between({parameter_1})_and({parameter_2})_exclusive()	Provides focus from {parameter_1} to {parameter_2} exclusive


label({label});					Caller assigns label {label} to the callee
label({label})
	_for({uuid/name}, …);		Assigns a label {label} to {uuid/name_1} … {uuid/name_n}
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
	_for()						_for({uuid/name}, …);	





TAE40116_DEL_AT1_TP_v1_.pdf
 where {paramter_1} is expected to respond or 

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


```diego

add_var({datetime},pit)_value(12-Jun-2022 11:00);
go_robot(beh)_to(waypoint1)_at[pit];    // <= 12-Jun-2022 11:00 - actually the pointer of the variable
go_robot(beh)_to(waypoint1)_at([pit]);  // <= 12-Jun-2022 11:00 - same, the value of the variable
go_robot(beh)_to(waypoint1)_at(pit);    // <= pit - error
```