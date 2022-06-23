# waypoint

The `waypoint` object is representation of an intermediate physical point or place on a route or line of travel, or simply, a stopping point. `Waypoint`s contain, at least, coordinates corresponding to a `map` object, whether in the form `x, y`, or form `latitude, longitude` for two dimensional coordinates, or an addition `z, altitude` value for three dimensional coordinates.

A `waypoint` is at the lowest hierarchical level of the 'Route Matrix', being similar to a `pose` (sometimes called `posepoint`) and a `goal`. Where a `waypoint` is a point with location, `pose` is a point with location and orientation, then a `goal` is a point with location, orientation, and, timed element.

| ![Route Matrix](route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

In the family of 'location-only' based navigation objects, one `itinerary` has many `route`s, one `route` has many `path`s, and, one `path` has many `waypoint`s.

## Creation Syntax

The common syntax for `waypoint` creation is...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`moniker|uuid`*`)_coords(`*`x_lat`*`, `*`y_long`*`);`

...for a single 2-dimensional `waypoint`., and...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`moniker|uuid`*`)_coords(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`);`

...for a single 3-dimensional `waypoint`.

This command can be expanded to create multiple `waypoint`s using a coma-spearated list of *`moniker|uuid`*s and mutliple `_coords` postposits, following the syntax...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`moniker1|uuid1`*`, `*`moniker2|uuid2`*`,...)_coords(`*`x_lat`*`, `*`y_long`*`)_coords(`*`x_lat`*`, `*`y_long`*`)...`

The position in the *`moniker|uuid`* list correcsponds to the same order of appended `_coords` postposits.

Note, the verbs `begin_`, `end_` are compatible with the `waypoint` object, to provide embedded functionality

***Diego*** allows for other apporaches for creating/loading mutilple `waypoint`s, such as...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`[moniker]`*`)_format(`*`format`*`)_json([{`*`x_lat`*`, `*`y_long`*`)}, {`*`x_lat`*`, `*`y_long`*`)}, ...])`

...creates miltilple `waypoints` from a literal json string.  The waypoint monikers are created in seqence using a combination of a _(base)-_*`moniker`* and a specified `format`.  To load `waypoints`, either from a file...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint()_load(`*`file_url`*`, `*`file_format`*`, `*`protocol`*`)`

...or using programming logic from an array (for instance)...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint()_load()_array(`*`moniker|uuid`*`);`

...or from a json string...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint()_load()_json(`*`moniker|uuid`*`);`

## Reference Syntax

Referencing the `waypoint` obejct can be achieved in the usual way with the `with_` verb...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`with_waypoint(`*`moniker|uuid`*`)_...`



```diego
add_waypoint({moniker|uuid})_coords({x_lat}, {y_long});		\\ 2-dimensional
add_waypoint({moniker|uuid})_coords({x_lat}, {y_long}, {z_alt});	\\ 3-dimensional
```




## Similar Objects

```Diego
pose
goal
landmark
poi
```

## Valid Verbs

```Diego
go_
nav_
```

## Valid Children

```Diego
_goal
_waypoint
_poi
```

## Valid Postposits

### Attributes
```Diego
_valid({valid_from_datetime}[, {valid_to_datetime}])
_abstract()
_aviat()
_aviat({aviat_moniker})
_type({2d|3d)
_coords({x_lat}, {y_long})
_coords({x_lat}, {y_long}, {z_alt})
_x({x})
_y({y})
_z({z})
_lat({lat})
_long({long})
_alt({alt})
_elevation({elevation})
_swapfrom({variable_list})_swapto({variable_list})
```

### Postverbs

```Diego
_waitat()
_waitat({waypoint_moniker|waypoint_uuid})
```

### Results

```Diego
_log()
_log()_forwho({moniker|uuid})
_log()_forwhen({valid_from_datetime}[, {valid_to_datetime}])
_log()_foraround({datetime})

```



---------------------
goal

```Diego
_navresult({0|1|2|3})
_navresult({unknown|succeeded|canceled|failed})
```