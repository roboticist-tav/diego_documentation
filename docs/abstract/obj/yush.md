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