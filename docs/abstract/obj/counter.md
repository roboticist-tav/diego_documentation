# Counter (object)

```diego
use_namespace(diego_sandbox);

add_counter(patrol complete)_withinc(++);

begin_instruct(border patrol);
  	
    go_route(border)
        ? (patrol complete);
        ? goback_route(border)
            ? (patrol complete);
            : err_instruct[]_err(issue on border patrol);
        ;
    	: err_instruct[]_err(issue on border patrol);
    ;

end_instruct(border patrol);

start_instruct(border patrol)_forof(droid1)_you(droid1)
    ? msg_human(Jim)_counter(patrol complete);
    : msg_human(Jim)_err();
;

reset_namespace[];
```