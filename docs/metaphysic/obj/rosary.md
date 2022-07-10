# Rosary (object)

Rosary is a diriviative of `path` and `way`



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
    add_route(perimeter);
    add_waypoint(x0)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x1)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x2)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x3)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x4)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x5)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x6)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x7)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x8)_route(perimeter)_coords(-26.812298, 153.082254);
    add_waypoint(x9)_route(perimeter)_coords(-26.812298, 153.082254);
    
    // Set up path (using rosary)
    add_rosary(perimeter_cc)_calc(x0→x1→x2→x3→x4→x5→x6→x7→x8→x9⥀x0);
    with_route(perimeter)_rosary(perimeter_cc);
```