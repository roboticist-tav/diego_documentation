# The Caterpillar Chain
The Caterpillar Chain is a baton movement of two or more agents who form a chain by association and follow, in common, a rectilinear locomotion. To simulate rectilinear locomotion, each agent must broadcast their last position to the next agent in line, soon after moving to a new position.

To demonstrate this movement we are going to use three drones (as the agents), and one route, made up of ten waypoints. We will let each robot learn new `pose`s, and `goal`, etc. if they so desire.

For realism, we will add a table with an self-connection charge station, so the drones can keep _caterpillar chaining_ for a substantial duration.

## Namespace
We are going to use common names, so we need to set up a namespace:
```diego
use_namespace(caterpillar_chain_demo);
```
## The Agents
The agents of this Caterpillar Chain demonstration will three drones, called 'alif', 'be' and , 'pe':
```diego
add_robot(alif)_type(drone);
add_robot({drone},be);
add_drone(pe);
```
## A Brave New World
So first we are going to start setting up the physical world...
```diego

// Set up physical world ready for the caterpillar chain movement:
begin_instruct(caterpillar_chain_physicals)_for(alif, be, pe);

    // Set up table with charge point on
    add_thing(chargepoint)_type(chargepoint);
    add_object({table},table);
    with_object(table)_thing(chargepoint);

    // Set up map
    add_map(map)_scope(global)_unit(dd)_altitude(47)_coords(x_lat, y_long, z_height);
    with_map(map)_pluscode(53QJ+3V Baringa, Queensland);

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
    
    // Set up paths (using rosary)
    add_rosary(perimeter_cc)_calc(x0→x1→x2→x3→x4→x5→x6→x7→x8→x9⥀x0);
    with_route(perimeter)_rosary(perimeter_cc);

    // Set up variables and label for use later
    add_var({int},penultimate_n)_default(0);
    add_sobriquet(all_waypoints)_specificto(x0, x1, x2, x3, x4, x5, x6, x7, x8, x9);
    add_sobriquet(penultimate_waypoint);

    // Add the table (with its charger) on the map
    with_map(map)_object(table)_at(-26.812298, 153.082254);

end_instruct(persian_chain_physicals);

exec_instruct(persian_chain_physicals)_for(alif, be, pe);
```

This is a simple composition instruction of the physical world for our three drones `alif`, `be`, and, `pe`. The table, we created it as an `object` with a `thing` child, the charger.

The waypoints produce an perimeter route, called `perimeter`, sequenced from waypoint `x0` to `x9` and then back to `x0`, around the house 21 Toyne Street, Baringa, QLD 4551, Australia.  There is no elevation on this route as the map, `map`, is set at an altitude of 47m above sea level, a close approximation. We added a pluscode for the extent of the map.

Finally the table, `table` has been placed on the map.

We execute the instruction immediately.

## There is a Beginning to Everything
To start the Caterpillar Chain we need one active agent and two loitering agents. We also have starting positions. `alif` will be the first active agent starting at waypoint `x9` to go along rosary `perimeter_cc` (on route `perimeter`), `be` and `pe` be will be the loitering agents, and they will loiter around waypoints `x8` and `x7` respectively...

```diego
begin_instruct(caterpillar_chain_starting_positions)_for(alif, be, pe)_onceonly();

    with_drone(alif)_sobriquet(active_agent)
        with_waypoint(x9)_sobriquet(active_startpoint);
        with_waypoint(x3)_sobriquet(active_endpoint);
    ;
    
    go_drone(active_agent)_rosary(perimeter_cc)_waypoint(active_startpoint)
        ? exec_instruct(activate_agent)_forof(active_agent)?;
    ;

    with_drone(be,pe)_sobriquet(loiterer);

    go_drone(be)_rosary(perimeter_cc)_waypoint(x8)
        ? exec_instruct(loiterise_agent)_forof(loiterer);
    ;

    go_drone(pe)_rosary(perimeter_cc)_waypoint(x7)
        ? exec_instruct(loiterise_agent)_forof(loiterer);
    :
    
end_instruct(persian_chain_starting_positions);
```
Note that we declare the rosary as a child of each drone, and all the waypoints as children of the rosary. This is intentional, as omitting the rosary, will instruct the drone to go straight to the waypoint and miss the route of the rosary entirely.

