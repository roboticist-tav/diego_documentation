# Battery

The `battery` object represents any controllable battery contained within and/or managed by a thingy. Posits of a `battery` are inherited to the `powersupply` object, most usually when a `battery` becomes a/the power supply (temporary ot otherwise) of a thingy.

## Syntax

The default declaration syntax is to provide at least the battery name. The shortened version is `batt`. The `_type` can be added at declaration or after declaration:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_battery(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_batt(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_batt(`*`moniker`*`)_type(`*`type`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_batt({`*`type`*`},`*`moniker`*`);`

Multiple batteries can be added as batteries or as part of a `bank` of batteries (treated like a farm or array). Battery banks can be indexed:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_battery(`*`moniker1`*`, `*`moniker2,...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_bank(`*`moniker`*`)_battery(`*`moniker1`*`, `*`moniker2,...`*`)_index(`*`index-form`*`, `*`base`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_bank(`*`moniker`*`)_batt_({`*`type`*`},`*`moniker1`*`,`*`moniker2,...`*`)`

Each battery is implied to have one default associated charge (one charger per battery), it is, therefore, not neccessary to declare or named, by can be:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_battery(`*`moniker`*`)_charger();`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_batt(`*`moniker`*`)_charger(`*`moniker`*`);`<br>

Any declaration/creation/serialisation on `battery`(s) can be undertaken by thingies themselves (_i.e._ using `me()`), by another authority on to the target thingy, or, as depiction of another thingy.

## Properties

| property | access | notes |
| --- | --- | --- |
| <a name="algor"></a>`_charger()_algorithm(algorithm)`<br>`_charger()_algor(algorithm)`<br>`_charger()_algo(algorithm)` | read (write by me) | **Charging Algorithm**<br>The charging algorithm, if known, that the charger using.  The `charger` postposit is implied with every battery.  The `_algorithm`/`algor`/`algo` postposit is implied to be a child of `charger`.<br>See [Algorithm Values](#algor_) |
| <a name="fettle"></a>`_fettle()`<br>`_fettle()_enum()` | read (write by human) | **Battery Fettle**<br>A human observation of the state of appearance of the battery.<br>See [Fettle Values](#fettle_) |
| <a name="health"></a>`_health()`<br>`_health()_enum()` | read only | **Battery Health**<br>The battery health, as defined within the battery logic.  It will display a string as default, unless the `_enum()` postposit is provided then it will provide a integer enumerator.<br>See [Health Values](#health_) |
| <a name="status"></a>`_stat()`<br>`_status()`<br>`_stat()_enum()`<br>`_status()_enum()` | read only | **Battery Status**<br>The battery status, as defined within the battery logic.  It will display a string as default, unless the `_enum()` postposit is provided then it will provide a integer enumerator.<br>See [Status Values](#stat_) |
| <a name="tech"></a>`_tech(`*`technology`*`)`<br>`_technology(`*`technology`*`)`<br>`_chem(`*`technology`*`)`<br>`_chemistry(`*`technology`*`)`<br>*`...`*`_enum()` | read (write by me) | **Battery Technology**<br>The technology (or chemistry) composition of the battery.  This is usually defined at declaration. It will display a string as default, unless the `_enum()` postposit is provided then it will provide a integer enumerator. This can only be set/changed by `me`.<br>See [Technology Values](#tech_) |

<a name="algor_"></a>
### Algorithm Values
| `algorithm` | `enum` | notes |
| --- | --- | --- |
| `unknown`, `error` | `-1` | unknown |
| *`null`* | `0` | no charge/unknown |
| `none`, `no-charge` | `1` | no charge |
| `trickle`, `slow` | `2` | Trickle charge, slow speed |
| `fast` | `3` | fast charge |
| `norm`, `normal`, `standard` | `4` | normal speed charge |
| `adaptive`, `adpt` | `5` | adaptive charge, dynamically adjusted speed |
| `custom` | `6` | custom charge algorithm |
| `long`, `longlife`, `long-life` | `7` | slow speed, longer life charge algorithm |

<a name="fettle_"></a>
### Fettle Values
| `fettle` | `enum` | notes |
| --- | --- | --- |
| `unknown`, `error` | `-1` |  |
| *`null`*, `not checked` | `0` | |
| `good` | `1` |  |
| `ok` | `2` |  |
| `bad-condition` | `3` |  |
| `deteriorated` | `4` |  |

<a name="health_"></a>
### Health Values
| `health` | `enum` | notes |
| --- | --- | --- |
| `unknown`, `error` | `-1` | unknown |
| *`null`* | `0` | |
| `good` | `1` | good |
| `overheat` | `2` | overheat |
| `dead` | `3` | dead |
| `overvoltage`, `overvolt` | `4` | unknown |
| `unspec`, `unspec-failure` | `5` | |
| `cold` | `6` | |
| `watchdog`, `watchdog-expire`, `watchdog-timer` | `7` | |
| `safety`, `safety-expire`, `safety-timer` | `8` | |

<a name="stat_"></a>
### Status Values
| `stat`, `status` | `enum` | notes |
| --- | --- | --- |
| `unknown`, `error` | `-1` |  unknown |
| *`null`*, `no`, `none` | `0` |  null state |
| `charging` | `1` |  charging |
| `discharging` | `2` |  discharging |
| `not charging`, `no`, `none` | `0` |  not charging |
| `full` | `4` |  full |


<a name="tech_"></a>
### Technology Values 

| `technology` | `enum` | notes |
| --- | --- | --- |
| `unknown` | `-1` | Unknown or not specified battery technology. Question target thingy with `ask_`. |
| `null` | `0` | No available property for battery technology.  Check to see if battery exists (use `_exists()`). |
| `NiMH`, `Ni–MH`, `nimh` | `1` | Nickel metal hydride battery. |
| `Li-ion`, `lion` | `2` | Lithium cobaltate (lithium-ion cobalt) battery. |
| `LiPo`, `lipo` | `3` | Lithium polymer battery (lithium-ion polymer) battery. |
| `LiFE`, `LiFEPO`, `life` | `4` | Lithium iron phosphate battery. |
| `NiCad`, `Ni-Cd`, `nicd` | `5` | Nickel–cadmium battery. |
| `LMO`, `LiMO`, `limo` | `6` | Lithium ion manganese oxide battery. |



## Metrics

| metric | notes |
| --- | --- |
| `_volt(`*`voltage`*`)`, `_voltage(`*`voltage`*`)`<br/> `_volt()_value(`*`voltage`*`)`, `_voltage()_value(`*`voltage`*`)` | The  voltage of the battery charge in volts (V).  If the thingy is intent on using another measurement then `_unit` must be supplied with intra-thingy communication.<br/>Variable assignment is available, using posits such as `_tovar` etc.<br/>See also [voltage limits](#voltstate). |


| metric | notes |
| --- | --- |
| `_volt(`*`voltage-state`*`)`, `_voltage(`*`voltage-state`*`)` | Voltage state |
| `_volt(`*`voltage-state`*`)_value(`*`voltage`*`)`, `_voltage(`*`voltage-state`*`)_value(`*`voltage`*`)`<br/>`_volt(`*`voltage`*`)_limit(`*`voltage-state`*`)`, `_voltage(`*`voltage`*`)_limit(`*`voltage-state`*`)`<br/>`_volt()_limit(max)_value(`*`voltage`*`)`, `_voltage()_limit(max)_value(`*`voltage`*`)` | |





| `_volt(`*`[voltage-state]`*`)_value(`*`voltage`*`)`, `_voltage(`*`[voltage-state]`*`)_value(`*`voltage`*`)` | Voltage status with value (in volts) |
| `_volt(`*`[voltage-state]`*`)_value(`*`voltage`*`)`, `_voltage(`*`[voltage-state]`*`)` | Voltage value (in volts) |


Examples:
 robot `alpha`, `beta`

```Deigo

// Robot `alpha` asks robot `beta` for its battery temperature
ask_robot(beta)_battery(b1)_temp();
tell_robot(alpha)_battery(b1)_temp(23.3);

// Robot `alpha` asks robot `beta` for its max battery temperature in the last 30 minutes
ask_robot(beta)_battery(b1)_temp()_limit(max)_inlast(30, min);
tell_robot(alpha)_battery(b1)_temp(23.3)_limit(max)_inlast(30, min)_datetime(2021-10-09 13:06:21.402);
```

```Diego

add_bank(bat-array)_battery(b1, b2, b3, b4)_index(0)_chem(nimh);
with_robot(beta)_bank(bat-array);

with_robot(beta)_battery(b2)_volt()_limit(maxdesign)_value(5.00);




```
_


## Limits

## Alerts



# Voltage (VBAT)

| syntax | |
| --- | --- |
| `_volt(`*`voltage-state`*`)`, `_voltage(`*`voltage-state`*`)` | Voltage state request. |
| `_volt(`*`voltage-state`*`)_value(`*`voltage`*`)`, `_voltage(`*`voltage-state`*`)_value(`*`voltage`*`)`<br/>`_volt(`*`voltage`*`)_limit(`*`voltage-state`*`)`, `_voltage(`*`voltage`*`)_limit(`*`voltage-state`*`)`<br/>`_volt()_limit(max)_value(`*`voltage`*`)`, `_voltage()_limit(max)_value(`*`voltage`*`)` | Voltage state response. |

| `voltage-state` | |
| --- | --- |
| `max` | Reports the maximum VBAT voltage permitted for the battery, during charging. |
| `min` | Reports the minimum VBAT voltage permitted for the battery, during discharging. |
| `maxdes`, `maxdesign` | Reports the designed maximum safe VBAT voltage permitted for the battery, during charging. |
| `mindes`, `mindesign` | Reports the designed minimum safe VBAT voltage permitted for the battery, during discharging. |
| `now` | Reports an instant, single VBAT voltage reading for the battery. This value is not averaged/smoothed. |
| `ocv` | The 'Open Circuit Voltage' of the battery. |






fettle


health()
// Stats:
| posit | |
| --- | --- |


This property can be used for platform shutdown policies and
can be useful for initial capacity estimations. |
| `max` | maximum voltage |

	POWER_SUPPLY_PROP_VOLTAGE_MAX,
	POWER_SUPPLY_PROP_VOLTAGE_MIN,
	POWER_SUPPLY_PROP_VOLTAGE_MAX_DESIGN,
	POWER_SUPPLY_PROP_VOLTAGE_MIN_DESIGN,
	POWER_SUPPLY_PROP_VOLTAGE_NOW,
	POWER_SUPPLY_PROP_VOLTAGE_AVG,
	POWER_SUPPLY_PROP_VOLTAGE_OCV,
	POWER_SUPPLY_PROP_VOLTAGE_BOOT,


| `_temp(`*`temperature`*`)`, `_temperature(`*`temperature`*`)` | Temperature in Degrees Celsius or `_unit()` |
| `_current` | Negative when discharging in Amps (A) or `_unit()` |
| `_charge _ah()` | Current charge in Ah |




	int ocv_temp[POWER_SUPPLY_OCV_TEMP_MAX];/* celsius */
	int temp_ambient_alert_min;             /* celsius */
	int temp_ambient_alert_max;             /* celsius */
	int temp_alert_min;                     /* celsius */
	int temp_alert_max;                     /* celsius */
	int temp_min;                           /* celsius */
	int temp_max;                           /* celsius */

    struct power_supply_resistance_temp_table {
	int temp;	/* celsius */
	int resistance;	/* internal resistance percent */

        `_temp(`*`)_level(`-`temperature-level`*`)_value(`*`temperature-value`*`)`
        _temp()
        
    | `temperature-level` | |
    | `max` | maximum


_temp()_level(max)


with_battery(ba1)_temp()_level(max)


begin_battery(ba1)_temp()_level(max)

    // Do something when the temperature of the battery gets to max

end_battery(ba1)_temp()_level(max)

	POWER_SUPPLY_PROP_TEMP,
	POWER_SUPPLY_PROP_TEMP_MAX,
	POWER_SUPPLY_PROP_TEMP_MIN,
	POWER_SUPPLY_PROP_TEMP_ALERT_MIN,
	POWER_SUPPLY_PROP_TEMP_ALERT_MAX,
	POWER_SUPPLY_PROP_TEMP_AMBIENT,
	POWER_SUPPLY_PROP_TEMP_AMBIENT_ALERT_MIN,
	POWER_SUPPLY_PROP_TEMP_AMBIENT_ALERT_MAX,
    
};
#define POWER_SUPPLY_OCV_TEMP_MAX 20



	struct power_supply_battery_ocv_table *ocv_table[POWER_SUPPLY_OCV_TEMP_MAX];
	int ocv_table_size[POWER_SUPPLY_OCV_TEMP_MAX];
	struct power_supply_resistance_temp_table *resist_table;

| `_cap`, `_capacity` | Capacity in Ah (last full capacity) |
| `_cap _des()`, `_capacity_design()` | Capacity in Ah (design capacity) |
| `_float32 percentage       # Charge percentage on 0 to 1 range  (If unmeasured NaN)
uint8   power_supply_status     # The charging status as reported. Values defined above
uint8   power_supply_health     # The battery health metric. Values defined above
uint8   power_supply_technology # The battery chemistry. Values defined above
bool    present          # True if the battery is present

)_voltage()_temp()
# Constants are chosen to match the enums in the linux kernel
# defined in include/linux/power_supply.h as of version 3.7
# The one difference is for style reasons the constants are
# all uppercase not mixed case.





std_msgs/Header  header
float32 voltage          # Voltage in Volts (Mandatory)
float32 temperature      # Temperature in Degrees Celsius (If unmeasured NaN)
float32 current          # Negative when discharging (A)  (If unmeasured NaN)
float32 charge           # Current charge in Ah  (If unmeasured NaN)
float32 capacity         # Capacity in Ah (last full capacity)  (If unmeasured NaN)
float32 design_capacity  # Capacity in Ah (design capacity)  (If unmeasured NaN)
float32 percentage       # Charge percentage on 0 to 1 range  (If unmeasured NaN)
uint8   power_supply_status     # The charging status as reported. Values defined above
uint8   power_supply_health     # . Values defined above
uint8   power_supply_technology # The battery chemistry. Values defined above
bool    present          # True if the battery is present

float32[] cell_voltage   # An array of individual cell voltages for each cell in the pack
                         # If individual voltages unknown but number of cells known set each to NaN
float32[] cell_temperature # An array of individual cell temperatures for each cell in the pack
                           # If individual temperatures unknown but number of cells known set each to NaN
string location          # The location into which the battery is inserted. (slot number or plug)
string serial_number     # The best approximation of the battery serial number

/* SPDX-License-Identifier: GPL-2.0-only */
/*
 *  Universal power supply monitor class
 *
 *  Copyright © 2007  Anton Vorontsov <cbou@mail.ru>
 *  Copyright © 2004  Szabolcs Gyurko
 *  Copyright © 2003  Ian Molton <spyro@f2s.com>
 *
 *  Modified: 2004, Oct     Szabolcs Gyurko
 */

#ifndef __LINUX_POWER_SUPPLY_H__
#define __LINUX_POWER_SUPPLY_H__

#include <linux/device.h>
#include <linux/workqueue.h>
#include <linux/leds.h>
#include <linux/spinlock.h>
#include <linux/notifier.h>

/*
 * All voltages, currents, charges, energies, time and temperatures in uV,
 * µA, µAh, µWh, seconds and tenths of degree Celsius unless otherwise
 * stated. It's driver's job to convert its raw values to units in which
 * this class operates.
 */





enum {
	POWER_SUPPLY_HEALTH_UNKNOWN = 0,
	POWER_SUPPLY_HEALTH_GOOD,
	POWER_SUPPLY_HEALTH_OVERHEAT,
	POWER_SUPPLY_HEALTH_DEAD,
	POWER_SUPPLY_HEALTH_OVERVOLTAGE,
	POWER_SUPPLY_HEALTH_UNSPEC_FAILURE,
	POWER_SUPPLY_HEALTH_COLD,
	POWER_SUPPLY_HEALTH_WATCHDOG_TIMER_EXPIRE,
	POWER_SUPPLY_HEALTH_SAFETY_TIMER_EXPIRE,
	POWER_SUPPLY_HEALTH_OVERCURRENT,
	POWER_SUPPLY_HEALTH_CALIBRATION_REQUIRED,
	POWER_SUPPLY_HEALTH_WARM,
	POWER_SUPPLY_HEALTH_COOL,
	POWER_SUPPLY_HEALTH_HOT,
};

enum {
	POWER_SUPPLY_TECHNOLOGY_UNKNOWN = 0,
	POWER_SUPPLY_TECHNOLOGY_NiMH,
	POWER_SUPPLY_TECHNOLOGY_LION,
	POWER_SUPPLY_TECHNOLOGY_LIPO,
	POWER_SUPPLY_TECHNOLOGY_LiFe,
	POWER_SUPPLY_TECHNOLOGY_NiCd,
	POWER_SUPPLY_TECHNOLOGY_LiMn,
};

_cap()_level()
enum {
	POWER_SUPPLY_CAPACITY_LEVEL_UNKNOWN = 0,
	POWER_SUPPLY_CAPACITY_LEVEL_CRITICAL,
	POWER_SUPPLY_CAPACITY_LEVEL_LOW,
	POWER_SUPPLY_CAPACITY_LEVEL_NORMAL,
	POWER_SUPPLY_CAPACITY_LEVEL_HIGH,
	POWER_SUPPLY_CAPACITY_LEVEL_FULL,
};

enum {
	POWER_SUPPLY_SCOPE_UNKNOWN = 0,
	POWER_SUPPLY_SCOPE_SYSTEM,
	POWER_SUPPLY_SCOPE_DEVICE,
};

enum power_supply_property {
	/* Properties of type `int' */
	POWER_SUPPLY_PROP_STATUS = 0,
	POWER_SUPPLY_PROP_CHARGE_TYPE,
	POWER_SUPPLY_PROP_HEALTH,
	POWER_SUPPLY_PROP_PRESENT,
	POWER_SUPPLY_PROP_ONLINE,
	POWER_SUPPLY_PROP_AUTHENTIC,
	POWER_SUPPLY_PROP_TECHNOLOGY,
	POWER_SUPPLY_PROP_CYCLE_COUNT,

	POWER_SUPPLY_PROP_CURRENT_MAX,
	POWER_SUPPLY_PROP_CURRENT_NOW,
	POWER_SUPPLY_PROP_CURRENT_AVG,
	POWER_SUPPLY_PROP_CURRENT_BOOT,
	POWER_SUPPLY_PROP_POWER_NOW,
	POWER_SUPPLY_PROP_POWER_AVG,
	POWER_SUPPLY_PROP_CHARGE_FULL_DESIGN,
	POWER_SUPPLY_PROP_CHARGE_EMPTY_DESIGN,
	POWER_SUPPLY_PROP_CHARGE_FULL,
	POWER_SUPPLY_PROP_CHARGE_EMPTY,
	POWER_SUPPLY_PROP_CHARGE_NOW,
	POWER_SUPPLY_PROP_CHARGE_AVG,
	POWER_SUPPLY_PROP_CHARGE_COUNTER,
	POWER_SUPPLY_PROP_CONSTANT_CHARGE_CURRENT,
	POWER_SUPPLY_PROP_CONSTANT_CHARGE_CURRENT_MAX,
	POWER_SUPPLY_PROP_CONSTANT_CHARGE_VOLTAGE,
	POWER_SUPPLY_PROP_CONSTANT_CHARGE_VOLTAGE_MAX,
	POWER_SUPPLY_PROP_CHARGE_CONTROL_LIMIT,
	POWER_SUPPLY_PROP_CHARGE_CONTROL_LIMIT_MAX,
	POWER_SUPPLY_PROP_CHARGE_CONTROL_START_THRESHOLD, /* in percents! */
	POWER_SUPPLY_PROP_CHARGE_CONTROL_END_THRESHOLD, /* in percents! */
	POWER_SUPPLY_PROP_INPUT_CURRENT_LIMIT,
	POWER_SUPPLY_PROP_INPUT_VOLTAGE_LIMIT,
	POWER_SUPPLY_PROP_INPUT_POWER_LIMIT,
	POWER_SUPPLY_PROP_ENERGY_FULL_DESIGN,
	POWER_SUPPLY_PROP_ENERGY_EMPTY_DESIGN,
	POWER_SUPPLY_PROP_ENERGY_FULL,
	POWER_SUPPLY_PROP_ENERGY_EMPTY,
	POWER_SUPPLY_PROP_ENERGY_NOW,
	POWER_SUPPLY_PROP_ENERGY_AVG,
	POWER_SUPPLY_PROP_CAPACITY, /* in percents! */
	POWER_SUPPLY_PROP_CAPACITY_ALERT_MIN, /* in percents! */
	POWER_SUPPLY_PROP_CAPACITY_ALERT_MAX, /* in percents! */
	POWER_SUPPLY_PROP_CAPACITY_ERROR_MARGIN, /* in percents! */
	POWER_SUPPLY_PROP_CAPACITY_LEVEL,




	POWER_SUPPLY_PROP_TIME_TO_EMPTY_NOW,
	POWER_SUPPLY_PROP_TIME_TO_EMPTY_AVG,
	POWER_SUPPLY_PROP_TIME_TO_FULL_NOW,
	POWER_SUPPLY_PROP_TIME_TO_FULL_AVG,
	POWER_SUPPLY_PROP_TYPE, /* use power_supply.type instead */
	POWER_SUPPLY_PROP_USB_TYPE,
	POWER_SUPPLY_PROP_SCOPE,
	POWER_SUPPLY_PROP_PRECHARGE_CURRENT,
	POWER_SUPPLY_PROP_CHARGE_TERM_CURRENT,
	POWER_SUPPLY_PROP_CALIBRATE,
	POWER_SUPPLY_PROP_MANUFACTURE_YEAR,
	POWER_SUPPLY_PROP_MANUFACTURE_MONTH,
	POWER_SUPPLY_PROP_MANUFACTURE_DAY,
	/* Properties of type `const char *' */
	POWER_SUPPLY_PROP_MODEL_NAME,
	POWER_SUPPLY_PROP_MANUFACTURER,
	POWER_SUPPLY_PROP_SERIAL_NUMBER,
};

enum power_supply_type {
	POWER_SUPPLY_TYPE_UNKNOWN = 0,
	POWER_SUPPLY_TYPE_BATTERY,
	POWER_SUPPLY_TYPE_UPS,
	POWER_SUPPLY_TYPE_MAINS,
	POWER_SUPPLY_TYPE_USB,			/* Standard Downstream Port */
	POWER_SUPPLY_TYPE_USB_DCP,		/* Dedicated Charging Port */
	POWER_SUPPLY_TYPE_USB_CDP,		/* Charging Downstream Port */
	POWER_SUPPLY_TYPE_USB_ACA,		/* Accessory Charger Adapters */
	POWER_SUPPLY_TYPE_USB_TYPE_C,		/* Type C Port */
	POWER_SUPPLY_TYPE_USB_PD,		/* Power Delivery Port */
	POWER_SUPPLY_TYPE_USB_PD_DRP,		/* PD Dual Role Port */
	POWER_SUPPLY_TYPE_APPLE_BRICK_ID,	/* Apple Charging Method */
	POWER_SUPPLY_TYPE_WIRELESS,		/* Wireless */
};

enum power_supply_usb_type {
	POWER_SUPPLY_USB_TYPE_UNKNOWN = 0,
	POWER_SUPPLY_USB_TYPE_SDP,		/* Standard Downstream Port */
	POWER_SUPPLY_USB_TYPE_DCP,		/* Dedicated Charging Port */
	POWER_SUPPLY_USB_TYPE_CDP,		/* Charging Downstream Port */
	POWER_SUPPLY_USB_TYPE_ACA,		/* Accessory Charger Adapters */
	POWER_SUPPLY_USB_TYPE_C,		/* Type C Port */
	POWER_SUPPLY_USB_TYPE_PD,		/* Power Delivery Port */
	POWER_SUPPLY_USB_TYPE_PD_DRP,		/* PD Dual Role Port */
	POWER_SUPPLY_USB_TYPE_PD_PPS,		/* PD Programmable Power Supply */
	POWER_SUPPLY_USB_TYPE_APPLE_BRICK_ID,	/* Apple Charging Method */
};

enum power_supply_notifier_events {
	PSY_EVENT_PROP_CHANGED,
};

union power_supply_propval {
	int intval;
	const char *strval;
};

struct device_node;
struct power_supply;

/* Run-time specific power supply configuration */
struct power_supply_config {
	struct device_node *of_node;
	struct fwnode_handle *fwnode;

	/* Driver private data */
	void *drv_data;

	/* Device specific sysfs attributes */
	const struct attribute_group **attr_grp;

	char **supplied_to;
	size_t num_supplicants;
};

/* Description of power supply */
struct power_supply_desc {
	const char *name;
	enum power_supply_type type;
	const enum power_supply_usb_type *usb_types;
	size_t num_usb_types;
	const enum power_supply_property *properties;
	size_t num_properties;

	/*
	 * Functions for drivers implementing power supply class.
	 * These shouldn't be called directly by other drivers for accessing
	 * this power supply. Instead use power_supply_*() functions (for
	 * example power_supply_get_property()).
	 */
	int (*get_property)(struct power_supply *psy,
			    enum power_supply_property psp,
			    union power_supply_propval *val);
	int (*set_property)(struct power_supply *psy,
			    enum power_supply_property psp,
			    const union power_supply_propval *val);
	/*
	 * property_is_writeable() will be called during registration
	 * of power supply. If this happens during device probe then it must
	 * not access internal data of device (because probe did not end).
	 */
	int (*property_is_writeable)(struct power_supply *psy,
				     enum power_supply_property psp);
	void (*external_power_changed)(struct power_supply *psy);
	void (*set_charged)(struct power_supply *psy);

	/*
	 * Set if thermal zone should not be created for this power supply.
	 * For example for virtual supplies forwarding calls to actual
	 * sensors or other supplies.
	 */
	bool no_thermal;
	/* For APM emulation, think legacy userspace. */
	int use_for_apm;
};

struct power_supply {
	const struct power_supply_desc *desc;

	char **supplied_to;
	size_t num_supplicants;

	char **supplied_from;
	size_t num_supplies;
	struct device_node *of_node;

	/* Driver private data */
	void *drv_data;

	/* private */
	struct device dev;
	struct work_struct changed_work;
	struct delayed_work deferred_register_work;
	spinlock_t changed_lock;
	bool changed;
	bool initialized;
	bool removing;
	atomic_t use_cnt;
#ifdef CONFIG_THERMAL
	struct thermal_zone_device *tzd;
	struct thermal_cooling_device *tcd;
#endif

#ifdef CONFIG_LEDS_TRIGGERS
	struct led_trigger *charging_full_trig;
	char *charging_full_trig_name;
	struct led_trigger *charging_trig;
	char *charging_trig_name;
	struct led_trigger *full_trig;
	char *full_trig_name;
	struct led_trigger *online_trig;
	char *online_trig_name;
	struct led_trigger *charging_blink_full_solid_trig;
	char *charging_blink_full_solid_trig_name;
#endif
};

/*
 * This is recommended structure to specify static power supply parameters.
 * Generic one, parametrizable for different power supplies. Power supply
 * class itself does not use it, but that's what implementing most platform
 * drivers, should try reuse for consistency.
 */

struct power_supply_info {
	const char *name;
	int technology;
	int voltage_max_design;
	int voltage_min_design;
	int charge_full_design;
	int charge_empty_design;
	int energy_full_design;
	int energy_empty_design;
	int use_for_apm;
};

struct power_supply_battery_ocv_table {
	int ocv;	/* microVolts */
	int capacity;	/* percent */
};




/*
 * This is the recommended struct to manage static battery parameters,
 * populated by power_supply_get_battery_info(). Most platform drivers should
 * use these for consistency.
 * Its field names must correspond to elements in enum power_supply_property.
 * The default field value is -EINVAL.
 * Power supply class itself doesn't use this.
 */

struct power_supply_battery_info {
	int energy_full_design_uwh;	    /* microWatt-hours */
	int charge_full_design_uah;	    /* microAmp-hours */
	int voltage_min_design_uv;	    /* microVolts */
	int voltage_max_design_uv;	    /* microVolts */
	int tricklecharge_current_ua;	    /* microAmps */
	int precharge_current_ua;	    /* microAmps */
	int precharge_voltage_max_uv;	    /* microVolts */
	int charge_term_current_ua;	    /* microAmps */
	int charge_restart_voltage_uv;	    /* microVolts */
	int overvoltage_limit_uv;	    /* microVolts */
	int constant_charge_current_max_ua; /* microAmps */
	int constant_charge_voltage_max_uv; /* microVolts */
	int factory_internal_resistance_uohm;   /* microOhms */

	int resist_table_size;
};

extern struct atomic_notifier_head power_supply_notifier;
extern int power_supply_reg_notifier(struct notifier_block *nb);
extern void power_supply_unreg_notifier(struct notifier_block *nb);
#if IS_ENABLED(CONFIG_POWER_SUPPLY)
extern struct power_supply *power_supply_get_by_name(const char *name);
extern void power_supply_put(struct power_supply *psy);
#else
static inline void power_supply_put(struct power_supply *psy) {}
static inline struct power_supply *power_supply_get_by_name(const char *name)
{ return NULL; }
#endif
#ifdef CONFIG_OF
extern struct power_supply *power_supply_get_by_phandle(struct device_node *np,
							const char *property);
extern struct power_supply *devm_power_supply_get_by_phandle(
				    struct device *dev, const char *property);
#else /* !CONFIG_OF */
static inline struct power_supply *
power_supply_get_by_phandle(struct device_node *np, const char *property)
{ return NULL; }
static inline struct power_supply *
devm_power_supply_get_by_phandle(struct device *dev, const char *property)
{ return NULL; }
#endif /* CONFIG_OF */

extern int power_supply_get_battery_info(struct power_supply *psy,
					 struct power_supply_battery_info *info);
extern void power_supply_put_battery_info(struct power_supply *psy,
					  struct power_supply_battery_info *info);
extern int power_supply_ocv2cap_simple(struct power_supply_battery_ocv_table *table,
				       int table_len, int ocv);
extern struct power_supply_battery_ocv_table *
power_supply_find_ocv2cap_table(struct power_supply_battery_info *info,
				int temp, int *table_len);
extern int power_supply_batinfo_ocv2cap(struct power_supply_battery_info *info,
					int ocv, int temp);
extern int
power_supply_temp2resist_simple(struct power_supply_resistance_temp_table *table,
				int table_len, int temp);
extern void power_supply_changed(struct power_supply *psy);
extern int power_supply_am_i_supplied(struct power_supply *psy);
extern int power_supply_set_input_current_limit_from_supplier(
					 struct power_supply *psy);
extern int power_supply_set_battery_charged(struct power_supply *psy);

#ifdef CONFIG_POWER_SUPPLY
extern int power_supply_is_system_supplied(void);
#else
static inline int power_supply_is_system_supplied(void) { return -ENOSYS; }
#endif

extern int power_supply_get_property(struct power_supply *psy,
			    enum power_supply_property psp,
			    union power_supply_propval *val);
#if IS_ENABLED(CONFIG_POWER_SUPPLY)
extern int power_supply_set_property(struct power_supply *psy,
			    enum power_supply_property psp,
			    const union power_supply_propval *val);
#else
static inline int power_supply_set_property(struct power_supply *psy,
			    enum power_supply_property psp,
			    const union power_supply_propval *val)
{ return 0; }
#endif
extern int power_supply_property_is_writeable(struct power_supply *psy,
					enum power_supply_property psp);
extern void power_supply_external_power_changed(struct power_supply *psy);

extern struct power_supply *__must_check
power_supply_register(struct device *parent,
				 const struct power_supply_desc *desc,
				 const struct power_supply_config *cfg);
extern struct power_supply *__must_check
power_supply_register_no_ws(struct device *parent,
				 const struct power_supply_desc *desc,
				 const struct power_supply_config *cfg);
extern struct power_supply *__must_check
devm_power_supply_register(struct device *parent,
				 const struct power_supply_desc *desc,
				 const struct power_supply_config *cfg);
extern struct power_supply *__must_check
devm_power_supply_register_no_ws(struct device *parent,
				 const struct power_supply_desc *desc,
				 const struct power_supply_config *cfg);
extern void power_supply_unregister(struct power_supply *psy);
extern int power_supply_powers(struct power_supply *psy, struct device *dev);

#define to_power_supply(device) container_of(device, struct power_supply, dev)

extern void *power_supply_get_drvdata(struct power_supply *psy);
/* For APM emulation, think legacy userspace. */
extern struct class *power_supply_class;

static inline bool power_supply_is_amp_property(enum power_supply_property psp)
{
	switch (psp) {
	case POWER_SUPPLY_PROP_CHARGE_FULL_DESIGN:
	case POWER_SUPPLY_PROP_CHARGE_EMPTY_DESIGN:
	case POWER_SUPPLY_PROP_CHARGE_FULL:
	case POWER_SUPPLY_PROP_CHARGE_EMPTY:
	case POWER_SUPPLY_PROP_CHARGE_NOW:
	case POWER_SUPPLY_PROP_CHARGE_AVG:
	case POWER_SUPPLY_PROP_CHARGE_COUNTER:
	case POWER_SUPPLY_PROP_PRECHARGE_CURRENT:
	case POWER_SUPPLY_PROP_CHARGE_TERM_CURRENT:
	case POWER_SUPPLY_PROP_CONSTANT_CHARGE_CURRENT:
	case POWER_SUPPLY_PROP_CONSTANT_CHARGE_CURRENT_MAX:
	case POWER_SUPPLY_PROP_CURRENT_MAX:
	case POWER_SUPPLY_PROP_CURRENT_NOW:
	case POWER_SUPPLY_PROP_CURRENT_AVG:
	case POWER_SUPPLY_PROP_CURRENT_BOOT:
		return true;
	default:
		break;
	}

	return false;
}

static inline bool power_supply_is_watt_property(enum power_supply_property psp)
{
	switch (psp) {
	case POWER_SUPPLY_PROP_ENERGY_FULL_DESIGN:
	case POWER_SUPPLY_PROP_ENERGY_EMPTY_DESIGN:
	case POWER_SUPPLY_PROP_ENERGY_FULL:
	case POWER_SUPPLY_PROP_ENERGY_EMPTY:
	case POWER_SUPPLY_PROP_ENERGY_NOW:
	case POWER_SUPPLY_PROP_ENERGY_AVG:
	case POWER_SUPPLY_PROP_VOLTAGE_MAX:
	case POWER_SUPPLY_PROP_VOLTAGE_MIN:
	case POWER_SUPPLY_PROP_VOLTAGE_MAX_DESIGN:
	case POWER_SUPPLY_PROP_VOLTAGE_MIN_DESIGN:
	case POWER_SUPPLY_PROP_VOLTAGE_NOW:
	case POWER_SUPPLY_PROP_VOLTAGE_AVG:
	case POWER_SUPPLY_PROP_VOLTAGE_OCV:
	case POWER_SUPPLY_PROP_VOLTAGE_BOOT:
	case POWER_SUPPLY_PROP_CONSTANT_CHARGE_VOLTAGE:
	case POWER_SUPPLY_PROP_CONSTANT_CHARGE_VOLTAGE_MAX:
	case POWER_SUPPLY_PROP_POWER_NOW:
		return true;
	default:
		break;
	}

	return false;
}

#ifdef CONFIG_POWER_SUPPLY_HWMON
int power_supply_add_hwmon_sysfs(struct power_supply *psy);
void power_supply_remove_hwmon_sysfs(struct power_supply *psy);
#else
static inline int power_supply_add_hwmon_sysfs(struct power_supply *psy)
{
	return 0;
}

static inline
void power_supply_remove_hwmon_sysfs(struct power_supply *psy) {}
#endif

#endif /* __LINUX_POWER_SUPPLY_H__ */



/*
 * For systems where the charger determines the maximum battery capacity
 * the min and max fields should be used to present these values to user
 * space. Unused/unknown fields will not appear in sysfs.
 */