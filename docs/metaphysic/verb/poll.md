# Poll (verb)

# Pollsters
## poll_distance(*moniker*)
#### poll_distance(*point_moniker*)
#### poll_distance(*point_moniker*)*[...]*_by(*distance_metric*)
A robot will poll all robots for their distance to *point_moniker* from their current position.  The additional *distance_metric* sub command determines the calculation used in the return poll. *distance_metric* is a enumerator:
|```distance_metric```| Description |
|--|--|
| ```direct``` | Calculates the distance based on 'euclidean distance' calculation on the ```local``` map and ```local``` map types.  For the ```global``` map and ```global``` map types the ‘haversine’ formula is used to calculate the great-circle distance.<br> Distance is returned in metres.   |
| ```cityblock``` | Calculates the distance based on 'manhattan distance' calculation on a  ```local``` map and ```local``` map types.  For the ```global``` map and ```global``` map types the ‘haversine’ formula is used to calculate the great-circle distance between each _nth_ axis..<br>Distance is returned in metres.   
| ```learned``` | Calculates the distance using averaged odometric past knowledge (if any).  Where the robot has no past knowledge, direct distance is used.<br>Distance in returned in metres with an additional percentage of _calculated_ distances (against direct distances) used.<br>**Note: By using the ```_under(```*```condition_moniker```*```)``` sub command the ```calc``` distance calculation will only use past knowledge matching the *```condition moniker```*.** |
<sub>For a simplified explanation of 'euclidean' and 'manhattan' distance calculations see:  https://www.analyticsvidhya.com/blog/2020/02/4-types-of-distance-metrics-in-machine-learning/</sub>

#### poll_distance(*route_moniker*)
#### poll_distance(*route_moniker*)_at(*start_point*, *end_point*)
#### poll_distance(*start_point*, *end_point*)

### poll_distance(*point_moniker*)_in(*distance*)

## poll_energy(*moniker*)
#### poll_energy(*point_moniker*)
#### poll_energy(*route_moniker*)
#### poll_energy(*route_moniker*)_at(*start_point*, *end_point*)


, unanimous__by(direct)
Each robot will send a 'poll' as: ```poll_distance(rallying point, unanimous__by(direct)```, and, in turn, each robot will return their results as ```poll_distance(rallying point)_in(```*```metres```*```)```.

Each will robot will wait for a unanimous consensus and the winner will run ```call_point(sentry point)``` with it's current position.  The loser(s) will run ```listen_point(sentry point)```.
