# Yush (object)

Yush is an abstract pointer, rather than an variable value.  Named after Kateryna Yushchenko.

```diego
add_var({level_5},varFuelLevel)_robot(myDrone)_fuelstatus();          // varFuelLevel = high
add_yush({level_5},yushFuelLevel)_robot(myOtherDrone)_fuelstatus();   // yushFuelLevel = high
  
go_drone(myDrone)_waypoint(greenFlag)
    ? loop_if([varFuelLevel]>low)                   // varFuelLevel = high > high > high > high
        ? (myDrone)_(greenFlag)_loiterat();         // die of exhaustion!  
        : (myDrone)_rtb();                          
    ;
;

go_drone(myOtherDrone)_waypoint(blueFlag)
    ? loop_if([yushFuelLevel]>low)                  // yushFuelLevel = high > medium > low
        ? (myOtherDrone)_(blueFlag)_loiterat();
        : (myOtherDrone)_rtb();                     // return to base!
    ;
;
```

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