# Demonstrating crosschain in a robot example

In this example we will be demonstrating hashtables and crosschain processes.

The elements and players in this scenario are `the base`, a geographic area (a `roi`) where human `Fred` and robot `alif` reside, initially.  There is a geographic area and communication zone ('mist') called `the mist`, a distance way from `the base`, enough that the robot `alif` will have to travel there before it can communicate with the other robots in `the mist`.  The other robots in `the mist` are: robot `bahh`, robot `tahh` and robot `thah`.  Within `the mist` communication is mostly reliable but infrequently becomes a bit sketchy.  All the robots and human know each other.

A human known a `Bob`, a a thingy called `daisy` make cameo appearances.

The goal is for 'Fred' to pass on a secret code to robots `bahh`, `tahh` and `thah`, and collect stat(istic)s, eye colour and colour of their socks. Then return back to base.

> ## Step 1: Write the instruction...

 So, Fred gets to work, opens his IDE and writes the following Diego code:

```Diego
begin_instuct(get_stats_from_bahh_tahh_and_thah)_forof(alif);
    goto_mist(the_mist)_you()?:;
        ? proclaim_var(secret_code)_value(1234)_forof(bahh,tahh,thah);
        : exec_instruct(report_back_to_base)_you();
    call_robot()_them()_unanimous()?|;
        ? ask_stat(eye_colour):;
            : report_err()_you();
        | ask_stat(sock_colour)_them():;
            : report_err()_you();
    ask_var(secret_code)__them();
    exec_instruct(report_back_to_base)_you();
end_instruct(get_stats_from_bahh_tahh_and_thah);
```

The command `exec_instruct(report_back_to_base)` executes (starts off) a previous instruction given and known to `alif` in this example.  Human interpretations of the commands in this instruction are shown, as well as, the crosschain hashtables which will be explained as we go along...

> ## Step 2: `Fred` and `alif` start talking...

Now we will observe the communication between `Fred` and `alif`, both from their perspectives...

Fred sends out the Diego commands by ececuting the _.dgo_ file.  During this process `Fred` (the thingy side of 'Fred') records them for prosperity into memory (`Fred`s hastable)...

### Human `Fred`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Fred`^♠^ | adc3^♠^ | 62e7 | | | `begin_instuct(get_stats_from_bahh_tahh_and_thah)_forof(alif);`<br /><br />_Okay `alif`, so here is what I want you to do..._ |

♠: The caller is actually a uuid, so are the hashes.  They are referred to as hashes for historical reasons.  The hashes have been shorted to 16bit for clarity.
♡: The use of `?` at `? ask_stat(eye_colour)` indicates this command is a *hey_diego* command of the preceding *go_diego* command, in this case: `call_robot()_forof(bahh,tahh,thah)_unanimous()?|;`.  We will see later an example of a sucess and a failure of the `call_robot` command...

The `begin_instuct` command has the `_forof(alif)` postposit to signify that this `instruct` is for the benefit of `alif` only. This is not strictly necessary as the execution of the `instruct` can be better handled by the `exec_instruct` command (we will see later...). If, for some reason, `alif` is not available to execute the command, the `with_instruct` command will be required to reassign the `instruct` to something else, _for example:_ `with_instuct(get_stats_from_bahh_tahh_and_thah)_forof(jeeem)_notforof(alif)`.