We do not want to execute instruction `caterpillar_chain_starting_positions` yet as the guys (`alif`, `be`, and, `pe`) don't yet know about instructions `activate_agent` and `loiterise_agent`. They will only complain that they haven't learnt that functionality if we execute `caterpillar_chain_starting_positions` now!

## Active Agent
In the Caterpillar Chain Movement the active agent scouts around the route from a starting position to an ending position. When it arrives penultimate to its ending position, it has to inform the others...

```Diego
// Activate the active_agent to go on route `perimeter`
begin_instruct(activate_agent)_for(active_agent);

    with_robot(active_agent)_gorosary(perimeter_cc)_startat(active_startpoint)_endat(active_endpoint)
        | with_robot(active_agent)_atrosary(active_endpoint)_change(--)
            ? exec_instruct(start_persian_chain)_for(loiterer) : wtf()
        ? exec_instruct(loiterise_agent)_for(active_agent) ? : wtf()
        : wtf();

    with_robot(active_agent)_sobriquet(loiterer) ? : ;
 
end_instruct(activate_agent);
```
> `with_robot(active_agent)_gorosary(perimeter_cc)_startat(active_startpoint)_endat(active_endpoint)`
> `        | with_robot(active_agent)_atrosary(active_endpoint)_change(--)`
>> With two commands one nested and concurrent in the other, we are instructing robot `active_agent` (which will be assigned previously) to follow rosary `perimeter_cc` (previously assigned to route `perimeter`) from rosarypoint `active_startpoint` to rosarypoint `active_endpoint`. Concurrently, robot `active_agent` is triggered on the rosarypoint at `active_endpoint` minus one (`_change(--)`).

> `? exec_instruct(start_persian_chain)_for(loiterer) : wtf()`
>> When `active_agent` reaches the penultimate rosarypoint of `active_endpoint_change(--`) it will execute `start_persian_chain` instruction.

> `? exec_instruct(loiterise_agent)_for(active_agent) ? : wtf()`
>> Finally when `active_agent` has reached `active_endpoint` it will execute `loiterise_agent` instruction.

> `with_robot(active_agent)_sobriquet(loiterer) ? : ;`
>> When all has been done `active_agent` becomes a `loiterer`.

> ...`wtf()`
>> Throughout this code black when the fickle finger of fate is at work, the *'where's the fire'* `_wtf()` is called to handle anything that's flung its way.  We will try and handle any known-knowns that could come our way later.

## Loiter Agent

So, above, we provided the 'activate_agent' instruction, now we need to build the instruction for `loiterise_agent`...

```Diego
begin_instruct(loiterise_agent)_for(loiterer);

    with_robot(loiterer)_loiterat()_placeat(perimeter_cc);

end_instruct(loiterise_agent);
```
> `with_robot(loiterer)_loiterat()_placeat(perimeter_cc);`
>> There are actually two loitering agents, at this time we do not need to separate/differentiate them apart because this command is executed as a 'blanket' command (by default) for both (or any) robot (or thingies) sobriquetled `loiterer`.

The default loitering parameters have been previously _drilled into_ these drones when they were young, so there is no need to repeat them, just instruct the drones to `_loiterat` and they will know what to do.  If they don't, there are many available packaging tools, which they can upgrade with: `apt_me()_forwhat(loiter);`

## Chain Reactions

Now the cornerstone of the Persian Chain Movement is to chain reaction, which occurs just before the `active_agent` arrives at it's endpoint on rosary `perimeter_cc`.  The chain reaction is tiggered by the `active_agent` drone executing the `start_persian_chain` instruct...

```Diego
begin_instruct(start_persian_chain)_for(loiterer);

    with_sobriquet(loiterer)_cardinatat()_placeat(perimeter_cc)_orderat(highest, 1);

    with_waypoint()_placeat(perimeter_cc)_sobriquet(active_startpoint)_forwho(loiterer_1);
    go_robot(active_agent)_rosary(perimeter_cc)_goto(active_startpoint) ? exec_instruct(activate_agent)_for(active_agent) : ;

    with_waypoint()_placeat(perimeter_cc)_sobriquet(active_startpoint)_forwho(loiterer_2);
    with_robot(loiterer_1)_sobriquet(loiterer);


end_instruct(start_persian_chain);
```

>> If we did need to separate/differentiate them, we could use the `_cardinatat` postposition such as: `with_sobriquet(loiterer)_cardinatat()_placeat(perimeter_cc);`
    
Clone Protocol 66


## End Namespace

```Diego
use_namespace(persian_chain_demo);
```