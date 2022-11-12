# Identity (property)
The `ident` property exposes the identity interface for most all objects, giving identity information in response to any requests such as `_ask`.

## Retrieval
Retrieval of all `ident` properties require an empty parameter set of the `_ident` posit. The `_id` posit is syntactically identical to `_ident` and can be used freely and interchangeably. The use of the `_value` (or shortened `_v`) posit is automatically implied and is not necessary. The default format of the output will be via a comma-separated list of key-value pairs, such as "*`key1=value1,key2=value2,…`*", alphabetical order. Formatting of the output can be achieved either by: using the `_format` posit; or, using the format as a type with curly brackets (`{}`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ident();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_format(`*`format`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id({`*`format`*`});`<br>

The `ident` *properties* or *subproperties* can be pass to an abstract storage *object* using the `_to`*`<object>`* syntax.  For instance for a *variable* (`var`) or an *array* (`ary`), the `_tovar` and `_toary` posit are use, respectively.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_tovar(`*`variable_name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_toary(`*`ary_name`*`);`<br>

Granulation of the individual properties can be achieved with proceeding properties as posits. However, common *subproperties* of `indent` are automatically promoted, the use of `_ident` (and `_id`) is not necessary.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ident()_make();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_model();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_model();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_make()_model();`<br>
<!--
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_manufacturer();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_manufact()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_manufact()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_model();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_model()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_model()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_badge();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_badge()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_badge()_tovar(`*`variablename`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_serialnumber();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sernum()_value();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sernum()_tovar(`*`variablename`*`);`<br>-->

## Declaration
Declaration requires parameters (of various signatures).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ident(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id(`*`manufacturer`*`,`*`model`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id(`*`manufacturer`*`,`*`model`*`,`*`badge`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id(`*`manufacturer`*`,`*`model`*`,`*`badge`*`,`*`serialnumber`*`);`<br>

Common *subproperties* of `indent` are automatically promoted, so the `_ident` (and shortened `_id`) posit, during declaration, can be ignored. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_manufacturer(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_manufact()_value(`*`manufacturer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_model(`*`model`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_model()_value(`*`model`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_badge(`*`badge`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_badge()_value(`*`badge`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_serialnumber(`*`serialnumber`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_sernum()_value(`*`serialnumber`*`);`<br>

!!! Important
    Syntax can be switched from declaration to retrieval upon various *verbs* used, such as `tell_`.  This most often occurs with non-human communication.

## Commonality
Uncommon posits require the `_ident` (or `_id`) posits, in both retrieval and declaration. The `moniker`, and, `nickname` are all the `moniker` of the thingy passed through, as read-only. All uncommon posits for `_ident` (or `_id`) are read-write-by-me.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ident()_moniker();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_name();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_nickname();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_species();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_version();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_softwarerelease();`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_name(`*`name`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_species(`*`species`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_version(`*`version`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_softrel(`*`_software_release`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_id()_softrel([`*`variable_name`*`]);`<br>

## Example
<!-- https://dev.bostondynamics.com/protos/bosdyn/api/proto_reference#robot-id-proto -->
In this example, in the mist is robot `rex`, a Boston Dynamics spot robot.  We (as a human call Diego, with moniker `diego`) will ask `rex` to identify itself:
```diego
ask_robot(rex)_ident();
 
```
`rex` responds as such:
```diego
tell_human(diego)_moniker(rex)_ident(Boston Dynamics,spot,spot,d349-7273-32e2)_name(20190601)_nickname(rex)_species(spot)_version(2.0.1)_softrel(2.0.1);
```
To see a human-friendly version:
```diego
me_msg()_robot(rex)_ident({yaml});
```
The output:
<pre>manufact: Boston Dynamics
make: spot
model: spot
serialnumber: d349-7273-32e2
badge: spot
name: 20190601
nickname: rex
sofrel: 2.0.1
species: spot
version: 2.0.1</pre>

## Posits

| method | description | API |
| --- | -------- | --- |
| <a name="_ident"></a> `_ident()` | Provides or sets identity information. | [ident](#ident) |

### Ident
# _type (id)
The `_type (id)` postposition is used to assign identication to a *thingy*.  It is only associated with the `id()` object.  The syntax is:
```Diego
{verb}_{object}_id()_type({id_type});
{verb}_{object}_id()_type({id_type})_value({id_value)});
```
<sub>For the case of `me` the syntax: `me_id()_type({id_type});` is included.</sub>

The `id_type`s available are as follows:

| `id_type`   | syntax                                     | notes                                                        |
| ----------- | ------------------------------------------ | ------------------------------------------------------------ |
| `serialnum` | `_type(serialnum)_value({serial_number});` | `{serial_number}` is the serial number of the *thingy*.         |
| `id`        | `_type(id)_value({id_number});`            | Any user defined identification number/code as `{id_number}`. |
| `ip`        | `_type(ip)_value({ip_address});`              | The current Internet Protocol address used at the time of the command by the *thingy*                                                            |
| `phonenum`  | `_type(phonenum)_value({phone_number});` <br />`_type(phonenum)_value({country_number},{region_number},{phone_number});`                                         | Phone number, usually for `cellphone` type *mobots*                                                            |
| `imei`      | `_type(imei)_value({imei});`                                            | International Mobile Equipment Identity, usually for the `cellphone` type *mobots*                                                             |
