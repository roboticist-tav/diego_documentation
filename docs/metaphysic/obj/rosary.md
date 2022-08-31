# Rosary (object)
A `rosary` *object* is looped chain of *objects* representing a physical ordered array of points to combine into a full route. In terms of orientation all physical coordinate locations follow the right-hand-rule.  A `rosary` is similar to an `ambit`, execpt a rosary cannot have forks and the last locational object must loop back on the first locational object.

The term 'linear ring' is often associated with the same principle of the `rosary` object.

## Definition & Assignment

## Operators 

| operator | unicode | notes<br>`example` |
| --- | --- | -- |
| `→`<br>`->` | U+2192 | Path to next point by best fit<br>`wp1→wp2` |
| `↠`<br>`->>` | U+21A0 | Path to next point by fastest means possible<br>`wp1↠wp2` |
| `↦`<br>`\|->` | U+21A6 | Path to next point, wait at left point until ready |
| `⥑`<br>`\|` | U+2951 | Termination of path, separator of paths<br>`wp1→wp2→wp3⥑wp1→wp3`

Example

```diego
    // Set up route
    add_route(perimeter)
        add_waypoint(x0)_coords(-26.812298, 153.082254);
        add_waypoint(x1)_coords(-26.812298, 153.082254);
        add_waypoint(x2)_coords(-26.812298, 153.082254);
        add_waypoint(x3)_coords(-26.812298, 153.082254);
        add_waypoint(x4)_coords(-26.812298, 153.082254);
        add_waypoint(x5)_coords(-26.812298, 153.082254);
        add_waypoint(x6)_coords(-26.812298, 153.082254);
        add_waypoint(x7)_coords(-26.812298, 153.082254);
        add_waypoint(x8)_coords(-26.812298, 153.082254);
        add_waypoint(x9)_coords(-26.812298, 153.082254);

        // Set up paths (using rosary)
        add_rosary(x0→x1→x2→x3→x4→x5→x6→x7→x8→x9⥀);
    ;

    
    with_route(perimeter)
        add_rosary(x0→x1→x2→x3→x4→x5→x6→x7→x8→x9⥀);
    ;
```

Rosary is a diriviative of `path` and `way`