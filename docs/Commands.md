# Tutorial

## Requirements
The problem we are going resolve in this tutorial involves six large-scale logistical robots ('*mule*' type robots), three factories, one showroom, and, one fuel station, all in the physical human world.  The requirement is to instruct the six robots to work as a swarm (team based, not form based) and perpetually keep the supply chain between each factory and the showroom, 24 hours/7 days per week.

The sole developer and human interaction with the swarm of robots, to begin with, is Bob.
## Variables
First we are going to set the global variables for displaying the map for Bob.  The map-type is the physical world (i.e. Earth) so the ```map_type``` should be set to ```global``` and not ````local````.  This means we will be using lat., long., alt. coordinates for all our position.  The coordinate system is already defaulted to ```decimal_degrees```, so we will not bother to set this global variable (usually referred as just '*global*').

The ```map_centre``` and ```map_zoom``` defaults are set up.  The location in the world we are working with is north of Brisbane, Queensland, Australia.

### Globals
```yaml
globals:
  map_type: global
  map_centre: -27.30948, 152.98256, 18.00000
  map_zoom: 12
```
### Capables
The '*capables*' are also global variables but developer specific rather the Diego Engine specific like the '*globals*'.  They are placed in the diego file so the data can be changed at design or run-time by ```bob``` using ```set_capable(```*```capable moniker```*```)``` command.
```yaml
capables:
- moniker: ready for loading
  data: /usr/share/xemacs21/xemacs-packages/etc/sounds/boing.wav
```
We have only one '*capable*' which points to a '.wav' file used for playing a sound.  We will see this '*capable*' used later in this tutorial.
### Humans
There is only one human involved in the '*diego*', monikered as '*bob*'.  Bob is the only human interaction and communication for the robots. Human interaction in the real physical world is required, such as refueling, loading and unloading payloads, other road users etc., however these humans need not be declared in the '*diego*',

Only the moniker of the human is need for this tutorial, however, we have given Bob a *robo-* rank of ```o4``` (*robotenant*). Bob's *robo-* rank is not required for this tutorial but added for demonstration purposes.
```yaml
humans:
- moniker: bob
  rank: o4
```
### Robots
There are six robots, monikered after the first six letters of the Arabic alphabet.  Each robot has different payload capacities and fuel consumption.

The ```payload_weight_capacity``` is the weight limit for each robots payload in Kg.

The ```fuel_consumption``` is the consumption of diesel fuel consumed in L/100Km.
```yaml  
robots:
- moniker: alif
  payload_weight_capacity: 6100
  fuel_consumption: 12.5
- moniker: ba
  payload_weight_capacity: 7200
  fuel_consumption: 12.1
- moinker: ta
  payload_weight_capacity: 7000
  fuel_consumption: 11.8
- moniker: tha
  payload_weight_capacity: 8845
  fuel_consuption: 13.8
- moniker: jim
  payload_weight_capacity: 8300
  fuel_consuption: 12.5
- moniker: ha
  payload_weight_capacity: 6900
  fuel_consuption: 12.4
```
All measurements use the metric system by default, but this can be changed at design-time using the ```measure_system``` global; adding ```set_measures``` in the diego code; or, in run-time using the ```set_measures(```*```measure_type```*```)``` call.
### Points
The pre-defined points on the map will be the factories, the showroom and the fuel station.

