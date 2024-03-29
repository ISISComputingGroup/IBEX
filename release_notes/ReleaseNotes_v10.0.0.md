See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

This file lists the changes between 9.0.0 and 10.0.0, if your instrument is on an earlier version of ibex then earlier release notes should also be read for intermediate changes etc. Due to the long shutdown it is likely that all the changes described in 8.0.0, 9.0.0 and 10.0.0 will apply, but check above link

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#6032](https://github.com/ISISComputingGroup/IBEX/issues/6032) | Major | Updated ORC code to cater for WISH collimator - Note this may effect the behaviour of the LET/MERLIN collimators as they share some code. |
| [#4669](https://github.com/ISISComputingGroup/IBEX/issues/4669) | Major | Updated Beckhoff IOC to include TC_0x prefix - this will allow us to run more than one twincat IOC if we need to. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| SANS2D | [#5588](https://github.com/ISISComputingGroup/IBEX/issues/5588)| Patch | Inhibit motion on server side for apertures and guides |
| IMAT   | [#6632](https://github.com/ISISComputingGroup/IBEX/issues/6632) | Minor | Tweaked configuration on IMAT so that axes names are consistent between OPI and Synoptic view|
| SANS2D | [#6785](https://github.com/ISISComputingGroup/IBEX/issues/6785) | Minor | Use delayed moves for tank collision avoidance|
| SANS2D | [#4608](https://github.com/ISISComputingGroup/IBEX/issues/4608) | Minor | Updated DAE live view. Added automatic shutter closing in case of rate overcount|

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#6040](https://github.com/ISISComputingGroup/IBEX/issues/6040)|PEARLPC|Created IOC, tests, emulator and OPI for the PEARL pressure controller|
|[#5952](https://github.com/ISISComputingGroup/IBEX/issues/5952)|DFKPS|Correct bug where autoonoff was always a step behind|
|[#6889](https://github.com/ISISComputingGroup/IBEX/issues/6889)|KEPCO|Remove immediate updates because they interfere with retrieval, tighter scan loop and remove non-required scan|
|[#6030](https://github.com/ISISComputingGroup/IBEX/issues/6030)|WISH: Keithley6517B|Created IOC, tests, emulator and OPI for Keithley6517B Electrometer|
|[#6033](https://github.com/ISISComputingGroup/IBEX/issues/6033)|WISH: Jaws|Created basic OPI implementation of WISH Jaws Manager|
|[#6099](https://github.com/ISISComputingGroup/IBEX/issues/6099)|LET: Additional IOC for new SKF controller for Chopper 1 |

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#4815](https://github.com/ISISComputingGroup/IBEX/issues/4815) | Minor | Mclennan | Set creep sped to HVEL when sending an internal home |
| [#6754](https://github.com/ISISComputingGroup/IBEX/issues/6754) | Minor | Beckhoff| The Beckhoff IOC will now automatically pick up how many axes are on the controller. |
| [#6797](https://github.com/ISISComputingGroup/IBEX/issues/6797) | Minor | ZFCNTRL | The ZFCNTRL ioc write tolerance default has been changed from 0.0002 to 0.0012 to support a kepco running in the higher current range. |
| [#6797](https://github.com/ISISComputingGroup/IBEX/issues/6797) | Minor | KEPCO | Added the ability to set and get current ranges. |
| [#6027](https://github.com/ISISComputingGroup/IBEX/issues/6027) | Patch | LKSH336 | Made it clearer that the 336 IOC can be used to control the 350 model. |
| [#6829](https://github.com/ISISComputingGroup/IBEX/issues/6829) | Patch | ORC | WISH ORC refinements + tests. |
| [#6823](https://github.com/ISISComputingGroup/IBEX/issues/6823) | Minor | Beckhoff | Beckhoff axes now contribute to the any moving flag and are stopped by stop all. |
| [#6748](https://github.com/ISISComputingGroup/IBEX/issues/6748) | Patch | SANS Sample Changer | Now logs less to avoid filling up disks. |
| [#6736](https://github.com/ISISComputingGroup/IBEX/issues/6736) | Patch | SANS Sample Changer | Now gives better error messages to the user. |
| [#4817](https://github.com/ISISComputingGroup/IBEX/issues/4187) | Minor | HVCAENA | Add model, number of channels, serial number and firmware release to board parameters. |
| [#6624](https://github.com/ISISComputingGroup/IBEX/issues/6624) | Minor | DFKPS | Expose Danfysik Baud Rate as IOC Macro. |
| [#6926](https://github.com/ISISComputingGroup/IBEX/issues/6926) | Minor | HVCAEN | Allow crate model to be specified, needed to communicate with newer HV crates |
| [#6827](https://github.com/ISISComputingGroup/IBEX/issues/6827) | Minor | KHLY2700 | Investigate and fix hang after long running time |
| [#6871](https://github.com/ISISComputingGroup/IBEX/issues/6871) | Minor | LSICORR | Refactor LSI Correlator to take steps towards decoupling from [PCASPy](https://pcaspy.readthedocs.io/en/latest/) |
| [#6915](https://github.com/ISISComputingGroup/IBEX/issues/6915) | Minor | Beckhoff | Added BENABLE propagation to the table of motors, added beckhoff engineering view |
| [#6865](https://github.com/ISISComputingGroup/IBEX/issues/6865) | Minor | Beckhoff | Beckhoff IOC now aliases axes to next controller if there are more than 8 |
| [#6874](https://github.com/ISISComputingGroup/IBEX/issues/6874) | Minor | Beckhoff | Sort out delayed ADS records updating in tcioc, such as BMOVING |
| [#6869](https://github.com/ISISComputingGroup/IBEX/issues/6869) | Minor | Triton | Remove T0/T1 workaround previously installed to workaround incorrect triton hardware reporting. This workaround is no longer nedeed and in some cases now causes problems |
| [#4745](https://github.com/ISISComputingGroup/IBEX/issues/4745) | Minor | Galil | Added PV to report if Galil has lost power. |

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
| [#6743](https://github.com/ISISComputingGroup/IBEX/issues/6743) | Minor | Motors can now be stopped directly from the SANS Sample Changer OPI advanced tab |
| [#6099](https://github.com/ISISComputingGroup/IBEX/issues/6099) | Minor | Additional tab on SKF OPI for new SKF controller for LET Chopper 1 |

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
| [6759](https://github.com/ISISComputingGroup/IBEX/issues/6759)| Patch | Created squish tests for adding a block to a config or component from OPI menu |
| [#6844](https://github.com/ISISComputingGroup/IBEX/issues/6844) | Patch| Created tests for checking if script generator does not stuck at reloading after python process is killed |
| [#6879](https://github.com/ISISComputingGroup/IBEX/issues/6879) | Minor| Created a script to convert .curve calibration files to .txt calibration files in IBEX calibration file format |
| [#6919](https://github.com/ISISComputingGroup/IBEX/issues/6919) | Minor| Check SANS2D motor setup |
| [#6924](https://github.com/ISISComputingGroup/IBEX/issues/6924) | Minor| Axis unit setting causing unwanted position resend on startup |
| [#6881](https://github.com/ISISComputingGroup/IBEX/issues/6881) | Minor| Moving simulated motors after setting MRES fails |

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
|[#6913](https://github.com/ISISComputingGroup/IBEX/issues/6913) | Patch | Update Tcioc from upstream - v2.2 |
|[#6901](https://github.com/ISISComputingGroup/IBEX/issues/6901) | Patch | Fix SMDP parser for streamdevice |
|[#6958](https://github.com/ISISComputingGroup/IBEX/issues/6958) | Minor | Update epics gateway |
|[#6937](https://github.com/ISISComputingGroup/IBEX/issues/6937) | Patch | Make MAX_ARRAY_BYTES consisten in GUI |

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
Log4J2 | 2.17.1 | Includes critical security vulnerability fix. |

### genie_python Dependencies
