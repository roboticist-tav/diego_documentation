# Pose (object)
The `pose` object is a representation of an orientation at a physical point. `Pose`s require a moniker; a current position (i.e. a waypoint); and an orientation coorespondence to their waypoint. The can be referred to their extended syntax, `posepoint`.

The `pose` is at the lowest hierarchical level of the 'Route Matrix', being similar to a `waypoint`  and a `goal`.

| ![Route Matrix](/_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

In the family of 'location-and-orientation' based navigation objects, one `excurs` has many `course`s, one `course` has many `way`s, and, one `way` has many `poses`s. `pose` can be extended to `posepoint`, both terms are syntactically the same and can be used freely and interchangabily. 

## Declaration
The default declaration of the `pose` object is to at least provide a *moniker*, however, at declaration it is common to provide a orientation using the `_orientat` posit. The `_orientat` has two signatures, one accepts Euler angles, the other accepts quaternions.  The Euler angles can be provided in radians or decimal degrees, so the thingies need to come to an agreement.  The units can be set at declaration using angle brackets or wider scoped using `set_angles(`*`angleunit`*`)`.  The order of Euler angles and quaternion paramaters can also be set at declartion or with the setters, `set_euler(`*`order`*`)` and `set_quatern(`*`order`*`)`, or directly in the declarations using curly brackets.

| ![Orientation](/_img/orientat.png "Orientation") |
| :---: |
| *Orientation* |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_posepoint(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker1`*`, `*`moniker2`*`,...);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat({`*`order`*`},`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(❬`*`unit`*`❭`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat({`*`order`*`},❬`*`unit`*`❭`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`)_euler(`*`order`*`)_angles(`*`unit`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)_quatern(`*`order`*`)_angles(`*`unit`*`);`

A orientation can also be declared using the `euler` or `quaternion` objects.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_euler(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_euler(`*`x`*`,`*`y`*`,`*`z`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_quatern(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_quatern(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`

## Declaration & Assignment
A `pose` is not complete unless it has a `waypoint` child or a declared waypoint child using the `_coords` posit. The parameters of `_coords`, `x_lat`, `y_long`, and, `z_alt`, all numeric.  When datatype of the `_coords` parameter are not specified, they will be implied to be `{double}`. Alternatively a previous waypoint can be appended or cast from.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)_coords(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` with_pose(`*`moniker`*`)_coords(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` with_pose(`*`posemoniker`*`)_waypoint(`*`waypointmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` with_pose(`*`moniker`*`)_wp([`*`variablename`*`);`

## Referencing & Assignment
Referencing a `pose` is achieved with the `with` verb, or the shortened `(`*`moniker`*`)` syntax. The `with_pose` (or expanded `with_posepoint`) command can be expanded to create multiple `poses`s using a coma-spearated list of *`moniker`* s and mutliple `_orientat` posits. The position in the *`moniker`* list corresponds to the same order of appended `_orientat` posits. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` with_pose(`*`moniker1`*`, `*`moniker2`*`,...)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)...`

For easy of reading for humans, either a `beginwith ... endwith` syntax, or a nested statement approach can be taken.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `beginwith_pose(`*`moniker1`*`, `*`moniker2`*`,...);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker1`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker2`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `endwith_wp();`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_pose(`*`moniker1`*`, `*`moniker2`*`,...)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker1`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`moniker2`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `;`

## Casting
Casting to `pose`s sibling, `waypoint` and `goal`, is the safest and most commonly used cast of `pose`, as they are related. Casting can be achieved by specifing the datatype using curly brackets (`{}`), or with the `with` verb.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_pose({goal},`*`posemoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_goal(`*`goalmoniker`*`);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_pose({wp},`*`posemoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp(`*`posemoniker`*`);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp({pose},`*`waypointpmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_landmark(`*`waypointmoniker`*`);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_wp({goal},`*`waypointpmoniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_poi(`*`waypointmoniker`*`);`<br>

## Verbs
| verb | description | API |
| --- | -------- | --- |
| <a name="add"></a> `add_`*`<pose>`* | Declaration of *<pose>* *object* | [add](../../abstract/verb/add.md#pose) |
| <a name="go"></a> `go_`*`<pose>`*<br>`goto_`*`<pose>`* | The proceeding *object* will go to the pose *<pose>* | [go](../verb/go.md#pose) |
| <a name="with"></a> `with_`*`<pose>`*<br>`(`*`moniker`*`)` | Referencing *<pose>* *object* | [with](../../abstract/verb/with.md) |


## Posits
| posit | description | API |
| --- | -------- | --- |
| <a name="parse"></a> `_parse()`<br>`_parse(`*`string`*`)`<br>`_parse({lang},`*`string`*`)` | Parses proceeding *object*<br>Parses the *string* and determines language<br>Parses *string* following language *lang* | [parse](../funct/parse.md#pose) |
| <a name="coords_a"></a> `_coords()`<br>`_coords_(`*`x_lat1`*`, `*`y_long1`*`, `*`z_alt`*`)` | Provides coordinates from proceeding *object*<br>Provides three-dimensional coordinates of `x_lat1`,`y_long1`,`z_alt` | [coords](../obj/coords.md#pose) |
| <a name="geojson"></a> `_geojson(`*`geojsonstring`*`)` | Direct parse of geoJSON `geojsonstring`| [geojson](../funct/geojson.md#pose) |
| <a name="shapefile"></a> `_shapefile(`*`shapefilestring`*`)` | Direct parse of Shapefile `shapefilestring`| [shapefile](../funct/shapefile.md#pose) |
| <a name="kml"></a> `_kml(`*`kmlstring`*`)` | Direct parse of KML `kmlstring`| [kml](../funct/kml.md#pose) |
| <a name="displacemto"></a> `_displacemto(`*`tomoniker`*`)`<br>`_displacemto([`*`variablename`*`])`<br>`_displacemto(❬`*`unit`*`❭,`*`tomoniker`*`)` | Provides the displacement from preceeding *object* to *tomoniker* *object*<br>Provides the displacement from preceeding *object* to *object* monikered to the value of *variablename*<br>Provides the displacement from preceeding *object* to *tomoniker* *object* with specified unit | [displacem](./displacem.md#pose) |
| <a name="around"></a> `_around()` | Reference to a [`zone`](./zone.md) of preceeding *object* defined by proceeding *object* | [around](../condit/around.md#pose) |
| <a name="coords_b"></a> `_x()`, `_x(`*`x`*`)`<br>`_y()`, `_y(`*`y`*`)`<br>`_z()`, `_z(`*`z`*`)`, `_w(`*`w`*`)` | Gets and sets the x, y, and z coordinates and w real part for quaternions, repsectively| [xyz](../../abstract/funct/xyz.md#pose) |
| <a name="coords_c"></a> `_lat()`, `_lat(`*`lat`*`)`<br>`_lng()`, `_lng(`*`lng`*`)`<br>`_alt()`, `_alt(`*`alt`*`)` | Gets and sets the x, y, and z coordinates (repsectively) of the preceeding *object* | [xyz](../funct/latlngalt.md#pose) |
| <a name="elevation"></a> `_elev()`<br>`_elevation(`*`elev`*`)` | Gets and sets the elevation of the preceeding *object* | [elev](../funct/elev.md#pose) |
| <a name="waitat"></a> `_waitat()`<br>`_waitat(`*`moniker`*`)` | Wait at proceeding *object*<br>Wait at pose *moniker* | [waitat](../funct/waitat.md#pose) |
| <a name="loiterat"></a> `_loiterat()`<br>`_loiterat(`*`moniker`*`)` | Loiter at proceeding *object*<br>Loiter at pose *moniker*  | [loiterat](../funct/loiterat.md#pose) |

---
## References

* [`set_euler`](../setter/euler.md); [`set_quatern`](../setter/quatern.md)
* [`euler`](./euler.md); [`quatern`(./quatern.md)
* [`waypoint`](./waypoint.md); [`goal`](./goal.md)