with_mobot(bedsideAlarmClock)
    alert_human(bob)_msg(Hi [bobFirstName] [bobLastName])_var(bobFirstName)_value(Bob)_str(Granger)_asvar(bobLastName);
;

with_mobot(fridge)
    alert_human(bob)_msg(Hi [bobFirstName] [bobLastName]);
;

with_mobot(frontdoor)
    add_var(bobGreeting)_calc('Hi '+[bobFirstName]+' '+[bobLastName]);
    alert_human(bob)_msg([bobGreeting]);
;