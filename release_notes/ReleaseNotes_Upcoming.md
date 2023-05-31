Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7515](https://github.com/ISISComputingGroup/IBEX/issues/7515) | Minor | Can now copy a component from one instrument to another. |
| [#7446](https://github.com/ISISComputingGroup/IBEX/issues/7446) | Minor | Motors (all) - Updated motor driver to R7-3 | 

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| OFFSPEC | [#7328](https://github.com/ISISComputingGroup/IBEX/issues/7328) | Minor | Added OPIs for the Reflectometry front panel. |
| ENGIN-X | [#7383](https://github.com/ISISComputingGroup/IBEX/issues/7383) | Patch | Allow `ARINST` and `ARACCESS` to run under a mini-instrument setup, to allow logging to work with new instron stress rig controller. |
| MuSR | [#6404](https://github.com/ISISComputingGroup/IBEX/issues/6404) | Minor | Add additional information and tolerance checks to a new MuSR-specific CAEN OPI. |
| RIKEN | [#5872](https://github.com/ISISComputingGroup/IBEX/issues/5872) | Minor | Added magnet PSU synoptic opi |
| Muons | - | Minor | Add `BOOSTER_TYPE` PV to `MUONTPAR_01` IOC. |
| POLREF | [#7399](https://github.com/ISISComputingGroup/IBEX/issues/7399) | Minor | Add calibration file for GMW Magnet. |
| RIKEN | [#7241](https://github.com/ISISComputingGroup/IBEX/issues/7241) | Minor | Add configuration files for main PLC. |
| RIKEN | [#7556](https://github.com/ISISComputingGroup/IBEX/issues/7556) | Minor | Add support for RB2 PSU. |
| RIKEN | [#5878](https://github.com/ISISComputingGroup/IBEX/issues/5878) | Minor | Added OPI to show overview of the Vacuum System. |
| LET/MERLIN | [#7625](https://github.com/ISISComputingGroup/IBEX/issues/7625) | Minor | Added more accurate 'moving' indicator for oscillating collimator and added to the OPI. |
| RIKEN | [#7629](https://github.com/ISISComputingGroup/IBEX/issues/7629) | Minor | Improved OPIs - tidied up and made more consistent. |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#2460](https://github.com/ISISComputingGroup/IBEX/issues/2460) | Keithley 2000 | Generic IOC for Keithley 2000 multimeters. |
| [#7543](https://github.com/ISISComputingGroup/IBEX/issues/7543) | Omron PLC | Added support for SANDALS gate valve PLC. |
| [#7468](https://github.com/ISISComputingGroup/IBEX/issues/7468) | Keithley 2290 High Voltage Power Supply | Allows programmable output voltage to 10kV. |
| [#7601](https://github.com/ISISComputingGroup/IBEX/issues/7601) | Basic IOC for the Catalytic Flow Reactor | |
| [#6678](https://github.com/ISISComputingGroup/IBEX/issues/6678) | Razorbill RP100 Strain Cell PSU | Used on WISH |
| [#7663](https://github.com/ISISComputingGroup/IBEX/issues/7663) | Keysight E4980AL LCR meter | Used on WISH |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6931](https://github.com/ISISComputingGroup/IBEX/issues/6931) | Minor | Eurotherm | Now has output rate control capability. |
| [#7405](https://github.com/ISISComputingGroup/IBEX/issues/7405) | Patch | T-Jump cell | Fixed protocol file for the t-jump cell apparatus. |
| [#6891](https://github.com/ISISComputingGroup/IBEX/issues/6891) | Minor | OxInst IPS | Do not wait for heater (if on) between setpoints in non-persistent mode |
| [#7561](https://github.com/ISISComputingGroup/IBEX/issues/7561) | Minor | Superlogics | Added support for Strain Gauge modules. |
| [#7598](https://github.com/ISISComputingGroup/IBEX/issues/7598) | Minor | SANS Sample Changer | Changed rack and position selection to be case insensitive. |
| [#7692](https://github.com/ISISComputingGroup/IBEX/issues/7692) | Minor | IPS | Fix "heater off" state calculation |
| [#7606](https://github.com/ISISComputingGroup/IBEX/issues/7606) | Minor | SKF G5 Chopper | Add method of skipping the MODBUS transaction ID for old firmware versions on SKF chopper controllers which implement it incorrectly |  
| [#7711](https://github.com/ISISComputingGroup/IBEX/issues/7711) | Patch | TC/Beckhoff | Archive Error ID so it can be plotted |
| [#7727](https://github.com/ISISComputingGroup/IBEX/issues/7727) | Patch | McLennan | improve logging and diagnostics |
| [#7658](https://github.com/ISISComputingGroup/IBEX/issues/7658) | Minor | SKF G5 Chopper | Added peak positions PVs. |  


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#7215](https://github.com/ISISComputingGroup/IBEX/issues/7215) | Minor | Fix for wrong velocity being cached in autosave |  

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7610](https://github.com/ISISComputingGroup/IBEX/issues/7610) | Patch | Fix a performance problem in the client when changing DAE settings very quickly (e.g. via a script) |



### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5876](https://github.com/ISISComputingGroup/IBEX/issues/5876) | Minor | Add an OPI for RIKEN Kicker and Separator HV settings |
| [#7592](https://github.com/ISISComputingGroup/IBEX/issues/7592) | System | Fix Strange permissions on files created by conserver and procServ. |
| [#7461](https://github.com/ISISComputingGroup/IBEX/issues/7461) | Minor | Zoom selection box and different cursors added for matplotlib plotting |
| [#7542](https://github.com/ISISComputingGroup/IBEX/issues/7542) | Minor | Added current error and open engineering view button to motor details for the Galil and Beckhoff motor controllers. |
| [#7636](https://github.com/ISISComputingGroup/IBEX/issues/7636) | Minor | Fix deadlock that could stop spectra graphs updating |
| [#7638](https://github.com/ISISComputingGroup/IBEX/issues/7638) | Patch | Fix spectra plots looking at INSTETC heartbeat rather than ISISDAE |
| [#7599](https://github.com/ISISComputingGroup/IBEX/issues/7599) | Minor | Add help icons in various places linking to the relevant user manual page in browser |
| [#4277](https://github.com/ISISComputingGroup/IBEX/issues/4277) | Minor | Add different icons for single and vertical strip apertures on LOQ |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7590](https://github.com/ISISComputingGroup/IBEX/issues/7590) | Minor | ARACCESS: MySQL connection pool resource leak |
| [#7631](https://github.com/ISISComputingGroup/IBEX/issues/7631) | Minor | Add script to allow genie python to be imported into mantid |
| [#7640](https://github.com/ISISComputingGroup/IBEX/issues/7640) | Minor | Fix `open_plot_window` function. Now takes a list of figures to open, defaults to opening all. |
| [#7686](https://github.com/ISISComputingGroup/IBEX/issues/7686) | Patch | Fix thread leak in use of CA library - mostly affects system tests. However also removed pyepcics in case multiple epics installations was causing an issue. Believe nothing depended on this.  |
| [#7610](https://github.com/ISISComputingGroup/IBEX/issues/7610) | Patch | Hide non-user-facing exceptions from the matplotlib plotting code. |


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7710](https://github.com/ISISComputingGroup/IBEX/issues/7710) | Minor | Improve behaviour of archivers under memory exhaustion and add diagnostics |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7490](https://github.com/ISISComputingGroup/IBEX/issues/7490) | Minor | Add service which can configure moxa allowed IPs by hostname (for moveable equipment/moxas). |
| [#7585](https://github.com/ISISComputingGroup/IBEX/issues/7585) | Patch | Resolve system test failure for blockserver starting/restarting IOCs. |
| [#7583](https://github.com/ISISComputingGroup/IBEX/issues/7583) | Patch | Dependency updates: Python 3.11, Java patch versions, MySQL patch versions. See table below for details. |

# Support Issues Solved

| Ticket | Type  | Change |
| ------ | ------| ------------- |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### Server dependencies

what | version | where | last updated/checked
|---- | ------- | ----- | --------------------|
| MySql | 8.0.32 | ibex_install_utils | 03/2023
| Make | 4.4 | utils_win32 | 03/2023 |
| Cygwin | 3.4.6 | ICP_Binaries | 03/2023 |
| Nicos | 23 | ScriptServer | 03/2023 |
|ActiveMQ|5.17.3| ISIS/ActiveMQ |03/2023|
|Joda-time|2.12.2| IOCLogServer |03/2023|
|Apache log4j|2.19.0| IOCLogServer |03/2023|
|Mockito|5.11| IOCLogServer |03/2023|
|MySql-connector J|8.0.32| IOCLogServer |03/2023|

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
|Gson|2.10.1|03/2023|
|efxclipse|3.9.0|03/2023|
|Nebula Visualsation Widgets|2.7.2|03/2023|
|Eclipse Releases|2023|03/2023|
|Eclipse RCP|4.26|03/2023|
|Eclipse Link Target Component|2.7.11|03/2023|
|Joda-time|2.12.2|03/2023|
|MySql-connector J|8.0.32|03/2023|
|Apache log4j|2.19.0|03/2023|
|ActiveMQ|5.17.3|03/2023|
|Tyrus|2.1.2|03/2023|
|Mockito|5.11|03/2023|
|JeroMQ|5.1.1|03/2023|
|Java Development Kit|17.0.6_10|03/2023|
|Orbit|R20221123021534|03/2023|
|PyDev|10.1.3|03/2023|
|Maven|3.9.0|03/2023|
|Control System Studio|03/2023|03/2023|
|Nicos|23|03/2023|

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
|Python|3.11.2|03/2023|
|ode|0.16.3|03/2023|
|Matplotlib|3.7.1|03/2023|
|Lewis|03/2023|03/2023|
