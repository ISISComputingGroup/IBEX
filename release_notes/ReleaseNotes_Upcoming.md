Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#6032](https://github.com/ISISComputingGroup/IBEX/issues/6032) | Major | Updated ORC code to cater for WISH collimator - Note this may effect the behaviour of the LET/MERLIN collimators as they share some code. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| [#6632](https://github.com/ISISComputingGroup/IBEX/issues/6632) | Minor | Tweaked configuration on IMAT so that axes names are consistent between OPI and Synoptic view|
| [#6785](https://github.com/ISISComputingGroup/IBEX/issues/6785) | Minor | Use delayed moves for tank collision avoidance|

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#6040](https://github.com/ISISComputingGroup/IBEX/issues/6040)|PEARLPC|Created IOC, tests, emulator and OPI for the PEARL pressure controller|
|[#5952](https://github.com/ISISComputingGroup/IBEX/issues/5952)|DFKPS|Correct bug where autoonoff was always a step behind|
|[#6889](https://github.com/ISISComputingGroup/IBEX/issues/6889)|KEPCO|Remove immediate updates because they interfere with retrieval, tighter scan loop and remove non-required scan|
|[#6030](https://github.com/ISISComputingGroup/IBEX/issues/6030)|WISH: Keithley6517B|Created IOC, tests, emulator and OPI for Keithley6517B Electrometer|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#4815](https://github.com/ISISComputingGroup/IBEX/issues/4815) | Minor | Mclennan | Set creep sped to HVEL when sending an internal home |
| [#6754](https://github.com/ISISComputingGroup/IBEX/issues/6754) | Minor | Beckhoff| The Beckhoff IOC will now automatically pick up how many axes are on the controller. |
| [#6797](https://github.com/ISISComputingGroup/IBEX/issues/6797) | Minor | ZFCNTRL | The ZFCNTRL ioc write tolerance default has been changed from 0.0002 to 0.0012 to support a kepco running in the higher current range. |
| [#6797](https://github.com/ISISComputingGroup/IBEX/issues/6797) | Minor | KEPCO | Added the ability to set and get current ranges. |
| [#6027](https://github.com/ISISComputingGroup/IBEX/issues/6027) | Patch | LKSH336 | Made it clearer that the 336 IOC can be used to control the 350 model. |
| [#6748](https://github.com/ISISComputingGroup/IBEX/issues/6748) | Patch | SANS Sample Changer | Now logs less to avoid filling up disks. |
| [#4817](https://github.com/ISISComputingGroup/IBEX/issues/4187) | Minor | HVCAENA | Add model, number of channels, serial number and firmware release to board parameters. |
| [#6624](https://github.com/ISISComputingGroup/IBEX/issues/6624) | Minor | DFKPS | Expose Danfysik Baud Rate as IOC Macro. |


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6627](https://github.com/ISISComputingGroup/IBEX/issues/6627) | Minor | There is now confirmation required before deleting confiruration or component |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |
| [#6483](https://github.com/ISISComputingGroup/IBEX/issues/6483) | Minor | Added expected finish time to script generator beneath total expected time. |
| [#6847](https://github.com/ISISComputingGroup/IBEX/issues/6847) | Minor | Add script definitions location to about dialog box |
| [#6690](https://github.com/ISISComputingGroup/IBEX/issues/6690) | Patch | Fix the Script Generator stuck at reloading page bug |
| [#6841](https://github.com/ISISComputingGroup/IBEX/issues/6841) | Minor | Add the ability to play, pause and stop execution of actions in the script generator. |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6586](https://github.com/ISISComputingGroup/IBEX/issues/6586) | Minor | Make it clearer that period 0 is the current period in the spectra plots |
| [#6831](https://github.com/ISISComputingGroup/IBEX/issues/6831) | Patch | Using built-in Java function rather than our own Converter class  |
| [#4957](https://github.com/ISISComputingGroup/IBEX/issues/4957) | Minor | Allow viewing of remote synoptic's structure |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6907](https://github.com/ISISComputingGroup/IBEX/issues/6907) | Minor | Correct rolling over of logs. |


# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6428](https://github.com/ISISComputingGroup/IBEX/issues/6428) | Minor| Replace all references to "waveguides" in relation to SANS2D within internal code with "guides"|
| [#858](https://github.com/ISISComputingGroup/IBEX/issues/858) | Minor | Added validation for duplicate PVs on synoptic components |
| [#3243](https://github.com/ISISComputingGroup/IBEX/issues/3243) | Minor | Web Dashboard: flag an error if instrument time and webserver time are different |
| [#858](https://github.com/ISISComputingGroup/IBEX/issues/858) | Minor | Added validation for duplicate PVs on synoptic components |


# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#6776](https://github.com/ISISComputingGroup/IBEX/issues/6776) | Patch | Beckhoff uses direction from PLC rather than calculating based on last position |
|[#6751](https://github.com/ISISComputingGroup/IBEX/issues/6751) | Minor | Merge the automation tools used for the Beckhoff test runner |
|[#6804](https://github.com/ISISComputingGroup/IBEX/issues/6804) | Minor | Refactored ILM200 IOC to follow new IOC testing format and to test non-ISOBUS functionality |
|[#4688](https://github.com/ISISComputingGroup/IBEX/issues/4688) | Minor | TwinCAT IOC now takes the .tpy file name rather than full path and searches config dir |
|[#6837](https://github.com/ISISComputingGroup/IBEX/issues/6837) | Minor | TwinCAT IOC config dir can now be overridden by using TWINCATCONFIG. Added Axes & motion setpoints load. |
|[#6352](https://github.com/ISISComputingGroup/IBEX/issues/6352) | Minor | ReadASCII made more extendable to variable amount of columns |
|[#6771](https://github.com/ISISComputingGroup/IBEX/issues/6771) | Minor | Experiment Database Populator: Update to latest version |
|[#6755](https://github.com/ISISComputingGroup/IBEX/issues/6755) | Minor | Added NUM_AXES pv to all motor controllers |
|[#6856](https://github.com/ISISComputingGroup/IBEX/issues/6856) | Minor | Set default retries for TWINCAT ioc motors to be 0 |
|[#6894](https://github.com/ISISComputingGroup/IBEX/issues/6894) | Minor | Create python 3.8 virtual environment bash setup script and modify Experiment DB Populator deployment to run inside Python virtual environment |


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
