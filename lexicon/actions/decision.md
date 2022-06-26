## set_decisiveness
Sets the decisiveness in milliseconds to be making decisions, particularly of polls.

The scope of the ```set_decisiveness```  settings is determined by the ```set_decisiveness``` command location in the diego code.  If the ```set_decisiveness``` command is placed after the ```go_diego``` command but before any ```instruct``` the decisiveness setting will be applied to the whole diego, unless overridden by the next ```set_decisiveness``` command in the diego code flow.

If the ```set_decisiveness``` command is placed after a ```begin_instruct``` command, the scope of decisiveness will be applied to the ```instruct```, unless overridden by the next ```set_decisiveness``` command (in the same ```instruct``` or a nested ```instruct```) in the diego code flow.

The lowest level of override occurs with the ```_with_decisiveness``` sub command, available on most decision commands.

The ```set_decisiveness``` command has privilege definition ability using both and each of the ```_for``` and  ```_not``` sub commands.

If the  ```set_decisiveness``` command is never used, the consensus is defaulted to *unanimous*.

The ```set_decisiveness``` command does **not** set consensus on elections, only on polls and robot decisions.

#### set_decisiveness(*time_period*)
Sets the decisiveness is a *time_period* (*in milliseconds*) given to robot(s) when making decisions.  When a robot polls other robots the decisiveness timer will start.  While collecting results the decisiveness timer will trigger when the *time_period* (*in milliseconds*) has expired.  For decisions with  ```decisive```  consensus the majority result will be chosen upon the decisiveness timer triggered.
#### set_decisiveness(*time_period*)_for(*moniker1*, *n...*)
Decisiveness of *time_period* will apply only to the whitelist of (*moniker1*, *n...*) of monikers (robots, swarms, labels of).
#### set_decisiveness(*time_period*)_not((*moniker1*, *n...*)
Decisiveness of *time_period* will **not** apply to the blacklist of (*moniker1*, *n...*) of monikers (robots, swarms, labels of).  The defaulted or last known consensus will apply to those blacklist monikers.
#### set_decisiveness(*time_period*)_for(*moniker1*, *n...*)_not(*moniker1*, *n...*)
An apply-list with a no-apply-list of monikers (robots, swarms, labels of) for decisiveness of *time_period*.