# Statement Terminator (special)
As with most java'esque and c'esque languages, ***Diego*** uses the semi-colon (`;`) as a terminator to a statement (command). However, statements in ***Diego*** can be nested inside other statements.  Also the use of [elvish operators](elvish.md) can be used between the end of a statement and the statement terminator. For example:
```diego
// Simple statement
add_yush({level_5},yushFuelLevel)_robot(myOtherDrone)_fuelstatus();

// Nested statement
go_drone(myDrone)_waypoint(greenFlag)
    msg_human(fred)_batt()_level();
;

// Nested statement with positive and negative outcomes
go_drone(myDrone)_waypoint(blueFlag)
    ? loop_if([yushFuelLevel]>low)
        ? (myOtherDrone)_(blueFlag)_loiterat();
        : (myOtherDrone)_rtb();
    ;
;
```
---
## References
* Statement Terminator in [Lexicon](../../lexicon/lexicon.md#;)
* [Elvish Operators](elvish.md)

