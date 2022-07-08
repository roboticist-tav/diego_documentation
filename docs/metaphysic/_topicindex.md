# Topological Metaphysic Object Index

An topological index of all metaphysic objects used by **diego** instruction programming language.

## Missions

| mission | notes<br>examples<br>`example` | API |
| --------- | ----- | ----- |
| `mission` |

## Naming & Labeling

| name/label    | notes<brexamples | API |
| --------- | ----- | ----- |
| `sobriquet` one each thingy can have one `sobriquet` with verb `_sobri()`
| `label` any thingy can have any number of labels
| `moniker` unique one moniker to one thingy
| `cognomen`
| `clepe`

## <a name="puff"></a> Puffs

| puffs     | notes<brexamples | API |
| --------- | ----- | ----- |
| `channel` | | An exclusive sub-section of a `workspace`, sometimes referred to as a _conversation_ |
| `cloud`   | A zone (`puff`) used for diego communication that utilises a cloud based platform like twitter, discord, slack, _etc._ |
| `fog`     | A zone (`puff`) used for diego communication that relies on UDP | |
| `mist`    | A zone (`puff`) used for diego communication that relies on TCP | |
| `workspace` | An exclusive section of a `puff`, sometimes called a _room_ |

## <a name="datamgt"></a> Data Management

| data management | notes<br>examples | API |
|--|:--|--|
| `attr`, `attribute` <a name="arena"></a> | Each `attr` is a immutable name-value pair (`{monniker|uuid}` as the name, `_value({value})` as the value). All data held in an `attr` should be immutable and have a one-to-one relationship (one name for one value).<br>Example: `add_attr(last_name)_value(Jones);` <br>See also: [spec](#spec) | [attr](/attr.md) |
| `blob` <a name="blob"></a> | **B**inary **L**arge **OB**ject |
| `var`, `variable` | | [var](/var.md) |
| `dict`, `dictionary` | | |
| `metric` | | [metric](/metric.md) |
| `scalar`
| `array`
| 

## <a name="datacomm"></a> Data Communication Management

| time management | notes<br>examples | API |
|--|:--|--|
| `funnel` | | |
| `lennuf` | | |

https://arxiv.org/pdf/1906.10641.pdf mavlink
https://docs.wpilib.org/en/stable/docs/romi-robot/index.html
https://www.bigocheatsheet.com/


## Routing
Routing dipicts the autonomous motion of robots, and twelve *objects* are provided as interface.  These twelve *objects* can be arranged in the route matrix:

| ![Route Matrix](/_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

### Location Routing
Location (location-only) routing involves four *objects* that consider physical locations within their spatial environment.

| l routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `itiner`<br>`itinerary` | An *object* *collection* of `route` *object* *collections* | - | [itiner](obj/itiner.md) |
| `route` | An *object* *collection* of `path` *objects* | [wayfind](../physic/obj/wayfind.md) | [route](obj/route.md) |
| `path` | A representation of the connections of `waypoint` *objects* | - | [path](obj/path.md) |
| `waypoint`<br>`wp` | A representation of a physical location in the physical world | [landmark](../physic/obj/landmark.md) | [waypoint](obj/waypoint.md) |

### Orientation-Location Routing
Location plus orientation routing involves four *objects* that consider physical locations and their orientation within their spatial and orientational environment. Orientation-location routing *objects* can inherit their physical locations from location routing *objects*.

| o+l routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `excurs`<br>`excursion` | An *object* *collection* of `course` *object* *collections* | | [excurs](obj/excurs.md) |
| `course` | An *object* *collection* of `way` *objects* | [valley](../physic/obj/valley.md) | [course](obj/course.md) |
| `way` | A representation of the connections of `pose` *objects* | - | [way](obj/way.md) |
| `pose` | A representation of an orientation in the physical world | *[heading](../physic/obj/heading.md)* | [pose](obj/pose.md) |

### Time-Orientation-Location Routing
Location plus orientation plus time routing involves four *objects* that consider physical locations, their orientation, and their temporal displacement within their spatial and orientational and temporal environment. Time-orientation-location routing *objects* can inherit their physical locations from location routing *objects* and their orientation pose from orientation-location routing *objects*.

| t+o+l routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `tour` | An *object* *collection* of `journ` *object* *collections* | - | [tour](obj/tour.md) |
| `journ`<br>`journey` | An *object* *collection* of `trip` *objects* | - | [journ](obj/journ.md) |
| `trip` | A representation of the connections of `goal` *objects* | - | [trip](obj/trip.md) |
| `goal` | A representation of a temporal position in the physical world | [finish line](../physic/obj/finline.md) | [goal](obj/goal.md) |

## Roundsup
| roundsup | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| (`route`) |  | [wayfind](../physic/obj/wayfind.md)  | ([route](obj/route.md)) |
| `geofence` |  | [border](../physic/obj/border.md) | [geofence](obj/geofence.md) |
| `lane` |  | [track](../physic/obj/track.md) | [lane](obj/lane.md) |
| `spine` |  | [rail](../physic/obj/rail.md)  | [spine](obj/spine.md) |

## <a name="timemgt"></a> Time Management

| time management | notes<br>examples | API |
|--|:--|--|
| `calendar` <a name="calendar"></a> | | [cal](obj/cal.md) |

## <a name="move"></a> Movement & Formation

| movement | notes<br>examples | API |
|--|:--|--|
| `form`<br/>`format`<br/>`formation` | | [form](verb/form.md) |
| `gait` | The thing version of `stride` | [gait](/gait.md) |
| `ghost` |  | [ghost](/ghost.md) |
| `stride` | The human version of `gait` | [stride](/stride.md) |
| `stance` | | [stance](/stance.md) |
| `swarm` | | [swarm](/swarm.md) |

## <a name="id"></a> Identification

| identification | notes<br>examples | API |
|--|:--|--|
| `ident` | | [ident](ident.md) |
| `manufactur`<br>`manufact`<br>`manufacturer` | | [manufactur](manufactur.md) |
| `make` | | [make](make.md) |
| `model` | | [model](model.md) |
| `serialnum`<br>`serialnumber`<br>`snum` | | [serialnum](serialnum.md) |
| `id()_moniker` | | [moniker](moniker.md) |
| `id()_name` | | [name](name.md) |
| `id()_nickname` | | [nickname](nickname.md) |
| `id()_species` | | [species](species.md) |
| `id()_version` | | [version](version.md) |
| `id()_softrel`<br>`id()_softwarerelease` | | [softrel](softrel.md) |
