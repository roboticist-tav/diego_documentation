# Translation of MAVLink Commands
As with ***Diego***, **MAVLink**, or Micro Air Vehicle Link, is a protocol for communicating with mobile systems. It was first released in early 2009 by Lorenz Meier under the LGPL license. However, MAVLink does not provide the same 'programability' as ***Diego***, although, messaging through MAVLink is exceptionally lighter. 

With the wide-acceptance and wide-use of MAVLink, ***Diego*** does not have to replace MAVLink, but can utilise MAVLink through the use of `funnel`s for telemetry.

So, this article will provide a best-approach translation of the common MAVLink commands:

## MAV_CMD_NAV_WAYPOINT ([16](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_WAYPOINT))

The `MAV_CMD_NAV_WAYPOINT` command will command a drone to *_"navigate to waypoint"_* *(sic.)*. In ***Diego***, this command can be achieved using the construction of the `go_` or `nav_` verbs, the `drone` object (or appropriate thingy object), and, the `waypoint` as a child object.

The object, in this case, a drone (a `robot` of type `drone` or the shorthand `drone` object) is to, *_"...to travel to the waypoint"_* or the waypoint^♣^ *_"..for the drone to travel to"_*.  These commands ***must***, however, include a `waypoint` child object.  There are various postpositions that can be used.

^♣^ The drone object can be any physical self-motivated (mobile) object in the physical world, and the waypoint object can be any physical located object.

Syntax examples for *_Diego_* translation of the `MAV_CMD_NAV_WAYPOINT` command...

```Diego
go_robot({moniker|uuid})_type(drone)_waypoint({moniker|uuid});
go_drone({moniker|uuid})_waypoint({moniker|uuid});
nav_robot({moniker|uuid})_type(drone)_waypoint({moniker|uuid});
nav_drone({moniker|uuid})_waypoint({moniker|uuid});
```

## MAV_CMD_NAV_LOITER_UNLIM ([17](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_UNLIM))

The `MAV_CMD_NAV_LOITER_UNLIM` command will command a drone to, _"loiter around this waypoint an unlimited amount of time"_.  In ***Diego***, the `loiter_` verb is the direct translation. The object can be either the drone _"...to loiter around the waypoint"_, or the waypoint _"...for the drone to loiter around to"_ using the `_loiterat` postposition. The `_hold` (with empty parameters) is used to maintain an _"unlimited amount of time"_. There are various other postpositions that can be used.

Syntax examples for a translation to match the `MAV_CMD_NAV_WAYPOINT` command...

```Diego
loiter_robot({moniker|uuid})_waypoint({moniker|uuid})_hold() ? : ;
with_robot({moniker|uuid})_loiterat({waypoint_moniker|waypoint_uuid})_hold() ? : ;
```

Nevertheless, the use of the above command structures are considered foolish.  If a drone is instructed to loiter for a unlimited time at a waypoint, when it has limited resources, it can't be expected to loiter for a *unlimited* amount of time. For instance, with no access to energy (fuel) it will surely run out of fuel and die; or, under threatening environment pressures it may suffer and die. Drones with common sense will realise the folly of this instruction and refuse to comply when it's nearing death.  The refusal is handled by the `refuse` object, and if the situation gets desperate the `wtf` object will be used.

The foolishness of loitering forever can be seen in the human translations of the **Diego** instructioning...

> Diego: `loiter_robot(my_drone)_waypoint(green_flag)_hold() ? : ;`
> Human: *"`my_drone`, go to `green_flag` and loiter there forever!"*

> Diego: `with_robot(my_drone)_loiterat(green_flag)_hold() ? : ;`
> Human: *"`my_drone`, go and loiter at `green_flag` forever!"*

> Diego: `with_waypoint(green_flag)_loiterat()_hold()_for(my_drone) ? : ;`
> Human: *"At `green_flag`, `my_drone`, you will loiter there forever!"*

*Note that a hit of resolution is provided in the above code snippits with the use of the  hey_diego operator (`?`) and oh_diego operator (`:`).*

To resolve this foolishness (before the drone calls `refuse`), an exit strategy should be deployed (at least)...

```Diego
with_robot(my_drone)_waypoint(green_flag)_loiterat()_hold() | ;
| with_cmd()_appliedto(msg)_specificfor(robot)_forwho(my_drone)_forwhy(msg)_whyfor(move!) ? ;
? with_robot(my_drone)_rtb();
```
The above command structure can be *translated* for humans as: *"`my_drone`, go and loiter at `green_flag`, when you get messaged "`move!`", (go the the next command) return to (the default) base"* . The "move!" command can be executed as `msg_robot(my_drone)_msg(move!);`.  Of course, the past experience and intelligence of `my_drone` drone will override any command when its life is on the line.  For instance, `my_drone` may detect that it needs more energy and therefore needs to return to a charging base.  In this scenario, `my_drone` will send its caller a command such as:

