# Metric (object)



add_metric({name/uuid})
	_scalar({scalar}[, {unit}])
	_unit({unit})
	_for({name/uuid_1}[, ...{name/uuid_n}])
	_pulse()
	_tracker()


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_metric(`*`moniker`*`)_set(...)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `set_metric(`*`moniker`*`,settings...)`<br>

## Properties

| property | datatype / unit | description |
| --- | --- | --- |
| `scalar` | {id} / {id_3}[^3btyehex] | A 3 Byte hexidecimal unique idendifier used in adsb messaging |

## Posits

| posit | datatype / unit | description |
| --- | --- | --- |
| `_scalar(`*`moniker`*`)`<br>`_scalar({dt},`*`moniker`*`)` | {id} / {id_3}[^3btyehex] | A 3 Byte hexidecimal unique idendifier used in adsb messaging |