`Fred` continues...

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Fred` | c682 | adc3 | | | &nbsp;&nbsp;&nbsp;&nbsp;`goto_mist(the_mist)_you()?:;`<br /><br />_Go to the place where robots `bahh`, `tahh` and `thah` hang out (`the_mist`)._ |
| `Fred` | 53d2 | c682 | | | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`? proclaim_var(secret_code)_value(1234)_forof(bahh,tahh,thah);`<br /><br />_When you get there proclaim them (`bahh`, `tahh` and `thah`) of the secret code._ |




| `Fred` | 438d | 53d2 | | | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`: exec_instruct(report_back_to_base)_you();`<br /><br />_If there are any problems report back to base._ |
| `Fred` | a261 | 438d | | | &nbsp;&nbsp;&nbsp;&nbsp;`call_robot()_forof(bahh,tahh,thah)_unanimous()?!;`<br /><br />_Perform a roll-call for robots `bahh`, `tahh` and `thah`._ |
| `Fred` | 7da0 | a261 | | | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`? ask_stat(eye_colour):;`^♡^<br /><br />_As soon as you get an unanimous response to the roll-call, ask anyone^♢^ their eye colour._ |
| `Fred` | f496 | 7da0 | | | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`: report_err()_you();`<br /><br />_Report anything wrong when you ask their (anyone's) eye colour._ |
| `Fred` | fa7e | f496 | | | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`| ask_stat(sock_colour)_them():;`<br /><br />_As soon as you get an unanimous response to the roll-call, also ask the colour of their (anyone's^♢^) socks._ |
| `Fred` | cb67 | fa7e | | | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`: report_err();`<br /><br />_Report anything wrong when you ask their sock colour._ |
| `Fred` | 5e31 | cb67 | | | &nbsp;&nbsp;&nbsp;`exec_instruct(report_back_to_base);`<br /><br />_If there are any problems report back to base._ |
| `Fred` | 600b | 5e31 | | | `end_instruct(get_stats_from_bahh_tahh_and_thah);`<br /><br />_That's it._ |


♢: There is no explicit discrimination given for both the `ask_stat(eye_colour)` and `ask_stat(sock_colour)` commands, so the diego engine will defer to any global discrimination setting (in the caller), if no such settings exist their will be no discrimination and **anyone** in the mist, `the mist` will respond to these `ask` commands.  Examples of possible discrimination settings include:

+ `ask_stat(eye_colour)_forof(bahh,tahh,thah);` *- explicit discrimination*
+ `ask_stat(eye_colour)_inherit();`*- inherited discrimination*
+ `set_discimination(menage)_givento(call)_value(true);` *- discrimination through menage of all `call`s for this _thingy_*
+ `set_discrimat(menage)_givento(call)_appliedto(robot)_value(true);` *- discrimination through menage of `call`s to `robot` kind* 
+ `set_discriminat(progeny)_givento(call)_value(true);` *- implied discrimination through progeny of all `call`s for this _thingy_*
+ `set_discrimat(progeny)_givento(call)_appliedto(robot)_value(true);` *- discrimination through progeny of `call`s to `robot` kind* 

While `Fred` is talking (to himself), robot `alif` is listening and taking it all in...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Fred` |  |  | adc3 | 62e7 | `begin_instuct(get_stats_from_bahh_tahh_and_thah)_forof(alif);`<br /><br />_Okay `Fred`, I'm talking notes..._ |
| `Fred` |  |  | c682 | adc3 | &nbsp;&nbsp;&nbsp;&nbsp;`goto_mist(the_mist)_you()?:;`<br /><br />_Right, so I go to `the_mist`._ |
| `Fred` |  |  | 53d2 | c682 | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`? proclaim_var(secret_code)_value(1234)_forof(bahh,tahh,thah);`<br /><br />_So, when I get there (`the_mist`) I proclaim `bahh`, `tahh` and `thah` of the secret code, `1234`._ |
| `Fred` |  |  | 438d | 53d2 | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`: exec_instruct(report_back_to_base);`<br /><br />_If there are any problems I will report back to base._ |
| `Fred` |  |  | a261 | 438d | &nbsp;&nbsp;&nbsp;&nbsp;`call_robot()_forof(bahh,tahh,thah)_unanimous()?!;`<br /><br />_Perform a roll-call for robots `bahh`, `tahh` and `thah`._ |
| `Fred` |  |  | 7da0 | a261 | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`? ask_stat(eye_colour):;`^♡^<br /><br />_As soon as I get an unanimous response to the roll-call, I will ask anyone^♢^ their eye colour._ |
| `Fred` |  |  | f496 | 7da0 | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`: report_err();`<br /><br />_I will report anything wrong when I ask anyone's eye colour._ |
| `Fred` |  |  | fa7e^♥^ | f496 | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`| ask_stat(sock_colour):;`<br /><br />_As soon as I get an unanimous response to the roll-call, I will also ask the colour of anyone's socks._ |
| `Bob`^♣^ |  |  | 7f49 | 5598^♣^ | `find_tool(5mm_spanner)_appliedto(robot);`<br /><br />_Ummm, human `Bob` is asking all robots if they know where the `5mm_spanner` is!_ |
| `alif` | a651 | 910a |  | 7f49 | `found_tool(5mm spanner)_forof(Bob)_value(false);`<br /><br />_Sorry `Bob`, I do not know where the `5mm_spanner` is._ |
| `Fred` |  |  | cb67 | fa7e^♥^ | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`: report_err();`<br /><br />_...back to Fred's `instruct`... I will then report anything wrong when I ask their sock colour._ |
| `Fred` |  |  | 5e31 | cb67 | &nbsp;&nbsp;&nbsp;`exec_instruct(report_back_to_base);`<br /><br />_Right oh, if there are any problems I will report back to base._ |
| `Fred` |  |  | 600b | 5e31 |`end_instruct(get_stats_from_bahh_tahh_and_thah);`<br /><br />_Okay, got it._ |

