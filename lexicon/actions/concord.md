## set_concord set_consensus
Sets the consensus to be used in polls.

The scope of the ```set_consensus```  settings is determined by the ```set_consensus``` command location in the diego code.  If the ```set_consensus``` command is placed after the ```go_diego``` command but before any ```instruct``` the consensus setting will be applied to the whole diego, unless overridden by the next ```set_consensus``` command in the diego code flow.

If the ```set_consensus``` command is placed after a ```begin_instruct``` command, the scope of consensus will be applied to the ```instruct```, unless overridden by the next ```set_consensus``` command (in the same ```instruct``` or a nested ```instruct```) in the diego code flow.

The lowest level of override occurs with the ```_with_consensus``` sub command, available on most decision commands.

The ```set_consensus``` command has privilege definition ability using both and each of the ```_for``` and  ```_not``` sub commands.

If the  ```set_consensus``` command is never used, the consensus is defaulted to *unanimous*.

The ```set_consensus``` command does **not** set consensus on elections, only on polls and robot decisions.

#### set_consensus(*consensus_type*)
Sets the consensus of *consensus_type*:
| ```consensus_type``` | Description |
|--|--|
| `dead_unanimous`<br>`unanimous_wait_for_the_dead` | Decisions are made only when there is a unanimous result but only after all dead robots have been resurrected and then resulted. |
| ```unanimous``` | Decisions are made on an unanimous result, any dead robots are disregarded. |
| ```authority``` | Decisions are based on the result of the highest authority robot(s) (using ```set_authority``` command). |
| ```human_only``` | Decisions can only be made by a human(s).<br>If there are no humans alive, consensus will automatically change to ```authority``` then back to ```human_only``` when one or more humans are resurrected. |
| `dead_majority`<br>`majority_wait_for_the_dead` | Decisions are made on a majority (>=50%) basis of the results over the number of robot members but only after enough resurrected robots have resulted to make the majority (if required). |
| ```majority``` | Decisions are made on a majority (>=50%) basis of the results over the number of robot members. |
| ```decisive``` | Decisions are made on the majority results when the decisiveness limit (defaulted to 5 secs or the value set with the ```set_decisiveness``` command) has expired. |
| ```first``` | Decisions are made on the first result. |
#### set_consensus(*consensus_type*)_for(*moniker1*, *n...*)
Consensus of *consensus_type* will apply only to the whitelist of (*moniker1*, *n...*) of monikers (robots, swarms, labels of).
#### set_consensus(*consensus_type*)_not((*moniker1*, *n...*)
Consensus of *consensus_type* will **not** apply to the blacklist of (*moniker1*, *n...*) of monikers (robots, swarms, labels of).  The defaulted or last known consensus will apply to those blacklist monikers.
#### set_consensus(*consensus_type*)_for(*moniker1*, *n...*)_not(*moniker1*, *n...*)
An apply-list with a no-apply-list of monikers (robots, swarms, labels of) for consensus of *consensus_type*.