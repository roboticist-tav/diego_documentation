# Labelers
Labeler commands are used to attach a label to an '*object(s)*' for a limited scope.  Labelling is useful for robot segregation and compartisation.

## label_robot
#### label_robot(*label_moniker*)_for(*robot_moniker1*, *n...*)
## label_winner
## label_ranker
## label_human
## label_inanimate(*animate_moniker*)
## label_winner()
#### label_winner(*label_moniker*)
## label_ranker()
#### label_ranker(*label_moniker*)_for(rank1, n...)
#### label_ranker(*label_moniker*)_for(rank1, n...)

#### label_ranker(rank1, n...)_
## label_authority
Labels list of monikers (or all) with authorization ranks.  Authorization ranks are used in make decisions upon ```authority``` consensus.
#### label_authority(*rank*) &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; label_authority(*rank_moniker*)
Sets all robots (robots, swarms, labels of) under the scope of ```instruct``` then ``go_diego``` with authorization rank '*rank*'.

A '*rank_moniker*' (shown in table below) can be used in place (or interchangably) with '*rank*'.
> Warning:
> Using the ```label_authority``` command with no privilege sub commands will set **all** robots/swarms to the *rank* which could result in delays/warnings/errors in achieving consensus.

Ranks and rank monikers available are shown below:
| ```rank``` | Ensignia | Rank Moniker | Example Human Equivalent[^human_ranks]<br>Army / Navy / Air Force / Police (Feds) |
|--|:--:|--|--|
| o11 | | robomiral | Field Marshal / Admiral of the Fleet / Marshal of the air force / Commissioner |
| o10 | | robommisssioner | General / Admiral / Air Chief Marshal /  Deputy Commissioner / Director |
| o9 | | roborshal | Lieutenant General / Vice Admiral / Air Marshal /  Assistant Commissioner |
| o8 | | roboneral | Major General / Rear Admiral / Air Vice-Marshal / Commander / Chief od Staff |
| o7 | | robomodore | Brigadier / Commodore / Air Commodore / Superintendent |
| o6 | | robolonel | Colonel / Captain / Group Captain / Deputy Director |
| o7 | | robommander | Lieutenant Colonel / Commander / Wing Commander |
| o6 | | robojor| Major / Lieutenant Commander / Squadron Leader |
| o5 | | roboptain | Captain / Lieutenant / Flight Lieutenant |
| o4 | | robotenant | Lieutenant / Sub Lieutenant / Flying Officer / Inspector |
| o3 | | roboilot | 2nd Lieutenant / Midshipman / Pilot / Sergeant |
| o2 | | roborector | Officer / Officer / Flight Cadet / Leading Senior Constable |
| o1 | | robofficer | Officer / Officer / Flight Cadet / Leading Senior Constable |
| e4 | | robonstable | Sergeant Major / Chief Petty Officer / Warrant Officer / Senior Constable |
| e3 | | robergeant | Sergeant /  Petty Officer / Sergeant / Constable First Class |
| e2 | | roborporal | Bombardier / Leading Seaman / Corporal / Constable / Special Agent |
| e1 | | roboagent | Private / Seaman / Airman / Recruit / Trainee |
[^human_ranks]: Australian military and a mix of state and federal Australian and US FBI police force ranks were used for equivalence.
#### label_authority(*rank*)_to(*moniker1*, *n...*) &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; label_authority(*rank_moniker*)_to(*moniker1*, *n...*) 
Sets monikers (robots, swarms, labels of) in the whitelist under the scope of ```instruct``` then ``go_diego``` with authorization rank '*rank*'.
#### label_authority(++)

#### label_authority(*rank*)_to(*moniker1*, *n...*)

####  label_authority(++)_to(*moniker1*, *n...*) &nbsp; &nbsp;authority_promote(*moniker1*, *n...*)

#### set_authority(*rank*)_to(*moniker1*, *n...*)
#### set_authority(*rank*)_not(*moniker1*, *n...*)

## alert_human(*moniker*)

## find_human(*human_moniker*)
## listen_find(*moniker*)





## ask_point(*point_moniker*)

## report_energy(*route_moniker*)





