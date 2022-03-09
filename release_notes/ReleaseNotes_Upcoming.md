Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7022](https://github.com/ISISComputingGroup/IBEX/issues/7022) | Minor| Passing `prepost=False` to begin, pause commands etc will now skip ioc/server pre/post commands. However client side pre/post command will now need to be modified to accept a prepost argument so they can decide what to do|


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#6440](https://github.com/ISISComputingGroup/IBEX/issues/6440)|Add support for CCD100 mk3|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6997](https://github.com/ISISComputingGroup/IBEX/issues/6997) | Minor | TC/Beckhoff | Fixed axes alias loading in the TwinCAT IOC |
| [#7019](https://github.com/ISISComputingGroup/IBEX/issues/7019) | Minor | ORC | Fixed ORC program name - was previously invalid 
| [#6989](https://github.com/ISISComputingGroup/IBEX/issues/6989) | Minor | MCLennan    | Fixed homing failing due to potential poll at wrong time. |
| [#7026](https://github.com/ISISComputingGroup/IBEX/issues/7026) | Minor | Eurotherm    | Extend number of available channels to 10 |

### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#6950](https://github.com/ISISComputingGroup/IBEX/issues/6950) | Minor | Reflectometry Server picks up when the velocity of a stationary axis has been changed at the motor level, and uses this value as the new velocity to restore after moves. |

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
| [#6307](https://github.com/ISISComputingGroup/IBEX/issues/6307) | Patch | Added way of assigning a block to a group on creation |
| [#7012](https://github.com/ISISComputingGroup/IBEX/issues/7012) | Patch | Removed unrequired functionality from WISH jaws OPI, added controls for 6th set, tidied layout |
| [#1396](https://github.com/ISISComputingGroup/ibex_gui/pull/1396) | Minor  | Groups in blocks menu can now be collapsed, stack vertically and can be sorted to occupy less space in the blocks panel |
| [#7062](https://github.com/ISISComputingGroup/IBEX/issues/7062) | Patch | Added hexed error ID, sensible default for axis num spinner, axis num indicator, etc into Beckhoff engineering view |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6694](https://github.com/ISISComputingGroup/IBEX/issues/6694) | Minor| Converted routines file script to Python without Pearl Pressure Controller support|


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |

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
