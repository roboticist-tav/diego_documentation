# Way (object)
The `way` object is a representation of an orientation at two physical points and their relationship with each other. 

The `way` is at the penultimate lowest hierarchical level of the 'Route Matrix', being similar to a `path` and a `trip`.

| ![Route Matrix](/_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

<a name="declare"></a>
## Declaration
The default declaration of the `way` object is to at least provide a *moniker*, however, at declaration it is common to provide two locations using either: a child `waypoint` (or shortened `wp`) assignment; or, using the `_coords` posit.


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_way(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_way(`*`moniker1`*`, `*`moniker2`*`,...);`<br>
`add_way(`*`way_moniker`*`, `*`way_uuid`*`)`
`add_way(`*`way_moniker`*`, `*`way_uuid`*`, `*`way_type`*`)`
human way

| `way_type`  | Description |
|--|--|
| `corridor` |  |
| `tube` |  |
| `road` | |
| `stairway` | |
| `pipe` | |
| `escalator` | |
| `travelator` | |
| `landing` | |
| `runway` | |
| `sidewalk` / `pavement` | |
| `cyclelane` / `sideroad` | |

`add_pipe(`*`pipe_moniker`*`, `*`pipe_uuid`*`)`
`add_pipe(`*`pipe_moniker`*`, `*`pipe_uuid`*`, `*`pipe_type`*`)`

| `pipe_type`  | Description |
|--|--|
| `pipe` |  |
| `tube` | |

non-human way (thing way)
> Written with [StackEdit](https://stackedit.io/).
