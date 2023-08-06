Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7515](https://github.com/ISISComputingGroup/IBEX/issues/7515) | Minor | Can now copy a component from one instrument to another. |
| [#7446](https://github.com/ISISComputingGroup/IBEX/issues/7446) | Minor | Motors (all) - Updated motor driver to R7-3 | 

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
| LET/MERLIN | [#7625](https://github.com/ISISComputingGroup/IBEX/issues/7625) | Minor | Added more accurate 'moving' indicator for oscillating collimator and added to the OPI. |
| RIKEN | [#7629](https://github.com/ISISComputingGroup/IBEX/issues/7629) | Minor | Improved OPIs - tidied up and made more consistent. |
| EMU | [#7880](https://github.com/ISISComputingGroup/IBEX/issues/7880) | Minor | Improved OPIs - Aeroflex Signal Generator - Remove control for modulation type |
| PEARL | [#6045](https://github.com/ISISComputingGroup/IBEX/issues/6045) | Minor | Added OPI for PEARL jaws |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#2460](https://github.com/ISISComputingGroup/IBEX/issues/2460) | Keithley 2000 | Generic IOC for Keithley 2000 multimeters. |
| [#7543](https://github.com/ISISComputingGroup/IBEX/issues/7543) | Omron PLC | Added support for SANDALS gate valve PLC. |
| [#7468](https://github.com/ISISComputingGroup/IBEX/issues/7468) | Keithley 2290 High Voltage Power Supply | Allows programmable output voltage to 10kV. |
| [#7601](https://github.com/ISISComputingGroup/IBEX/issues/7601) | Basic IOC for the Catalytic Flow Reactor | |
| [#6678](https://github.com/ISISComputingGroup/IBEX/issues/6678) | Razorbill RP100 Strain Cell PSU | Used on WISH |
| [#7663](https://github.com/ISISComputingGroup/IBEX/issues/7663) | Keysight E4980AL LCR meter | Used on WISH |
| [#6044](https://github.com/ISISComputingGroup/IBEX/issues/6044) | PACE 5000 Pressure Controller | Used on PEARL |
| [#6041](https://github.com/ISISComputingGroup/IBEX/issues/6041) | MEASM905 Pressure Transducer | Used on PEARL |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6931](https://github.com/ISISComputingGroup/IBEX/issues/6931) | Minor | Eurotherm | Now has output rate control capability. |
| [#7405](https://github.com/ISISComputingGroup/IBEX/issues/7405) | Patch | T-Jump cell | Fixed protocol file for the t-jump cell apparatus. |
| [#6891](https://github.com/ISISComputingGroup/IBEX/issues/6891) | Minor | OxInst IPS | Do not wait for heater (if on) between setpoints in non-persistent mode |
| [#7561](https://github.com/ISISComputingGroup/IBEX/issues/7561) | Minor | Superlogics | Added support for Strain Gauge modules. |
| [#7598](https://github.com/ISISComputingGroup/IBEX/issues/7598) | Minor | SANS Sample Changer | Changed rack and position selection to be case insensitive. |
| [#7692](https://github.com/ISISComputingGroup/IBEX/issues/7692) | Minor | IPS | Fix "heater off" state calculation |
| [#7606](https://github.com/ISISComputingGroup/IBEX/issues/7606) | Minor | SKF G5 Chopper | Add method of skipping the MODBUS transaction ID for old firmware versions on SKF chopper controllers which implement it incorrectly |  
| [#7711](https://github.com/ISISComputingGroup/IBEX/issues/7711) | Patch | TC/Beckhoff | Archive Error ID so it can be plotted |
| [#7646](https://github.com/ISISComputingGroup/IBEX/issues/7646) | Patch | TC/Beckhoff | Revert patch and permanently fix autoparamhandler incompatibility with motion setpoints causing crashes |
| [#7715](https://github.com/ISISComputingGroup/IBEX/issues/7715) | Minor | Muon ZF System | Add check to Setpoint Readback from PSUs  |
| [#7697](https://github.com/ISISComputingGroup/IBEX/issues/7697) | Minor | Eurotherm | Increase replytimeout for EI-BISYNCH protocol for better reliability. |
| [#7727](https://github.com/ISISComputingGroup/IBEX/issues/7727) | Minor | McLennan | improve logging and diagnostics |
| [#7821](https://github.com/ISISComputingGroup/IBEX/issues/7821) | Minor | McLennan | extra home modes and grey out parameters set as macros |
| [#7658](https://github.com/ISISComputingGroup/IBEX/issues/7658) | Minor | SKF G5 Chopper | Added peak positions PVs. |  
| [#7830](https://github.com/ISISComputingGroup/IBEX/issues/7830) | Minor | Keithley2700 | handle overflow in timestamp. |  
| [#7664](https://github.com/ISISComputingGroup/IBEX/issues/7664) | Minor | Various | Reduce repeated error reporing for disconnected devices in some circumstances |
| [#7701](https://github.com/ISISComputingGroup/IBEX/issues/7701) | Minor | ISIS MK3 Disc Chopper | Support for v8.7 DLL |
| [#7716](https://github.com/ISISComputingGroup/IBEX/issues/7716) | Minor | Kepco | Added initial ramp rate macro. |
| [#4390](https://github.com/ISISComputingGroup/IBEX/issues/4390) | Minor | Galil | Added homing routine name field to motor details page and galil engineering view. |
| [#7837](https://github.com/ISISComputingGroup/IBEX/issues/7837) | Minor | McLennan | Protect status update button during McLennan home/jog. |
| [#7904](https://github.com/ISISComputingGroup/IBEX/issues/7904) | Minor | TC/Beckhoff | Use home icon on table of motors page to say if a beckhoff is homed |
| [#7899](https://github.com/ISISComputingGroup/IBEX/issues/7899) | Patch | TC/Beckhoff | Propagate jog velocity from controller to motor record as we do for normal velocity. |
| [#7877](https://github.com/ISISComputingGroup/IBEX/issues/7877) | Minor | Aeroflex | Add Carrier ON/OFF control on the Aeroflex signal generator OPI so that RF excitation can be enabled/disabled remotely. |
| [#7879](https://github.com/ISISComputingGroup/IBEX/issues/7879) | Minor | Aeroflex | Fix units of frequency to be MHz on the Aeroflex signal generator. |
| [#7881](https://github.com/ISISComputingGroup/IBEX/issues/7881) | Minor | Aeroflex | Remove ‘Reset to Factory Settings’ button on the Aeroflex signal generator OPI |
| [#7882](https://github.com/ISISComputingGroup/IBEX/issues/7882) | Minor | Aeroflex | Removed "Set" buttons on Aeroflex OPI; PVs now update when value is entered directly from text field. |
| [#6628](https://github.com/ISISComputingGroup/IBEX/issues/6628) | Patch | TTIEX355P | Fix error when opening device screen without set macro. |
| [#7916](https://github.com/ISISComputingGroup/IBEX/issues/7916) | Minor | Keithley 2700 | Add timestamp till next overflow indicator and reset button to OPI |
| [#7929](https://github.com/ISISComputingGroup/IBEX/issues/7929) | Minor | Aeroflex | Refactoring of system tests and IOC |
| [#7893](https://github.com/ISISComputingGroup/IBEX/issues/7893) | Minor | DG645 |  The value setpoint boxes on the DG645 OPI are now restored on IOC restart. |


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#7215](https://github.com/ISISComputingGroup/IBEX/issues/7215) | Minor | Fix for wrong velocity being cached in autosave |  

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7610](https://github.com/ISISComputingGroup/IBEX/issues/7610) | Patch | Fix a performance problem in the client when changing DAE settings very quickly (e.g. via a script) |



### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |
| [#7843](https://github.com/ISISComputingGroup/IBEX/issues/7843) | Major | Moved several of the script generator buttons into the right-click menu. |
| [#6922](https://github.com/ISISComputingGroup/IBEX/issues/6922) | Minor | Steps in the script generator are now read-only once they are being executed, this is to avoid confusion, as updating them once running would not update the running script. |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5876](https://github.com/ISISComputingGroup/IBEX/issues/5876) | Minor | Add an OPI for RIKEN Kicker and Separator HV settings |
| [#7592](https://github.com/ISISComputingGroup/IBEX/issues/7592) | System | Fix Strange permissions on files created by conserver and procServ. |
| [#7461](https://github.com/ISISComputingGroup/IBEX/issues/7461) | Minor | Zoom selection box and different cursors added for matplotlib plotting |
| [#7542](https://github.com/ISISComputingGroup/IBEX/issues/7542) | Minor | Added current error and open engineering view button to motor details for the Galil and Beckhoff motor controllers. |
| [#7636](https://github.com/ISISComputingGroup/IBEX/issues/7636) | Minor | Fix deadlock that could stop spectra graphs updating |
| [#7638](https://github.com/ISISComputingGroup/IBEX/issues/7638) | Patch | Fix spectra plots looking at INSTETC heartbeat rather than ISISDAE |
| [#7599](https://github.com/ISISComputingGroup/IBEX/issues/7599) | Minor | Add help icons in various places linking to the relevant user manual page in browser |
| [#4277](https://github.com/ISISComputingGroup/IBEX/issues/4277) | Minor | Add different icons for single and vertical strip apertures on LOQ |
| [#7825](https://github.com/ISISComputingGroup/IBEX/issues/7825) | Minor | Updated icons for several devices to new icons or pre-existing ones |
| [#7852](https://github.com/ISISComputingGroup/IBEX/issues/7852) | Minor | Update Beam Status screen to include two new PVs: Decoupled Moderator Beam Limit & Decoupled Moderator Charge Change Time |
| [#7403](https://github.com/ISISComputingGroup/IBEX/issues/7403) | Minor | Make Web Links the default view when opening client |
| [#7895](https://github.com/ISISComputingGroup/IBEX/issues/7895) | Minor | Add PV address to tooltip hover in display blocks. |
| [#7815](https://github.com/ISISComputingGroup/IBEX/issues/7815) | Minor | In the table of motors perspective motors get coloured amber when they are paused and have not done moving. |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7590](https://github.com/ISISComputingGroup/IBEX/issues/7590) | Minor | ARACCESS: MySQL connection pool resource leak |
| [#7631](https://github.com/ISISComputingGroup/IBEX/issues/7631) | Minor | Add script to allow genie python to be imported into mantid |
| [#7640](https://github.com/ISISComputingGroup/IBEX/issues/7640) | Minor | Fix `open_plot_window` function. Now takes a list of figures to open, defaults to opening all. |
| [#7686](https://github.com/ISISComputingGroup/IBEX/issues/7686) | Patch | Fix thread leak in use of CA library - mostly affects system tests. However also removed pyepcics in case multiple epics installations was causing an issue. Believe nothing depended on this.  |
| [#7610](https://github.com/ISISComputingGroup/IBEX/issues/7610) | Patch | Hide non-user-facing exceptions from the matplotlib plotting code. |
| [#7459](https://github.com/ISISComputingGroup/IBEX/issues/7459) | Minor | Get machine details function now looks up machines in INSTLIST PV to connect to right host name. |
| [#7867](https://github.com/ISISComputingGroup/IBEX/issues/7867) | Minor | `load_script` records the name of the script being loaded. |
| [#7865](https://github.com/ISISComputingGroup/IBEX/issues/7865) | Minor | More detail has been added to the error message in change_tables if there is a problem with the file paths |


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7710](https://github.com/ISISComputingGroup/IBEX/issues/7710) | Minor | Improve behaviour of archivers under memory exhaustion and add diagnostics |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7490](https://github.com/ISISComputingGroup/IBEX/issues/7490) | Minor | Add service which can configure moxa allowed IPs by hostname (for moveable equipment/moxas). |
| [#7585](https://github.com/ISISComputingGroup/IBEX/issues/7585) | Patch | Resolve system test failure for blockserver starting/restarting IOCs. |
| [#7583](https://github.com/ISISComputingGroup/IBEX/issues/7583) | Patch | Dependency updates: Python 3.11, Java patch versions, MySQL patch versions. See table below for details. |
| [#7716](https://github.com/ISISComputingGroup/IBEX/issues/7716) | Major | Added initial ramp rate to ReadASCII `ReadASCIIConfigure` function. |
| [#7835](https://github.com/ISISComputingGroup/IBEX/issues/7835) | Minor | Device generator script can now grant permissions to teams for the newly created repository. |

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
|---- | ------- | ----- | --------------------|
| MySql | 8.0.32 | ibex_install_utils | 03/2023
| Make | 4.4 | utils_win32 | 03/2023 |
| Cygwin | 3.4.6 | ICP_Binaries | 03/2023 |
| Nicos | 23 | ScriptServer | 03/2023 |
|ActiveMQ|5.17.3| ISIS/ActiveMQ |03/2023|
|Joda-time|2.12.2| IOCLogServer |03/2023|
|Apache log4j|2.19.0| IOCLogServer |03/2023|
|Mockito|5.11| IOCLogServer |03/2023|
|MySql-connector J|8.0.32| IOCLogServer |03/2023|

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
|Gson|2.10.1|03/2023|
|efxclipse|3.9.0|03/2023|
|Nebula Visualsation Widgets|2.7.2|03/2023|
|Eclipse Releases|2023|03/2023|
|Eclipse RCP|4.26|03/2023|
|Eclipse Link Target Component|2.7.11|03/2023|
|Joda-time|2.12.2|03/2023|
|MySql-connector J|8.0.32|03/2023|
|Apache log4j|2.19.0|03/2023|
|ActiveMQ|5.17.3|03/2023|
|Tyrus|2.1.2|03/2023|
|Mockito|5.11|03/2023|
|JeroMQ|5.1.1|03/2023|
|Java Development Kit|17.0.6_10|03/2023|
|Orbit|R20221123021534|03/2023|
|PyDev|10.1.3|03/2023|
|Maven|3.9.0|03/2023|
|Control System Studio|03/2023|03/2023|
|Nicos|23|03/2023|

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
|Python|3.11.2|03/2023|
|ode|0.16.3|03/2023|
|Matplotlib|3.7.1|03/2023|
|Lewis|03/2023|03/2023|
