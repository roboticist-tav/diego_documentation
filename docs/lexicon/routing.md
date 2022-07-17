### Location Routing
Location (location-only) routing involves four *objects* that consider physical locations within their spatial environment.

| l routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `itiner`<br>`itinerary` | An *object* *collection* of `route` *object* *collections* | - | [itiner](../metaphysic/obj/itiner.md) |
| `route` | An *object* *collection* of `path` *objects* | [wayfind](../physic/obj/wayfind.md) | [route](../metaphysic/obj/route.md) |
| `path` | A representation of the connections of `waypoint` *objects* | - | [path](../metaphysic/obj/path.md) |
| `waypoint`<br>`wp` | A representation of a physical location in the physical world | [landmark](../physic/obj/landmark.md) | [waypoint](../metaphysic/obj/waypoint.md) |

### Orientation-Location Routing
Location plus orientation routing involves four *objects* that consider physical locations and their orientation within their spatial and orientational environment. Orientation-location routing *objects* can inherit their physical locations from location routing *objects*.

| o+l routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `excurs`<br>`excursion` | An *object* *collection* of `course` *object* *collections* | | [excurs](../metaphysic/obj/excurs.md) |
| `course` | An *object* *collection* of `way` *objects* | [valley](../physic/obj/valley.md) | [course](../metaphysic/obj/course.md) |
| `way` | A representation of the connections of `pose` *objects* | - | [way](../metaphysic/obj/way.md) |
| `pose` | A representation of an orientation in the physical world | *[heading](../metaphysic/funct/heading.md)* | [pose](../metaphysic/obj/pose.md) |

### Time-Orientation-Location Routing
Location plus orientation plus time routing involves four *objects* that consider physical locations, their orientation, and their temporal displacement within their spatial and orientational and temporal environment. Time-orientation-location routing *objects* can inherit their physical locations from location routing *objects* and their orientation pose from orientation-location routing *objects*.

| t+o+l routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `tour` | An *object* *collection* of `journ` *object* *collections* | - | [tour](../metaphysic/obj/tour.md) |
| `journ`<br>`journey` | An *object* *collection* of `trip` *objects* | - | [journ](../metaphysic/obj/journ.md) |
| `trip` | A representation of the connections of `goal` *objects* | - | [trip](../metaphysic/obj/trip.md) |
| `goal` | A representation of a temporal position in the physical world | [finish line](../physic/obj/finline.md) | [goal](../metaphysic/obj/goal.md) |