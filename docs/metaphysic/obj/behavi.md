# Behaviour (object)
The `behavi` object reprent





# Behaviours

```Diego
begin_behaviour();

end_behaviour();
```



begin_behaviour(envelop)

envelop_robot()


begin_verb(envelop)

envelop_subject(target_poi)_for(drone_1);
with_subject(target_poi)_envelop()_for(drone_1);
with_drone(drone_1)_envelop(target_poi);

obj: base

_deploy({ready|commit|not_ready})

with_base({moniker|uuid})_robot();
f
ff'';';ff fjfjfjjfjfffffwwww   
"Go an play 'Piano Sonata No. 1 in C major' on the piano."
"Make me a cup of tea"
"Count to 10"

1] Play the piano, then immediately drop everything (forget about the piano), go to the kitchen and make a cup of tea. `_decision(asynchronous)`

2] Play the piano 'Piano Sonata No. 1 in C major', then when finished go to the kitchen and make a cup of tea. `_decision(stack)`

3] Play the piano and make a cup of tea at the same time. `_decision(synchronous)`

4] Make a cup of tea, then play 'Piano Sonata No. 1 in C major' on the piano. `_decision(order/priority/authority)`

5] Play 10% of piano playing then 10% of making a cup of tea, then 10% piano playing... `_decision(simultaneous)`

6] Go to the kitchen put the kettle on, go to the piano and play, when kettle has boiled go to the kitchen and make the tea, go back to the piano and finish playing. `_decision(coeval)`

7] Play the piano, ignore/refuse to make the tea (or visa versa). `_decision(optional)`

8] Refuse to do either because they conflict. `_decision(defiant)`

9] You cannot play the piano (or do not know 'Piano Sonata No. 1 in C major'), do you ignore the piano and make a cup of tea. `_decision(incompetency)`

10] An asteroid is going to hit the earth in two minutes, you decide to play the piano for the last time and forget about making the tea (not enough time) `_decision(inability)`

What is my motive(s) / agenda?
Perhaps I would like a cup of tea, so I make a cup of tea for the caller and myself ... or I make the cup of tea and tell the caller to piss off.




In all programming languages the programmer owns the context, knows the consequences, and provides the decision tree.  Yet in the real world humans _program_ other humans with in a shared context, with shared knowledge of the consequences (if they are honest with each other), and a consensus of suggested decisions.

Take for instance the `if` condition _hello world_ example in the Go language:

```golang
package main
import ("fmt")

func main() {
  time := 20
  if (time < 18) {
    fmt.Println("Good day.")
  } else {
    fmt.Println("Good evening.")
  }
}
```

There is no context here, the program (in the main function) does not know the greeting to use when `(time < 18)` is `"Good day."`, the program is only told to `Println` the `"Good day."` sting when `(time < 18)`. At the last `}` the program effectively dies and does not know remember nor learn to 
`Println` `"Good day."` when `(time < 18)`.  The program does not even know that `"Good day."` is a greeting.  The context is completely owned by the programmer.

Only the programmer knows and understands the consequences of the program he has written.  This could be a sense of self-achievement, perhaps the programmer is learning this programming language for the first time.  This could be similar code to a greeting made in an app giving the human, that interfaces with the app, a polite greeting _ a sense of connection with the app.  The program is not a stakeholder in the consequences of its code.

If the program has at least a sense of context and an understanding of the consequences, it could make its own decisions.  Yet, the programmer provides the decision and the basis for making that decision.

So what is being proposed here? Do we write thousands of lines of code to give context, build an elaborate web of consequences and all the conceivable consequences of consequences?  Do we give the program all the possible decisions that the programmer could think of?  The answer is Yes, but not all at once, and definitely in a flash of life, _run-kill-and-repeat_, paradigm that _'programming'_ offers.

The next question which is predictably raised now is: Is this enough?  Surely providing all possible context, consequences, and decisions will be indefinite. 

```Diego
begin_diego()_givento_(greet)_appliedto(human)

begin_context()_givento_(greet)_appliedto(human)

begin_consequence()



_givento({verb})
_appliedto({object})
_specificto({postpos})
_forwhat(object_moniker)
_forwho(child_moniker)
_forwhy(postpos_param)



add_coco()



go_robot(alpha)_waypoint(waypoint_1);

go_robot(alpha)_waypoint(waypoint_1)_refuse(conflict);



go_robot(alpha)_waypoint(waypoint_1);
with_robot()_goto(waypoint_1)_for(alpha);
with_robot(alpha)_goto(waypoint_1);
with_robot(alpha)_goto()_waypoint(waypoint_1);
with_waypoint(waypoint_1)_go()_robot(alpha);
goto_waypoint(waypoint_1)_for(alpha);
goto_waypoint(waypoint_1)_for()_robot(alpha);

nav_robot(alpha)_waypoint(waypoint_1);
with_robot()_navto(waypoint_1)_for(alpha);
with_robot(alpha)_navto(waypoint_1);
with_robot(alpha)_navto()_waypoint(waypoint_1);
with_waypoint(waypoint_1)_nav()_robot(alpha);
navto_waypoint(waypoint_1)_for(alpha);
navto_waypoint(waypoint_1)_for()_robot(alpha);



{verb}_{object}({moniker|uuid})_{childobject|postposition}({moniker|uuid}) ? : ;


| `dca_` | | https://www.autonodyne.com/AUTO_behaviors2.html |
| `decoy_` | | https://www.autonodyne.com/AUTO_behaviors2.html |