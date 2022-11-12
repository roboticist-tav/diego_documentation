# Navigation Planning
 
Navigation planning involves the declaration and execution of various components in order for a mobile thingy (a `robot` object) to travel in a designated way in the physical real world.

## Navigation Planning Objects

There are various objects available for navigation planning in **_Diego_**, which can conveniently be depicted in the 'route matrix'…

| ![Route Matrix](https://raw.githubusercontent.com/tavman7/diego.github.io/main/_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *fig. 1 : Route Matrix* |

Each column of the 'route matrix' are a _'family'_ of objects used for navigation planning. The left column (blue objects) represent the location only navigation planning objects. These objects require at least coordinates to be effective. From the bottom of the column up, the `waypoint` The object is representation of an intermediate physical point or place on a route or line of travel, or simply, a stopping point. Next is the `path` object, which in the strictest terms is a collection of two waypoints and their relationship to each other but only in terms of location.  The `route` object is a collection of `path`s arranged in a logical order with relationships defined for each `path`.  For each `route` object there are man `path`s. The `itinerary` is the top-most location-only navigation planning object.

In a similar fashion to the location-only objects, the green objects have similar scope to their adjacent objects.  The green object represent the orientation objects, that have location **and** orientation attributes.  The `excurs`_(ion)_ object has many `course` objects, each `course` object has many `way` objects, an each `way` object has usually two `pose` (or `posepoint`) objects.

The orange objects are known as the logging navigation planning objects, as they log the 'journey' between `goal`s. The `tour` object has many `journey` objects, each `journey` object has many `trip` objects, an each `trip` object has usually two `goal`s.  The attributes if the logging navigation planning objects are location **and** orientation **and** time-logging.

## Navigation Planning Example

To demostrate the various syntax available in ***Diego*** for navigation planning we are going to use a simple route long a curve of a road, intended for ground-based robots.

The location is Aura Business Park, QLD, Australia, along Strong Road, an industrial/commercial zoned area.  So first, we add the waypoint to appear as such:

| ![Waypoints](https://raw.githubusercontent.com/tavman7/diego.github.io/main/_img/abp_waypoints.jpeg "Waypoints") |
| :---: |
| *fig. 2: Strong Road, Aura Business Park - Waypoints* |

***Diego*** is a multi-discourse language, meaning there a many ways command can be structure/built.  Therfore the example code shows multi approaches to adding waypoints to an itinerary…

```Diego
use_namespace(aura_business_park);
begin_itinerary(strong_road);
    // maps
    heed_map(aura_business_park)_asglobal()_gnps()_measure(lat, long);
    
    // waypoints
    add_waypoint(w1)_coords(-26.803923, 153.069252);
    add_waypoint(w2, w3)_coords(-26,804316, 153.069225)_coords(=26.804465, 153,069238);
    add_waypoint()_geojson(
        {
            "type": "Feature",
            "geometry" : {
                "type": "Point"
                "coordinates": [-26.804596, 153.069332]
            },
            "properties": {
                "name": "w4"
            }
        }
    )_dialect(std);
    add_coords(w5)_lat(-26.804673)_long(153,069491);
    add_waypoint(w5)_coords(w5)_elevat(37.2);
    add_array(w6)_value(-26.804711, 153.069783);
    add_waypoint(w6)_lat()_valof(w6[0])_long()_valof(w6[1]);

    …
```
To start, a namespace called `aura_business_park` is used to segregate object names from other experiences. Then to develop all the location-only navigation planning object (blue objects) they are encapsulated into an `itinerary` called `strong_road`.

 a


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_waypoint(`*`moniker|uuid`*`)_point(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`);`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_pose(`*`moniker|uuid`*`)_point(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`)_orientat((`*`x`*`, `*`y`*`, `*`z`*`, `*`w`*`);`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_pose(`*`moniker|uuid`*`)_waypoint(`*`moniker|uuid`*`)_orientat((`*`x`*`, `*`y`*`, `*`z`*`, `*`w`*`);`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_goal(`*`moniker|uuid`*`)_point(`*`x_lat`*`, `*`y_long`*`, `*`z_alt`*`)_orientat((`*`x`*`, `*`y`*`, `*`z`*`, `*`w`*`)_datetimein(`*`datetime`*`);`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`add_goal(`*`moniker|uuid`*`)_pose(`*`moniker|uuid`*`);`

`_posein(`*`moniker|uuid`*`)`


`_timein(`*`datetime`*`)`
`_datetimein(`*`datetime`*`)`
`_timeout(`*`datetime`*`)`
`_datetimeout(`*`datetime`*`)`

`_weather()`
`_visitor()`
`_orientatin()`
`_orientatout()`



```