# Operating System (object)
The `opsys` *object* represents the operating system of the preceding objects.  An operating system is the software that manages computer hardware, software resources, and provides common services for computer programs.  Some *objects* can have more than one (an array) of operating systems.

<a name="get"></a>
## Getting
To get the operating system of the proceeding object, use the `_opsys()` posit. The return will be a comma separated list of operating system *enumerator* *types*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys();`

For an *object* wil multiple operating systems, use the `index` or `i` posit to determine which operating system you are getting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys()_i(`*`index_integer`*`);`

<a name="set"></a>
## Setting
When adding the operating system as a child of the preceding *object*, by using the posit `_opsys`, the operating system is effectively set.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system}`*`);`

Some *objects* allow for multiple operating systems. To set more than one operating system, multiple `opsys` posit are required. Alternatively an array can be used to set operating systems in one `opsys` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system1}`*`)_opsys(`*`{operating_system2}`*`)_`*`…`*<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys([`*`operating_system_array_moniker`*`]);`

<a name="cast"></a>
## Casting
Casting an operating system is identical syntax to setting an operating system, both one and more than operating systems.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system_to_cast_to}`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys(`*`{operating_system_to_cast_to}`*`)_i(`*`index_integer`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_opsys([`*`operating_system_to_cast_to_array_moniker`*`]);`

<a name="type"></a>
## Typing



<a name="posit"></a>
## Posits

<a name= "object"></a>
## Objects

<a name= "computer"></a>
### Computer
The [`computer`](../../physic/obj/computer.md) (also `pc`) object allows for multiple operating systems, since a computer can be partitioned or use multiple hard drives to duel (multi) boot.

The operating systems provided for the `computer` object are determined from user agent statistics from statcounter GlobalStats using 'Top 6 Desktop OSs from Jan - Dec 2021' (*eliminating 'unknown' and 'other'*)`, as shown:

<div id="desktop-os_combined-ww-monthly-202101-202112" width="100%" height="400" style="width:100%; height: 400px;"></div><sub>Source: <a href="https://gs.statcounter.com/os-market-share/desktop/worldwide/2021">StatCounter Global Stats - OS Market Share</a></sub><script type="text/javascript" src="https://www.statcounter.com/js/fusioncharts.js"></script><script type="text/javascript" src="https://gs.statcounter.com/chart.php?desktop-os_combined-ww-monthly-202101-202112&chartWidth=600"></script>

| `{op_sys}` | description | API |
| --- | --- | --- |
| <a name="win"></a>  `{win}` | Microsoft&reg; Windows&#8482;. | [win](#win) |
| <a name="osx"></a> `{osx}` &nbsp; `{os_x}` | Apple&reg; OS X&#8482;. | [osx](#osx) |
| <a name="linux"></a> `{linux}` | Linux.  | [linux](#linux) |
| <a name="chrom"></a> `{chrome}` &nbsp; `{chrome_os}` | Google&reg; Chrome OS&#8482;. | [chrome](#chrome) |

<a name= "cellphone"></a>
### Cell Phone
The [`cellphone`](../../physic/obj/cellphone.md) object only allows for one operating system. There are seven available operating system for `cellphone` object

The operating systems provided for the `cellphone` object are determined from user agent statistics from statcounter GlobalStats using 'Top 8 Mobile OSs from Jan - Dec 2021' (*eliminating 'unknown' and 'other'*)`, as shown:

<div id="mobile_os_combined-ww-monthly-202101-202112" width="100%" height="400" style="width:100%; height: 400px;"></div><sub>Source: <a href="https://gs.statcounter.com/os-market-share/mobile/worldwide/#monthly-202101-202112-bar">StatCounter Global Stats - OS Market Share</a></sub><script type="text/javascript" src="https://gs.statcounter.com/chart.php?mobile_os_combined-ww-monthly-202101-202112&chartWidth=600"></script>

| `{op_sys}` | description | API |
| --- | --- | --- |
| <a name="android"></a>  `{android}` &nbsp; `{and}` | Google&reg; Android&#8482;. | [android](#android) |
| <a name="ios"></a> `{ios}` &nbsp; `{i_os}` | Apple&reg; iOS&#8482;. | [ios](#ios) |
| <a name="tizen"></a> `{tizen}` &nbsp; `{samsung}` | Samsung&reg; Tizen&#8482;. | [tizen](#tizen) |
| <a name="kaios"></a> `{kaios}` &nbsp; `{kai_os}` | KaiOS&#8482;. | [kaios](#kaios) |
| <a name="asha"></a> `{asha}` &nbsp; `{nokia}` | Nokia&reg; Asha&#8482;. | [asha](#asha) |
| <a name="win"></a>  `{win}` &nbsp; `{win_mobile}` | Microsoft&reg; Windows Mobile&#8482;. | [win](#win_mobile) |
| <a name="linux"></a> `{linux}` | Linux. | [linux](#linux) |

<a name= "tablet"></a>
### Tablet
The [`tablet`](../../physic/obj/tablet.md) object allows for multiple operating systems.

The operating systems provided for the `tablet` object are determined from user agent statistics from statcounter GlobalStats using 'Top 8 Tablet OSs from Jan - Dec 2021' (*eliminating 'other'*)`, as shown:

<div id="tablet-os_combined-ww-monthly-202101-202112" width="100%" height="400" style="width:100%; height: 400px;"></div><sub>Source: <a href="https://gs.statcounter.com/os-market-share/tablet/worldwide/#monthly-202101-202112-bar">StatCounter Global Stats - OS Market Share</a></sub><script type="text/javascript" src="https://www.statcounter.com/js/fusioncharts.js"></script><script type="text/javascript" src="https://gs.statcounter.com/chart.php?tablet-os_combined-ww-monthly-202101-202112&chartWidth=600"></script>

| `{op_sys}` | description | API |
| --- | --- | --- |
| <a name="ios"></a> `{ios}` &nbsp; `{i_os}` | Apple&reg; iOS&#8482;. | [ios](#ios) |
| <a name="android"></a>  `{android}` &nbsp; `{and}` | Google&reg; Android&#8482;. | [android](#android) |
| <a name="win"></a>  `{win}` | Microsoft&reg; Windows&#8482;. | [win](#win) |
| <a name="linux"></a> `{linux}` | Linux.  | [linux](#linux) |

<a name= "robot"></a>
### Robot
The [`robot`](../../physic/obj/robot.md) object only allows for one operating system.  Although 'ROS2' is called an operating system, it is not considered an `opsys` property. However, the operating systems available for a `robot` object are taken from the options available from the lastest distribution of ROS2. There are three available operating systems for the `robot` *object*.

| `{op_sys}` | description | API |
| --- | --- | --- |
| <a name="linux"></a> `{ubuntu}` &nbsp; `{ubuntu_linux}` &nbsp; `{linux}` | Ubuntu&reg; Linux. | [linux](#linux_ubuntu) |
| <a name="osx"></a> `{osx}` &nbsp; `{os_x}` | Apple&reg; OS X&#8482;. | [osx](#osx) |
| <a name="win"></a>  `{win}` | Microsoft&reg; Windows&#8482;. | [win](#win) |


