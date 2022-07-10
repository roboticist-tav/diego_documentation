# Abstract
The term **abstract** is used to define statements in ***diego*** that represent abstract objects, usually used in a programming environment.

## <a name="self"></a> Self
As with most object-orientated programming langauges, the idea of self is used in **Diego**. However, since there are multiple intelects that are interpreting ***Diego*** code, there needs to be several levels of self. The differing level of self are usful for discernment, discrimination, and, swarming.

All four *self* objects are metaphysical, however, `me` is considered to be also abstract as this is associated with '*this*' in other programming languages.  However, the four *self* objects are:

| self | description | API |
| --- | --- | --- |
| <a name="me"></a> `me_`*`<object>`*<br>`_me()` | A representation of the self thingy, similar to '*this*' in other programming languages | [me](./special/me.md) |
| <a name="we"></a> `_we()` | A representation of a group of thingys, through the viewpoint of a `spox` | [we](../metaphysic/special/we.md)<br>[spox](../metaphysic/obj/spox.md) |
| <a name="us"></a> `_us()` | Declaration of a group of thingys | [us](../metaphysic/special/us.md) |
| <a name="them"></a> `_them()` | A representation of a group of thingys from the viewpoint of `me` | [them](../metaphysic/special/them.md) |
| <a name="you"></a> `_you()` | A assignment member of the a group of thingys from the viewpoint of the `spox` of the group | [you](../metaphysic/special/you.md) |

## <a name="declarable_data"></a> Declarable Data

| data | description | API |
| --- | --- | --- |
| <a name="deed"></a> `_deed(`*`moniker`*`)`  | A basic one-dimensional data storage object called *moniker*, immutable except for *deed owner* |  [deed](./obj/deed.md) |
| <a name="indent"></a> `_indent(`*`moniker`*`)`<br>`indenture(`*`moniker`*`)`  | A basic one-dimensional data storage object called *moniker*, immutable except for *indenture owners* |  [indent](./obj/indent.md) |
| <a name="val"></a> `val(`*`moniker`*`)`<br>`valuable(`*`moniker`*`)`  | A basic one-dimensional immutable data storage object called *moniker* |  [val](./obj/val.md) |
| <a name="var"></a> `var(`*`moniker`*`)`<br>`variable(`*`moniker`*`)`  | A basic one-dimensional mutable data storage object called *moniker* |  [var](./obj/var.md) |

## <a name="primitive_data"></a> Primitive Data

| data | description | API |
| --- | --- | --- |
| <a name="tempor"></a> `tempor(`*`moniker`*`)`<br>`temporal(`*`moniker`*`)`<br>`_tempor(`*`moniker`*`)`<br>`_temporal(`*`moniker`*`)`<br>`{tempor}`<br>`{temporal}` | A primitive data object representing a date off a calendar monikered *moniker* | [tempor](./obj/tempor.md) |




## <a name="Collections"></a> Collections

| collection | description | API |
| --- | --- | --- |
| <a name="array"></a> `array(`*`moniker`*`)`<br>`ary(`*`moniker`*`)` | A collection of multiple mutable elements under a single *object* called *moniker* | [array](./obj/ary.md) |
| <a name="list"></a> `list(`*`moniker`*`)` | A database-assigned collection *object* called *moniker* | [list](./obj/list.md) |
| <a name="arran"></a> `arran(`*`moniker`*`)`<br>`arn(`*`moniker`*`)`<br>`arrangem(`*`moniker`*`)`<br>`arrangement(`*`moniker`*`)` | A collection of multiple mutable elements under a single variable name of *moniker* | [arran](./obj/ary.md) |
| <a name="matrix"></a> `matrix(`*`moniker`*`)`<br>`_matrix(`*`moniker`*`)`| A two-dimensional collection data storage *object* called *moniker* | [matrix](./obj/matrix.md) |
| <a name="clump"></a> `clump(`*`moniker`*`)` | A multi-dimensional  collection of data storage *object* called *moniker* | [clump](./obj/clump.md) |
| <a name="dict"></a> `dict(`*`moniker`*`)`<br>`_dict(`*`moniker`*`)`<br>`dictionary(`*`moniker`*`)`<br>`_dictionary(`*`moniker`*`)` | A keyed collection, with key-value pairs, data storage *object* called *moniker* | [dict](./obj/dict.md) |
| <a name="hash"></a> `hash(`*`moniker`*`)` | A two-dimensional collection data storage *object* called *moniker*, with hashed keys | [hash](./obj/hash.md) | 
| <a name="lexi"></a> `lexi(`*`moniker`*`)`<br>`lexikon(`*`moniker`*`)` | A two-dimensional collection data storage *object* called *moniker*, with unique keys | [lexi](./obj/lexi.md) |


