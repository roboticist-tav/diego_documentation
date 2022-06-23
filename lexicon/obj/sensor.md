# Sensor

A sensor is an child object of a thing the records specific data from its environment.  Data is usually communicated through `stat`s and `metric`s.

Examples:
```Diego
add_sensor(gyro)_me()
with_me()_sensor(gyro)_type(gyro);
```

