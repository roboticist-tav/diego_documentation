
`with_me()_spec(`*`spec_type`*`, `*`value`*`)`
`with_me()_spec(`*`spec_type`*`, `*`spec_sub_type`*`, `*`value`*`)`
`with_me()_spec(`*`spec_type`*`, `*`spec_sub_type`*`, `*`value`*`, `*`sample_type`*`)`
| *`spec_type`* | *`spec_sub_type`* | Description | Example |
|:--:|:--:|--|--|
| `volume` or<br>`vol` |  | Volume or maximum volume capacity.<br>See also: `set_vol` | `with_me()_spec(volume, 500);`
| `use_by_date` | | Use by date (food & beverages).<br>See also: `best_before_date` | `with_me()_spec(use_by_date, 2020-11-10);` |
| `ingredient`<br>or `ingred` | `coffee`<br>`milk`<br>`reduced_fat_milk`<br>`sugar` | Ingredient (food & beverages). | `with_me()_spec(ingred, sugar);` |
| 




with_me()_spec(ingred, coffee);

  
with_me()_spec(ingred, reduced_fat_milk);
with_me()_spec(serv_pack, 1);

with_me()_spec(serv_size, 500, ml);

with_me()_spec(nutrit, energy, 1480, per_serving);


Items

Burger
```diego
set_vel(ms);
set_mass(kg);
set_dim(mm);

with_me()_spec(max_trans_vel, 0.22);		# Maximum translational velocity (m/s)
with_me()_spec(max_rot_vel, 2.84, rads);	# Maximum rotational velocity (rad/s)
with_me()_spec(max_rot_vel, 162.72, degs);	# Maximum rotational velocity (deg/s)
with_me()_spec(max_payload, 15);		# Maximum payload (kg)
with_me()_spec(dim, 138, 178, 192);		# Dimensions (mm)
with_me()_dim(138, 178, 192);			# Dimensions (mm)
with_me()_spec(weight, 1);			# Weight (kg)  ??? what weight ???

with_me()_spec(climb_threshold, <10, mm);	# Threshold of climbing [10 mm or lower]
with_me()_spec(exp_op_time, 2:30);		# Expected operating time


with_me()_jigger(turtle1_sbc)_ident(raspberry_pi, 4, model_a);
with_jigger(turtle1_sbc)_jigger(turtle1_mcu);
with_jigger(turtle1_mcu)_ident(arm, cortex_m7, 32bit);
with_jigger(turtle1_mcu)_spec(bit, 32);
with_jigger(turtle1_mcu)_spec(fpu, 216, mhz);
with_jigger(turtle1_mcu)_spec(dmips, 462);

with_me()_jigger(acutator_left)_ident(robotis, dynamixel, XL430-W250);
with_me()_jigger(acutator_right)_ident(robotis, dynamixel, XL430-W250);

with_me()_sensor(lds, dist, laser)_ident(LDS-01);
with_me()_sensor(imu);
with_sensor(imu)_sensor(imu_g, gyroscope)_spec(axis, 3);
with_sensor(imu)_sensor(imu_a, accelerometer)_spec(axis, 3);
with_sensor(imu)_sensor(imu_m, magnetometer)_spec(axis, 3);

with_me()_humaport(power, 3.3, 800

```

 
humaport
roboport




Power connectors

3.3V / 800mA  
5V / 4A  
12V / 1A

Expansion pins

GPIO 18 pins  
Arduino 32 pin

Peripheral

UART x3, CAN x1, SPI x1, I2C x1, ADC x5, 5pin OLLO x4

DYNAMIXEL ports

RS485 x 3, TTL x 3

Audio

Several programmable beep sequences

Programmable LEDs

User LED x 4

Status LEDs

Board status LED x 1  
Arduino LED x 1  
Power LED x 1

Buttons and Switches

Push buttons x 2, Reset button x 1, Dip switch x 2

Battery

Lithium polymer 11.1V 1800mAh / 19.98Wh 5C

PC connection

USB

Firmware upgrade

via USB / via JTAG

Power adapter (SMPS)

Input : 100-240V, AC 50/60Hz, 1.5A @max  
Output : 12V DC, 5A



Internal (*`turtle4`*):  `with_me()_jigger(sbc)_ident(raspberry_pi, 4, model_a);`
Request (*from `turtle4`*):  `poke_robot(turtle1)_jigger(sbc)_ident();`
Response (*from `turtle1`*):  `poke_robot(turtle1)_jigger(sbc)_ident(raspberry_pi, 4, model_a);`


Internal (*`turtle4`*):  `with_me()_jigger(sbc)_ident(raspberry_pi, 4, model_a);`
Request (*from `turtle4`*):  `poke_jigger(sbc)_ident();`
Responses: `poke_jigger(sbc)_ident(raspberry_pi, 4, model_a)`	(*from `turtle1`*)
`poke_jigger(sbc)_ident(raspberry_pi, 3, model_b);`	(*from `turtle2`*)
`poke_jigger(sbc)_ident(raspberry_pi, 3, model_b);`	(*from `turtle3`*)
`poke_jigger(sbc)_ident(raspberry_pi, 4, model_a);`	(*from `turtle5`*)


Internal (*`turtle4`*):  `add_jigger(turtle1_sbc)_ident(raspberry_pi, 4, model_a);`
Request (*from `turtle4`*):  `poke_jigger(turtle1_sbc)_ident();`
Response (*from `turtle1`*):  `poke_jigger(turtle1_sbc)_ident(raspberry_pi, 4, model_a);`


Internal (*`turtle4`*):  `add_jigger(turtle1_sbc)_ident(raspberry_pi, 4, model_a);`
Request (*from `turtle4`*):  `poke_robot(turtle1)_jigger(turtle1_sbc)_ident();`
Response (*from `turtle1`*):  `poke_robot(turtle1)_jigger(turtle1_sbc)_ident(raspberry_pi, 4, model_a);`



```diego
begin_instruct(open_behaviour_tree);
  verb1_noun1(params)_sub(params);
  verb2_noun2(params)_sub(params);
  verb3_noun3(params)_sub(params);
end_instruct(open_behaviour_tree);
start_instruct(open_behaviour_tree);

with_instruct(open_behaviour_tree)_report();
with_instruct(open_behaviour_tree)_report(success);
with_instruct(open_behaviour_tree)_report(failure);

```
The `verb1_noun1` command will execute first.  When `verb1_noun1` has executed  `verb2_noun2` will execute regardless of the success or failure of `verb1_noun1`.  When `verb2_noun2` has executed  `verb3_noun3` will execute regardless of the success or failure of `verb2_noun2`.  


```diego
verb1_noun1(params)_sub(params) ?;
verb2_noun2(params)_sub(params) ?;
verb3_noun3(params)_sub(params) ?;
```

verb_noun(params)_sub(params) ? verb_noun(params)_sub(params) : verb_noun(params)_sub(params)
verb_noun(params)_sub(params) > verb_noun(params)_sub(params) : verb_noun(params)_sub(params)
verb_noun(params)_sub(params) >> verb_noun(params)_sub(params) : verb_noun(params)_sub(params)



```
