
add_me(ugv1);
add_me(ugv1)_id(a4ba88a5-5fe6-4727-aeaf-89b6b75e2737);
add_me(ugv1: a4ba88a5-5fe6-4727-aeaf-89b6b75e2737);
with_me()_manufact(Praesidium)_make(MAPS)_model(Mk9)_badge(e2737);
with_me()_ident(Praesidium: MAPS: Mk9: e2737);
with_me()_type(ugv);
with_me()_base(ground_only);
with_me()_thing(robot);





begin_instruct(diego_me)_me();
    add_me(ugv1, a4ba88a5-5fe6-4727-aeaf-89b6b75e2737);
    with_me()_ident(Praesidium, MAPS, Mk9, e2737);
    with_me()_type(ugv);
    with_me()_base(ground_only);
end_instruct[];

begin_instruct(diego_iot)_me();
    with_me()_thing(robot);
    
    iot_me(GoogleIoTCore)_me(ugv1, a4ba88a5-5fe6-4727-aeaf-89b6b75e2737)_ident(Praesidium, MAPS, Mk9, e2737);
    iot_me(AWSIoTCore)_ident(Praesidium, MAPS, Mk9, e2737);
    iot_me(AzureIoTCore);
end_instruct(diego_iot);

begin_instruct(diego_sensors)_me();
    with_me()
        add_sensor(ugv1_lidar, lidar);
        add_sensor(ugv1_imu, imu);
        add_sensor(ugv1_gnss, gnss);
        add_sensor(ugv1_radar , radar);
        add_sensor(ugv1_hygrometer , hygrometer);
        add_sensor(ugv1_shooter_detector , shooter_detector);
        add_sensor(ugv1_cam_rgb_front, cam_rgb);
        add_sensor(ugv1_cam_rgb_rear, cam_rgb);
        add_sensor(ugv1_cam_thermal, cam_thermal);
        add_sensor(ugv1_cam_3d, cam_3d);
        add_sensor(ugv1_cam_360, cam_360);
    ;
end_instruct(deigo_sensors);

begin_instruct(diego_equip)_me();
    with_me()
        add_equip(ugv1_robotic_arm, manip);
        add_equip(ugv1_gun, weapon);
        add_equip(ugv1_pump, pump);
        add_equip(ugv1_casevac, casevac);
    ;
end_instruct(diego_equip);

begin_instruct(diego_capability);
    set_measure(metric);
    set_dim(m);
    set_vol(l);
    set_mass(kg);
    set_weight(kg);

    with_me()_capab(ugv1_payload, payload);
    with_capab(ugv1_payload)_dim(2, 4, 2.6);
    with_capab(ugv1_payload)_vol(20.8);
    with_metric(ugv1_max_payload, max_payload)_value(15, kg);

    with_me()_capab(ugv1_available_mode, mode);
    with_capab(ugv1_available_mode)_mode(tethered);
    with_capab(ugv1_available_mode)_mode(teleop);
    with_capab(ugv1_available_mode)_mode(follow_me);
    with_capab(ugv1_available_mode)_mode(navigation);
    with_capab(ugv1_available_mode)_mode(mapping);
    with_capab(ugv1_available_mode)_mode();
    with_capab(ugv1_available_mode)_mode();
end_instruct(diego_capability);

begin_instruct(diego_metrics);
    set_measure(metric);
    set_speed(ms);
    set_velocity(ms);
    set_angles(rad);

    with_me()_add_metric(ugv1_top_speed, max_vel)_value(8, ms);
    with_me()_add_metric(ugv1_max_trans_vel, max_trans_vel)_value(8, ms);   # Maximum translational velocity
    with_me()_add_metric(ugv1_max_rot_vel, max_rot_vel)_value(2.84, rads);   # Maximum rotational velocity
    with_me()_add_metric(ugv1_max_rot_vel, max_rot_vel)_value(162.72, degs);   # Maximum rotational velocity
    
    with_me()_add_metric(ugv1_dim, dim)_value(0.138, 0.178, 0192);  # Dimensions
    # or: with_me()_add_metric(ugv1_dim, dim)_dim(0.138, 0.178, 0192);
end_instruct(diego_metrics);

begin_instruct(diego_jiggers);
    set_measure(metric);
    set_speed(ms);
    set_velocity(ms);
    set_angles(rad);
    set_dim(mm);

    with_me()_jigger(ugv1_actuator_left, actuator)_ident(Robotis, DYNAMIXEL, XL430-W250-T);
    with_jigger(ugv1_actuator_left)_dim(28.5, 46.5, 34);
    with_jigger(ugv1_actuator_left)_weight(57.20);
    with_jigger(ugv1_actuator_left)_metric(ugv1_actuator_left_gear_ratio, gear_ratio)_value(258.5, 1);

    with_me()_jigger(ugv1_actuator_right, actuator)_core(GoogleIoTCore, Robotis, DYNAMIXEL, XL430-W250-T);
end_instruct(diego_jiggers);

start_instruct(deigo_me);
start_instruct(deigo_iot);
start_instruct(deigo_sensors);
start_instruct(diego_equip);
start_instruct(diego_capability);
start_instruct(diego_metrics);
start_instruct(diego_jiggers);
