# Parse (function)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`[moniker]`*`)_format(`*`format`*`)_json([{`*`x_lat`*`, `*`y_long`*`)}, {`*`x_lat`*`, `*`y_long`*`)}, …])`

***Diego*** allows for other apporaches for creating/loading mutilple `waypoint`s, such as…

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`[moniker]`*`)_format(`*`format`*`)_json([{`*`x_lat`*`, `*`y_long`*`)}, {`*`x_lat`*`, `*`y_long`*`)}, …])`

…creates miltilple `waypoints` from a literal json string.  The waypoint monikers are created in seqence using a combination of a _(base)-_*`moniker`* and a specified `format`.  To load `waypoints`, either from a file…

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint()_load(`*`file_url`*`, `*`file_format`*`, `*`protocol`*`)`

<br>`_parse({json},`*`string`*`)` Parses json *jsonstring*
 
## Posits

| posit | description | API |
| --- | -------- | --- |
| <a name="json"></a> `_json()`<br>`_json(`*`jsonstring`*`)` | Provides json of proceeding *object*<br>Provides json *jsonstring* | [json](../../abstract/funct/json.md) |

| <a name="at"></a> `_at(`*`index`*`)`<br>`_at()` | Provides the element at index *index* |


…or using programming logic from an array (for instance)…

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint()_load()_array(`*`moniker`*`);`

…or from a json string…

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint()_load()_json(`*`moniker`*`);`