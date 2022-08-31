<!-- http://wiki.ros.org/mavros#mavcmd -->
<!-- sethome             Request change home position -->


# `set_home`

The `set_home` verb-object setter statement will set the physical position as the designated 'home' waypoint.  Each thingy can only have one 'home', so and new declarations of 'home' will replace that last one.

## Syntax

`set_home(`*`moniker`*`)_at_(`*`map`*`, `*`x_lat`*`, `*`y_lat`*`)`
`set_home(`*`moniker`*`)_around(`*`map`*`, `*`x_lat`*`, `*`y_lat`*`, `*`radius`*`)`

### Example
```diego
with_robot(alif)
    set_home()_around(localMap,422.334,234.123,10.2,4);
;

go_robot(alif)_home();
```

