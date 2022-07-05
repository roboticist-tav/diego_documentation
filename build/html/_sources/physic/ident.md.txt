# Ident
The `Ident` object exposes the identity interface for most all objects, giving identity information in response to any requests such as `_ask`. All it's posits are automatically promoted, so the `_ident` (and shortened `_id`) posit can be ignored.

## Syntax
Declaration only requires *`moniker`* as the minimum, all the other arguments are optional by ordered:

Get:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_ident();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_tovar(`*`variablename`*`);`<br>
Set:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_ident(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id(`*`manufacturer`*`,`*`model`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id(`*`manufacturer`*`,`*`model`*`,`*`badge`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id(`*`manufacturer`*`,`*`model`*`,`*`badge`*`,`*`serialnumber`*`);`<br>

Common `_dent`s posits are automatically promoted, so the `_ident` (and shortened `_id`) posit can be ignored. 

Get:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_manufacturer();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_manufact()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_manufact()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_model();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_model()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_model()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_badge();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_badge()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_badge()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_serialnumber();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_sernum()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_sernum()_tovar(`*`variablename`*`);`<br>
Set:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_manufacturer(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_manufact()_value(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_model(`*`model`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_model()_value(`*`model`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_badge(`*`badge`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_badge()_value(`*`badge`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_serialnumber(`*`serialnumber`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_sernum()_value(`*`serialnumber`*`);`<br>

Uncommon posits require the `_ident` (or `_id`) posits. The `moniker`, and, `nickname` are all the `moniker` of the thingy passed through, as read-only. All uncommon posits for `_ident` (or `_id`) are read-write-by-me:

Get:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_ident()_moniker();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_name();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_nickname();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_species();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_species()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_species()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_version();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_version()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_version()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_softwarerelease();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_softrel()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_softrel()_tovar(`*`variablename`*`);`<br>
Set:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_name(`*`name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_name()_value(`*`name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_name([`*`variablename`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_species(`*`species`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_species()_value(`*`species`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_species([`*`variablename`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_version(`*`version`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_version()_value(`*`version`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_version([`*`variablename`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_softwarerelease(`*`_softwarerelease`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_softrel()_value(`*`_softwarerelease`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_id()_softrel([`*`variablename`*`]);`<br>

## Example
<!-- https://dev.bostondynamics.com/protos/bosdyn/api/proto_reference#robot-id-proto -->
In this example, in the mist is robot `rex`, a Boston Dynamics spot robot.  We will ask `rex` to identify itself:
```diego
ask_robot(rex)_ident();
```
`rex` responds as such:
```diego
tell_human(diego)_moniker(rex)_ident(Boston Dynamics,spot,spot,d349-7273-32e2)_name(20190601)_nickname(rex)_species(spot)_version(2.0.1)_softrel(2.0.1);
```
To see a human-friendly version:
```diego
me_msg()_robot(rex)_ident();
```
The output:
<pre>manufact=Boston Dynamics
make=spot
model=spot
serialnumber=d349-7273-32e2
badge=spot
name=20190601
nickname=rex
sofrel=2.0.1
species=spot
version=2.0.1</pre>