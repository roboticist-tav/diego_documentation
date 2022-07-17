# Goal (object)
The `goal` object is a representation of a temporal event in an orientation at a physical point. `goal`s require a moniker;, a current position (i.e. a waypoint); an orientation coorespondence to their waypoint (i.e. a pose), and temporal coordinates. 

The `goal` is at the lowest hierarchical level of the 'Route Matrix', being similar to a `waypoint`  and a `goposeal`.

| ![Route Matrix](/_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

In the family of 'location-and-orientation-and-time' based navigation objects, one `tour` has many `journ`s, one `journ` has many `trip`s, and, one `trip` has many `goals`s.

# Declaration
The default declaration of the `goal` object is to at least provide a *moniker*, however, at declaration it is common to provide a temporal coordingate using the `_boutat` posit. The `_boutat` posits accepts a `bout` object, and so uses the same `bout` child posits.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_goal(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_goal(`*`moniker1`*`, `*`moniker2`*`,...);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_goal(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat({`*`order`*`},`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(❬`*`unit`*`❭`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat({`*`order`*`},❬`*`unit`*`❭`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`)_euler(`*`order`*`)_angles(`*`unit`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;` add_pose(`*`moniker`*`)_orientat(`*`x`*`,`*`y`*`,`*`z`*`,`*`w`*`)_quatern(`*`order`*`)_angles(`*`unit`*`);`


---------------------
goal

```Diego
_navresult({0|1|2|3})
_navresult({unknown|succeeded|canceled|failed})
```