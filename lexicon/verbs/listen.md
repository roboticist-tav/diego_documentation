## listen_robot(*robot_moniker*)


# Listeners
Listener commands instruct the robot to 'listen out' for a type of object that match specific criteria and then trigger the _hey_diego_ event.  Listener commands can have an _oh_diego_ command which is triggered (the _oh_diego_ event) when the cursor (focus) leaves an ``instruct`` without any _hey_diego_ event triggered.

All listener commands 'leak', meaning that the _hey_diego_ and _oh_diego_ events are disassociated to the listener command.  To prevent the leakage seeping into the rest of your instructions use the listener keep command ``keep_listening()``.

## listen_point
Listens for a point  from ``call_point`` with matching *```point_moniker```*; ``call_point`` matching a _focal(s)_ (``_around``, ``_in``, ``_within``) with/without a matching *```point_moniker```*; ``found_point`` matching a _focal(s)_ (``_around``, ``_in``, ``_within``) with/without a matching *```point_moniker```*; and, ``at_point`` matching a _focal(s)_ (``_around``, ``_in``, ``_within``) with/without a matching *```point_moniker```*
### Linking & Events
| | do_diego | hey_diego | oh_diego |
|--|:--:|:--:|:--:|
| events: | ``keep_listening`` |  ``call_point``<br>``found_point``<br>``detect_point``<br>*matching criteria* | *non-event leaving the ``instruct``* |
| cmds: | ``listen_point`` | ✅ required | ✅ optional |
The _go_diego_ event of the ```listen_point``` command begins on a matching _call_ ( ```call_point(```*```point_moniker```*```)```*```...```*); _find_ ```fall_point(```*```point_moniker```*```)```*```...```*).  There is no _nogo_diego_ event.
### Commands
There are only two ``listen_point`` commands: parameter-less (``listen_point()``) and using the *``point_moniker``* parameter ( ``listen_point(``*``point_moniker``*``)``).
#### listen_point()
The robot will remember a _listener_ for any point and update/add the point in its world memory.

The ``listen_point()`` command with no _focal sub commands_ is redundant, since the default is for a _diego_ to always listen for all points. However using `listen_point()` with a _focal sub command_ may be required in certain scenarios, such as, a '*discover-then-detect*' scenario.

When a ``listen_point()`` command with matching _focal sub commands_ is triggered, the point will be updated/added to the robot's world memory, even if the _point_moniker_ is unknown.  An unknown point_moniker will be given a temporary moniker by the robot.  A robot can use ``sync_point`` to collaborate with other robots/humans on the correct _point_moniker_.
#### listen_point(*point_moniker*)
The robot will remember a _listener_ for the *point_moniker*, and add the *point_moniker* as a _point_ in its world memory.  The robot will listen only for the lifetime of the ```instruct``` or if the command ```deafon_point(```*```point_moniker```*```)```  is instructed.  If the robot, leaves and then returns to the ```instruct```, the _listener_ will automatically be re-established.


