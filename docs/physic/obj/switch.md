# Switch (object)

A `switch` is an child object of a thing that records specific boolean data from its environment.  Data is usually communicated through `flag`s.

## Syntax
The default declaration syntax is to provide at least the switch name and type:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_switch{`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_switch(`*`moniker`*`)_type(`*`type`*`);`

Just referencing the switch, or using an empty `_value()` posit will read the state of the switch. To set the state of the switch, the `_set`, or, `_on()`/`_off()`, or, `_true()`/`_false()`, or, valued `_value` posits can be used (if write access):

Get:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch(`*`moniker`*`)_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch(`*`moniker`*`)_tovar(`*`variablename`*`);`<br>
Set:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_set(`*`boolean`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_value(`*`boolean`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_on();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_off();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_true();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_false();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_value(`*`boolean`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_switch{`*`moniker`*`)_value([`*`variablename`*`]);`<br>

## Switch Types

| sensor type | access | definition |
| --- | --- | --- |
| <a name="level"></a>`{level}`<br>`_type(level)` | read-only |**Level Switch / Float Level Switch**<br>A component used to detect when the level of liquid rises to a set level, within a tank. |
| <a name="light"></a>`{light}`<br>`_type(light)` | read write |**Light Switch**<br>A switch most commonly used to operate electric lights, permanently connected equipment, or electrical outlets. |
| <a name="prox"></a>`{prox}`<br>`_type(prox)` | read-only | **Proximity Switch**<br>A sensor able to detect when the presence of nearby objects are at a set displacement. |
| <a name="relay"></a>`{relay}`<br>`_type(relay)` | read write | **Solid State Relay / Solid State Switch**<br>An electronic switching device that switches on or off when an external voltage is applied across its control terminals. |
| <a name="tilt"></a>`{tilt}`<br>`_type(tilt)` | read write | **Tilt Switch**<br>A device triggered when the tilt of an object in multiple axes has reference to an absolute level plane. |
