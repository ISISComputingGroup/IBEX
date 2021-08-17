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
| [#6416](https://github.com/ISISComputingGroup/IBEX/issues/6416) | Minor | DFKPS | Add units to slew rate, rename labels to make more descriptive |
| [#5303](https://github.com/ISISComputingGroup/IBEX/issues/5303) | Minor | LSICORR | Added controls to wait between and before repetitions of taking data. Added controls to throw away data with time lags less than a given minimum. |


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
| [#6434](https://github.com/ISISComputingGroup/IBEX/issues/6434) | Patch | Renamed "Line" to "Action" in script generator for consistency with buttons |
| [#6402](https://github.com/ISISComputingGroup/IBEX/issues/6402) | Patch | Correct version number for script generator produced by build. |
| [#6478](https://github.com/ISISComputingGroup/IBEX/issues/6478) | Minor | Get script generator version number in standalone UI. |
| [#5616](https://github.com/ISISComputingGroup/IBEX/issues/5616) | Minor | Added abillity to set global parameters on generated scripts. |
| [#4169](https://github.com/ISISComputingGroup/IBEX/issues/4169) | Minor | Queue scripts in the script server directly in the script generator. |
| [#6493](https://github.com/ISISComputingGroup/IBEX/issues/6493) | Minor | Added time & date of last generated script. |
| [#6492](https://github.com/ISISComputingGroup/IBEX/issues/6492) | Minor | Tied together the workflow of generating and loading scripts, removing the confusion of parameters files from the user. |
| [#5967](https://github.com/ISISComputingGroup/IBEX/issues/5967) | Minor | Focus next action on action delete, added key shortcuts for deleting actions and selecting all actions.|
| [#6692](https://github.com/ISISComputingGroup/IBEX/issues/6692) | Patch | Script file is opened in Notepad when Notepad++ is missing. Notepad++ is still recommended. |
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
|[#6576](https://github.com/ISISComputingGroup/IBEX/issues/6576) | Minor | All release branches have been converted into tags (including submodules)|

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
