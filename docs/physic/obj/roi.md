# Region of Interest (object)
A `roi` *object* (also `region`) is an array of multi-point physical positions, used to represent a physical location in physical space, or on a map.  The term 'place of interest' can refer to a 'roi' (region of interest), however, this is avoided so as not to be confused with a `poi` 'Point of Interest' which has the same initialisms. The `roi` *object* also has the operator (`⌘`) to be used in *expressions*. 

## Declaration & Assignment
The default declaration of `roi` is to at least provide a *moniker*. However, the definition of the roi can be assigned or declared using either: the [`shape`](../../metaphysic/funct/shape.md) posit; or, the [`ambit`](../../metaphysic/obj/ambit.md) posit.  There are various signatures for the `shape` and `ambit` posits.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`);`<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_shape(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_shape({`*`shape`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_shape({`*`shape`*`},`*`x_lat1`*`,`*`y_lng1`*`,`*`x_lat2`*`,`*`y_lng2`*`,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_shape({`*`shape`*`},`*`[object1]`*`,`*`[object2]`*`,`*`...`*`);`<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_ambit(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_ambit(`*`x_lat1`*`,`*`y_lng1`*`,`*`x_lat2`*`,`*`y_lng2`*`,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_roi(`*`moniker`*`)_ambit(`*`[object1]`*`,`*`[object2]`*`,`*`...`*`);`<br>

## Referencing
Referencing the `roi` *object* is achieved using the verb `with` or  implied with the use of brackets (`()`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_roi(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`roi_moniker`*`);`

## Posits
The majority of posits for the `roi` *object* are concerned with developing the physical location and shape of the region of interest.

| `posit` | description | API |
| --- | --- | --- |
| <a name="_ambit"></a> `_ambit` | Use a 'linear ring' to define the roi. | [ambit](#ambit) |
| <a name="_area"></a> `_area` | Provide or set the area of the roi (using default or explicit units). | [area](#area) |
| <a name="_extrude"></a> `_extrude` | Extrude the ambit or shape of the roi along a plane. | [extrude](#extrude) |
| <a name="_flatten"></a> `_flatten` | Flatten (or convert to two-dimensions) the ambit or shape of the roi. | [flatten](#flatten) |
| <a name="_grow"></a> `_grow` | Grow the ambit or shape of the roi. | [grow](#grow) |
| <a name="_shape"></a> `_shape` | Use a geometry shape with multi-points to define the roi. | [shape_2d](#shape_2d)<br>[shape_3d](#shape_3d) | 
| <a name="_shrink"></a> `_shrink` | Shrink the ambit or shape of the roi. | [shrink](#shrink) |
| <a name="_skin"></a> `_skin` | Apply a skin to roi shape for graphical displays. | [skin](#skin) |
| <a name="_surface"></a> `_surface` &nbsp; `_sarea` | Provide or set the surface area of the roi (using default or explicit units). | [surface](#surface) |
| <a name="_text"></a> `_text` | Provide text in a human language describing the roi.  | [text](#text) |
| <a name="_tip"></a> `_tip` | Provide a human tip in human language to briefly describe the roi. | [tip](#tip) |
| <a name="_to3d"></a> `_to3d` | Convert the ambit or shape of the roi to three-dimensions. | [to3d](#to3d) |
| <a name="_volume"></a> `_vol` &nbsp; `_volume` | Provide or set the volume of the roi (using default or explicit units). | [vol](#vol) |
<!--| <a name=""></a> `_` |  | [](#) |-->


single <--> range

s   point <--> region
i   waypoint <--> locat
ng  way <--> place
le  goal <--> venue

mu  mpoint <--> mregion
lt  mwaypoint <--> mlocat
pl  mway <--> mplace
e   mgoal <--> mvenue 

`add_locat(`*`moniker`*`);`<br>
`add_location(`*`moniker`*`);`<br>
`add_locat({`*`geometry`*`},`*`moniker`*`);`


| 2D *`{geometry_type}`* | operator | description | API |
| --- | --- | --- | --- |
| *`{circle}`* | ◯ | [circle](./circle.md) |
| *`{square}`* | ◻ | [square](./square.md) |
| *`{rect}`* &nbsp; *`{rectangle}`*| ▭ | [rect](./rect.md) |
| *`{triangle}`* &nbsp; *`{tri}`* | △ | [triangle](./triangle.md) |


| 3D *`{geometry}`* | operator | description | API |
| --- | --- | --- | -- |
| *`{sphere}`* | 🏀 | | [circle](./circle.md) |
| *`{cube}`* | :fa-cube: | | [cube](./cube.md) |
| *`{cuboid}`* | ◳ |  | [cuboid](./cuboid.md) |
| *`{pyramid}`* | :fa-cubes: | | [pyramid](./pyramid.md) |













`add_reg({locat},`*`moniker`*`);`<br>
`add_region({locat},`*`moniker`*`);`<br>



