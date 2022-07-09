# Translation of MAVLink Commands
As with ***Diego***, **MAVLink**, or Micro Air Vehicle Link, is a protocol for communicating with mobile systems. It was first released in early 2009 by Lorenz Meier under the LGPL license. However, MAVLink does not provide the same 'programability' as ***Diego***, although, messaging through MAVLink is exceptionally lighter. 

With the wide-acceptance and wide-use of MAVLink, ***Diego*** does not have to replace MAVLink, but can utilise MAVLink through the use of `funnel`s for telemetry.

So, this article will provide a best-approach translation of the common MAVLink commands:

## MAV_CMD_NAV_WAYPOINT ([16](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_WAYPOINT))

The `MAV_CMD_NAV_WAYPOINT` command will command a drone to _"navigate to waypoint"_. In Diego, this command can be achieved using the construction of the `go_` verb, the `drone` object, and, the `waypoint` child object.

***Diego*** syntax allows either: the drone[^drone] (a `robot` of type `drone` or the shorthand `drone` object) _"...to travel to the waypoint"_; or, the waypoint[^wp] _"..for the drone to travel to"_. However, throughout these translations we will stick to the _moving-object-to-the-stationary-object_  approach. These commands **must**, however, include a `waypoint` child object.  There are various posits that can be used.

### Syntax

> MAVLink: `MAV_CMD_NAV_WAYPOINT(`*`holdsecs`*`, NaN, NaN, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and hold at waypoint for `holdsecs` seconds."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_hold(`*`holdsecs`*`)?;`[^?;]

> MAVLink: `MAV_CMD_NAV_WAYPOINT(NaN, `*`acceptradius`*`, NaN, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and accept waypoint reached when within `acceptradius` radius of waypoint in metres."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_around({m},`*`acceptradius`*`)?;`

> MAVLink: `MAV_CMD_NAV_WAYPOINT(NaN, NaN, 0, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and pass through waypoint."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)?;`

> MAVLink: `MAV_CMD_NAV_WAYPOINT(NaN, NaN, 1, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and ambire[^orbit] clockwise of 1 m radius, allowing for trajectory."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_ambire({m},1)?;`

> MAVLink: `MAV_CMD_NAV_WAYPOINT(NaN, NaN, -1, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and ambire counter-clockwise of 1 m[^int] radius, allowing for trajectory."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_ambire({m},-1.33)?;`

> MAVLink: `MAV_CMD_NAV_WAYPOINT(NaN, NaN, NaN, `*`headingdeg`*`, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and with desired heading[^yaw] of `headingdeg` degrees."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_aimin()_heading({deg},`*`headingdeg`*`)?;`

> MAVLink: `MAV_CMD_NAV_WAYPOINT(NaN, NaN, NaN, NaN, `*`lat`*`, `*`long`*`, `*`alt`*`)`<br>
> Human: *"Navigate to waypoint and with desired latitude of `lat`, longitude of `long`, and altitude of `alt`."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_aimin(`*`lat`*`,`*`long`*`,`*`alt`*`)?;`

See: [go](../../metaphysic/verb/go.md); [drone](../../physic/obj/drone.md); [waypoint](../../metaphysic/obj/waypoint.md)

[^drone]: The drone object can be any phyical self-motivated object in the physical world.
[^wp]: The waypoint object can be any physical located object.
[^?;]: The elvish operator combination of the command terminator (`?;`) is used to instruct the robot to finish the command before starting it's next one.
[^orbit]: MAVLink states, 'orbit' however, orbit implies a full orbital trajectory around the given object, whereas, ambire means to go around on an arc trajectory.
[^int]: MAVLink only allows `NaN` and `INT32_MAX` paramaters, however, Diego accepts any numeric values.
[^yaw]: MAVLink uses 'yaw', however, the heading is used.


## MAV_CMD_NAV_LOITER_UNLIM ([17](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_UNLIM))

The `MAV_CMD_NAV_LOITER_UNLIM` command will command a drone to, _"loiter around this waypoint an unlimited amount of time"_.  In ***Diego***, the `loiter_` verb is the direct translation. The object can be either the drone _"...to loiter around the waypoint"_, or the waypoint _"...for the drone to loiter around to"_ using the `_loiterat` postposition. The `_hold` posit (with empty parameters) is used to maintain an _"unlimited amount of time"_. There are various other postpositions that can be used.

Nevertheless, the use of a command to _"loiter ... [for] unlimited amount of time"_ is considered foolish.  If a drone is instructed to loiter for a unlimited time at a waypoint, when it has limited resources, it can't be expected to loiter for a *unlimited* amount of time. For instance, with no access to energy (fuel) it will surely run out of fuel and die; or, under threatening environment pressures it may suffer and die. Drones with common sense will realise the folly of this instruction and refuse to comply when it's nearing death.  The refusal is handled by the `refuse` object, and if the situation gets desperate the `wtf` object will be used.

The foolishness of loitering forever can be seen in the human translations of the following **Diego** instructioning...

> Diego: `loiter_robot(myDrone)_waypoint(greenFlag)_hold()?:;`<br>
> Human: *"`myDrone`, go to `greenFlag` and loiter there forever!"*

> Diego: `with_robot(myDrone)_loiterat(greenFlag)_hold()?:;`<br>
> Human: *"`myDrone`, go and loiter at `greenFlag` forever!"*

> Diego: `with_waypoint(greenFlag)_loiterat()_hold()_for(myDrone)?:;`<br>
> Human: *"At `greenFlag`, `myDrone`, you will loiter there forever!"*

Of course, the past experience and intelligence of `myDrone` drone will override any command when its life is on the line.  For instance, `myDrone` may detect that it needs more energy and therefore needs to return to a charging base.  In this scenario, `myDrone` will send its caller a command such as:

```Diego
with_robot(myDrone)_waypoint(greenFlag)_loiterat()_hold()_refuse(x101, low on energy, returning to charge);
```
.., and return to base (perhaps).

To resolve this foolishness (before the drone calls `refuse`), an exit strategy should be deployed (at least)...

Diego:
```diego
add_yush({level_5},myDrone-fuelLevel)_robot(myDrone)_fuelstatus(); 

