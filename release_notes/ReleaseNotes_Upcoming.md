Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#6700](https://github.com/ISISComputingGroup/IBEX/issues/6700) | Major | Removed RKNPS IOC as the daisy-chained danfysiks have now been decommissioned  |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#6543](https://github.com/ISISComputingGroup/IBEX/issues/6543)|DANFYSIK9100/DANFYSIK9700|Updated Danfysik OPI and added db file so that the 9100 and 9700 danfysiks are properly handled|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6571](https://github.com/ISISComputingGroup/IBEX/issues/6571) | Minor | EUROTHERM | Update database file to include millivolts (mV) units and create new tab in OPI to display millivolts for each sensor when active |

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
| [#6620](https://github.com/ISISComputingGroup/IBEX/issues/6620) | Patch | Global parameters are now usable in script validation. |
| [#6703](https://github.com/ISISComputingGroup/IBEX/issues/6703) | Minor | Global parameters can now be validated individually. |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6238](https://github.com/ISISComputingGroup/IBEX/issues/6238) | Patch | Ctrl+C before scripting console is open will no longer freeze the GUI. |
| [#5305](https://github.com/ISISComputingGroup/IBEX/issues/5305) | Patch | Fix IOC logs only searching messages by date (and not time). |

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
