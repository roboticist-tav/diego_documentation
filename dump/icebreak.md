
begin_instruct(diego_me);
    add_me(ice_break_929d, f2d5f245-1660-4d18-9634-1461c1eb929d);
    with_me()_ident(Lactalis, Ice Break, regular_strength_500ml_aus, f2d5f245-1660-4d18-9634-1461c1eb929d);
    with_me()_type(human_consumable, beverage);

    with_me()_base(human_haul);
    with_me()_base(store_chilled)_value(-5);
    with_me()_base(transport_chilled)_value(-5);
end_instruct(deigo_me);

begin_instruct(diego_iot);
    with_me()_thing(bottle_drink);
    with_me(ice_break_929d_, f2d5f245-1660-4d18-9634-1461c1eb929d);
    with_me()_ident(Lactalis, Ice Break, regular_strength_500ml_aus, f2d5f245-1660-4d18-9634-1461c1eb929d);
    with_me()_batch(059751, 668, 297, 11:34, F2);

    iot_me(GoogleIoTCore)_me(ice_break_929d, f2d5f245-1660-4d18-9634-1461c1eb929d)_ident(Lactalis, Ice Break, regular_strength_500ml_aus, f2d5f245-1660-4d18-9634-1461c1eb929d);
    iot_me(AWSIoTCore)_ident(Lactalis, Ice Break, regular_strength_500ml_aus, f2d5f245-1660-4d18-9634-1461c1eb929d);
    iot_me(AzureIoTCore);
end_instruct(diego_iot);

begin_instruct(diego_sensors);
    with_me()_identbeacon(ib_929d);
    

end_instruct(deigo_sensors);

begin_instruct(diego_equip);

end_instruct(diego_equip);

begin_instruct(diego_specs);
  set_vol(ml);
  set_energy(KJ);
  set_mass(g);

  with_me()_spec(max_volume, 500);
  with_me()_spec(use_by_date, 2020-11-10);
  with_me()_spec(coffee_cups, 2);
  
  with_me()_spec(ingred, reduced_fat_milk);
  with_me()_spec(ingred, sugar);
  with_me()_spec(ingred, coffee);

  with_me()_spec(serv_pack, 1);
  with_me()_spec(serv_size, 500, ml);
  with_me()_spec(nutrit, energy, 1480, per_serving);
  with_me()_spec(nutrit, energy, 295, per_100ml);
  with_me()_spec(nutrit, protein, 16.5, per_serving);
  with_me()_spec(nutrit, protein, 3.3, per_100ml);
  with_me()_spec(nutrit, fat_total, 8.5, per_serving);
  with_me()_spec(nutrit, fat_total, 1.7, per_100ml);
  with_me()_spec(nutrit, fat_sat, 5.5, per_serving);
  with_me()_spec(nutrit, fat_sat, 1.1, per_100ml);
  with_me()_spec(nutrit, carbs_total, 52, per_serving);
  with_me()_spec(nutrit, carbs_total, 10.4, per_100ml);
  with_me()_spec(nutrit, carbs_sugars, 52, per_serving);
  with_me()_spec(nutrit, carbs_sugars, 10.4, per_100ml);
  
  with_me()_spec(nutrit, caffine, 140, per_serving);


end_instruct(diego_specs);

begin_instruct(diego_metrics);
  set_vol(ml);

  with_me()_spec(volume);
end_instruct(diego_metrics);

begin_instruct(diego_jiggers);

end_instruct(diego_jiggers);

start_instruct(deigo_me);
start_instruct(deigo_iot);
start_instruct(deigo_sensors);
start_instruct(diego_equip);
start_instruct(diego_specs);
start_instruct(diego_metrics);
start_instruct(diego_jiggers);


metric: A mutable, measurable and testable value as a charateristic of the object.
spec[ification]: An immutable, measurable and testable values as a charateristic of the object.

```diego
set_vol(ml);
  
  with_
```

```diego
  with_me()_metric(
```

```diego
if_metric(cur_volume <= 0) ? :;
```

^f2d5f245-1660-4d18-9634-1461c1eb929d^





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

with_me()_spec(
with_me()_spec(

```


Size (L x W x H)

138mm x 178mm x 192mm

Weight (+ SBC + Battery + Sensors)

1kg

Threshold of climbing

10 mm or lower

Expected operating time

2h 30m

Expected charging time

2h 30m

SBC (Single Board Computers)

Raspberry Pi 3 Model B and B+

MCU

32-bit ARM Cortex®-M7 with FPU (216 MHz, 462 DMIPS)

Remote Controller

-

Actuator

XL430-W250

LDS(Laser Distance Sensor)

360 Laser Distance Sensor LDS-01

Camera

-

IMU

Gyroscope 3 Axis  
Accelerometer 3 Axis  
Magnetometer 3 Axis

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

