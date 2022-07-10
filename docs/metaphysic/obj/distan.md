# Distance (object)
Distance is the scalar quantity of the total length travelled by an *object* from one *point* to another.  In abstract ***Diego*** the *points* will be [`point`](/abstract/obj/point.md), in metaphysical ***Diego*** *points* will be either [`waypoint`](/metaphysic/obj/waypoint.md), [`pose`](/metaphysic/obj/pose.md), or, [`goal`](/metaphysic/obj/goal.md). In physical ***Diego*** *points* will be [`landmark`](/physic/obj/landmark.md) or [`poi`](/physic/obj/poi.md).

Distance can be represented as both an object and a [property](/metaphysic/prop/distan.md).

For a vector quantity for the distance from one *point* to another, refer to [`displacem`](displacem.md).

| ![Distance vs. Displacement](/_img/Distancedisplacement.svg "Distance vs. Displacement") |
| :---: |
| *Distance vs. Displacement*<br/><sub>Credits: <a href="https://commons.wikimedia.org/wiki/File:Distancedisplacement.svg">Stannered</a>, <a href="http://creativecommons.org/licenses/by-sa/3.0/">CC BY-SA 3.0</a>, via Wikimedia Commons</sub> |

## Syntax
The default declaration syntax, for the `distan` object, is to provide at least a *moniker*. The lengthened version of `distance` can also be used:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_distan(`*`moniker`*`);`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_distance(`*`moniker`*`);`

The distance *object* can be attached to a preceeding *object*, or many preceeding *objects* by just appending the `distan` *object* as it child.  For example:
```diego
add_distan(a-to-z-distance)_value({km},4.2);

add_route(a-to-z)_distance(a-to-z-distance);

log_console()_distan(a-to-z-distance);    // 4.2km
```

In addition to a direct declaration, the `distan` *object* can be declared from the *moniker* of another *object*, if that *object* used a [`distan`](/metaphysic/prop/distan.md) *property*. The *object-type* is implied or can be provided (or cast):

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_distan(`*`ofmoniker`*`);`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_distance(`*`ofmoniker`*`);`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_distance({`*`objtype`*`},`*`ofmoniker`*`);`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_distance({`*`objtype`*`},`*`ofmoniker`*`);`

For example:
```diego
add_route(a-to-b)_distance({m},34.2);
add_route(b-to-c);

log_console()_distan(a-to-b);    // 34.2m

log_console()_distan({route},b-to-c);    // no distan defined
// callee will return with_log()_distan({route},b-to-c)_err(no distan defined);
```
