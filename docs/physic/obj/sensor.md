# Sensor (object)
A `sensor` is an child object of a thing (and/or a child object of a `module`) that records specific data from its environment.  Data is usually communicated through `stat`s and `metric`s.

## Syntax
The default declaration syntax is to provide at least the sensor moniker and type:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_sensor({`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_sensor(`*`moniker`*`)_type(`*`type`*`);`

Some commonly used sensors have their own object name, so in syntax declaring the type is not neccesary, for example:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_compass(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_tacho(`*`moniker`*`);`

Where a sensor is combined with other sensors, this is known as a `module`.  A `module` is optional, however, more granuality is provided if used.  The syntax, is such:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_module({`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_module(`*`moniker`*`)_type(`*`type`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_module({`*`type`*`},`*`moniker`*`)_sensor({`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_module(`*`moniker`*`)_type(`*`type`*`)_sensor(`*`moniker`*`)_type(`*`type`*`);`

Some commonly used modules have their own object name, so in syntax declaring the type is not neccesary, for example:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_imu(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_oplight(`*`moniker`*`);`

## Example
Many sensor declarations are used when serialising a new robot, for example:
```diego
use_namespace(alif_setup)_me();

with_me()
    add_lidar(lidar);
;
```

## Sensor Types

| sensor type | definition |
| --- | --- |
| <a name="accelero"></a>`{accelero}`<br>`_type(accelero)` | **Accelerometer**<br>A tool that measures proper acceleration. |
| <a name="amblight"></a>`{amblight}`<br>`_type(amblight)` | **Ambient Light Sensor**<br>A type of photoelectric sensor that is used to sense the amount of ambient light present, and appropriately dim.<br>See modules [oplight](#oplight). |
| <a name="amp"></a>`{amp}`<br>`_type(amp)` | **Amplifier**<br>An electronic component for increasing the amplitude of electrical signals, used chiefly in sound reproduction. |
| <a name="colo"></a>`{colo}`<br>`_type(colo)`<br>`_colo()` | **Colour Sensor**<br>A type of photoelectric sensor which emits light from a transmitter, and then detects the light reflected back from the detection object with a receiver.<br>See derivative: [colo](colo.md). See sensors: [photoelect](#photoelect). See modules: [optical](#optical). |
| <a name="compass"></a>`{compass}`<br>`_type(compass)`<br>`_compass()` | **Compass**<br>a device that shows the cardinal directions used for navigation and geographic orientation. *Usually combined into an [imu](#imu).*<br>See modules: [magnet](#magnet); [ins](#ins); [gnss/ins](#gnss_ins); [imu](#imu); [agm](#agm). |
| <a name="curren"></a>`{curren}`<br>`_type(curren)` | **Current Sensor**<br>A component that detects and converts current to an easily measurable output voltage, which is proportional to the current through the measured path. |
| <a name="encode"></a>`{encode}`<br>`_type(encode)` | **Encoder**<br>A one-hot to binary converter. |
| <a name="float"></a>`{float}`<br>`_type(float)` | **Float Sensor**<br>A a type of level sensor, a component used to detect the level of liquid within a tank.<br>See sensors: [level](#level). |
| <a name="flow"></a>`{flow}`<br>`_type(flow)` | **Flow Sensor**<br>An electronic component that measures or regulates the flow rate of liquids and gasses within pipes and tubes. |
| <a name="force"></a>`{force}`<br>`_type(force)` | **Force Sensor**<br>A component that converts the magnitude of force into related electrical signals. |
| <a name="gas"></a>`{gas}`<br>`_type(gas)` | **Gas Sensor**<br>A component that detects the presence of gases in an area, often as part of a safety system. |
| <a name="gyro"></a>`{gyro}`<br>`_type(gyro)`<br>`_gyro()` | **Gyroscope**<br>A component used for measuring or maintaining orientation and angular velocity. *Usually combined into an [imu](#imu).*<br>See modules: [ins](#ins); [gnss/ins](#gnss_ins); [imu](#imu); [agm](#agm); [motion](#motion). |
| <a name="hygro"></a>`{hygro}`<br>`_type(hygro)` | **Hygrometer / Humidity (Moisture) Sensor**<br>A component used to measure the amount of water vapor in air, in soil, or in confined spaces. |
| <a name="inclino"></a>`{inclino}`<br>`_type(inclino)` | **Inclinometer / Clinometer**<br>An instrument used for measuring angles of slope, elevation, or depression of an object with respect to gravity's direction.<br>See modules: [ins](#ins); [gnss/ins](#gnss_ins); [imu](#imu); [agm](#agm). |
| <a name="irda"></a>`{irda}`<br>`_type(irda)` | **IrDA Transceiver Module**<br>Hardware that sends information from an infrared remote control to another device by receiving and decoding signals. |
| <a name="level"></a>`{level}`<br>`_type(level)` | **Level Sensor / Float Level Sensor**<br>Used to detect the level of liquids and other fluids and fluidized solids, including slurries, granular materials, and powders that exhibit an upper free surface.<br>See sensors: [float](#float). |
| <a name="linear"></a>`{linear}`<br>`_type(linear)` | **Linear Position Sensor**<br>Measures the distance between an object and a point of reference, as well as changes in position.<br>See sensors: [posit](#posit); [prox](#prox). See modules: [magnet](#magnet). |
| <a name="lvdt"></a>`{lvdt}`<br>`_type(lvdt)` | **LVDT Transducer**<br>A device that converts energy from one form to another.  |
| <a name="mems"></a>`{mems}`<br>`_type(mems)` | **Magnet Field Sensor / MEMS / Magnetic Sensor**<br>A small-scale microelectromechanical systems device for detecting and measuring magnetic fields.<br>See modules: [magnet](#magnet). |
| <a name="posit"></a>`{posit}`<br>`_type(posit)` | **Position Sensor**<br>Measures the distance between an object and a point of reference.<br>See sensors: [linear](#linear); [prox](#prox). See modules: [magnet](#magnet). |
| <a name="press"></a>`{press}`<br>`_type(press)` | **Pressure Sensor**<br>A device for pressure measurement of gases or liquids.<br>See modules: [pth](#pth). |
| <a name="prox"></a>`{prox}`<br>`_type(prox)` | **Proximity Sensor**<br>A sensor able to detect the presence of nearby objects without any physical contact.<br>See sensors: [posit](#posit); [linear](#linear). See modules: [magnet](#magnet). |
| <a name="tacho"></a>`{tacho}`<br>`_type(tacho)`<br>`_tacho()` | **Tachometer / Speed Sensor**<br>A sender device used for reading the speed of a vehicle's wheel rotation..<br>See modules: [magnet](#magnet). |
| <a name="thermo"></a>`{thermo}`<br>`_type(thermo)`<br>`_thermo()` | **Thermometer / Temperature Sensor**<br>A two terminal integrated circuit temperature transducer that produces an output current proportional to absolute temperature.<br>See modules: [magnet](#magnet). |
| <a name="tilt"></a>`{tilt}`<br>`_type(tilt)` | **Tilt Sensor**<br>A device used for measuring the tilt of an object in multiple axes with reference to an absolute level plane. |
| <a name="vibrat"></a>`{vibrat}`<br>`_type(vibrat)` | **Vibration Sensor**<br>A device that measures the amount and frequency of vibration in a given system, machine, or piece of equipment. |

<!--| <a name="optimot"></a>`{optimot}`<br>`_type(optimot)` | **Optical Motion Sensor**<br>A small-scale microelectromechanical systems device for detecting and measuring magnetic fields.<br>See modules: [magnet](#magnet). |-->

## Module Types

| sensor type | definition |
| --- | --- |
| <a name="imu"></a>`{imu}`<br>`_type(imu)`<br>`_imu()` | **Inertial Measurement Unit**<br>IMUs can carry: [accelerometer](#accelero); [gyroscopes](#gyro);... [thermometer](#temp); [linear position sensor](#linear); [tachometer](#tacho)  |
| <a name="magnet"></a>`{magnet}`<br>`_type(magnet)` | **Magnetic Module**<br>Magnetic modules can carry: [compass](#compass); [magnetic field sensor](#mems); [thermometer](#temp); [linear position sensor](#linear); [tachometer](#tacho)  |
| <a name="motion"></a>`{motion}`<br>`_type(motion)` | **Motion Sensors**<br>Motion modules can carry: [accelerometer](#accelero); [gyroscopes](#gyro);... [thermometer](#temp); [linear position sensor](#linear); [tachometer](#tacho)  |
| <a name="oplight"></a>`{oplight}`<br>`_type(oplight)`<br>`_oplight()` | **Optical Light Module**<br>Motion modules can carry: [ambient light sensor](#amblight); [infra-red light sensor](#irlight); [ultra-violet light sensor](#uvlight). |
| <a name="pth"></a>`{pth}`<br>`_type(pth)` | **Pressure / Temperature/ Humidity Module**<br>Motion modules can carry: [pressure sensor](#press); [thermometer](#temp); [hygrometer](#hygro). |




| `sensor` | The thing version of an `apparatus`.<br>See also: [apparat](#apparat) |