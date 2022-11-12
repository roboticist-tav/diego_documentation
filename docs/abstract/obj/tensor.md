# Tensor (object)

```mermaid
    flowchart TB
        subgraph orientation
            Excurs((excurs)) --> course(Course)
            course --> way(Way)
            way --> pose(Pose)

        end
        subgraph time
            tour(Tour) --> journ(Journ)
            journ --> trip(Trip)
            trip --> goal(Goal)
            
        end
        subgraph abstract
            tensor1(Tensor) --> tensor2(Tensor)
            tensor2 --> Vector(Vector)
        end
        subgraph location
            intiner(Itinerary) --> Route(route)
            route --> Path(path)
            path --> wp(Waypoint)
        end
        
```
<div style="text-align: right"><sub>Time-Space Hierarchy</sub></div>

<!-- Abstract-Location-Orientation-Time -->

<a name="declare"></a>
## Declaration

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment

<a name="initial"></a>
## Initialisation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="assign"></a>
## Assignment

<a name="reference"></a>
## Referencing
Referencing a ` ` *object* is achieved with the `with` verb, or the shortened `(`*` `*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`_moniker`*`);`

<a name="type"></a>
## Typing

<a name="get"></a>
## Getting

<a name="set"></a>
## Setting

<a name="cast"></a>
## Casting

<a name="properties"></a>
## Properties

<a name="example"></a>
## Examples