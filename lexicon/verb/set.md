# set

## Here

### Syntax:

```Diego
_set(Thing Here)_false();
_set(Thing Here)_true();
```

## Rank

### Syntax:

```Diego
set_rank({rank/rank_code});
```

| `rank`       | `rank_code` |
| ------------ | ----------- |
| `President`  | `O`         |
| `Admiral`    | `O-10`      |
| `General`    | `O-9`       |
| `Lieutenant` | `O-8`       |
| `Marshal`    | `O-7`       |
| `Director`   | `O-6`       |
| `Colonel`    | `O-5`       |
| `Commander`  | `O-4`       |
| `Major`      | `O-3`       |
| `Captain`    | `O-2`       |
| `Officer`    | `O-1`       |
| `Cadet`      | `E-10`      |
| `Corporal`   | `E-9`       |
| `Starshina`  | `E-8`       |
| `Chief`      | `E-7`       |
| `Sergeant`   | `E-6`       |
| `Agent`      | `E-5`       |
| `Private`    | `E-4`       |
| `Trainee`    | `E-3`       |
| `Reserve`    | `E-2`       |
| `Intern`     | `E-1`       |



## Birth Event

### Syntax:

```Diego
_self_birth();

_self_birth()_dateime({birth_datetime});
_self_birthdate({birth_datetime});

_self_coord({coord_system},{coord_universe},{birth_coords});
_self_gps({birth_coords});	_self_coord(gps,{coord_universe},{birth_coords});
_self_lps({birth_coords});	_self_coord(lps,{coord_universe},{birth_coords});
```

## Genera

Syntax:

```Diego
_self_what({genus});
_self_human();
_self_ai();
_self_robot();
_self_thing();
_self_console();

```

## See Also:

```Diego
prog_self




see_robot(AQLD:605 BS5)_see()_gps()



----







```



