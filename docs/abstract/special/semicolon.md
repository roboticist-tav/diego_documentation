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



```diego
with_map(map1)
    _circ(poi1)_at(4,3)_r(❬m❭,0.332)
        _square(sq1)_cnr(5,7)_cnr(6,8)
;


log_console()_(map1)_shapes();
// poi1,poi1.sq1

with_map(map2)
    _circ(poi2)_at(4,3)_r(❬m❭,0.332)
    ()_square(sq2)_cnr(5,7)_cnr(6,8);
;


log_console()_(map2)_shapes();
// poi2,sq2


with_map(map3)
    ()_circ(poi3)_at(4,3)_r(❬m❭,0.332);
    ()_square(sq3)_cnr(5,7)_cnr(6,8);
;


log_console()_(map3)_shapes();
// poi3,sq3


