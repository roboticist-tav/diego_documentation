##
## Robot Composition of standard Robotis Turtlebot 3 Burger
## Author: Tavis Pitt [tavis.pitt7@gmail.com]
##

## Instructions:
## Run this file in a human shell (yours): shell_human()_me();
## Execute this file with: exec_diego({filepath_filename});

## root Instruction:
begin_funct([], shellLabelHumanMe)_param({String}, label);
                                                                        | caller | *hash | ←hash | ↓hash | ↑hash | Diego commands<br />_Human talk_ |
    find_human()_me()                                                   | a36d3  | 5bffa |       |       |       | find_human_me()<br />_Get a human_ |
                                                                                 |
        ? add_label[label]_me();
        : find_human()_authority(highest)
            ? add_label[label]_me();
            : exit_funct[this]_err(Where's the humans?);
    ;

    has_authority(shell)_me()
        ? shell_human[label];
        : exit_funct[this]_err(No permission for shell);
    ;

end_funct[shellLabelHumanMe];
c20-646f-437c-bf9d-1a067d37286a


begin_instruct(robotis_turtlebot3_burger_composition);

    # Name the robot:
    exec_funct[shellLabelHumanMe]_param([label],human_compositor)
        : exit_instruct[]_err([shellLabelHumanMe]_err());
        ? exit_instruct(robotis_turtlebot3_burger_composition)_err()
        : shell_human()_me()
            ? add_label(human_compositor)_me()
            : find_human()_authority(highest)
                ? add_label(human_compositor)
                    | shell_human(human_compositor)
                        : exit_instruct(robotis_turtlebot3_burger_composition)_err()
                
        ;
    with_human(human_compositor)_request(Moniker of Robotis Turtlebot 3 Burger:)_confirm()_var([robot],thisRobot) ? exec_instruct(name_robot) : exec_instruct(retry_name_robot);

    find_human()_me() {
        ? add_label()
        shell_human()_me()
    }

    # Add default specifications:
    with_robot[thisRobot]_spec(maximum_translational_velocity)_value(0.22,ms);
    with_robot[thisRobot]_spec(maximum_rotational_velocity)_value(2.84,rads)_value(162.72,degs);
    with_robot[thisRobot]_spec(maximum_payload)_value(15,kg);
    with_robot[thisRobot]_dim(138,178,192,mm);
    with_robot[thisRobot]_weight(1,kg)_note(+ SBC + BAtter + Sensors);
    with_robot[thisRobot]_spec(operating_time)_value(~2:30,hrmin);
    with_robot[thisRobot]_spec(charging_time)_value(~2:30,hrmin);

    # Add wheel actuators
    add_actuat(left_actuator)_manufact(DYNAMIXEL)_model(XL430-W250-T);
    add_actuat(right_actuator)_manufact(DYNAMIXEL)_model(XL430-W250-T);
    add_processor(arm_cortex_m3_mcu)_manufact(arm)_model(Cortex-M3)_type(mcu)_for(left_actuator,right_actuator);
    ## with_actuat(left_actuator)_and(right_actuator)_processor(arm_cortex_m3_mcu);
    with_robot[thisRobot]_actuat(left_actuator);
    with_robot[thisRobot]_actuat(right_actuator);

    add_sbc(sbc)_manufact(Raspberry Pi)_model(3 Model B)_for(💬name_robot.moniker💬);
    add_processor(bcm2837)_manufact(Boradcom)_model(BCM2837)_for(Raspberry Pi);
    add_microcontrol(embedded_controller)_manufact(OpenCR)_for(💬name_robot.moniker💬);



    # Tidy up
    del_label(human_compositor);


end_instruct(robotis_turtlebot3_burger_composition);

## Name the robot the answer passed to this instruct:
begin_instruct(name_robot);

    with_answer()_invar(robot_name);
    ## add_robot()_outvar(robot_name)_manufact(Robotis)_make(turtlebot3)_model(burger)_onceonly();
    add_robot(💬robot_name💬)_manufact(Robotis)_make(turtlebot3)_model(burger)_onceonly();

end_instruct(name_robot);

## Handle errors for 'ask_human_for_name'
begin_instruct(retry_name_robot);

    alert_err();
    ## _retry_caller()_caller()_caller();
    retry_rootcaller();
    
end_instruct




## OK, Go!
exec_instruct(robotis_turtlebot3_burger_composition)_me();





shell_human()_me();
exec_diego(/robotis_turtlebot3_burger_composition.dgo);






exec_diego({dgo_url})_me();
apt_diego({apt})_me();
apt_github()_me();
apt_datasheet(datasheet.diego_lang.com/arm_cortex_m3_mcu);
apt_ **A**dvanced **P**ackaging **T**ool







controller (human)       controller (human)

diego_lang               javascript

diego_engine             diego_javascript_library

ROS2 (C)                 ROS2

robot                    robot   
