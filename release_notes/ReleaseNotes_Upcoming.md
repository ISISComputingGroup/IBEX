Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7515](https://github.com/ISISComputingGroup/IBEX/issues/7515) | Minor | Can now copy a component from one instrument to another. |

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


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#2460](https://github.com/ISISComputingGroup/IBEX/issues/2460) | Keithley 2000 | Generic IOC for Keithley 2000 multimeters. |
| [#7543](https://github.com/ISISComputingGroup/IBEX/issues/7543) | Omron PLC | Added support for SANDALS gate valve PLC. |
| [#7468](https://github.com/ISISComputingGroup/IBEX/issues/7468) | Keithley 2290 High Voltage Power Supply | Allows programmable output voltage to 10kV. |

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6931](https://github.com/ISISComputingGroup/IBEX/issues/6931) | Minor | Eurotherm | Now has output rate control capability. |
| [#7405](https://github.com/ISISComputingGroup/IBEX/issues/7405) | Patch | T-Jump cell | Fixed protocol file for the t-jump cell apparatus. |
| [#6891](https://github.com/ISISComputingGroup/IBEX/issues/6891) | Minor | OxInst IPS | Do not wait for heater (if on) between setpoints in non-persistent mode |
| [#7561](https://github.com/ISISComputingGroup/IBEX/issues/7561) | Minor | Superlogics | Added support for Strain Gauge modules. |

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


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5876](https://github.com/ISISComputingGroup/IBEX/issues/5876) | Minor | Add an OPI for RIKEN Kicker and Separator HV settings |
| [#7592](https://github.com/ISISComputingGroup/IBEX/issues/7592) | System | Fix Strange permissions on files created by conserver and procServ. |
| [#7461](https://github.com/ISISComputingGroup/IBEX/issues/7461) | Minor | Zoom selection box and different cursors added for matplotlib plotting |
| [#7542](https://github.com/ISISComputingGroup/IBEX/issues/7542) | Minor | Added current error and open engineering view button to motor details for the Galil and Beckhoff motor controllers. |
| [#7636](https://github.com/ISISComputingGroup/IBEX/issues/7636) | Minor | Fix deadlock that could stop spectra graphs updating |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7490](https://github.com/ISISComputingGroup/IBEX/issues/7490) | Minor | Add service which can configure moxa allowed IPs by hostname (for moveable equipment/moxas). |
| [#7585](https://github.com/ISISComputingGroup/IBEX/issues/7585) | Patch | Resolve system test failure for blockserver starting/restarting IOCs. |

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
