Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#6700](https://github.com/ISISComputingGroup/IBEX/issues/6700) | Major | Removed RKNPS IOC as the daisy-chained danfysiks have now been decommissioned  |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| [#6632](https://github.com/ISISComputingGroup/IBEX/issues/6632) | Minor | Tweaked configuration on IMAT so that axes names are consistent between OPI and Synoptic view|

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#6543](https://github.com/ISISComputingGroup/IBEX/issues/6543)|DANFYSIK9100/DANFYSIK9700|Updated Danfysik OPI and added db file so that the 9100 and 9700 danfysiks are properly handled|
|[#6203](https://github.com/ISISComputingGroup/IBEX/issues/6203)|INTER: Weeder WTDAC-M|Created IOC, tests, emulator and OPI for Weeder WTDAC-M|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6424](https://github.com/ISISComputingGroup/IBEX/issues/6424) | Minor | SANS Sample Changer | XML order of positions will be maintained in OPI, this required some large changes and so retesting is adviced |
| [#6571](https://github.com/ISISComputingGroup/IBEX/issues/6571) | Minor | EUROTHERM | Update database file to include millivolts (mV) units and create new tab in OPI to display millivolts for each sensor when active |
| [#6416](https://github.com/ISISComputingGroup/IBEX/issues/6416) | Minor | DFKPS | Add units to slew rate, rename labels to make more descriptive |
| [#5303](https://github.com/ISISComputingGroup/IBEX/issues/5303) | Minor | LSICORR | Added controls to wait between and before repetitions of taking data. Added controls to throw away data with time lags less than a given minimum. |
| [#6637](https://github.com/ISISComputingGroup/IBEX/issues/6637) | Minor | Twincat | Modified to work with latest version of code on the Beckhoff controllers |
| [#6744](https://github.com/ISISComputingGroup/IBEX/issues/6744) | Minor | HIFIMAGS | Correct issue with statemachine getting stuck in quench state even when not quenching |
| [#4130](https://github.com/ISISComputingGroup/IBEX/issues/4130) | Minor | CAEN HV | Fixed buttons appearing outside of the display |

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
| [#5811](https://github.com/ISISComputingGroup/IBEX/issues/5811) | Minor | Reformulate handling of actions table changes and updates to improve performance. |
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
| [#6696](https://github.com/ISISComputingGroup/IBEX/issues/6696) | Patch | Stopped NICOS window flashing |
| [#6635](https://github.com/ISISComputingGroup/IBEX/issues/6635) | Patch | New icons for Sample Stack in Synoptic and added diagram to OPI. |
| [#6577](https://github.com/ISISComputingGroup/IBEX/issues/6577) | Minor | There is now a warning if the user tries to open multiple IBEX clients. |
| [#6568](https://github.com/ISISComputingGroup/IBEX/issues/6568) | Minor | Added right click menu to beam info |
| [#1154](https://github.com/ISISComputingGroup/IBEX/issues/1154) | Minor | Added warning before killing a console in Scripting perspective |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6666](https://github.com/ISISComputingGroup/IBEX/issues/6666) | Minor | Improve logging: log exceptions + simulation mode. |
| [#6519](https://github.com/ISISComputingGroup/IBEX/issues/6519) | Minor | Added function to get time since start including pauses |
| [#6645](https://github.com/ISISComputingGroup/IBEX/issues/6645) | Minor | Added central logging to Graylog server |


# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6229](https://github.com/ISISComputingGroup/IBEX/issues/6229) | Minor | Added IBEX logo to "About IBEX" box |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#6372](https://github.com/ISISComputingGroup/IBEX/issues/6372) | Minor | Manual tests performed on each release were streamlined |
|[#6576](https://github.com/ISISComputingGroup/IBEX/issues/6576) | Minor | All release branches have been converted into tags (including submodules)|
|[#6751](https://github.com/ISISComputingGroup/IBEX/issues/6751) | Minor | Merge the automation tools used for the Beckhoff test runner |

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
