# Operating System (object)
The `opsys` *object* represents the operating system of the preceding objects.  An operating system is the software that manages computer hardware, software resources, and provides common services for computer programs.  Some *objects* can have more than one (an array) of operating systems.

<a name="get"></a>
## Getting
To get the operating system of the proceeding object, use the `_opsys()` posit. The return will be a comma separated list of operating system *enumerator* *types*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys();`

For an *object* wil multiple operating systems, use the `index` or `i` posit to determine which operating system you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
When adding the operating system as a child of the preceding *object*, by using the posit `_opsys`, the operating system is effectively set.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system}`*`);`

Some *objects* allow for multiple operating systems. To set more than one operating system, multiple `opsys` posit are required. Alternatively an array can be used to set operating systems in one `opsys` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system1}`*`)_opsys(`*`{operating_system2}`*`)_`*`...`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys([`*`operating_system_array_moniker`*`]);`

<a name="cast"></a>
## Casting
Casting an operating system is identical syntax to setting an operating system, both one and more than operating systems.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system_to_cast_to}`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system_to_cast_to}`*`)_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys([`*`operating_system_to_cast_to_array_moniker`*`]);`

<a name="posit"></a>
## Posits

<a name= "object"></a>
## Objects

### Computer