♣:  While `alif` is *transribing* `Fred`s instruction, human `Bob` interrupts the conversation asking all the robots if they know where the `5mm_spanner` is. Note that the ↑hash `5598` of message `910a` **does not** match the ↓hash of the previous message, this indicates to `alif` that this message is not part of the conversation with `Fred` and therefore also not part of the `instruct`.

♥: By matching the ↑hash `fa7e` of message `f3d0` with the ↓hash `fa7e` of message `9cf1`, `alif` can get back to its conversation with `Fred`.

Let's have a quick peep at `Bob`'s crosschain hashtable...

### Human `Bob`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Bob` | 7f49^ʃ^ | 5598 | | | `find_tool(5mm_spanner)_appliedto(robot);`<br /><br />_Do any of you robots kno where the `5mm_spanner` is?_ |
| `alif` |  |  | a651 | 7f49^ʃ^ | `found_tool(5mm spanner)_forof(Bob)_value(false);`^Ꜭ^<br /><br />_Sorry `Bob`, I do not know where the `5mm_spanner` is._ |
| `droid1` |  |  | e0bd | 7f49^ʃ^ | `found_tool(5mm spanner)_forof(Bob)_insub(toolbox_red);`^ⱷ^ ^Ꜭ^<br /><br />_Yeah, the `5mm_spanner` is in the `toolbox_red`._ |

ʃꜬ: Since `Bob`'s *hash matches the ↑hashes from `alif` and `droid1`, `Bob` knows these are responses to his `find_` verb.  If `Bob` wants to respond back he will use the ↓hashes.  The use of `_forof(Bob)_` isn't strickly neccessary as the ↑hash (`7f49`) in `alif`'s and `droid1`'s ledger will be referrenced to `Bob`'s *hash (`7f49`) , it can be omitted.

ⱷ: The `_insub` postposit means _..the preceding part of this command is..._ in `sub`ject `toolbox_red`. See [obs_and_subs.md](obs_and_subs.md).

> ## Step 3: Let's go...

