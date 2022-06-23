https://mavlink.io

ask_position()_global()_protocol(mavlink);
ask_position()_scope(global)_protocol(mavlnk);

example:
```Diego
add_pact(rat_pack)_all();
ask_position(pos_in_mavlink)_protocol(mavlink)_for(rat_pack);
tell_position(pos_in_mavlink)_value()
```



## Translation of MAVLink Commands

### MAV_CMD_NAV_WAYPOINT ([16](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_WAYPOINT))

The `MAV_CMD_NAV_WAYPOINT` command will command a drone to _"navigate to waypoint"_. In Diego, this command can be achieved using the construction of the `go_` or `nav` verbs, the `drone` object, and, the `waypoint` child object.

The object can be either the drone^@^ (a `robot` of type `drone` or the shorthand `drone` object) _"...to travel to the waypoint"_ or the waypoint^@^ _"..for the drone to travel to"_.  These commands **must**, however, include a `waypoint` child object.  There are various postpsitions that can be used.

^@^ The drone object can be any phyical self-motivated object in the physical world, and the waypoint object can be any physical located object.

Examples for _Diego_ translation of the `MAV_CMD_NAV_WAYPOINT` command...

```Diego
go_robot({moniker|uuid})_type(drone)_waypoint({moniker|uuid});
go_drone({moniker|uuid})_waypoint({moniker|uuid});
nav_robot({moniker|uuid})_type(drone)_waypoint({moniker|uuid});
nav_drone({moniker|uuid})_waypoint({moniker|uuid});
```

See: [go](verb/go,md); [nav](verb/nav.md); [drone](obj/drone.md); [waypoint](obj/waypoint.md)

___

### MAV_CMD_NAV_LOITER_UNLIM ([17](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_UNLIM))

The `MAV_CMD_NAV_LOITER_UNLIM` command will command a drone to _"loiter around this waypoint an unlimited amount of time"_  In Diego the `loiter_` verb is the direct translation. The object can be either the drone _"...to loiter around the waypoint_ or the waypoint _"..for the drone to loiter around to"_ using the `_loiterat` postposition. The `_hold` (with empty parameters) is used for maintain an _"unlimited amount of time"_. There are various other postpositions that can be used.

Examples for a translation to match the `MAV_CMD_NAV_WAYPOINT` command...

```Diego
loiter_robot({moniker|uuid})_waypoint({moniker|uuid})_hold() ? : ;
with_robot({moniker|uuid})_loiterat({waypoint_moniker|waypoint_uuid})_hold() ? : ;
```

**Nevertheless, the use of the above command structures are considered foolish, since if a drone is instructed to loiter for a unlimited time at a waypoint, when itself is finite with finite resources. For instance, with no access to energy (fuel) it will surely run out of fuel and die; or, under threatening environment pressures it may suffer and die. Drones with common sense will realise the folly of this instruction and refuse to comply when it's nearing death.  The refusal is handled by the `refuse` object, and if the situation gets desperate the `wtf` object will be used.**

The foolishness of loitering forever can be seen in the human translations of the **Diego** instructioning...

> Diego: `loiter_robot(my_drone)_waypoint(green_flag)_hold() ? : ;`
>> Human: *"`my_drone`, go to `green_flag` and loiter there forever!"*
>> mavlink: `<entry name="MAV_CMD_NAV_LOITER_UNLIM"><param index="1"></param><param index="2"></param><param index="3">"`

> `with_robot(my_drone)_loiterat(green_flag)_hold() ? : ;`
>> *"`my_drone`, go and loiter at `green_flag` forever!"*

> `with_waypoint(green_flag)_loiterat()_hold()_for(my_drone) ? : ;`
>> *"At `green_flag`, `my_drone`, you will loiter there forever!"*

To resolve this foolishness (before the drone calls `refuse`), an exit strategy should at lease be deployed...

```Diego
with_robot(my_drone)_waypoint(green_flag)_loiterat()_hold()
        | exit()_appliedto(msg)_specificfor(robot)_forwho(my_drone)_why(move!) ? :
    ? : ;
```
>> *"`my_drone`, go and loiter at `green_flag`, when you get messaged "`move!`", go the the next command"*

See: [loiter](verb/loiter,md); [drone](obj/drone.md); [waypoint](obj/waypoint.md); [loiterat](postpos/loiterat.md)

___

## MAV_CMD_NAV_LOITER_TURNS ([18](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_TURNS))

Mavlink defines the `MAV_CMD_NAV_LOITER_TURNS` command as, _"[to instruct a drone to] ...loiter around this waypoint for X turns.




with_override()_appliedto()

| loiter type | description  |
|---|---|
|   | rotate on x-y plane on axis |
| | |



{object}
```Diego
thingy({moniker|uuid})_type({thingy_type});
robot({moniker|uuid});
waypoint(nav_to_x1);
```
{child_object}:
```Diego
_waypoint(x1)
_waypoint({x_lat},{y_long},{z_alt})
_waypoint({map},{x_lat},{y_long},{z_alt})
```
{postposition}:
```Diego
_onroute({moniker|uuid})
_holdfor({hold_time})
_tosphere({moniker})
_tosphere({radius})
_tosphere({x_lat},{y_long},{z_alt},{r})
_yawto({yaw}[, {unit}])

_me()
_for({moniker_1|uuid_1}[, ... {moniker_n|uuid_n}])
```
loiter_
navigat_waypoint(nav_to_x1)_waypoint(x1)_hold({hold_time})_insphere({aradius},{bradius})

```

### MAV_CMD_NAV_LOITER_TURNS (18)



navigat_, nav_, navigate_
```
With `go_` will travel to the `{object}` or travel the `{object}` to / using a straight-line algorithm, obstacle we will ny-passed on most efficient route.
`navigat_`, `nav_`, `navigate_` The `thingy` will travel to the `{object}` using any remembered.specified route(s).
{object}:
```Diego
thingy({moniker|uuid})_type({thingy_type});
robot({moniker|uuid});
waypoint(nav_to_x1);
```
{child_object}:
```Diego
_waypoint(x1)
_waypoint({x_lat},{y_long},{z_alt})
_waypoint({map},{x_lat},{y_long},{z_alt})
```
{postposition}:
```Diego
_onroute({moniker|uuid})
_holdfor({hold_time})
_tosphere({moniker})
_tosphere({radius})
_tosphere({x_lat},{y_long},{z_alt},{r})
_yawto({yaw}[, {unit}])

_me()
_for({moniker_1|uuid_1}[, ... {moniker_n|uuid_n}])