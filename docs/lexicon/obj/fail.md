# Fail, Failure

[HL_FAILURE_FLAG](https://mavlink.io/en/messages/common.html#HL_FAILURE_FLAG)

with_fail(gnps_failure)_num(ff101)_mavlink(HL_FAILURE_FLAG,1);

```Deigo
// General failure flags (ff###)
set_fail()_truefortypeof(gen_fail);

# General failure of GPNS:
add_fail(gnps_failure)_uuid(25c29ec5-a5ac-4448-8b63-d529f1e7c0d0)
    _num(ff101)_mavlink(HL_FAILURE_FLAG,HL_FAILURE_FLAG_GPS,1)
    _err(General failure of GPNS)_type(gen_fail);
with_fail(gnps_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(gpns);
with_fail(gnps_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(sensor)_forwhat(type)_forwho(gpns);

# General failure of LPNS:
add_fail(lnps_failure)_uuid(881fbae0-1bc6-492b-a7eb-ebf39e74ffcd)
    _num(ff102)_mavlink()_err(General failure of LPNS);
with_fail(lnps_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(lpns);
with_fail(lnps_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(sensor)_forwhat(type)_forwho(lpns);

# General failure of differential pressure sensor:
add_fail(p_diff_failure)_uuid(95517c3a-f243-4772-a09e-f726c9aa8f29)
    _num(ff1)_mavlink(HL_FAILURE_FLAG,HL_FAILURE_FLAG_DIFFERENTIAL_PRESSURE,2)
    _err(General failure of differential pressure sensor);
with_fail(diffp_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(sensor)_forwhat(type)_forwho(p_diff);

# General failure of absolute pressure sensor:
add_fail(abs_diff_failure)_uuid(096b2edc-3356-44fa-8789-64ca82aa6add)
    _num(ff1)_mavlink(HL_FAILURE_FLAG,HL_FAILURE_FLAG_ABSOLUTE_PRESSURE,4)
    _err(General failure of absolute pressure sensor);
with_fail(abs_diff_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(sensor)_forwhat(type)_forwho(abs_diff);


```

`telemet`, `telementry` *"lorem ipsum"*


```Diego

add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
add_fail(_failure)_num(ff1)_mavlink()_err(General failure of );
```




# General Failure

A _general failure_ of a `thingy` (usually a `sensor` or `actuat`) should be triggered 


set_fail()_truefortypeof(gen_fail);


set
add_fail(gnps_failure)_uuid(25c29ec5-a5ac-4448-8b63-d529f1e7c0d0)
    _num(ff101)_mavlink(HL_FAILURE_FLAG,HL_FAILURE_FLAG_GPS,1)
    _err(General failure of GPNS)_type(gen_fail);
with_fail(gnps_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(gpns);
with_fail(gnps_failure)
    _fordiego(oh)_doto(with,test,check)_appliedto(sensor)_forwhat(type)_forwho(gpns);



`_fordiego(do)` Only the *do_diego* command of the override is applied.
`_fordiego(hey)` Only the *hey_diego* command of the override is applied.

`_appliedto({object_moinker|object_uuid})` The specified object(s) are overridden.
_doto()
_givento()
_forwhat()
_forwho()

`_specificto({})

_fordiego(oh)_doto(with,test,check)_appliedto(sensor)_forwhat(type)_forwho(gpns);



{do_diego_1} | {do_diego_2} ? {hey_diego_2} : {oh_diego_2} ? {hey_diego_1} : {oh_diego_1};

`_fordeigo(do)` | `_fordiego(|do)` | `_fordiego(|hey)` | `_fordiego(|oh)` | `_fordiego(hey)` | `_fordiego(oh)`


`{verb}_{object}({object_moinker})_{child_object}({child_moniker})_{postpos}({postpos_param})_{discrim_postpos}({discrim_moniker})`

`doto({verb})` | `_appliedto({object})` | `_paraquem({object_moinker})` | `_givento({child_object})` | `_forwhat({child_moniker})` | `_specificto({postpos})` | `_forwhy({postpos_param})` | `_forwhom({discrim_moniker})` | `_paraquem({object_moinker & discrim_moniker})`

xdoto()

begin_override(loiter_persian_chain)_doto(loiter)_paraquem(alif, be, pe);

inc_override(loiter_persian_chain)_paraquem(alif, be, pe)_specificto(loiterat);

    with_loiter()_type(hover)_angvelocity(0, 0, -1.4)_unit(rads);

end_override(loiter_persian_chain);

exec_override(loiter_persian_chain)_for(alif, be, pe)


https://www.autonodyne.com/AUTO_behaviors2.html#behave-swarm