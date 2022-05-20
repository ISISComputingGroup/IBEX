Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7022](https://github.com/ISISComputingGroup/IBEX/issues/7022) | Minor| Passing `prepost=False` to begin, pause commands etc will now skip ioc/server pre/post commands. However client side pre/post command will now need to be modified to accept a prepost argument so they can decide what to do|

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| SANS2D | [#7047](https://github.com/ISISComputingGroup/IBEX/issues/7047) | Patch | Fix vacuum status in SANS2D front end screen |
| WISH | [#7116](https://github.com/ISISComputingGroup/IBEX/issues/7116) | Patch | Fix issue with galil initialisation of a moving motor on IOC startup, affected oscillating collimator |
| TOSCA | [#6101](https://github.com/ISISComputingGroup/IBEX/issues/6101) | Patch | TOSCA sample positioner OPI improvements |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#4371](https://github.com/ISISComputingGroup/IBEX/issues/4371)|Rotating Stirrer Rack|IOC and OPI added to control Rotating Stirrer Rack|
|[#5154](https://github.com/ISISComputingGroup/IBEX/issues/5154)|DG645|Created IOC, tests, emulator and modular OPI|
|[#6440](https://github.com/ISISComputingGroup/IBEX/issues/6440),[#7096](https://github.com/ISISComputingGroup/IBEX/issues/7096)|CCD100|Add support for CCD100 mk3|
|[#7146](https://github.com/ISISComputingGroup/IBEX/issues/7146)|WEBCAM|Visualise webcams diretly in IBEX using EPICS areaDetector rather than web browser|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6975](https://github.com/ISISComputingGroup/IBEX/issues/6975) | Minor | GALIL | Add smoothing option for noisy analogue feedback encoders  |
| [#6997](https://github.com/ISISComputingGroup/IBEX/issues/6997) | Minor | TC/Beckhoff | Fixed axes alias loading in the TwinCAT IOC |
| [#7019](https://github.com/ISISComputingGroup/IBEX/issues/7019) | Minor | ORC | Fixed ORC program name - was previously invalid 
| [#6989](https://github.com/ISISComputingGroup/IBEX/issues/6989) | Minor | MCLennan    | Fixed homing failing due to potential poll at wrong time. |
| [#7026](https://github.com/ISISComputingGroup/IBEX/issues/7026) | Minor | Eurotherm    | Extend number of available channels to 10 |
| [#7111](https://github.com/ISISComputingGroup/IBEX/issues/7111) | Patch | TekAFG    | Fix connection leak when device gets into partially working state |
| [#7161](https://github.com/ISISComputingGroup/IBEX/issues/7116) | Patch | TOSCA sample positioner | Only show positioning box in sample changer device screen if in manager mode |

### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#6950](https://github.com/ISISComputingGroup/IBEX/issues/6950) | Minor | Reflectometry Server picks up when the velocity of a stationary axis has been changed at the motor level, and uses this value as the new velocity to restore after moves. |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7075](https://github.com/ISISComputingGroup/IBEX/issues/7075) | Minor | Remove separate plot window from Reflectometry perspective, now opens as a tab on the right.  |
| [#7024](https://github.com/ISISComputingGroup/IBEX/issues/7024) | Minor | Made unapplied changes to Experiment Setup more obvious (larger button and added indicator on DAE front panel)  |
| [#5238](https://github.com/ISISComputingGroup/IBEX/issues/5238) | Minor | There are now settings to enable and disable perspectives  |
| [#7134](https://github.com/ISISComputingGroup/IBEX/issues/7134) | Minor | Reflectometry OPI was removed in favor of reflectometry perspective  |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6853](https://github.com/ISISComputingGroup/IBEX/issues/6853) | Minor | Created Squish tests for right-click menu from Beam Status |
| [#6307](https://github.com/ISISComputingGroup/IBEX/issues/6307) | Patch | Added way of assigning a block to a group on creation |
| [#7012](https://github.com/ISISComputingGroup/IBEX/issues/7012) | Patch | Removed unrequired functionality from WISH jaws OPI, added controls for 6th set, tidied layout |
| [#1396](https://github.com/ISISComputingGroup/ibex_gui/pull/1396) | Minor  | Groups in blocks menu can now be collapsed, stack vertically and can be sorted to occupy less space in the blocks panel |
| [#7062](https://github.com/ISISComputingGroup/IBEX/issues/7062) | Patch | Added hexed error ID, sensible default for axis num spinner, axis num indicator, etc into Beckhoff engineering view |
| [#6574](https://github.com/ISISComputingGroup/IBEX/issues/6574) | Minor | Added a button to remake PV connections in the IBEX client |
| [#3597](https://github.com/ISISComputingGroup/IBEX/issues/3597) | Patch  | Redesigned icon for Disc Chopper |
| [#7083](https://github.com/ISISComputingGroup/IBEX/issues/7083) | Minor | Retry upload on blockserver XML to avoid occasional issues seen in cycle |
| [#7023](https://github.com/ISISComputingGroup/IBEX/issues/7023) | Minor | Synoptic displays error dialog when PV cannot be written to |
| [#7013](https://github.com/ISISComputingGroup/IBEX/issues/7013) | Minor | Replaced lists of IOCs with trees of IOCs that can be collapsed to hide multipe IOCs of the same type |
| [#7123](https://github.com/ISISComputingGroup/IBEX/issues/7123) | Patch | When jaws moved wide open, move to limit +-1 depending on direction to avoid move being rejected |
| [#7125](https://github.com/ISISComputingGroup/IBEX/issues/7125) | Minor | Remove old BKHOFF IOC (no longer used on IMAT) |
| [#7092](https://github.com/ISISComputingGroup/IBEX/issues/7092) | Minor | Remove EDNEXT IOC reference |
| [#6991](https://github.com/ISISComputingGroup/IBEX/issues/6991) | Patch | Fix missing a failed client install in some circumstances |
| [#7143](https://github.com/ISISComputingGroup/IBEX/issues/7143) | Minor | Add asynInterposeThrottleConfig() to allow rate limiting writes to a device |
| [#7137](https://github.com/ISISComputingGroup/IBEX/issues/7137) | Patch | Start/Stop IOCs button is now greyed out if server is down |



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
| [#7045](https://github.com/ISISComputingGroup/IBEX/issues/7045) | Minor | Fix tolerance setting in motionsetpoints | 
| [#5078](https://github.com/ISISComputingGroup/IBEX/issues/5078) | Minor | Make output from IBEX start/stop server scripts more concise |
| [#7086](https://github.com/ISISComputingGroup/IBEX/issues/7086) | Minor | Improved time performance of starting IOCs | 

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
