*[ripl]:Robot Instruction Programming Language
*[uuid]:Universally Unique IDentifier
*[AI]: Artificial Intelligence
*[KIA]: Killed In Action
*[PCS]: Personal Communication System
# Tank Intercept Tutorial
## Introduction
This tutorial, '**Tank Intercept Tutorial**', will demonstrate an approach to develop a set of instructions, using the **GoDiego** robot instruction programming language [ripl], for a military application.

There are eight steps in this tutorial which must be followed sequentially.  A full set of code is provided at the end of tutorial.  For the impatience or code-phobic go here, to get the code.

## Scenario
Please note, this scenario is fictional (i.e. not a real in the physical world).  This is stated because it involves killer robots, if the idea of killer robots is offensive to you then please leave this tutorial.

The scenario involves a battlefield with two opposing forces battling each other.  The ailed force (*us*) is armed with nine battle-ready robots: four gunner robots (one ground-to-air, three ground-to-ground); four intelligence/surveillance robots (three ground robots, one drone); and one mule-type robot.  The enemy force (*them*) have a traditional armoury consisting of: three manned tanks, one manned armoured personnel carrier, and one aircraft.  In terms of personnel, *us* have one guy (*with his robots*), while *them* have 21 soldiers, ranging from refuelling guys, tank drivers and co-drivers, to, aircraft pilots, etc.

Both forces have a base setup of each opposing corner of the map, but this is unknown to each force.  The enemy have a two tanks (each with three soldiers) on manoeuvres to an area of the map they believe their enemy (*us*) are, we are not there.  However, *us* have previously spotted the tanks using our drone.

The goal is to command the squad of robots to intercept and destroy the tanks.  Since this is a scenario that wasn't planned for, the _diego_ instructions will have to be executed on a run-time (*ad-hoc*) approach.

## Tutorial

### Players
So let's introduce our assets.  We have one human known in the real physical world as Fred.  In _diego_ he is known as `fred` with a secret uuid ^(version^ ^4)^  of `10ef559e-24f8-49ac-a6ae-a9c85430e822`, please don't tell the enemy that!

Fred has the following robots:
- `alpha`: A gunner robot with a huge ground-to-air missile launcher
- `beta`: A gunner robot with a large (tank busting) gun.
- `gamma`: Another gunner robot with a large (tank busting) gun.
- `delta`: A sniper robot with long-range sniper armaments.
- `epsilon`: A camouflaged surveillance ground robot.
-  `zeta`: Another camouflaged surveillance ground robot.
- `eta`: Yet another camouflaged surveillance ground robot.
- `theta`: A surveillance drone (small scale).
- `iota`: A mule robot.

The map is called (as least to *us*) as `warnia`, a global type map.

## Step 1: Follow the tanks
This tutorial starts with a call coming in from the drone, `theta`, as a call command:
```diego
  call_foreigner(foreigner1, f9285065-e630-4831-b166-9507a1d5ec64);
  call_foreigner(foreigner2, 471b5552-9273-49b2-837b-4b6df049cd5d);
  call_foreigner(foreigner3, af4d7a32-d9c2-4c7a-94a9-f2b588768e93);
```
The drone, `theta`, has been taught (machine learning) to recognise a tanks. `theta` has determined it has seen three tanks and reports them to the whole swarm (`fred` and all the robots).  These are the first tanks `theta` has seen since being alive and incrementally labels them as `foreigner1`, `foreigner2` etc., and gives each one a uuid.

At this point every robot, including `fred`s computer will remember `foreigner1` into their world memory, `fred` can refer to it as `foreigner1`, the robot (internally) will refer to it as `f9285065-e630-4831-b166-9507a1d5ec64`.  The same with the other *foreigners*.



The AI in `theta` determines the type of tank and reports this to the others (*in case it is KIA*):
```diego
  ident_foreigner(foreigner1)_species(mech)_model(m3a2_bradley);
  ident_foreigner(foreigner1)_species(mech)_model(m3a2_bradley);
  ident_foreigner(foreigner1)_species(mech)_model(m3a2_bradley);
```
`theta` has determined '`foreigner1` as being a `mech` (i.e. not `organic`), and a MC Bradley tank. `fred`s computer and all the robots will remember this.


```diego
  rename_label(foreigner1)_to(tank1);
  rename_label(foreigner2)_to(tank2);
  rename_label(foreigner3)_to(tank3);
  label(tanks)_for(tank1, tank2, tank3);
  
  join_swarm(follow tanks)_for(delta, epsilon, zeta);
  form_swarm(follow tanks)_as(vee snoop, vee);
    with_formation(vee snoop)_pos(0)_for(epsilon);
    with_formation(vee snoop)_pos(1)_for(zeta);
    with_formation(vee snoop)_pos(2)_for(delta);

with_swarm(vee snoop)_snoop(tanks);
```
 
```diego
join_swarm(head off tanks)_for(beta, gamma)_form(line intercept, line)

add_point(head off point)_at(warnia, 23.54345, 23.3232, 4.334)_for(beta, gamma);

go_point(head off point)_for(beta, gamma) ? with_swarm(head off tanks)_intercept(tanks)_atfuture();
with_swarm(head off tanks)_intercept(tanks)_atfuture() ? kill_mech(tanks);
kill_mech(tanks);
```

```diego
  detect_human();
  call_human(human45, a2b9f7dd-606b-4fd0-923f-a4ed25d53e90);
  kill_human(human45)_for(delta);
  #
  
  
  	

```

> Written with [StackEdit](https://stackedit.io/).


`human1` selects robot `alfa` to PCS mode:
```diego
  with_robot(alfa)_mode(pcs)_for(human1);
```
`human1` selects robot `bravo` to PCS mode when robot `alfa` is already in PCS mode:
```diego
  with_robot(alfa)_mode(standby);
  with_robot(bravo)_mode(pcs)_for(human1);
  ```
`human1` selects robot `charlie` to follow UWB sensor `c4n34` :
```diego
  with_robot(charlie)_mode(follow)_follow(c4n34, uwb);
```
`human1` selects robot `delta` to follow optical sensor `665b-aef3c` :
```diego
  with_robot(charlie)_mode(follow)_follow(665b-aef3c, optic);
```
`human1` selects robot `echo` to autonomously go to point ` :

