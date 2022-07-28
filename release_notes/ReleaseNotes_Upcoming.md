Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7022](https://github.com/ISISComputingGroup/IBEX/issues/7022) | Minor| Passing `prepost=False` to begin, pause commands etc will now skip ioc/server pre/post commands. However client side pre/post command will now need to be modified to accept a prepost argument so they can decide what to do|
| [#7135](https://github.com/ISISComputingGroup/IBEX/issues/7135) | Major| The NICOS script server daemon (`NICOSDAEMON`) is no longer started by default, and instead should be added to appropriate configurations or components if it is required - for example, on instruments using the script generator. |
| [#7181](https://github.com/ISISComputingGroup/IBEX/issues/7181) | Minor| There should be no longer be many brief flashes of windows during ibex startup|

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
|[#6440](https://github.com/ISISComputingGroup/IBEX/issues/6440),[#7096](https://github.com/ISISComputingGroup/IBEX/issues/7096)|Add support for CCD100 mk3|
|[#5874](https://github.com/ISISComputingGroup/IBEX/issues/5874), [#7129](https://github.com/ISISComputingGroup/IBEX/issues/7129)|Technix PSU|IOC and OPI for Technix power supply for RIKEN|
|[#6440](https://github.com/ISISComputingGroup/IBEX/issues/6440),[#7096](https://github.com/ISISComputingGroup/IBEX/issues/7096)|CCD100|Add support for CCD100 mk3|
|[#7146](https://github.com/ISISComputingGroup/IBEX/issues/7146)|WEBCAM|Visualise webcams diretly in IBEX using EPICS areaDetector rather than web browser|
|[#6003](https://github.com/ISISComputingGroup/IBEX/issues/6003)|FMR|Add device screen for Ferro Magnetic Resonance equipment|
|[#5790](https://github.com/ISISComputingGroup/IBEX/issues/5790)|Huber Sample Stack|IOC added to control Huber Sample Stack from Motors View|
|[#6850](https://github.com/ISISComputingGroup/IBEX/issues/6850)|Birmingham 17T cryomagnet|IOC created|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6975](https://github.com/ISISComputingGroup/IBEX/issues/6975) | Minor | GALIL | Add smoothing option for noisy analogue feedback encoders  |
| [#6997](https://github.com/ISISComputingGroup/IBEX/issues/6997) | Minor | TC/Beckhoff | Fixed axes alias loading in the TwinCAT IOC |
| [#7019](https://github.com/ISISComputingGroup/IBEX/issues/7019) | Minor | ORC | Fixed ORC program name - was previously invalid |
| [#6989](https://github.com/ISISComputingGroup/IBEX/issues/6989) | Minor | MCLennan    | Fixed homing failing due to potential poll at wrong time. |
| [#7026](https://github.com/ISISComputingGroup/IBEX/issues/7026) | Minor | Eurotherm    | Extend number of available channels to 10 |
| [#5877](https://github.com/ISISComputingGroup/IBEX/issues/5877) | Minor | TPG300 | Added support for setting and reading switching functions |
| [#7111](https://github.com/ISISComputingGroup/IBEX/issues/7111) | Patch | TekAFG    | Fix connection leak when device gets into partially working state |
| [#6774](https://github.com/ISISComputingGroup/IBEX/issues/6774), [#6770](https://github.com/ISISComputingGroup/IBEX/issues/6770), [#6764](https://github.com/ISISComputingGroup/IBEX/issues/6764), [#7193](https://github.com/ISISComputingGroup/IBEX/issues/7193), [#7043](https://github.com/ISISComputingGroup/IBEX/issues/7043) | Minor | Pearl Pressure Controller | Added cell, pump pressure and pressure difference indicators, and pressure threshold controls. |
| [#7168](https://github.com/ISISComputingGroup/IBEX/issues/7168) | Patch | HE3Sorb    | Post-hardware test fixes for the ITC-powered he3 sorb insert  |
| [#7161](https://github.com/ISISComputingGroup/IBEX/issues/7161) | Patch | TOSCA sample positioner | Only show positioning box in sample changer device screen if in manager mode |
| [#6898](https://github.com/ISISComputingGroup/IBEX/issues/6898) | Minor | Danfysik | Now supports up to 35 IOCs |
| [#7025](https://github.com/ISISComputingGroup/IBEX/issues/7025) | Minor | WISH/LET collimator | Fixed maths/logic issues in LET/ORC collimator records causing incorrect swept angle calculations on restart |
| [#7152](https://github.com/ISISComputingGroup/IBEX/issues/7152) | Patch | Eurotherm | Add a warning on the eurotherm OPI if no channels are defined |
| [#7206](https://github.com/ISISComputingGroup/IBEX/issues/7206) | Minor | Mezei Flipper | Allow and enforce user-specified port as part of HOST macro |
| [#5554](https://github.com/ISISComputingGroup/IBEX/issues/5554) | Minor | Rotating Sample Changer | Reduced ambiguity of dropped sample messages |
| [#3019](https://github.com/ISISComputingGroup/IBEX/issues/3019) | Minor | Eurotherm | Remove the RETRYCNT alarm as it was generally ignored |

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
| [#5238](https://github.com/ISISComputingGroup/IBEX/issues/5238) | Major | There are now settings to enable and disable perspectives  |
| [#7134](https://github.com/ISISComputingGroup/IBEX/issues/7134) | Minor | Reflectometry OPI was removed in favor of reflectometry perspective  |
| [#1357](https://github.com/ISISComputingGroup/IBEX/issues/1357) | Patch | Preview blocks from components as they are added to the configuration  |
| [#6309](https://github.com/ISISComputingGroup/IBEX/issues/6309) | Patch | Prevent adding blocks from right click menu if you cannot write to the configuration  |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |
| [#6810](https://github.com/ISISComputingGroup/IBEX/issues/6810) | Minor | Prevent actions from disappearing or being reordered when table header is clicked  |

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
| [#7125](https://github.com/ISISComputingGroup/IBEX/issues/7125) | Major | Remove old BKHOFF IOC (no longer used on IMAT) |
| [#7092](https://github.com/ISISComputingGroup/IBEX/issues/7092) | Major | Remove EDNEXT IOC reference |
| [#6991](https://github.com/ISISComputingGroup/IBEX/issues/6991) | Patch | Fix missing a failed client install in some circumstances |
| [#7143](https://github.com/ISISComputingGroup/IBEX/issues/7143) | Minor | Add asynInterposeThrottleConfig() to allow rate limiting writes to a device |
| [#7137](https://github.com/ISISComputingGroup/IBEX/issues/7137) | Patch | Start/Stop IOCs button is now greyed out if server is down |
| [#7118](https://github.com/ISISComputingGroup/IBEX/issues/7118) | Patch | Motionsetpoints    | Allow duplicate positions |
| [#7163](https://github.com/ISISComputingGroup/IBEX/issues/7163) | Patch | Hide nicos git window, stops it popping up on failed connections |
| [#7059](https://github.com/ISISComputingGroup/IBEX/issues/7059) | Patch | Hide graypy exceptions to avoid showing a huge exception stack to user |
| [#7138](https://github.com/ISISComputingGroup/IBEX/issues/7138) | Patch | Fixed issue of DAE settings not being saved from a script |
| [#7034](https://github.com/ISISComputingGroup/IBEX/issues/7034) | Patch | Make deployment process for genie_python and GUI more robust against old, stale files. This solves an issue seen on some beamlines with `pylint` failing to execute. |
| [#7178](https://github.com/ISISComputingGroup/IBEX/issues/7178) | Patch | Added the ability to install the GUI client only without stand alone python |
| [#7208](https://github.com/ISISComputingGroup/IBEX/issues/7208) | Minor | Added a system test for checking the DAE runs even if INSTETC is unavailable |
| [#7227](https://github.com/ISISComputingGroup/IBEX/issues/7227) | Minor | Removed duplicate external Genie Python installations during upgrades |
| [#7230](https://github.com/ISISComputingGroup/IBEX/issues/7230) | Minor | Removed "add block to a config" (not current config) option on right-click - see https://github.com/ISISComputingGroup/IBEX/issues/7224 |
| [#7236](https://github.com/ISISComputingGroup/IBEX/issues/7236) | Minor | Added the ability to search IOCs when adding to configuration and in Start/Stop IOCs dialog |
| [#7229](https://github.com/ISISComputingGroup/IBEX/issues/7229) | Minor | Use https links in GUI help pages |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7054](https://github.com/ISISComputingGroup/IBEX/issues/7054) | Minor | Added a new silent parameter to waitfor commands that suppresses notifications |

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
| [#7179](https://github.com/ISISComputingGroup/IBEX/issues/7179) | Patch | Stop flashing console window on GUI archve reload | 
| [#7177](https://github.com/ISISComputingGroup/IBEX/issues/7177) | Minor | Added an ignored IOC folder list for building IOC startups
| [#6980](https://github.com/ISISComputingGroup/IBEX/issues/6980) | Patch | Investigated waiting dialogue warnings and listed possible solutions |

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
