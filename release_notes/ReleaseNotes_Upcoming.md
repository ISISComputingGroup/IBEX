Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7216](https://github.com/ISISComputingGroup/IBEX/issues/7216) | Minor| Improved DAE spectra display handling to hopefully make disconnected/pink borders less common.|
| [#6947](https://github.com/ISISComputingGroup/IBEX/issues/6947) | Major | A new software pressure control for VTI cryostats has been added for the MercuryiTC. This involves some updates to macro and PV names, which will break old configs. An upgrade script is included.

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| OFFSPEC | [#7328](https://github.com/ISISComputingGroup/IBEX/issues/7328) | Minor | Added OPIs for the Reflectometry front panel. |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6861](https://github.com/ISISComputingGroup/IBEX/issues/6861) | Patch | TC/Beckhoff | Get velocity from ADS rather than setting to 1 by default |
| [#7198](https://github.com/ISISComputingGroup/IBEX/issues/7198) | Patch | TC/Beckhoff | Fix moving/done flip-flop from 1 to 0 inversely. | 
| [#7283](https://github.com/ISISComputingGroup/IBEX/issues/7283) | Major | TC/Beckhoff | Fix setting fields on disabled axis and use motor energised to display/control whether an axis is enabled |
| [#7255](https://github.com/ISISComputingGroup/IBEX/issues/7255) | Minor | TPG300 | Fix previously added switching function and an error when setting units. |
| [#7324](https://github.com/ISISComputingGroup/IBEX/issues/7324) | Minor | TC/Beckhoff | Fix motionsetpoints loading. |
| [#4318](https://github.com/ISISComputingGroup/IBEX/issues/4318) | Minor | JSCO4180 | Added JSCO4180_2 and JSCO4180_3 IOCs. |
| [#7344](https://github.com/ISISComputingGroup/IBEX/issues/7344) | Patch | TC/Beckhoff | Update Tcioc to version 2.3. |
| [#7343](https://github.com/ISISComputingGroup/IBEX/issues/7343) | Patch | Lakeshore336 | Use different command to read channels 3&4 |
| [#7322](https://github.com/ISISComputingGroup/IBEX/issues/7322) | Minor | MecuryiTC | Updated value pattern for pressure, level and temp macros |
| [#7296](https://github.com/ISISComputingGroup/IBEX/issues/7296) | Minor | Instron | Add ability to communicate with new MiniTower stress rig via manufacturer DLL |
| [#7352](https://github.com/ISISComputingGroup/IBEX/issues/7352) | Minor | TEKAFG3XXX | Reduce and make configurable polling rate. |
| [#7277](https://github.com/ISISComputingGroup/IBEX/issues/7277) | Minor  | Huber motor now properly resets its setpoint after homing. |
| [#7366](https://github.com/ISISComputingGroup/IBEX/issues/7366) | Minor | DG645 | Added DG645_2 and DG645_3 IOCs. |
| [#7376](https://github.com/ISISComputingGroup/IBEX/issues/7376) | Minor | Keylkg | Added scan rate controls. |
| [#7397](https://github.com/ISISComputingGroup/IBEX/issues/7397) | Patch | HTS Magnet | Various minor patches. |
| [#7397](https://github.com/ISISComputingGroup/IBEX/issues/6433) | Patch | Multiple | Unit setter uses NPP by default |
| [#4240](https://github.com/ISISComputingGroup/IBEX/issues/4240) | Minor | Eurotherm | Also allow control of Eurotherms via modbus protocol. Default behaviour is unchanged and remains to use the ei-bisynch protocol. | 


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |



### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |
| [#6382](https://github.com/ISISComputingGroup/IBEX/issues/6382) | Minor | Added custom estimates. |
| [#7416](https://github.com/ISISComputingGroup/IBEX/issues/7416) | Patch | Improve startup reliability. |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#4673](https://github.com/ISISComputingGroup/IBEX/issues/4673) | Minor | Added Eurotherm single temperature sensor OPI |
| [#5470](https://github.com/ISISComputingGroup/IBEX/issues/5470) | Minor | Added hide title and users checkbox to experiment details view; Adjusts its wording |
| [#7342](https://github.com/ISISComputingGroup/IBEX/issues/7342) | Patch | Fixed `Stop` button in Galil Engineering View OPI. |
| [#7277](https://github.com/ISISComputingGroup/IBEX/issues/7277) | Minor  | Home button on motor OPI is now disabled when at high limit, this is to make it clear that you cannot forward home while at the high limit. Likewise reverse home is disabled when at lower limit. |
| [#7381](https://github.com/ISISComputingGroup/IBEX/issues/7381) | Minor | Improved detection of multiple client instances. |
| [#7386](https://github.com/ISISComputingGroup/IBEX/issues/7386) | Patch | Fixed null value of local OPI variables causing pink border around spectra plots. |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5470](https://github.com/ISISComputingGroup/IBEX/issues/5470) | Minor | Added command to hide an experiment's title and users |
| [#7373](https://github.com/ISISComputingGroup/IBEX/issues/7373) | Patch | Prevent a deadlock that could occur on Python interpreter shutdown under Python 3.10+ |


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7132](https://github.com/ISISComputingGroup/IBEX/issues/7132) | Minor | Make `do_sans` and `do_trans` instrument scripts for SANS instruments more robust and add tests. |
| [#7132](https://github.com/ISISComputingGroup/IBEX/issues/7132) | Minor | Renamed the following functions to follow Python conventions: `FOMin` -> `frame_overload_mirror_in`, `ShortPolariserin`- > `short_polariser_in`, `LongPolariserin` -> `long_polariser_in`, `BSInOut` -> `beam_stop_in_out`, `homecoarsejaws` -> `home_coarse_jaws`, `homea1` -> `home_a1`, `homes1` -> `home_s1`, `homes2` -> `home_s2`, `movebench` -> `move_bench`, `rotatebench` -> `rotate_bench`, `J1` -> `run_off_julabo_1`, `J2` -> `run_off_julabo_2`, `printsamplepars` -> `print_sample_pars`. |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5764](https://github.com/ISISComputingGroup/IBEX/issues/5764) | Minor | fte not checked if mode is not 2 in splitCharWaveform |



# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7240](https://github.com/ISISComputingGroup/IBEX/issues/7240) | Minor | Schneider PLC IOC: Refactor to make generic |
| [#7332](https://github.com/ISISComputingGroup/IBEX/issues/7332) | Patch | Motion setpoints: add units to offset setpoint |
| [#7266](https://github.com/ISISComputingGroup/IBEX/issues/7266) | Minor | IOC Test Framework: Refactor device disconnection logic |

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
---- | ------- | ----- | --------------------

### GUI Dependencies

Dependency | Version | last updated/checked
---- | ------- | --------------------

### genie_python Dependencies
