<style>div.mermaid { text-align: center; }</style>
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
| ![Route Matrix](route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

### Location Routing
| location routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `itiner`<br>`itinerary` | | | [itiner](itiner.md) |
| `route` | | [wayfind](../physic/wayfind.md) | [route](route.md) |
| `path` | |  | [path](path.md) |
| `waypoint`<br>`wp` | | [landmark](../physic/landmark.md) | [waypoint](waypoint.md) |

### Orientation-Location Routing
| location routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `excurs`<br>`excursion` | | | [excurs](excurs.md) |
| `course` | | [valley](../physic/valley.md) | [course](course.md) |
| `way` | |  | [way](way.md) |
| `pose` | | *[heading](../physic/heading.md)* | [pose](pose.md) |

### Time-Orientation-Location Routing
| location routing | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| `tour` | | | [tour](tour.md) |
| `journey`<br>`journ` | | | [journey](journey.md) |
| `trip` | |  | [trip](trip.md) |
| `goal` | | [finishline](../physic/finishline.md) | [goal](goal.md) |

## Roundsup
| roundsup | notes<br>examples | physic version | API |
|--|:--|:-:|--|
| (`route`) |  | [wayfind](../physic/wayfind.md)  | ([route](route.md)) |
| `geofence` |  | [border](../physic/border.md) | [geofence](geofence.md) |
| `lane` |  | [track](../physic/track.md) | [lane](lane.md) |
| `spine` |  | [rail](../physic/rail.md)  | [spine](spine.md) |


## <a name="timemgt"></a> Time Management

| time management | notes<br>examples | API |
|--|:--|--|
| `calendar` <a name="calendar"></a> | | [cal](/cal.md) |

## <a name="move"></a> Movement & Formation

| movement | notes<br>examples | API |
|--|:--|--|
| `form`, `formation` | | [form](/form.md) |
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