```Diego
with_robot(my_drone)_waypoint(green_flag)_loiterat()_hold()_refuse(x101, low on energy, returning to charge);
```

## MAV_CMD_NAV_LOITER_TURNS ([18](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_LOITER_TURNS))

Mavlink defines the `MAV_CMD_NAV_LOITER_TURNS` command as, _"[to instruct a drone to] ...loiter around this waypoint for X turns."_. The unexplicit behaviour is to circle around a given waypoint at a set radius (from the waypoint as centre) using the sign (of the radius) for clockwise/counter-clockwise direction.  The 'circle' is intended to be on the *XY-Plane*.  The optional extra functionality, known as the `Xtrack Location`, provides specifications for the object to converge to an exit location and/or path of the next waypoint.

MAVLink provides an excellent condensed parameter array for a multifaceted function, so translating this behaviour in ***Diego*** is going to be more *'wordy'* than ***Diego*** normally is.

Firstly, the circle behaviour is managed in ***Diego*** with the `motion` object, which has, among several options, a `circle` pattern parameter.  Other parameters are available under different overloads, including pose parameters, `{point}` and `{orientation}`, provided by name or explicit '*x*, *y*, *z*' for point and a quaternion '*x*, *y*, *z*, *w*' form  (or named quatern) for orientation.  Other postpositions and child objects can be appended to suit requirements.  The syntax, with overloads, are as such:

```Diego
_motion({pattern})			// General syntax
_motion({pattern}, {point})	// Pattern & Point
_motion({pattern}, {point}, {orientation})		// Complex syntax
```

The `motion` object can be used (or declared then used) as a child object, or as a parent object, such as in these examples:

```Diego
// using motion as a child object under the verb loiter (named point):
loiter_drone(my_drone)_motion(circle, green_flag)_radius(0.98)_forcounter(4);

// Using motion as a parent object (with declaration)
add_motion(my_circle_clockwise)_motion(circle)_radius(0.98)_point(green_flag);
with_motion(my_circle_clockwise)_waypoint(green_flag)_forof(my_drone)_forcounter(2);

// Developing (then executing) motion object (linking waypoint to point)
begin_motion(my_cicle_counterclockwise);
	with_motion(my_cicle_counterclockwise)_motion(circle)_radius(-0.98);
	with_motion(my_cicle_counterclockwise)_point()_specificfor(waypoint);
end_motion(my_cicle_counterclockwise);
exec_motion(my_cicle_counterclockwise)_waypoint(green_flag)_forof(my_drone)_forcounter(3);
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
loiter_drone(my_drone)_motion(circle, green_flag)_radius(0.98)_fortime(54000);

// Loiter for 54 seconds (explicit, local scope for this command only)
loiter_drone(my_drone)_motion(circle, green_flag)_radius(0.98)_fortime(54, sec);

// Loiter for 0.9 minutes (explicit, command scope for all '_fortime' postposits forever after)
loiter_drone(my_drone)_motion(circle, green_flag)_radius(0.98)_fortime(0.9)_unit(min);

// Set global default of seconds unit for _fortime postposits
set_unit(sec)_specificto(fortime);
```

The unit for the 'amount of time' to loiter can be set in the usual manner: default, explicit-local, _from-now-on_, or, globally set.

## MAV_CMD_NAV_RETURN_TO_LAUNCH ([20](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_RETURN_TO_LAUNCH))

Often used as a _failsafe_ mechanism, the `MAV_CMD_NAV_RETURN_TO_LAUNCH` command will instruction the object to, _"...return to the 'home' location or the nearest 'rally point', if closer"_[^1]. 

```Deigo
// Return to base
rtb_drone(my_drone);

// Return to secified location
rtb_drone(my_drone)_waypoint(home base);

// Return to nearest location type
rtb_drone(my_drone)_waypoint()_type(rally_point)_forwhere(nearest);

// Return all drones to a specified location:
with_waypoint(west rally point)_rtb()_drone();

// Return all drones (in flight) to the nearest rally point
rtb_drone()_status(in_flight)_waypoint()_type(rally_point)_forwhere(nearest);
```

[^1]: https://ardupilot.org/copter/docs/common-mavlink-mission-command-messages-mav_cmd.html#mav-cmd-nav-return-to-launch



| ![Route Matrix](route_matrix.jpeg "Route Matrix") |
| :----------------------------------------------------------: |
|                *Route Matrix*                 |

