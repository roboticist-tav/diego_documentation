# Waypoint
The `waypoint` object is a representation of an intermediate physical point or place on a map, place on a path, or route, or line of travel, or simply, a stopping point. `Waypoint`s contain, at least, a moniker, and, coordinates corresponding to a `map` object, whether in the form `x, y`, or form `latitude, longitude` for two dimensional coordinates, or an addition `z, altitude` property for three dimensional coordinates.

A `waypoint` is at the lowest hierarchical level of the 'Route Matrix', being similar to a `pose` (sometimes called `posepoint`) and a `goal`. Whereas, a `waypoint` is a point with location, `pose` is a point with location and orientation, then a `goal` is a point with location, orientation, and, timed elements.  This is depicted in the 'Route Matrix'.

| ![Route Matrix](/_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

In the family of 'location-only' based navigation objects, one `itinerary` has many `route`s, one `route` has many `path`s, and, one `path` has many `waypoint`s.

## Declaration & Assignment
The default declaration of the `waypoint` object is to at least provide a *moniker*, however, at declaration it is common to provide a location using the `_coords` posit. The parameters of `_coords` are numeric, when not specified they will be implied to be `{double}`. Providing `x_lat` and `y_long` only implies a two-dimensional waypoint, and adding the `z_alt` parameter implies a three-dimensional waypoint. `waypoint` can be shortened to `wp`, both terms are syntactically the same and can be used freely and interchangabily. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_waypoint(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_waypoint(`*`moniker1`*`, `*`moniker2`*`,…);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_wp(`*`moniker`*`)_coords(`*`x_lat`*`, `*`y_long`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_waypoint(`*`moniker`*`)_coords(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`);`

## Referencing & Assignment
Referencing a `waypoint` is achieved with the `with` verb, or the shortened `(`*`moniker`*`)` syntax. The `with_waypoint` (or shortened `with_wp`) command can be expanded to create multiple `waypoint`s using a coma-spearated list of *`moniker`* s and mutliple `_coords` posits. The position in the *`moniker`* list corresponds to the same order of appended `_coords` posits. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_waypoint(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` with_wp(`*`moniker1`*`, `*`moniker2`*`,…)_coords(`*`x_lat1`*`, `*`y_long1`*`)_coords(`*`x_lat2`*`, `*`y_long2`*`)…`

For easy of reading for humans, either a `beginwith … endwith` syntax, or a nested statement approach can be taken.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `beginwith_waypoint(`*`moniker1`*`, `*`moniker2`*`,…);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker1`*`)_coords(`*`x_lat1`*`, `*`y_long1`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker2`*`)_coords(`*`x_lat1`*`, `*`y_long1`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `endwith_wp();`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp(`*`moniker1`*`, `*`moniker2`*`,…)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker1`*`)_coords(`*`x_lat1`*`, `*`y_long1`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker2`*`)_coords(`*`x_lat1`*`, `*`y_long1`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `;`

## Casting
Casting to `waypoint`s sibling, `pose` and `goal`, is the safest and most commonly used cast of `waypoint`, as they are related.  There are also two cousins of `waypoint`, `landmark` and `poi`, which can be safely cast into. Casting can be achieved by specifing the datatype using curly brackets (`{}`), or with the `with` verb.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp({pose},`*`waypointpmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_pose(`*`waypointmoniker`*`);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp({goal},`*`waypointpmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_goal(`*`waypointmoniker`*`);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp({pose},`*`waypointpmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_landmark(`*`waypointmoniker`*`);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp({goal},`*`waypointpmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_poi(`*`waypointmoniker`*`);`<br>

Since `pose`, `goal`, `landmark`, and, `poi` are closely related, any extra circiculum posit will automatically imply the object has been recast. The *moniker* of the _cast-from_ *object* will be given to the  _cast-to_ *object*, the moniker of the _cast-from_ *object* will then be empty (unnamed). For example:
```diego
add_wp(point1)_coords(4,2,8);
log_console()_typeof(point1);   // {waypoint}

with_wp(point1)_orientat(0.229,-0.246,-0.785,-0.520);
log_console([]: [])_nameof()_typeof(point1);        // point1: {pose}
log_console([]: [])_nameof()_typeof(point1)_wp();   // : {waypoint}
```

## Referencing
Referencing the `waypoint` obejct can be achieved in the usual way with the `with_` verb.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`with_waypoint(`*`moniker`*`)_…`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`with_wp(`*`moniker`*`)_…`

## Similar Objects

The objects `pose` and `goal` are sibling objects in the route matrix, and behave in a similar way to the `waypoint`.  The only difference is `pose` also includes orientation, whereas `waypoint` does not, and `goal` includes orientetion and time which `waypoint` does not.

Two other objects, `landmark` and `poi` are use in the same manner as `waypoint` but are used in a specific way.

## Verbs
| verb | description | API |
| --- | -------- | --- |
| <a name="add"></a> `add_`*`<waypoint>`* | Declaration of *<waypoint>* *object* | [add](../../abstract/verb/add.md) |
| <a name="go"></a> `go_`*`<waypoint>`*<br>`goto_`*`<waypoint>`* | The proceeding *object* will go to the waypoint *<waypoint>* | [go](../verb/go.md#waypoint) |
| <a name="with"></a> `with_`*`<waypoint>`*<br>`(`*`wpmoniker`*`)` | Referencing *<waypoint>* *object* | [with](../../abstract/verb/with.md) |


## Posits
| posit | description | API |
| --- | -------- | --- |
| <a name="parse"></a> `_parse()`<br>`_parse(`*`string`*`)`<br>`_parse({lang},`*`string`*`)` | Parses proceeding *object*<br>Parses the *string* and determines language<br>Parses *string* following language *lang* | [parse](../funct/parse.md#waypoint) |
| <a name="coords_a"></a> `_coords()`<br>`_coords_(`*`x_lat1`*`, `*`y_long1`*`)`<br>`_coords_(`*`x_lat1`*`, `*`y_long1`*`, `*`z_alt`*`)` | Provides coordinates from proceeding *object*<br>Provides two-dimensional coordinates of `x_lat1`,`y_long1`<br>*Provides three-dimensional coordinates of `x_lat1`,`y_long1`,`z_alt` | [coords](../obj/coords.md#waypoint) |
| <a name="geojson"></a> `_geojson(`*`geojsonstring`*`)` | Direct parse of geoJSON `geojsonstring`| [geojson](../funct/geojson.md) |
| <a name="shapefile"></a> `_shapefile(`*`shapefilestring`*`)` | Direct parse of Shapefile `shapefilestring`| [shapefile](../funct/shapefile.md) |
| <a name="kml"></a> `_kml(`*`kmlstring`*`)` | Direct parse of KML `kmlstring`| [kml](../funct/kml.md) |
| <a name="displacemto"></a> `_displacemto(`*`tomoniker`*`)`<br>`_displacemto([`*`variablename`*`])`<br>`_displacemto(❬`*`unit`*`❭,`*`tomoniker`*`)` | Provides the displacement from preceeding *object* to *tomoniker* *object*<br>Provides the displacement from preceeding *object* to *object* monikered to the value of *variablename*<br>Provides the displacement from preceeding *object* to *tomoniker* *object* with specified unit | [displacem](./displacem.md) |
| <a name="around"></a> `_around()` | Reference to a [`zone`](./zone.md) of preceeding *object* defined by proceeding *object* | [around](../condit/around.md) |
| <a name="coords_b"></a> `_x()`, `_x(`*`x`*`)`<br>`_y()`, `_y(`*`y`*`)`<br>`_z()`, `_z(`*`z`*`)` | Gets and sets the x, y, and z coordinates, repsectively| [xyz](../../abstract/funct/xyz.md) |
| <a name="coords_c"></a> `_lat()`, `_lat(`*`lat`*`)`<br>`_lng()`, `_lng(`*`lng`*`)`<br>`_alt()`, `_alt(`*`alt`*`)` | Gets and sets the x, y, and z coordinates (repsectively) of the preceeding *object* | [xyz](../funct/latlngalt.md) |
| <a name="elevation"></a> `_elev()`<br>`_elevation(`*`elev`*`)` | Gets and sets the elevation of the preceeding *object* | [elev](../funct/elev.md) |
| <a name="waitat"></a> `_waitat()`<br>`_waitat(`*`wpmoniker`*`)` | Wait at proceeding *object*<br>Wait at waypoint *wpmoniker* | [waitat](../funct/waitat.md) |
| <a name="loiterat"></a> `_loiterat()`<br>`_loiterat(`*`wpmoniker`*`)` | Loiter at proceeding *object*<br>Loiter at waypoint *wpmoniker*  | [loiterat](../funct/loiterat.md) |

---
## References

* [`pose`](./pose.md); [`goal`](./goal.md)