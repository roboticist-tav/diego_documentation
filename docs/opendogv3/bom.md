# Bill of Materials

![OpenDogV3](https://hackaday.com/wp-content/uploads/2021/11/Snap-2021-11-30-at-22.16.15-featured.png?w=800)

add_robot(opendogv3)
    // Motors

    add_dict(motors)
        ()_k(fl_mtr_knee)_v(front-left motor (knee));
        ()_k(fr_mtr_knee)_v(front-right motor (knee));
        ()_k(hl_mtr_knee)_v(hind-left motor (knee));
        ()_k(hr_mtr_knee)_v(hind-right motor (knee));
        ()_k(fl_mtr_hip)_v(front-left motor (hip));
        ()_k(fr_mtr_hip)_v(front-right motor (hip));
        ()_k(hl_mtr_hip)_v(hind-left motor (hip));
        ()_k(hr_mtr_hip)_v(hind-right motor (hip));
        ()_k(fl_mtr_waist)_v(front-left motor (waist));
        ()_k(fr_mtr_waist)_v(front-right motor (waist));
        ()_k(hl_mtr_waist)_v(hind-left motor (waist));
        ()_k(hr_mtr_waist)_v(hind-right motor (waist));
    ;
    add_motor()
        ()_moniker()_kof(motors);
        ()_text()_vof(motors);
    ;

    // Motor ranges (in radians)
    with_motor(flhip,hlhip)_fromtoroll(❬rad❭,-1.5708,-0.785398);
    with_motor(frhip,hrhip)_fromtoroll(❬rad❭,-1.5708,-0.785398);
    
    add_actuat({motor_driver},x_mtr_drv)

    add_sensor({encode},fl_menc_knee,   // front-left motor encoder (knee)
        fr_menc_knee,                   // front-right motor encoder (knee)
        hl_menc_knee,                   // hind-left motor encoder (knee)
        hr_menc_knee,                   // hind-right motor encoder (knee)
        fl_menc_hip,
        fr_menc_hip,
        hl_menc_hip,
        hr_menc_hip,
        fl_menc_waist,
        fr_menc_waist,
        hl_menc_waist,
        hr_menc_waist);

    add_imu(imu);

    add_transceiver(wf_transceiver);

    add_batt(ZIPPY_Compact_4000mAh_6S_60c_Lipo_Pack)_cap(❬Ah❭,4);


-0.785398,-2.35619




with_robot(opendogv3)
    log_console()_help(hl_mtr_hip);
;
// hind-left motor (hip)

with_robot(opendogv3)
    log_console()_()_typeof()_help(hl_mtr_hip);
;
// opendogv3,{robot},hind-left motor (hip)


    GIN

# Absolute

`_abs(`*`numeric`*`);` &nbsp; *`…`*`|`*`sub-expression`*`|`*`…`*



add_rec => add_record

https://www.youtube.com/watch?v=hPpvlKLeYYA

    add_rec(User)_str(FullName);

    add_pegu()
        with_get(hello)_ret(Hello World!);
        with_get(helloobj)_ret()
            add_process(message)_v(Hello World);
        ;
        with_get(user)_result(OK)_rec(User)_v(Nick Chapsas);
        with_get(special)_async()_hippo()
            ()_ret()_await()_json()_requery();
        ;
        with_post(extra/[{int},year])_int(year)_fromquery()_name(a)_int(age)
            _fromHeader({str},accept)_tempor(provider)
            _rec(User)
            ()_ret()_json([year],[age],[accept],[User],[])_(provider)_now();
        ;
    ;

    run_gin();

GET http://localhost:5001/special?age=19
Accept: application/json

```json
[{"key":"age","value":["19"]}]
```



hippo()

Adds:
    HttpRequest request             -> `req()` &nbsp; `requery()`
    HttpResponse response           -> `resp()`
    CancellationToken token         -> `token()`


