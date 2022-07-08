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

