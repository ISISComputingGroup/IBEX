Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#6032](https://github.com/ISISComputingGroup/IBEX/issues/6032) | Major | Updated ORC code to cater for WISH collimator - Note this may effect the behaviour of the LET/MERLIN collimators as they share some code. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6754](https://github.com/ISISComputingGroup/IBEX/issues/6754) | Minor | Beckhoff| The Beckhoff IOC will now automatically pick up how many axes are on the controller. |

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


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#6776](https://github.com/ISISComputingGroup/IBEX/issues/6776) | Patch | Beckhoff uses direction from PLC rather than calculating based on last position |
|[#6751](https://github.com/ISISComputingGroup/IBEX/issues/6751) | Minor | Merge the automation tools used for the Beckhoff test runner |
|[#6804](https://github.com/ISISComputingGroup/IBEX/issues/6804) | Minor | Refactored ILM200 IOC to follow new IOC testing format and to test non-ISOBUS functionality |

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
PyDev | 8.3.0 | Modified fork of PyDev is now used. Same base version is used as before (8.3.0)

### genie_python Dependencies