## <a name="Function_Properties"></a> Function Properties


## <a name="Functional_Objects"></a> Functional Objects

## <a name="Error_Objects"></a> Error Objects

| err | description | API |
| --- | --- | --- |
| `err` | | |

## <a name="Numerics"></a> Numerics

## <a name="Dates"></a> Dates

## <a name="Text Processing"></a> Text Processing



## <a name="Control Flow"></a> Control Flow

## <a name="Declarations"></a> Declarations

## <a name="Functions_Classes"></a> Functions & Classes

## <a name="Iterations"></a> Iterations

## <a name="primary_expressions"></a> Primary Expressions
## Collection Dimensions
Data storage can be achieved in ***diego*** 
```mermaid
flowchart RL
    subgraph multi-dimension
        clump(["<code>clump</code>"])
    end
    subgraph two-dimension
        matrix(["<code>matrix</code>"])
        dict(["<code>dict</code>"])
        hash(["<code>hash</code>"])
    end
    subgraph one-dimension
        var(["<code>var</code>"])
        array(["<code>ary</code>"])
    end
```
<div style="text-align: right"><sub>Dimensions of collections</sub></div><br>

All *physic*al objects in ***diego*** are detrived from the `thingy` object, which represents all *physic*al objects.  There are only four[^morethingies] types of `thingies`: `human`, human beings interacting with ***diego*** through a `console`; `organic`, organic non-human beings, such as a dog, a cat, a flower, a bush, etc.; `robot`, a self-propelled thingy in the physical world; and a, `thing`, an object in the physical world represented in **diego**.

There are other sub-types of thingies. A `sobot` is a stationary `robot`, that although can be self-propelled, does not neccesarily interact physically in the physical world outside its own environment, such as a *robot arm*. A `thing` can be sub-typed as: `mobot`, a conveyed smart device, such as a smart watch, smart doorbel, etc.; and a, `ject`, a traditional physical object that is not smart enough to think.  There are two variants of a `ject`: an `object` (ob ject), an immoveable ject such as a rock, a chair; and, a `subject` (sub ject), a self-propelled or moveable ject such as a trolley, wheeled tool cabinet, etc.

## Physic Composition Hierarchy (Organs / Components / Devices)
Each of the four `thingies` has associated *components* that are further categorised, as such:
```mermaid
flowchart TD
    thingy --> human
    thingy --> organic
    thingy --> robot
    thingy --> thing
    human --> apparat_human(apparat)
    human --> device_human(device)
    organic --> apparat_organic(apparat)
    organic --> device_organic(device)
    robot --> equip_robot(equip)
    robot --> compon_robot(compon)
    robot --> peripher_robot(peripher)
    thing --> equip_thing(equip)
    thing --> compon_thing(compon)
    thing --> peripher_thing(peripher)
```
<div style="text-align: right"><sub>Physic Hierarchy (by component)</sub></div><br>

There are effectively three *components* that come with each `thingy`.  The `apparat`us/`equip`ment are non-smart *components* that are carried or attached to the thingy, so, for `human`s this could be a traditional watch or a jacket. For `organic`s this could be a collar on a dog or cat.  For `robot`s this is a *component* like wheels, or the chassis.  For a `thing` this could be the door of a fridge, or a cushion on a chair.

Each of the four `thingies` also have a `compon`ent. A `compon` is a *component* that moves in the physical world, so for `human`s and `organic`s this would be a limb or an organ.  Since **diego** is not, yet, concerned with controlling human and organic anotomy, they are not represented here.  However, `compon`s for `robots` and `things` include actuators, projectile launchers, encoders, motors, switches, etc.

Then there are `device`s and `peripher`als, which are smart components that are carried or attached to the thingy, so for `human`s this could be a smart watch or a cellphone[^devicesobot].  For `organic`s this could be a microchip implanted in a dog.  For `robot`s and `thing`s this is termed a `peripher` and includes hygrometers, proximity sensors, sensors, cameras, etc. 

## Notes
[^morethingies]: There are some *fringe* `thingy` types such as `mech`, `applian`, `mach`, and, `vehicle`.
[^devicesobot]: Smart devices are can also be treated a `sobot`s.

---

## References