go_robot(myDrone)_waypoint(greenFlag)
    ? loop_if([myDrone-fuelLevel]>low)
        ? with_robot(myDrone)_waypoint(greenFlag)_loiterat();
        : with_robot(myDrone)_rtb();
    ;
;
```
Human:

*"Before we start `myDrone`, learn how to read your fuel status.<br>
OK, `myDrone` go to `greenFlag`.  When you get there, check your fuel status.<br>
If your fuel status is better than 'low' then loiter at `greenFlag`, otherwise return to base."*

The `MAV_CMD_NAV_LOITER_UNLIM` command has seven paramaters, however, the first two are empty, so should be subtituted with `NaN`. To avoid the _loiter-till-you-drop-down-dead_ scenario, we will command the drone to loiter for a `durat`ion of 1 minute. The other paramater settings can be translated as follows:

> MAVLink: `MAV_CMD_NAV_LOITER_UNLIM(NaN, NaN, 1, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and loiter by yaw rotating on axis clockwise at a 1 m radius, allowing for trajectory."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_loiteraround({m},1)_durat({min},1)?;`

> MAVLink: `MAV_CMD_NAV_LOITER_UNLIM(NaN, NaN, -1, NaN, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and loiter by yaw rotating on axis counter-clockwise at a 1 m radius, allowing for trajectory."*<br>
> Diego: `go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_loiteraround({m},-1)_durat({min},1)?;`

> MAVLink: `MAV_CMD_NAV_LOITER_UNLIM(NaN, NaN, NaN, `*`headingdeg`*`, NaN, NaN, NaN)`<br>
> Human: *"Navigate to waypoint and enter loiter at heading[^yaw] of `headingdeg` degrees."*<br>
> Diego:<br>
`go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_aimin()_heading({deg},`*`headingdeg`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`? with_drone(`*`moniker`*`)_loiterat(`*`wpmoniker`*`)_durat({min},1)?;`<br>
`;`

> MAVLink: `MAV_CMD_NAV_LOITER_UNLIM(NaN, NaN, NaN, NaN, `*`lat`*`, `*`long`*`, `*`alt`*`)`<br>
> Human: *"Navigate to waypoint and enter loiter with desired latitude of `lat`, longitude of `long`, and altitude of `alt`."*<br>
> Diego:<br>
`go_drone(`*`moniker`*`)_waypoint(`*`moniker`*`)_aimin(`*`lat`*`,`*`long`*`,`*`alt`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`? with_drone(`*`moniker`*`)_loiterat(`*`wpmoniker`*`)_durat({min},1)?;`<br>
`;`



## MAV_CMD_NAV_LOITER_TURNS ([18](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_TURNS))

MAVLink defines the `MAV_CMD_NAV_LOITER_TURNS` command as, _"[to instruct a drone to] ...loiter around this waypoint for X turns."_. The unexplicit behaviour is to circle around a given waypoint at a set radius (from the waypoint as centre) using the sign (of the radius) for clockwise/counter-clockwise direction.  The 'circle' is intended to be on the *XY-Plane*.  The optional extra functionality, known as the `Xtrack Location`, provides specifications for the object to converge to an exit location and/or path of the next waypoint.

MAVLink provides an excellent condensed parameter array for a multifaceted function, so translating this behaviour in ***Diego*** is going to be more *'wordy'* than ***Diego*** normally is.

Firstly, the circle behaviour is managed in ***Diego*** with the `motion` object, which has, among several options, a `circle` pattern parameter.  Other parameters are available under different overloads, including pose parameters, `{point}` and `{orientation}`, provided by name or explicit '*x*, *y*, *z*' for point and a quaternion '*x*, *y*, *z*, *w*' form  (or named quatern) for orientation.  Other postpositions and child objects can be appended to suit requirements.  The syntax, with overloads, are as such:

```Diego
_motion({pattern})			// General syntax
_motion({pattern}, {point})	// Pattern & Point
_motion({pattern}, {point}, {orientation})		// Complex syntax
```

The `motion` object can be used (or declared then used) as a child object, or as a parent object, such as in these examples:

```diego
// using motion as a child object under the verb loiter (named point):
loiter_drone(myDrone)_motion(circle, greenFlag)_radius(0.98)_forcounter(4);

// Using motion as a parent object (with declaration)
add_motion(my_circle_clockwise)_motion(circle)_radius(0.98)_point(greenFlag);
with_motion(my_circle_clockwise)_waypoint(greenFlag)_forof(myDrone)_forcounter(2);

// Developing (then executing) motion object (linking waypoint to point)
begin_motion(my_cicle_counterclockwise);
	with_motion(my_cicle_counterclockwise)_motion(circle)_radius(-0.98);
	with_motion(my_cicle_counterclockwise)_point()_specificfor(waypoint);
end_motion(my_cicle_counterclockwise);
exec_motion(my_cicle_counterclockwise)_waypoint(greenFlag)_forof(myDrone)_forcounter(3);
```

The number of turns in the MAVLink command is parameter 1 `Turns`, which has a direct translation with the `_forcounter` postposition, as shown in the examples above.

The 'Xtrack Location' (parameter 4) of  the `MAV_CMD_NAV_LOITER_TURNS` command, instructs the object how to exit the loiter circle to converge on the 'Xtrack' (the line between the current waypoint and the next waypoint). This sub-instruction has been directly translated using the `xtrack` postposit with four options as:

To converge the exit loiter along direct line to next waypoint use: `_xtrack({1|true|yes|OK|direct})`. This is equivalent to (`xtrack=1`) in MAVLink.

To converge to a direct line from the exit point to the centre of the next waypoint use: `_xtrack({0|false|no)`.  This is equivalent to (`xtrack=0`) in MAVLink.

| ![loiter heading](https://mavlink.io/assets/protocols/mission_loiter/xtrack1_0_heading_1.png "xtrack=1 and xtrack=0 (Source: MAVLink)") | 
|:--:| 
| *xtrack=1 and xtrack=0 (Source: MAVLink)* |

To use the default `xtrack` either miss out the `_xtrack` posposit or use: `_xtrack()` or `_xtrack({null|nul|nan})`.  This is equivalent to (`xtrack=NaN`) in MAVLink.  The default is usually set in the object(s) childhood, however if not set use `with_me()_xtrack({default})__specificto(loiter);` or just `set_xtrack({default});`.  If the object has no recollection of the default `xtrack` setting it will use `_xtrack(direct)` and set the default to `direct` at the same time.

To  for a specified tangent angle use `_xtrack({degrees/radians})` or `_xtrack({degrees/radians}, {unit})` or `_xtrack({degrees/radians})_unit({deg/rad})`.  When units are not specified the default `set_unit({deg|rad})_measure(angles)` will be used.

| ![loiter heading](https://mavlink.io/assets/protocols/mission_loiter/xtrack_30.png "xtrack=30 (Source: MAVLink)") |
| :----------------------------------------------------------: |
|                *xtrack=30 (Source: MAVLink)*                 |

Parameters 5, 6, and 7 (`Latitude`, `Longitude`, and, `Altitude`, respectively) of the `MAV_CMD_NAV_LOITER_TURNS` command are redundant as ***Diego*** will use the coordinates of the child object or any implied coordinates in the instruction dialogue.  With absolutely no known or implied coordinates the object will loiter at its own position at the point of executing the command.

## MAV_CMD_NAV_LOITER_TIME ([19](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_TIME))

The `MAV_CMD_NAV_LOITER_TIME` command will instruct the object to, _"...loiter ar the specified latitude, longitude and altitude for a certain amount of time"_. In ***Diego*** the same interface used for the `MAV_CMD_NAV_LOITER_TURNS` command (translated above) can be used here.

The same 'circle as loiter' behaviour can be commanded using the `motion(circle)` object-parameter, and the `_xtrack` postposit is used as the direct translation of the Xtrack Location parameter (parameter number 4) in the `MAV_CMD_NAV_LOITER_TIME` command.  The only difference in the `MAV_CMD_NAV_LOITER_TIME` command is the `_forcounter({counter})` postposit is replace with `_fortime({time})` posposit.  For example:

```Diego
// Loiter for 54000 milliseconds (as default)
loiter_drone(myDrone)_motion(circle, greenFlag)_radius(0.98)_fortime(54000);

// Loiter for 54 seconds (explicit, local scope for this command only)
loiter_drone(myDrone)_motion(circle, greenFlag)_radius(0.98)_fortime(54, sec);

// Loiter for 0.9 minutes (explicit, command scope for all '_fortime' postposits forever after)
loiter_drone(myDrone)_motion(circle, greenFlag)_radius(0.98)_fortime(0.9)_unit(min);

// Set global default of seconds unit for _fortime postposits
set_unit(sec)_specificto(fortime);
```

The unit for the 'amount of time' to loiter can be set in the usual manner: default, explicit-local, _from-now-on_, or, globally set.

## MAV_CMD_NAV_RETURN_TO_LAUNCH ([20](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_RETURN_TO_LAUNCH))

Often used as a _failsafe_ mechanism, the `MAV_CMD_NAV_RETURN_TO_LAUNCH` command will instruction the object to, _"...return to the 'home' location or the nearest 'rally point', if closer"_[^1]. 

```Deigo
// Return to base
with_drone(myDrone)_rtb();  // or...
rtb_drone(myDrone);
(myDrone)_rtb();        
rtb(myDrone);


// Return to secified location
with_drone(myDrone)_rtb()_waypoint(homeBase);   // or...
rtb_drone(myDrone)_waypoint(homeBase);
(myDrone)_rtb()_wp(homeBase);
rtb(myDrone)_(homeBase);

// Return to nearest suitable location
with_drone(myDrone)_waypoint()_type(rally_point)_forwhere(nearest); // or...
rtb_drone(myDrone)_waypoint({rally_point})_forwhere(nearest);
(myDrone)_rtb()_wp({rally_point}{nearest});
(myDrone)_({wp},{rally_point}{nearest});

// Return all drones to a specified location:
with_drone()_rtb()_waypoint(westRallyPoint);    // or...
with_waypoint(westRallyPoint)_rtb()_drone();
(westRallyPoint)_rtb()_drone();
rtb(westRallyPoint)_drone();

// Return all drones (in flight) to the nearest rally point
with_drone()_status(in_flight)_rtb()_waypoint()_type(rally_point)_forwhere(nearest);    // or...
rtb_drone()_status(in_flight)_waypoint()_type(rally_point)_forwhere(nearest);
({drone})_stat(if)_rtb({wp},{rally_point},{nearest});           ---???
rtb({drone})_stat(1)_wp({rally_point},{nearest});           ---???
```

[^1]: https://ardupilot.org/copter/docs/common-MAVLink-mission-command-messages-mav_cmd.html#mav-cmd-nav-return-to-launch






_________________________

https://MAVLink.io

ask_position()_global()_protocol(MAVLink);
ask_position()_scope(global)_protocol(mavlnk);

example:
```Diego
add_pact(rat_pack)_all();
ask_position(pos_in_MAVLink)_protocol(MAVLink)_for(rat_pack);
tell_position(pos_in_MAVLink)_value()
```





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

> Diego: `loiter_robot(myDrone)_waypoint(greenFlag)_hold() ? : ;`
>> Human: *"`myDrone`, go to `greenFlag` and loiter there forever!"*
>> MAVLink: `<entry name="MAV_CMD_NAV_LOITER_UNLIM"><param index="1"></param><param index="2"></param><param index="3">"`

> `with_robot(myDrone)_loiterat(greenFlag)_hold() ? : ;`
>> *"`myDrone`, go and loiter at `greenFlag` forever!"*

> `with_waypoint(greenFlag)_loiterat()_hold()_for(myDrone) ? : ;`
>> *"At `greenFlag`, `myDrone`, you will loiter there forever!"*

To resolve this foolishness (before the drone calls `refuse`), an exit strategy should at lease be deployed...

```Diego
with_robot(myDrone)_waypoint(greenFlag)_loiterat()_hold()
        | exit()_appliedto(msg)_specificfor(robot)_forwho(myDrone)_why(move!) ? :
    ? : ;
```
>> *"`myDrone`, go and loiter at `greenFlag`, when you get messaged "`move!`", go the the next command"*

See: [loiter](verb/loiter,md); [drone](obj/drone.md); [waypoint](obj/waypoint.md); [loiterat](postpos/loiterat.md)

___

## MAV_CMD_NAV_LOITER_TURNS ([18](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_TURNS))

MAVLink defines the `MAV_CMD_NAV_LOITER_TURNS` command as, _"[to instruct a drone to] ...loiter around this waypoint for X turns.




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


<!-- http://wiki.ros.org/mavros#mavcmd -->