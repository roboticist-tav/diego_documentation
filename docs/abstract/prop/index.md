# Index (property)
The `index` property provides the ordinal index of a multi-data storage object.  The shortened version of `i` can be used.

<a name="get"></a>
## Getting
To get the index from the preceding object, use the `index` posit (or shortened `i`). The return will be a the value at the ordinal position of the preceding multi-data storage *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_index();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_i();`

For an *object* with an array of hours, use the `index` (or shortened, `i`) posit to determine which hour in the array you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour()_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hr()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
As the `hour` posit with a *`hour_value`* paramter to set the temporal hour as a child (and so property) of the preceding *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour(`*`hour_value`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour(`*`hour_value`*`);`

Some *objects* allow for an array of hours. To set an array of hours, use multiple `hour` posits. Alternatively an array can be used to set hours in one `hour` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour(`*`{hour_value1}`*`)_hr(`*`{hour_value2}`*`)_`*`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hour([`*`hour_array_moniker`*`]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_hr([`*`hour_array_moniker`*`]);`



```diego

add_
add_ary(legs)_v(front_left,front_right,hind_left,hind_right);

log_console()_(legs)_i(0);


add_var(front_legs)_(legs)_i(0,1);

add_ary(hind)_v(2,3)
add_var(hind_legs)_(legs)_i([hind]);