Fred, after running the above code (Step #2), `Fred` checks everything is ready and runs the following command:

```Diego
exec_instuct(get_stats_from_bahh_tahh_and_thah)_you(alif)_them(bahh, tahh, thah);
```

### Human `Fred`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Fred` | 9be9 | 600b | | | `exec_instuct(get_stats_from_bahh_tahh_and_thah)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_you(alif)_them(bahh, tahh, thah);`<br /><br />_Okay `alif`, off you go..._ |

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Fred` |  |  | 9be9 | 600b | `exec_instuct(get_stats_from_bahh_tahh_and_thah)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_you(alif)_them(bahh, tahh, thah);`<br /><br />_Right, here I go..._ |

At this point `alif` will check its memory for the `begin_` and `end_` of the `get_stats_from_bahh_tahh_and_thah` `instruct`, knowing it has most likely come from `Fred`. Another robot, called `Driod1`, is also in ear-shot of `Fred`, but since `Fred` has used `_forof(alif)` and there isn't implication of relaying messages, `Droid1` will ignore this message in its ledger (if it wants to _i.e. has been setup to ignore messages that have nothing to do with it_).

So once `alif` has remembered  `get_stats_from_bahh_tahh_and_thah` it starts to loop through the `instuct`...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `Fred` |  |  | aaf9 | 4816 |`begin_instuct(get_stats_from_bahh_tahh_and_thah);`<br /><br />_Okay, let's get the `instruct`ions to follow..._ |
| `alif` | 44de | a651 | 9778 | aaf9 | `goto_mist(the_mist)_me()?:;`<br /><br />Perform the previously defined action `goto_mist(the_mist)`... |

The `begin_` verb and its command is located in memory, then to signify following the instructions (_any commands after the `begin_` verb_), alif will call the instruction to command itself from the instruction, as can bee seen witht he first command  `goto_mist(the_mist)`.  Since `alif` knows this command is only for itself, it appends `_me()` to the end on the instruction to signify to others this is command `alif` only must follow and this command is not being _re-_commanded by `alif`.

In the physical *real* world `alif` manoeuvres itself along a predefined route (called `base_to_mist`) to get `the mist` where `bahh`, `tahh`, and `thah` are hanging out.

For this example, `alif` is very chatty (has a setting to be chatty from itself, or others), so its going to chat about its achievement and issues...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` | 2e11 | 44de | | 9778 | `goto_mist(the_mist)_me()_success(+103, successful goto);`<br /><br />_Hey (anyone who is interested), I have arrived safely at `the_mist`!_ |
| `alif` | a5ca | 2e11 ||9778| `add_valid(+103, arrival at location)_givento(goto)_appliedto(mist)_specificto(the_mist);`<br /><br />_Note to self, successfully arrived at `the mist`._ |

Two examples are given for robot `alif` to records its own actions, in its own ledger.  The rules of crosschain are that other thingies should have a chain of messages and any broken chain rectified.  So, anyone else in ear-shot of `alif` will record `alif` chatting away to itself. (which we will see later !!!!!!!!!!!!!!!!!!!!!!)

> ## Step 4: Into the mist...

So `alif` has entered `the mist` and will continue following the instructions set by human `Fred` when it was back at `the base`.  Now within `the mist` the robots (and others) can hear `alif` talking and take notice...

`alif` is quick to get into action and gets straight into it, proclaiming `bahh`, `tahh`, and `thah` of the secret code...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` | b707 | a5ca | 4743 | 9778 | ` ? proclaim_var(secret_code)_value(1234)_for(bahh,tahh,thah);`<br /><br />_Proclaim `bahh`, `tahh`, and `thah` of the secret code._ |
| `alif` | ad70 | b707 | | | `proclaim_var(secret_code)_value(1234)_forof(bahh,tahh,thah)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_success(+103, successful proclaim)_me();`<br /><br />_I have proclaimed `secret_code` `1234` to `bahh`, `tahh`, and, `thah`._ |
| `alif` | 32a2 | ad70 | | | `add_valid(+101,proclaim complete)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_givento(proclaim)_appliedto(var)_specificto(secret_code)_me();`<br /><br />✅ _Proclaimed `secret_code` `1234` to `bahh`, `tahh`, and, `thah`._ |

> ### Step 4a: Pssh, I have the secret code...

**Everyone** listens, even a fridge (called `daisy`) that is sitting in the corner in `the mist`!  Let's follow each conversation, one command at a time...


### Robot  `bahh`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |

...it seems robot `bahh` is not listening...

### Robot  `tahh`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` |  |  | b707 | a5ca | `proclaim_var(secret_code)_value(1234)_for(bahh,tahh,thah);`<br /><br />_The `secret_code` is `1234`, thanks `alif`._ |
| `tahh` | 5c52 | 127d | 910a | b707 | `request_gossip()_last(910a)_recent(b707)_forof(alif);` |
| `alif` | | | a651 | 910a |`found_tool(5mm spanner)_forof(Bob)_value(false);` |
| `alif` |  |  | 44de | a651 | `goto_mist(the_mist)_me()?:;` |
| `alif` |  |  | 2e11 | 44de | `goto_mist(the_mist)_me()_success(+103, successful goto);` |
| `alif` |  |  | a5ca |2e11| `add_valid(+103, arrival at location)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_givento(goto)_appliedto(mist)_specificto(the_mist);` |


### Robot  `thah`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` |  |  | b707 | a5ca | `proclaim_var(secret_code)_value(1234)_for(bahh,tahh,thah);`<br /><br />_So the secret code is `1234`, and `bahh` & `tahh` know this `secret_code` also, hey_ |
| `thah` | 107a | 8b74 | 910a | b707 | `request_gossip()_last(910a)_recent(b707)_forof(alif);` |
| `alif` | | | a651 | 910a |`found_tool(5mm spanner)_forof(Bob)_value(false);` |
| `alif` |  |  | 44de | a651 | `goto_mist(the_mist)_me()?:;` |
| `alif` |  |  | 2e11 | 44de | `goto_mist(the_mist)_me()_success(+103, successful goto);` |
| `alif` |  |  | a5ca |2e11| `add_valid(+103, arrival at location)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_givento(goto)_appliedto(mist)_specificto(the_mist);` |

Robots `tahh` and `thah` know robot `alif` very well and both these robots haven't heard whats been going on when `alif` has been away so both of them catch up on gossip.

Out of the three robots, everyone but `bahh` has heard the proclamation. This is because the communication connection for `bahh`, in this case, is a little sketchy.  Since, by default, `proclaim_` does not expect neither a delivery receipt nor a received receipt, `alif` is unaware and will never to know that `bahh` didn't get the proclamation. Also robot 'bahh' would be oblivious to the proclamation.  Furthermore, a 'proclaim_' with no specified delivery or receive receipt will return as a success, the *oh_diego* command, `exec_instruct(report_back_to_base);` will not be executed by `alif`.

Now a twist in this ~~tale~~ example! A fridge called `daisy` is 'diego-compatible' and its part of `the mist` like all the robots there (including **now** `alif`), so, by design, daisy can hear `alif` and also takes notes:

### Fridge `daisy`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` |  |  | b707 | a5ca | `proclaim_var(secret_code)_value(1234)_forof(bahh,tahh,thah);`<br /><br />_The variable `secret_code` is `1234`!_ |

Even though `alif` followed its instructions and proclaimed the variable `secret_code` as `1234` for `bahh`, `tahh`, and `thah`, the `_forof` postposit is meant to differentiate those who should act upon the command, not those who should receive it.  So although `daisy` the fridge knows the `secret_code`, it will not act upon it.  Technically `daisy` will not tell anyone of the secret code, unless  `bahh`, `tahh`, and `thah` or a higher ranking thingy asks for it.

`daisy` has not gossipy like `tahh` and `thah`, since it has changed its default setting for get gossip (`set_gossip()`) from true to false (`set_gossip(false)`) so will keep its blockchain in tact, but has its crosschains broken. Unless it caves into gossip and want to get all the gossip is has missed since it set its _'catch-up-on-gossip'_ setting to false.  Note a thingy can set its gossip to particular thingies, group of thingies, genera of thingy, _etc._.

> ### Step 4b: Attention please

`alif` continues...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` | 1169 | a5ca | bab3 | 9778 | &nbsp;&nbsp;&nbsp;&nbsp;`call_robot()_forof(bahh,tahh,thah)_unanimous()?!;`<br /><br />_Roll Call! This is a roll call for robots `bahh`, `tahh`, and, `thah`!_ |

The `call_` verb demands a reply, and in this actual case a `_unanimous` reply. So the others respond...

### Robot  `bahh`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` |  |  | 1169 | a5ca | `call_robot()_forof(bahh,tahh,thah)_unanimous()?!;`<br /><br />_Roll Call! This is a roll call for robots `bahh`, `tahh`, and, `thah`!_ |
| `bahh` | a14b | 53ce | 910a | 1169 | `request_gossip()_last(910a)_recent(1169)_forof(alif);`<br /><br />_Hey, `alif`, I'm confused, am I missing something you said earlier?_ |
| `alif` | | | a651 | 910a |`found_tool(5mm spanner)_forof(Bob)_value(false);` |
| `alif` |  |  | 44de | a651 | `goto_mist(the_mist)_me()?:;` |
| `alif` |  |  | 2e11 | 44de | `goto_mist(the_mist)_me()_success(+103, successful goto);` |
| `alif` |  |  | a5ca | 2e11 | `add_valid(+103, arrival at location)`<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`_givento(goto)_appliedto(mist)_specificto(the_mist);` |
| `alif` | | | b707 | a5ca | `proclaim_var(secret_code)_value(1234)_forof(bahh,tahh,thah);`<br /><br />_The `secret_code` is `1234`, got it!_ |
| `bahh` | 40c2 | a14b | | 1169 | `here_me();`<br /><br />_Here!_ |
| `tahh` |  |  | 4eae | 1169 | `here_me();` |
| `thah` |  |  | b28f | 1169 | `here_me();` |

### Robot  `tahh`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` |  |  | 1169 | 32a2 | `call_robot()_forof(bahh,tahh,thah)_unanimous()?!;`<br /><br />_Roll Call for `bahh`, `tahh`, and, `thah`!_ |
| `tahh` | 4eae | 5c52 |  | 1169 | `here_me();`<br /><br />_I'm here `alif`!_ |
| `bahh` |  |  | 40c2 | 1169 | `here_me();` |
| `thah` |  |  | b28f | 1169 | `here_me();` |


### Robot  `thah`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `alif` |  |  | 1169 | 32a2 | `call_robot()_forof(bahh,tahh,thah)_unanimous()?!;`<br /><br />_Roll Call!_ |
| `thah` | b28f | 107a | | 1169 | `here_me();`<br /><br />_Present and correct!_ |
| `bahh` |  |  | 40c2 | 1169 | `here_me();` |
| `tahh` |  |  | 4eae | 1169 | `here_me();` |

Robots `tahh` and `thah` have a straightforward conversation to the roll call.  As for robot `bahh` we can see one side of its conversation with `alif`, so let's look at `alif`'s crosschain hashtable first...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |
| `bahh` | da16 | 1169 | a14b | 53ce | `request_cmd(32a2)_forof(alif);`<br /><br />_Roll Call! This is a roll call for robots `bahh`, `tahh`, and, `thah`!_

`bahh` | 32a2<br /><br />_Hey, `alif`, I'm confused, am I missing something you said earlier?_



----

e028----886481fbf8af

e15d3907-477d-44af-bf5f-e67758423484

newbi

> ### Look into my eyes...

`alif` continues...

### Robot `alif`

| caller  | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
| :-----: | :---: | :---: | :---: | :---: | ---- |  
| `alif` | 32a2 | b707 |`ask_stat(eye_colour);`<br />What colour eyes do you have? | 4904 |  | |  |





### Robot `alif`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|
| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | 4904 | b707 | | 32a2 |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? |  | 4904 | | |







, and then asking everyone in `the mist` their eye colours and colours of their socks. 

Everyone in the mist hears `alif` ask for the colour of their eyes...

### Robot  `bahh`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|
| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | b707 | 0f57 |
| `bahh` | `tell_stat(eye_colour)_value(#4a83b6);`<br />Blue | b9f2 | 9599 | 8a85 | b707 |




--------

----90bbe3eb



### Robot  `tahh`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 7b72 | 8771 | 4904 |
| `tahh` | Blue | c269 | 7b72 | | 4904 |
| `bahh` | Brown | bdfc | c269 | eab7 | 4904 |


| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | 2b38 | b577 |b707 |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 274b | 2b38 | 4904 |
| `bahh` | `tell_stat(eye_colour)_value(#4a83b6);`<br />Well, `alif` I have blue eyes. | 8a85 | 274b | | b707 |
| `tahh` | Blue | 5fd2 | 4f09 | c269 | 4904 |
| `bahh` | Brown | eab7 | 5fd2 | | 4904 |


### Robot  `thah`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|    
| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | f0d4 | 5d16 |b707 |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 532a | f0d4 | 4904 |


| `bahh` | `tell_stat(eye_colour)_value(#4a83b6);`<br />Blue | 4714 | 4904 | 8a85 | b707 |
| `tahh` | Blue | 05fb | cec8 | c269 | 4904 |
| `bahh` | Brown | 4bee | 05fb | eab7 | 4904 |




```Diego
begin_action(goto_the_mist)_givento(goto)_appliedto(mist)_specificto(the_mist)_forwhat(robot);
    goto_point(base) ? : ;
    go_route(base_to_mist) ? with_point(mist_centre)_report() : report_err();
    with_action(goto_the_mist)_msg(⚙️me⚙️ @ the mist);
end_action(goto_the_mist);
```
_givento({verb})
_appliedto({object})
_specificto({postpos})
_forwhat(object_moniker)
_forwho()



----

`grant_shell()_allowfor({moniker1|uuid1}[, ... {moniker_n|uuid_n}])_for({moniker1|uuid1}[, ... {moniker_n|uuid_n}]);`
`grant_shell()_allowforme()_for({moniker1|uuid1}[, ... {moniker_n|uuid_n}]);`



```Diego
? add_valid({code},{description})       : add_error({code},{description})


set_discriminat(progeny)_givento(call)_value(true);

progeny
inherit
initial
menage



set_discrimat(progeny)_givento(begin)_appliedto(instruct)_value(true);

set_discriminat({disciminat_type})_givento({verb})_appliedto_({object})_value({value});


```

### Human `Fred`
| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|

### Robot `alif`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|
| `alif` | `proclaim_var(secret_code)_value(1234);`<br />The secret code is 1234  | 0f57 | 9c1c | | |
| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | b707 | 0f57 | |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 4904 | b707 | |
| `bahh` | `tell_stat(eye_colour)_value(#4a83b6);`<br />Blue | 4714 | 4904 | 8a85 | b707 |
| `tahh` | Blue | 05fb | cec8 | c269 | 4904 |
| `bahh` | Brown | 4bee | 05fb | eab7 | 4904 |

### Robot  `bahh`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|
| `alif` | `proclaim_var(secret_code)_value(1234);`<br />The secret code is 1234  | b577 | b041 | 0f57 | |
| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | 2b38 | b577 |b707 |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 274b | 2b38 | 4904 |
| `bahh` | `tell_stat(eye_colour)_value(#4a83b6);`<br />Blue | 8a85 | 274b | | b707 |
| `tahh` | Blue | 5fd2 | 4f09 | c269 | 4904 |
| `bahh` | Brown | eab7 | 5fd2 | | 4904 |

### Robot  `tahh`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|
| `alif` | `proclaim_var(secret_code)_value(1234);`<br />The secret code is 1234  | 8771 | aae6 | 0f57 | |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 7b72 | 8771 | 4904 |
| `tahh` | Blue | c269 | 7b72 | | 4904 |
| `bahh` | Brown | bdfc | c269 | eab7 | 4904 |
| `bahh` | `tell_stat(eye_colour)_value(#4a83b6);`<br />Blue | 69da | bdfc | 8a85 | b707 |

### Robot  `thah`

| caller  | cmd. | *hash | ←hash | ↓hash | ↑hash |
|:-:|---|:-:|:-:|:-:|:-:|    
| `alif` | `ask_stat(eye_colour);`<br />What colour eyes do you have? | f0d4 | 5d16 |b707 |
| `alif` | `ask_stat(sock_colour);`<br />What colour socks do you have? | 532a | f0d4 | 4904 |


      e13d 81b7


`tahh` : `ask_cmd(b707,8a85)_for(bahh);`
`bahh` : `ask_stat(eyes_colour)_from(alif)_for(tahh);`