### Sub Commands
The  ``listen_point()`` and ``listen_point(``*``point_moniker``*``)``commands have two categories of sub commands: _zonals_, which provide criteria for a match for a zonal as a shape (``_around``, ``_in``) or as an ploygon/area (``_within``); and _privileges_ (``_for`` and ``_not``). 
#### _around(*circle_moniker*)
A _zonal sub command_ using a known circle of *circle_moniker* (_zone_ of _circle_ type) as criteria for matching the *point_moniker* or any point's position ( *x_lat*, *y_lat*) on the x-y plane only (2D) against the encompassing ( *x_lat*, *y_lat*) of the  *circle_moniker* circle.  The circle can be: pre-defined in _zones_ of _circle_ type in _diego declarations_; or in executed in code using ``call_zone(``*``zone_moniker``*``, circle)_at``*``...``*.
#### _around(*map*, *x_lat*, *y_lat*, *radius*)
A _zonal sub command_ using a defined circle on map *``map``* at position *``x_lat``*, *``y_lat``* with radius *``radius``* as criteria for matching the *point_moniker* or any point's position ( *x_lat*, *y_lat*) on the x-y plane only (2D) against the positions ( *x_lat*, *y_lat*) of the  *circle_moniker* circle.
#### _around(*ring_moniker*)
A _zonal sub command_ using a known ring of *ring_moniker* (_zone_ of _ring_ type) as criteria for matching the *point_moniker* or any point's position ( *x_lat*, *y_lat*) on the x-y plane only (2D) against the encompassing ( *x_lat*, *y_lat*) of the  *ring_moniker* ring.  The ring can be: pre-defined in _zones_ of _ring_ type in _diego declarations_; or in executed in code using ``call_zone(``*``zone_moniker``*``, ring)_at``*``...``*.
#### _around(*map*, *x_lat*, *y_lat*, *z_alt*, *minor_radius*, *major_radius*)
A _zonal sub command_ using a defined ring on map *``map``* at position *``x_lat``*, *``y_lat``* with minor radius *``minor_radius``* and major radius *``major_radius``* as criteria for matching the *point_moniker* or any point's position ( *x_lat*, *y_lat*) on the x-y plane only (2D) against the positions ( *x_lat*, *y_lat*) of the  *ring_moniker* ring.
#### _around(*sphere_moniker*)
A _zonal sub command_ using a known sphere of *sphere_moniker* (_zone_ of _sphere_ type) as criteria for matching the *point_moniker* or any point's position ( *x_lat*, *y_lat*, *z_alt*) in 3D against the encompassing ( *x_lat*, *y_lat*, *z_lat*) of the  *sphere_moniker* sphere.  The sphere can be: pre-defined in _zones_ of _sphere_ type in _diego declarations_; or in executed in code using ``call_zone(``*``zone_moniker``*``, sphere)_at``*``...``*.
#### _around(*map*, *x_lat1*, *y_lat1*, *z_alt1*, *x_lat2*, *y_lat2*, *z_alt2*, *radius*)
A _zonal sub command_ using a defined circle on map *``map``* at position *``x_lat``*, *``y_lat``* with radius *``radius``* as criteria for matching the *point_moniker* or any point's position ( *x_lat*, *y_lat*) on the x-y plane only (2D) against the positions ( *x_lat*, *y_lat*) of the  *circle_moniker* circle.
#### _around(*torus_moniker*)
#### _around(*map*, *x_lat1*, *y_lat1*, *z_alt1*, *x_lat2*, *y_lat2*, *z_alt2*, *minor_radius*, *major_radius*, *roll*, *pitch*, *yaw*)
### Zonal (_in)
#### listen_point(*point_moniker*)_in(*rect_moniker*)
#### listen_point(*point_moniker*)_in(*map*, *x_lat1*, *y_lat1*, *z_alt1*, *x_lat2*, *y_lat2*, *z_alt2*, *x_lat3*, *y_lat3*, *z_alt3*)
#### listen_point(*point_moniker*)_in(*cubeoid_moniker*)
#### listen_point(*point_moniker*)_in(*map*, *x_lat1*, *y_lat1*, *z_alt1*, *x_lat2*, *y_lat2*, *z_alt2*, *x_lat3*, *y_lat3*, *z_alt3*)
### Zonal (_within)
#### listen_point(*point_moniker*)_within(*zone_moniker*)
### Privileges
#### listen_point(*point_moniker*)*[...]*_for(*moniker1*, *n...*)
A whitelist (*moniker1*, *n...*) of robots (and/or robots with labels) that should listen for the *point_moniker*.
#### listen_point(*point_moniker*)*[...]*_not((*moniker1*, *n...*)
A blacklist (*moniker1*, *n...*) of robots (and/or robots with labels) that are denied to listen for the *point_moniker*.
## listen_geofence


## listen_formation(*formation_moniker*)
## listen_robot
## listen_human
## listen_route
## listen_swarm(*swarm_moniker*)

## call_point(*point_moniker*)
#### call_point(*point_moniker*)
#### call_point(*point_moniker*)_at(*map*, *x_lat*, *y_long*, *z_alt*)
#### call_point(*point_moniker*)_at(*map_type*, *x_lat*, *y_long*, *z_alt*)
#### call_point(*point_moniker*)*[...]*_for(*moniker1*, *n...*)
#### call_point(*point_moniker*)*[...]*_not(*moniker1*, *n...*)

rallying point)_at(```*```map```*```, ```*```x```*```, ```*```y```*```, ```*```z```*```)```. When matched save point coordinates in memory, then run ```poll_distance(rallying point, unanimous__by(direct);```.

```diego

  poll_distance(intruder)_getrank(1) ? add_label(2nd);
  poll_distance(intruder)_getrank(2) ? add_label(2nd);
  
```



## listen_point(sentry point)
 Each robot will check all 'calls' for ```call_point(sentry point)_at(```*```map```*```, ```*```x```*```, ```*```y```*```, ```*```z```*```)```. When matched each robot will save the point coordinates, and then run ```go_point(sentry point)```.

## keep_listening()
### keep_listening()
All robots will not move pass this command until a ```listen``` command is run and matched.

