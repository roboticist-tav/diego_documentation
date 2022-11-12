[HTML]: HyperText Markup Language
*[IoT]: Internet Of Things
*[uuid]: Universally Unique IDentifier
# Getting Started with diego (turtlesim)
## Start diego
Open a new terminal window.

Now you will run the _diego_ console, type:
```
diego
```
The _diego_ application will load showing the console window and a command window.

## Start diego console
To start turtlesim, enter the following command in your terminal:
```ros2
ros2 run deigo diego_console_node
```

## Start ROS2 turtlesim
To start turtlesim, enter the following command in your terminal:
```ros2
ros2 run turtlesim turtlesim_diego_node
```
The simulator window should appear, with a random turtle in the centre, such as:
![https://index.ros.org/doc/ros2/_images/turtlesim.png](https://index.ros.org/doc/ros2/_images/turtlesim.png)
In the terminal under the command, you will see messages from the node, similar to these:
```
[INFO] [turtlesim]: Starting turtlesim with node name /turtlesim
[INFO] [turtlesim]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]
```
Here you can see your default turtle’s name is `turtle1`, and the default coordinates where it spawns.

In the _diego_ console you see the similar to the following appear:
```diego
turtle_ocean1: add_map(turtle_ocean1, 97ed41b0-b2c1-41a5-83cc-efddf74ddbf0);
               with_me()_bound(box, 0.00, 0.00, 11.08889, 11.08889);
               with_me()_centre(5.544445, 5.544445);
               with_me()_pixel(box, 500, 500);
               with_me()_bgcolour(blue);
               with_me()_pac(ros2)_node(/turtlesim);
turtle1: add_simulat(turtle1, efea0397-d9f7-48b5-a4d6-5dd514200cf9);
         with_me()_at(turtle_ocean1, 5.544445, 5.544445);
         with_me()_represent(foxy);
         with_me()_pac(ros2)_ns(/turtle1);
```
In this world, represented by map `turtle_ocean1` there are two `thing`s: the map `turtle_ocean_1` and the `simulat`*[ion]  `turtle1`.  Each `thing` has explained themselves to the _puff_, so each `thing` is aware of each other.

## Roll Call
When you started turtlesim there is activity in the _puff_ which can be seen in console window, similar to:
```diego
add_thing(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8)_thing(meta)_type(sim);
add_map(map1, 4d20e7d3-1c89-44c6-bd31-0f353090d6e4);
```
In the command window type,:
```diego
rollcall();
```
The console window should then show:
```diego
[diego]: rollcall();
```
The `rollcall` command will ask for the identities of all in the _puff_.  If everything is at default, such as this is the very first time you have executed any _diego_ commands, a reply in the console window, such as the following, may return:
```diego
[diego]: rollcall();
turtle1: with_me(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8)_thing(meta)_type(sim);
map1: with_me(map1, 4d20e7d3-1c89-44c6-bd31-0f353090d6e4)_thing(meta)_type(map);
```
At this point, `turtle1` has received the `rollcall` command and has replied with the basic identification information it knows about itself: _moniker_, _uuid_, type of _human_/_thing_; and, _thing type_ or _thingy_.  In addition, `turtle1` has some information of its world,  given to it when it was ~~born~~ spawned _ `map1`.  `turtle1` has realised that no other `thing`s in the _puff_ have mentioned the presence of `map1`, so `turtle1` speaks up for `map1`, broadcasting the uuid of `map1`, in response to `rollcall`.


To find out more of `turtle1` we enter the following command in the command window:
```diego
with_thing()_for(turtle1);
```
, or…
| Command | Result |
|:--|:--|
| `with_thing();` | Returns all known 'self-information' from all `thing`s in the _puff_. |
| `with_thing()_for(turtle1, turtle2, `*`n…`*`);` | Returns all known 'self-information' from `turtle1`, `turtle2`, *`n…`* only if they are `thing`s. |
| `with_thing()_notfor(turtle2, `*`n…`*`);` | Returns all known 'self-information' from all `thing`s in the _puff_ except for  `turtle2`, *`n…`* `thing`s. |
| `with_thing()_of(simulat, `*`n…`*`);` |  Returns all known 'self-information' from all `thing`s in the _puff_ of type `simlat`, *`n…`*. | |
| `with_thing()_notof(mach, `*`n…`*`);` | Returns all known 'self-information' from all `thing`s in the _puff_ except for '`thing`s of type `mach`, *`n…`*. |
| `with_simulat(turtle1);` | Returns all known 'self-information' from `turtle1` only if `turtle1` is a `simulat`. |
| `with_simulat();` | Returns all known 'self-information' from all `simulat`s in the _puff_. |
| `with_simulat()_for(turtle1, turtle2, `*`n…`*`);` | Returns all known 'self-information' from `turtle1`, `turtle2`, *`n…`* only if they are `simulat`s. |
| `with_simulat()_notfor(turtle2, `*`n…`*`);` | Returns all known 'self-information' from all `simulat`s in the _puff_ except for  `turtle2`, *`n…`* `simulat`s. |


A reply will be similar to:
```diego
[diego]: with_thing()_for(turtle1);
turtle1: with_thing(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8)_me();
           with_thing(turtle1)_thing(meta)_me();
           with_thing(turtle1)_type(simulat)_me();
           with_thing(turtle1)_ident(ros, turtlesim, foxy)_me();
           with_thing(turtle1)_pac(ros2, foxy)_node(/turtlesim)_me();
           with_thing(turtle1)_map(map1)_me();
           with_thing(turtle1)_at(map1, 5.544445, 5.544445, 0.000000)_me();
```
At this point there are two `thing`s and one every`thing`.  The two `things` are `turtle1` and `map1`, and the every`thing` is the _diego_.  Both `turtle1` and `map1` are listening - learning - remembering all the activity in the _diego_, so `map1` is learning about `turtle1` and visa versa.  To test this let's ask `map1` what it knows of the world.  Type the following in the command window:
```diego
ask_simlat(turtle1)_for(map1);
```
, or…
| Command Cookbook | Result |
|:--|:--|
| `ask_thing(turtle1)_for(map1);` | Returns all known 'community-information' of `thing` `turtle1` from `map`. |
| `ask_thing(turtle1);` | Returns all known 'community-information' of `thing` `turtle1` from any`thing` (or anyone, *i.e.* any `human`) in the _puff_ (including `turtle1` itself if `turtle1` is in the _puff_ and `set_ofself` is set to *`true`*). |
The response (in the console window) should be similar to:
```diego
diego: ask_simlat(turtle1)_for(map1);
map1: of_simulat(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8);
      of_simlate(turtle1)_thing(meta);
      of_simlate(turtle1)_type(simulat);
      of_simlate(turtle1)_ident(ros, turtlesim, foxy);
      of_simlate(turtle1)_pac(ros2, foxy)_node(/turtlesim);
      of_simlate(turtle1)_map(map1);
      of_simlate(turtle1)_at(map1, 5.544445, 5.544445, 0.000000);
```
## Give birth to a human
With the _diego_ application in our hands we have the power to add 'any`thing`' (or anyone) to this world, even ourselves (i.e. a human)!  So let's do that…

Add the command window type the following:
```diego
add_human(fred);
```
Here a human called `fred` is created, and given at birth a uuid. In the console window as similar message should show:
```diego
[deigo]: add_human(fred, e009d5fb-baf6-4285-813b-02fdf6014271);
```
In the control drop-down there are now two entries: `[diego]` and `fred`.  From this deigo application we can speak for `[diego]` and `fred`.


 Keeping with `[diego]`  type a `rollcall` in the command window.  You will notice that `fred` is also responding:
```diego
[diego]: rollcall();
turtle1: with_me(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8)_thing(meta)_type(sim);
map1: with_me(map1, 4d20e7d3-1c89-44c6-bd31-0f353090d6e4)_thing(meta)_type(map);
fred: with_me(fred, e009d5fb-baf6-4285-813b-02fdf6014271)_human();
```
During this roll call `fred` would have learnt and remembered `map1` and `turtle1` and conversely  `map1` and `turtle1` now know of the existence of `fred`.
## Adding attributes
Any `human` and `thing` can have attributes
```diego
with_human(fred)_attr(favourite_colour, blue);
```
, or…
| Command | Result |
|:--|:--|
| `with_human(fred)_attr()_config(json, "{"favourite_colour":"blue"}");` | Adds attribute '*favourite_colour*' as '*blue*' to `human` `fred` using JSON string. |
| `with_human(fred)_attr()_config(json, /attr/fred/attr.json);` | Adds attribute(s) to `human` `fred` from  JSON file `/attr/fred/attr.json`. |
| `with_human(fred)_attr()_config(yaml, "favourite_colour: blue");` | Adds attribute '*favourite_colour*' as '*blue*' to `human` `fred` using YAML string. |
| `with_human(fred)_attr()_config(yaml, /attr/fred/attr.yaml);` | Adds attribute(s) to `human` `fred` from  YAML file `/attr/fred/attr.yaml`. |


```diego
add_zone(blue_zone)_map(map1)_bound(box, 2.3, 2.3, 6.8, 6.8)_colour(blue);
add_zone(red_zone)_map(map1)_bound(box 12.3, 2.3, 16.8, 6.8)_colour(red);
```
```diego
[diego]: add_zone(blue_zone, eb43a636-99ec-4b08-b360-62227d236609)_map(map1)_bound(box, 2.3, 2.3, 6.8, 6.8)_colour(blue);
           add_zone(red_zone, 9b135d40-733d-4160-9ad6-298749b4a4a0)_map(map1)_bound(box 12.3, 2.3, 16.8, 6.8)_colour(red);
```




```diego
begin_instruct(move_to_colour_zone_on_whistle);
  listen_event(whistle) ? start_instruct(move_to_colour_zone)_thing();
end_instruct(move_to_colour_zone_on_whistle);

begin_instruct(move_to_colour_zone)
  with_thing()_attr(favourite_colour)_value(blue) ? label_thing(blueie);
  with_thing()_attr(favourite_colour)_value(red) ? label_thing(redie);
  with_thing(blueie) ? go_zone(blue_zone);
  with_thing(redie) ? go_zone(red_zone);
  with_thing(blueie)_zone(blue_zone) ? alert_world(at_blue_zone);
   ? alert_world(at_red_zone);
end_instruct(move_to_colour_zone);

start_instruct(move_to_colour_zone_on_whistle);
```
At this point we have written two `instruct`s, or two '*small programs*', that will be executed on the *`whistle`* `event`.  We could go ahead and trigger these two `instruct`s with the *`whistle`* `event`, but we will test our `instruct`s first.

At the **Scope:** drop-down, select `[test]`.  Now let's test this by '*blowing the whistle*', so enter (with scope at `[test]`):
```diego
call_event(whistle);
```
The console will should similar:
```diego
[test]: call_event(whistle);
[turtle1]:
listen_event(whistle);
  start_instruct(move_to_colour_zone)_thing(); 
[turtle2]:
listen_event(whistle);
  start_instruct(move_to_colour_zone)_thing(); 
[map1]: listen_event(whistle);
[move_to_colour_zone_on_whistle]: listen_event(whistle);
[blue_zone]: listen_event(whistle);
[red_zone]: listen_event(whistle);
…
```
Straight away the test view shows that all `thing`s are listening for *`whistle`* `event`, yet for this case we only need `thing`s (actually `simulat`*[tion]*s) to listen for the *`whistle`* `event`.
```deigo
begin_instruct(move_to_colour_zone_on_whistle);
  listen_event(whistle)_of(simulat) ? start_instruct(move_to_colour_zone)_of(simulat);
end_instruct(move_to_colour_zone_on_whistle);

begin_instruct(move_to_colour_zone);
  with_simulat()_attr(favourite_colour)_value(blue) ? label_simulat(blueie);
  with_simulat()_attr(favourite_colour)_value(red) ? label_simulat(redie);
  with_simulat(blueie) ? go_zone(blue_zone);
  with_simulat(redie) ? go_zone(red_zone);
  with_simulat(blueie)_zone(blue_zone) ? alert_world(at_blue_zone);
  with_simulat(redie)_zone(red_zone) ? alert_world(bubble)_msg("At Red Zone!");
end_instruct(move_to_colour_zone);

start_instruct(move_to_colour_zone_on_whistle)_simulat()_map(map1);
```

```diego
[diego]: call_event(whistle);
turtle1: listen_event(whistle)_simulat();
           start_instruct(move_to_colour_zone)_simulat(); 
turtle2: listen_event(whistle)_simulat();
           start_instruct(move_to_colour_zone)_simulat();
turtle1: with_simulat()_attr(favourite_colour)_value(blue);
          label_simulat(blueie);
turtle2: with_simulat()_attr(favourite_colour)_value(red);
          label_simulat(redie);
turtle3: with_simulat()_attr(favourite_colour)_value(red);
          label_simulat(redie);
turtle1: with_simulat(blueie);
	  go_zone(blue_zone);
turtle2: with_simulat(redie);
           go_zone(red_zone);
turtle3: with_simulat(redie);
           go_zone(red_zone);
turtle1: with_simulat(blueie)_zone(blue_zone)
           alert_world(at_blue_zone);
turtle2: with_simulat(redie)_zone(red_zone)
           alert_world(bubble)_msg("At Red Zone!");
turtle3: with_simulat(redie)_zone(red_zone)
           alert_world(bubble)_msg("At Red Zone!");
```

```diego
with_simulat(redie) ? go_zone(red_zone);
```

```deigo
[diego]: with_simulat(redie) ? go_zone(red_zone);
turtle2: go_zone(red_zone);
turtle3: go_zone(red_zone);
```

```deigo
[diego]: with_simulat(redie);
turtle2: with_simulat(turtle2)_label(redie);
turtle3: with_simulat(turtle3)_label(redie);
```

```deigo
[diego]: go_zone(red_zone);
turtle1: go_zone(red_zone);
turtle2: go_zone(red_zone);
turtle3: go_zone(red_zone);
map1: go_zone(red_zone);
move_to_colour_zone_on_whistle: go_zone(red_zone);
move_to_colour_zone: go_zone(red_zone);
blue_zone: go_zone(red_zone);
red_zone: go_zone(red_zone);
```
The command `go_zone(red_zone)` is indiscriminate so it will can change the world indiscriminately.  This effect is not what is intended, then …
… however all instructs by default have `set_go(false)`, so they will not react to the `go_` verb.  Other `things`, such as `zone`s are defaulted to `set_go(false)`, however, you may wish a zone to move to a new location on the map, so to 	`set_go` pm all `zones` use any of the following:

```diego
[diego]: set_go(true)_to(zone);
[diego]: set_go()_to(zone);
[diego]: with_zone()_set(go, true);  # depreciated in version 1.1.
```
To `set_go` on a specific `zone` use any of the following (target zone: `zone_x`):
```diego
[diego]: set_go(true)_for(zone_x);
[diego]: set_go()_for(zone_x);
[diego]: with_zone(zone_x)_set(go, true);  # depreciated in version 1.1.
zone_x: set_go(true);
zone_x: set_go();
zone_x: with_me()_set(go, false);  # depreciated in version 1.1.
zone_x: with_me(zone_x)_set(go, false);  # depreciated in version 1.1.


```
zone_n: set_go(false)
```



Every `thing`, that received and remembered the `move_to_colour_zone_on_whistle` `instruct`, will be listening to a `whistle` `event` and will start `instruct`  `move_to_colour_zone`.  The `move_to_colour_zone` `instruct` (itself a meta-`thing`) will request `with_thing()_attr(favourite_colour)_value(blue)` to the _puff_, requesting all `things` with `attr`[*ibute*] of `favourite_colour` as `blue`.  In addition of a response to the _puff_ the `move_to_colour_zone` `instruct` instructs these `thing`s to `label_thing(blueie)` _ label themselves `blueie`s.

A similar instruction to `blueie`s is given for `redie`s.  Then `move_to_colour_zone` `instruct`

```diego
[deigo]: call_event(whistle);
turtle1:
listen_event(whistle);
  start_instruct(move_to_colour_zone)_thing(); 
turtle2:
listen_event(whistle);
  start_instruct(move_to_colour_zone)_thing(); 
map1: listen_event(whistle);
move_to_colour_zone_on_whistle: listen_event(whistle);
blue_zone: listen_event(whistle);
red_zone: listen_event(whistle);






```
```
  listen_event(whistle) ? start_instruct(move_to_colour_zone);
end_instruct(move_to_colour_zone_on_whistle);

begin_instruct(move_to_colour_zone)
```
 ? label_thing(blueie);
  
  label_thing(blueie) ? 
  label_thing(redie) ? with_thing(redie)_gozone(red_zone);
  
[diego]: rollcall_thing()_attr(favourite_colour)_value(blue);
turtle1: with_me(turtle1)_attr(favourite_colour)_value(blue);

[diego]: with_thing()_attr(favourite_colour)_value(blue);
turtle1: with_thing(turtle1)_attr(favourite_colour)_value(blue);

[diego]: with_simulat()_attr(favourite_colour)_value(blue);
turtle1: with_simulat(turtle1)_attr(favourite_colour)_value(blue);

[diego]: with_thing()_attr(favourite_colour)_value(blue) ? label_thing(blueie);
turtle1: with_thing(turtle1)_label(blueie);

[diego]: with_thing(blueie)_gozone(blue_zone);
turtle1: with_label(blueie)_gozone(blue_zone);

[diego]: with_thing(blueie)_gozone(blue_zone) ? alert_world(at_blue_zone);
turtle1: with_label(blueie)_gozone(blue_zone);
turtle1: alert_world(at_blue_zone);







  
  
```

favourite_color: blue

`with_thing()_transcript();`

`with_simulat(turtle1)_transcript();`
```diego
[diego]: with_simulat(turtle1)_transcript();
turtle1: 2020-11-28-18:59.374534 [deigo]: rollcall();
           2020-11-28-18:59.548992 turtle1: with_me(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8)_thing(meta)_type(sim);
           2020-11-28-18:59.558992 map1: with_me(map1, 4d20e7d3-1c89-44c6-bd31-0f353090d6e4)_thing(meta)_type(map);
…
```
`with_simulat(turtle1)_journal();`
```diego
[diego]: with_simulat(turtle1)_transcript();
turtle1: 2020-11-28-18:59.374534 [deigo]: rollcall();
           2020-11-28-18:59.548992 turtle1: with_me(turtle1, bdc09e2f-5a26-4e55-9ca2-ab6ea297a0b8)_thing(meta)_type(sim);
…
```
Journal - only diego messages that relate to the thing
Transcript - all diego messages

| Command Recipe | Description |
|---|---|
| `ask_transcript()` | Requests the transcript (for `get_transcript` time period) for all in the _puff_. |
| `ask_transcript()_me()` | Requests the transcript (for `get_transcript` time period) for the `thing`. |
| `get_transcript(`*`hours`*`)`<br>`get_transcript(`*`hours`*`, `*`mins`*`)`<br>`get_transcript(`*`hours`*`, `*`mins`*`, `*`secs`*`)` | Returns transcript recall time period (in hours) when `ask_transcript` command is executed. |
| `ask_transcript()_for(`*`thing_moniker1`*`, `*`thing_moniker2`*`, `*`n…`*`)` | Returns the transcript (for `get_transcript` time period) of *`thing_moniker1`*, *`thing_moniker2`*, *`n…`*. |
| `ask_transcript()_to(`*`thingy1`*`, `*`thingy2`*`, `*`n…`*`)` | Returns the transcript (for `get_transcript` time period) of `thing`s of type (_thingy_) *`thingy1`*, *`thingy2`*, *`n…`*. |
| `ask_transcript(`*`datetime_from`*`, `*`datetime_to`*`)` | Returns transcript of  |

recall_journal()


`ask_thing(`*`thing_moniker`*`)`


`ask_thing(`*`thing_moniker`*`)`

with_thing(












`_ident(`*`make_manufacturer`*`, `*`model`*`, `*`badge_trim`*`)`
`_serial(`*`serial_number`*`)`
Request:
```diego
with_robot(alpha);
```
Reply:
```diego
with_robot(alpha, 456f3-6fg-273-83hg46s);
```

Request:
```diego
with_mech(alpha);
```
Reply:
```diego
with_mech(alpha);
```

Request:
```diego
with_robot(alpha)_ident();
```
Reply:
```diego
with_robot(alpha)_ident(ROBOTIS, turtlebot3, burger);
```



Now the *robot* has the bare minimum to join the world of other robots, so set your




begin_instruct(go_diego);
  # Identity:
  with_me()_moniker(alpha, 456f3-6fg-273-83hg46s);
  with_me()_thing(robot);
  with_me()_ident(ROBOTIS, turtlebot3, burger);
  
  # Listeners:
  listen_point();
  listen_map();
end_instruct(go_diego);

start_instruct(go_diego);

  
  
  set_map()_last() : alert_human()


  alert_human(finding map);
  listen_map() ? alert_human(found map);
  
  alert_human(pos);
  listen_pos() ? alert_human(found pos);
  listen_orient() ? alert_human(found orient);

end_instruct(go_diego);

start_instruct(go_diego);




begin_instruct(diego_ready);
  listen_alert();
  alert_world(ready);
  alert_human(ready);
  listen_alert(full_aisle_scan) ? start_instruct(full_aisle_scan)

  learn_aisle();
end_instruct(go_diego);

begin_instruyc

detect_aisle()




ROS2

/Register

moniker:
uuid:
thing:
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA0NzA0MDE2NV19
-->