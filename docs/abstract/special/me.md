# Me (special)

# me

`me` depicts the caller from its perspective.  It is a special case object that can also be used as a verb.  Options and postpositions of `me` are dependent on the genera of the caller (of the `me`).  `me` also has the required '*genesis event*' for every genera of *thingy* (excluding `console`). 

## Genesis Event

### Syntax:

```Diego
me();
```
The simplest and recommended approach to starting the genesis event for a *thingy* is to just command `me();`.  However, there are several other anthropomorphic approaches to initiate the genesis event, if `me();` has not already been commanded…
```Diego
me({moniker});
with_me({moniker});
me_id({id});
with_me()_id({id});
me_moniker({moniker});
with_me()_moinker({moinker});
me_name({name});
with_me()_name({name});
```
The genesis event can also be initiated by assigning its `uuid`, however, this approach cannot secure reliable uniqueness.

```Diego
me_uuid({me_uuid});
me_id(me_uuid);
with_me()_uuid({me_uuid});
```

## Identification

### Syntax:

```Diego
me_id(self_uuid);
me_id()_type(serial_number)_value({serial_number});
me_id()_type(phone_number)_value({phone_number});
me_id()_type(phone_number)_value({country_number},{region_number},{phone_number});

me_id({id});
with_me()_id({id});
me_serialnum({serial_number});
with_me()_me_serialnum({serial_number});
me_id()_type({id_type})_value({id_value});
with_me()_id()_type({id_type})_value({id_value});
```

The `id_type`s available for the `me_id()_type({id_type})…` and `with_me()_id()_type({ide_type})` are as follows:

| `id_type`   | syntax                                     | notes                                                        |
| ----------- | ------------------------------------------ | ------------------------------------------------------------ |
| `serialnum` | `_type(serialnum)_value({serial_number});` | `{serial_number}` is the serial number of the ***me** thingy*.         |
| `id`        | `_type(id)_value({id_number});`            | Any user defined identification number/code as `{id_number}`. |
| `ip`        | `_type(ip)_value({ip_address});`              | The current Internet Protocol address used at the time of the command by the ***me** thingy*                                                            |
| `phonenum`  | `_type(phonenum)_value({phone_number});` <br />`_type(phonenum)_value({country_number},{region_number},{phone_number});`                                         | Phone number for the ***me*** `cellphone` type *mobot*                                                            |
| `imei`      | `_type(imei)_value({imei});`                                            | International Mobile Equipment Identity for the ***me*** `cellphone` type *mobot*                                                             |
See also: [_type (id)](file://home/tav/Enterprise/Diego/lexicon/postpostions/_type&20(id).md "_type (id)")

## Children



```

me_id()_type(serialnum)_value({serial_number});
me_id()_type(phonenum)_value({phone_number});
me_id()_type(phonenumber)_value({country_number},{region_number},{phone_number});
me_id()_type(imei)_value({imei});
```

## Naming Event

### Syntax:

```Diego
me_name({me_name});
with_me()_name({me_name});
```

## Birth Event

### Syntax:

```Diego
me_birth();

me_birth()_dateime({birth_datetime});
me_birthdate({birth_datetime});

me_coord({coord_system},{coord_universe},{birth_coords});
me_gps({birth_coords});	me_coord(gps,{coord_universe},{birth_coords});
me_lps({birth_coords});	me_coord(lps,{coord_universe},{birth_coords});
```

## Genera

### Syntax:

```Diego
me_what({genus});	with_me()_genus({genus});
me_human();			with_me()_human();
me_ai();			with_me()_ai();
me_robot();			with_me()_robot();
me_thing();			with_me()_thing();
me_console();		with_me()_console();
```

| Genus     | Default Rank  | Max Rank         |
| --------- | ------------- | ---------------- |
| `human`   | `O-2 Captain` | `O President`    |
| `ai`      | `O-1 Officer` | `O-8 Lieutenant` |
| `robot`   | `O-1 Officer` | `O-6 Director`   |
| `thing`   | `E-10 Cadet`  | `O-4 Commander`  |
| `console` | `E-1 Intern`  | `E-1 Intern`     |




## Rank

### Syntax:

```Diego
me_rank({rank});

```

*See: `set_rank` for list of possible ranks.*

## Death-Resurrection / Sleep-Wake

### Syntax:

```Diego
me_death();	me_death()_datetime({death_datetime});
me_resurrect();	me_death()_datetime({resrrect_datetime});
me_sleep();	me_sleep()_datetime({sleep_datetime});
me_wake();	me_wake()_datetime({wake_datetime}); 
```





## See Also:

```Diego
progme








----

---
----512ceaaa00ef

ad43f779-74df-49d2-ad55-2e08c29278d4

28758a7c-7998-4e6e-b5e7-3e8615992cc3

```