Since we are using the ```global``` *map_type* ```loc``` will be used (instead of ````pos````) to provide the specific location on the points.  The ```z-alt```  value (*altitude*) has been kept at 18m, roughly the correct elevation of these points on Earth.  Since all the robots in this tutorial are ground based robots the altitude (used as elevation) is of no concern for this tutorial.
```yaml
points:
- moniker: factory 1
  loc: -27.31556, 152.97592, 18.00000
- moniker: factory 1 bay 1
  loc: -27.31556, 152.97592, 18.00000
- moniker: factory 1 bay 2
  loc: -27.31556, 152.97592, 18.00000
- moniker: factory 1 bay 3
  loc: -27.31556, 152.97592, 18.00000
- moniker: factory 2
  loc: -27.32559, 152.99008, 18.00000
- moniker: factory 3
  loc: -27.28723, 152.98965, 18.00000
- moniker: showroom
  loc: -27.30597, 152.99015, 18.00000
- moniker: fuel station
  loc: -27.32642, 152.97474, 18.00000
````
### Routes
A *diego* can have no routes defined at start up and routes can be calculated; requested from map providers; shared; broadcast etc. between robots and humans in run-time, however, it is recommended for humans to provide all the possible variables needed by the robot(s) before the *diego* runs on each robot.

There are four routes defined, at the moment we will just moniker them, with self-explanatory monikers.  We will use a map provider to give us the route from any point to the fuel station.
```yaml
routes: 
- moniker: factory 1 to factory 2
- moniker: factory 2 to factory 3
- moniker: factory 3 to showroom
- moniker: showroom to factory 1
```
>\> Next Step: Instructions

## Instructions
All diego instructions must start with the ```go_diego``` command.  We will add the ```north brisbane supply chain management``` *diego_moniker*.  All monikers can be in any case, however, to avoid link bugs in the code, it is recommended to use all lowercase, and never use the characters ``` , ( ) ? : ```.  White-space can be used for monikers, but white-space is never used when entering types.
```diego
go_diego(north brisbane supply chain management);
```
We start the '*diego*' with all six robots unpacked and lined up on the car park of ```factory 1```. We switch each robot on and then we must decide who goes first.  We can leave the robots to do this, however, just for the initial (once-only) '*out of the box allocation*' Bob will decide from the outside physical world. 
````diego
start_instruct(out of the box allocation)_asvirgin();

begin_instruct(out of the box allocation);

  listen_point(factory 1) ? start_instruct(load at factory 1);

  keep_listening();

end_instruct(out of the box allocation);
````
The ````start_instruct(out of the box allocation)_asvirgin()```` command can be placed in this location (below ````go_diego````), however, it is common practice to place the first ```start_instruct``` command at the bottom of the program.  It is really up to the developers preference. The ```_asvirgin()``` parameter-less sub command tells the robot to execute the ```instruct``` once-only (even if the robot is switched off).[^switch_off_robot_equals_murder]

We create a simple ```instruct``` using ```begin_instruct(out of the box allocation)```. The ```instruct``` only creates a _point listener_ on *factory 1* point moniker, using ```listen_point(factory 1)``` command.   The ```listen_point``` command has a _hey_diego_ command, but no _oh_diego_ command.

The ```keep_listening()``` command will keep each robot waiting for a _point call_, and prevent the ```end_instruct``` command from executing and finishing the '*out of the box allocation*' ```instruct``` prematurely.

Meanwhile, in the real physical world, Bob has a tablet computer connected to the swarm network and through his GUI calls each robot by name using the ```call_point``` command, first for ```alif``` robot...
```diego
call_point(factory 1)_for(alif)
``` 
... and then for the other robots...

If at this point Bob had sent ```call_point(factory 1)``` with no ````_for```` sub command, all the robots would execute the  '*out of the box allocation*' ```instruct``` at the same time.  This would not cause a problem as each robot has good manners and will and give way to each other, or at least inform the human(s) (that's ```bob```) of their predicament.

When Bob sends the ```calll_point``` to ```alif```, ```alif```, the robot, will pick this up at command ```listen_point(factory 1)``` and its _hey_diego_ event will be triggered.  Then the _program cursor_ will execute  ```start_instruct(load at factory 1)``` .  This will break in the '*out of the box allocation*' ```instruct``` to go on to the '*load at factory 1*' ```instruct```, marking the ```instruct```s end, which would call the _hey_diego_ event of ```end_instruct(load at factory 1)``` (if there was one).

>\< Previous Step: Diego Declarations
\> Next Step: Load at Factory One








```diego
begin_instruct(load at factory 1)

  go_point(factory 1) ? check_point(factory 1 bay 1);
  
  check_point(factory 1 bay 1) ? go_point(factory 1 bay 1) : check_point(factory 1 bay 2);
  check_point(factory 1 bay 2) ? go_point(factory 1 bay 2) : check_point(factory 1 bay 3);
  check_point(factory 1 bay 3) ? go_point(factory 1 bay 3) : 

  go_point(factory 1 bay 1) ? alert_world(ready for loading);
  go_point(factory 1 bay 2) ? alert_world(ready for loading);
  go_point(factory 1 bay 3) ? alert_world(ready for loading);
  
  alert_world(ready for loading)_until(acknowl);

  listen_call(payload loaded)_onlyme() ? start_instruct(supply to factory 2);

  keep_listening();
  
end_instruct(load at factory 1);

begin_instruct(supply to factory 2);

  go_point(factory 2);
  
end_instruct(supply to factory 2)


start_instruct(out of the box allocation)_asvirgin();
```
ddd
...
```call_point(factory 1)_for(alif)```




> Written with [StackEdit](https://stackedit.io/).

[^switch_off_robot_equals_murder]: Killing a robot is offensive and should be avoided.  Switching a robot off is effectively killing the robot.  In order for a robot to learn from its experiences and knowledge, both personal and shared, it needs to be kept alive and have very little to zero reincarnations.  Each robot has a short-term memory (which is wiped when switched off) and a long-term memory (a database), which could become damaged if a robot is switched off.

