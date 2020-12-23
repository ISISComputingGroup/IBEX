# Merged changes

## Instrument Specific Changes
| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| GEM | [#3353](https://github.com/ISISComputingGroup/IBEX/issues/3353) | Patch | GEM sample changer will no longer raise then lower the arm when told to move to the position it is currently in. |
| GEM | [#3017](https://github.com/ISISComputingGroup/IBEX/issues/3017) | Patch | GEM Jaws can be controlled individually with opi. |
| GEM | [#3018](https://github.com/ISISComputingGroup/IBEX/issues/3018) | Minor | Added button to GEM Jaws OPI to copy beam dimensions to beamscraper jaws. |
| HRPD | [#3327](https://github.com/ISISComputingGroup/IBEX/issues/3327) | Minor| HRPD intermediate shutter support. |
| MAPS | [#3212](https://github.com/ISISComputingGroup/IBEX/issues/3212) | Patch | Analogue fermi chopper working on MAPS. |
| MERLIN | [#2988](https://github.com/ISISComputingGroup/IBEX/issues/2988) | Patch | Changes to protect against 600Hz issue in MERLIN chopper controller |
| MERLIN | [#3135](https://github.com/ISISComputingGroup/IBEX/issues/3135) | Patch | Remove confusing options from oscillating collimator |
| MERLIN | [#3264](https://github.com/ISISComputingGroup/IBEX/issues/3264) | Minor | Synchronize setpoint and frequency for MERLIN Fermi chopper. |
| RIKEN-FE | [#3304](https://github.com/ISISComputingGroup/IBEX/issues/3304) | Minor | Added support for RIKEN FE digital I/O device. |
| RIKEN-FE | [#3315](https://github.com/ISISComputingGroup/IBEX/issues/3315) | Patch| Merge the RIKEN FE PLC code into a single IOC |
| ZOOM | [#2936](https://github.com/ISISComputingGroup/IBEX/issues/2936) | Patch | ZOOM: Employ the collision detection system to the baffle and detector trolley axes. |


## All instruments

## IBEX changes

### Features

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2069](https://github.com/ISISComputingGroup/IBEX/issues/2069) | Patch | Format values the same way on the web dashboard as the GUI. |
| [#3381](https://github.com/ISISComputingGroup/IBEX/issues/3381) | Minor | Changes in ISISDAE to support live view. |

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3214](https://github.com/ISISComputingGroup/IBEX/issues/3214) | Patch | Add emulator to TGP300. |
| [#3223](https://github.com/ISISComputingGroup/IBEX/issues/3223) | Patch | Add emulator to Lakeshore 218. | 
| [#3275](https://github.com/ISISComputingGroup/IBEX/issues/3275) | Minor | Added support for SP2XX syringe pump |
| [#2279](https://github.com/ISISComputingGroup/IBEX/issues/2279) | Minor | Read in ISIS calibration files which can contain metadata including units. Allows us to run the eurotherm with sensor calibrated in degrees Celsius. |
| [#3162](https://github.com/ISISComputingGroup/IBEX/issues/3162) | Patch | Made the Beckhoff simulator run on windows. | 
| [#3258](https://github.com/ISISComputingGroup/IBEX/issues/3258) | Minor | Added support for the Keyence TM-3001P Optical Micrometer. | 
| [#3176](https://github.com/ISISComputingGroup/IBEX/issues/3176) | Minor | Add additional configuration options to the Keithley 2400 IOC. |
| [#3343](https://github.com/ISISComputingGroup/IBEX/issues/3343) | Patch | Beckhoff now uses motor record with special resolution, this fixes issues in [#3246] and [#3248] regarding limits and small moves
| [#1922](https://github.com/ISISComputingGroup/IBEX/issues/1922) | Minor| Created an IOC for NGPS power supply unit including IOC, OPI, tests and an emulator. |
| [#3328](https://github.com/ISISComputingGroup/IBEX/issues/3328) | Patch | Fixed some potential issues with calibration. |
| [#2578](https://github.com/ISISComputingGroup/IBEX/issues/2578) | Patch | Make TPG300 alarms configurable. |
| [#3289](https://github.com/ISISComputingGroup/IBEX/issues/3289) | Minor| Expose DAE veto counters as PVs. |
| [#3373](https://github.com/ISISComputingGroup/IBEX/issues/3373) | Minor| Add LUA as IOC scripting language. |
| [#3248](https://github.com/ISISComputingGroup/IBEX/issues/3248) | Patch| Fix SECI2IBEX memory leak. |
| [#3327](https://github.com/ISISComputingGroup/IBEX/issues/3327) | Minor| HRPD intermediate shutter support. |
| [#2947](https://github.com/ISISComputingGroup/IBEX/issues/2947) | Minor| Sync galil motor and encoder values. |
| [#2970](https://github.com/ISISComputingGroup/IBEX/issues/2970) | Minor| Support polling in NetSHrVar. |

###  IBEX Client

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#2872](https://github.com/ISISComputingGroup/IBEX/issues/2872) | Minor | In the E4 prototype, parts can no longer be minimised/maximised and the instrument status and blocks parts can no longer be closed. |
| [#3183](https://github.com/ISISComputingGroup/IBEX/issues/3183) | Patch | Eurotherm sensors 2+ no longer has needless scrollbars. |
| [#3223](https://github.com/ISISComputingGroup/IBEX/issues/3132) | Patch | DAE Run information tab, Period Duration now shows correct value. |
| [#3186](https://github.com/ISISComputingGroup/IBEX/issues/3186) | Patch | Correct sort key in DAE detector diagnostics. |
| [#2698](https://github.com/ISISComputingGroup/IBEX/issues/2698) | Patch | Edit synoptic macros in place. |
| [#3244](https://github.com/ISISComputingGroup/IBEX/issues/3244) | Patch | Changed the URL for the MCR news display. |
| [#3227](https://github.com/ISISComputingGroup/IBEX/issues/3227) | Patch | Make web links perspective use web browser (fixes crash on disconnected network). |
| [#2873](https://github.com/ISISComputingGroup/IBEX/issues/2873) | Minor | E4 - show current config |
| [#3205](https://github.com/ISISComputingGroup/IBEX/issues/3205) | Patch | Removed tick button on synoptic PVs. |
| [#3131](https://github.com/ISISComputingGroup/IBEX/issues/3131) | Patch | Added new event mode display items to the DAE run information tab. |
| [#3280](https://github.com/ISISComputingGroup/IBEX/issues/3280) | Patch | Removed a bunch of eclipse warnings from gui code. |
| [#3213](https://github.com/ISISComputingGroup/IBEX/issues/3213) | Patch | Added half second wait for manager mode PV. |
| [#3204](https://github.com/ISISComputingGroup/IBEX/issues/3204) | Patch | Added a column to the start/stop Control IOCs panel's table to check if an IOC is in the current configuration. |
| [#3236](https://github.com/ISISComputingGroup/IBEX/issues/3236) | Patch | Matched the Slits' gap and position PVs displayed in the block and the synoptic display for the MUON_FE. |
| [#3017](https://github.com/ISISComputingGroup/IBEX/issues/3017) | Patch | GEM Jaws can be controlled individually with opi. |
| [#3156](https://github.com/ISISComputingGroup/IBEX/issues/3156) | Minor | E4: Improved perspective switcher aesthetics. |
| [#3241](https://github.com/ISISComputingGroup/IBEX/issues/3241) | Minor | Added Ctrl+C to interrupt a script in the scripting perspective. |
| [#3203](https://github.com/ISISComputingGroup/IBEX/issues/3203) | Minor | Added option to switch to new config when using "save as" in edit current config. |
| [#3211](https://github.com/ISISComputingGroup/IBEX/issues/3211) | Patch | Added warning when trying to delete synoptic in any configuration. |
| [#2876](https://github.com/ISISComputingGroup/IBEX/issues/2876) | Patch | E4: Scripting perspective launches faster and more cleanly. |
| [#1909](https://github.com/ISISComputingGroup/IBEX/issues/1909) | Patch | Added an OPI for a device to move between one to three set points. |
| [#3063](https://github.com/ISISComputingGroup/IBEX/issues/3063) | Patch | E4: Update to Java 8. |
| [#3292](https://github.com/ISISComputingGroup/IBEX/issues/3292) | Minor | Added LED display to signal problem in interlock water flow for Danfysik 8800 OPI. |
| [#3153](https://github.com/ISISComputingGroup/IBEX/issues/3153) | Minor | E4: Alerts added to perspective switcher. |
| [#3305](https://github.com/ISISComputingGroup/IBEX/issues/3305) | Minor | Trimmed any leading or following white space from the user name and institute name in the experiment team table.|
| [#3303](https://github.com/ISISComputingGroup/IBEX/issues/3303) | Patch| Fixed configuration saving issues. |
| [#3311](https://github.com/ISISComputingGroup/IBEX/issues/3311) | Patch | E4: put PV configuration inside GUI. |
| [#2620](https://github.com/ISISComputingGroup/IBEX/issues/2620) | Minor | Added a warning when creating a block pointing at a setpoint.  |
| [#2835](https://github.com/ISISComputingGroup/IBEX/issues/2835) | Minor | Auto selects first device screens macro. |
| [#3293](https://github.com/ISISComputingGroup/IBEX/issues/3293) | Minor | Added option to copy blocks when editing a configuration. |
| [#3238](https://github.com/ISISComputingGroup/IBEX/issues/3238) | Patch | Fix a GUI issue affecting spectra plots.  |
| [#2583](https://github.com/ISISComputingGroup/IBEX/issues/2583) | Patch | Disallowed opening OPIs from synoptic preview. |
| [#2008](https://github.com/ISISComputingGroup/IBEX/issues/2008) | Patch | Changed motor OPI to new style. |
| [#3294](https://github.com/ISISComputingGroup/IBEX/issues/3294) | Patch | Disabled SPMG buttons on motor OPI and restricted motor details to manager. |
| [#3268](https://github.com/ISISComputingGroup/IBEX/issues/3268) | Minor | Made the CAEN HV channel and slot configurable for all monitors. |
| [#3286](https://github.com/ISISComputingGroup/IBEX/issues/3286) | Patch | E4: keyboard shortcuts to interrupt scripts and change perspectives. |
| [#2883](https://github.com/ISISComputingGroup/IBEX/issues/2883) | Patch | E4: The `synoptic` drop down menu displays default synoptic when opening the configuration editing dialog. |
| [#2544](https://github.com/ISISComputingGroup/IBEX/issues/2544) | Minor | Allow control of NICOS queue. |
| [#3362](https://github.com/ISISComputingGroup/IBEX/issues/3362) | Patch | Added representative icons for Fermi Choppers |
| [#3364](https://github.com/ISISComputingGroup/IBEX/issues/3364) | Patch | Improved appearance of "Instrument Updating" pop-up box |
| [#2834](https://github.com/ISISComputingGroup/IBEX/issues/2834) | Minor | Highlight current line in script server view |
| [#3136](https://github.com/ISISComputingGroup/IBEX/issues/3136) | Patch | E4: Made the plots in the Instron Stress Rig more user friendly. |
| [#2230](https://github.com/ISISComputingGroup/IBEX/issues/2230) | Minor | Added detector live view to the GUI. |
| [#3333](https://github.com/ISISComputingGroup/IBEX/issues/3333) | Patch | E4 - Fixed the HV CAEN OPI. |
| [#3339](https://github.com/ISISComputingGroup/IBEX/issues/3339) | Minor | Use E4 as the main branch of the user interface. Listed as "minor" because there aren't any backwards-incompatible changes. For detailed discussion about what this means, see https://github.com/ISISComputingGroup/ibex_user_manual/wiki/eclipse_4_changes.ppt |
| [#3338](https://github.com/ISISComputingGroup/IBEX/issues/3338) | Patch | Perspectives can be hidden using Eclipse preferences store. |
| [#3395](https://github.com/ISISComputingGroup/IBEX/issues/3395) | Patch | Changed NICOS Scripting perspective name to Script server, and gave it a new icon. |
| [#3058](https://github.com/ISISComputingGroup/IBEX/issues/3058) | Major | Matplotlib windows are now served in the IBEX gui. Scripts that use standard matplotlib plotting commands will be unaffected, but scripts that depend on matplotlib implementation details may no longer work. Additionally, the syntax to add a spectrum to an existing spectrum plot has changed. |
| [#3344](https://github.com/ISISComputingGroup/IBEX/issues/3344) | Patch | The motor details OPI has been changed to the new OPI style. |
| [#3300](https://github.com/ISISComputingGroup/IBEX/issues/3300) | Patch | The SPMG motion control is now controlled via a set of radio buttons in the motor details OPI. |
| [#3295](https://github.com/ISISComputingGroup/IBEX/issues/3295) | Patch | There is a STOP button allowing to stop the motor in the motor details OPI. |
| [#1890](https://github.com/ISISComputingGroup/IBEX/issues/1890) | Patch | The units in the motor details OPI are now easily readable and correct. |
| [#3421](https://github.com/ISISComputingGroup/IBEX/issues/3421) | Patch | Added keyboard shortcut to "Reset Layout" button. |
| [#3401](https://github.com/ISISComputingGroup/IBEX/issues/3401) | Patch | Log plotter no longer asks if you want to save the plot. |
| [#3397](https://github.com/ISISComputingGroup/IBEX/issues/3397) | Patch | Fixed a case where some items in the configuration menu could be greyed out erroneously. |
| [#3418](https://github.com/ISISComputingGroup/IBEX/issues/3418) | Patch | Underline available keyboard shortcuts in configuration -> blocks |
| [#3438](https://github.com/ISISComputingGroup/IBEX/issues/3438) | Patch | No error thrown when duplicating a duplicated block after the original was deleted.|
| [#3391](https://github.com/ISISComputingGroup/IBEX/issues/3391) | Patch | Added ability to save and load scripts from the GUI|
| [#3205](https://github.com/ISISComputingGroup/IBEX/issues/3205) | Patch | Removed the checkbox next to the synoptics writable PV components in the GUI. |
| [#3399](https://github.com/ISISComputingGroup/IBEX/issues/3399) | Patch | Stop all button is permanently enabled when it is writable. |
| [#3326](https://github.com/ISISComputingGroup/IBEX/issues/3326) | Patch | Fixed issue with setting run control limits and tidied up code. |
| [#3319](https://github.com/ISISComputingGroup/IBEX/issues/3319) | Patch | E4: Tell user when layout has changed |
| [#3420](https://github.com/ISISComputingGroup/IBEX/issues/3420) | Patch | Users are now informed when they are disconnected from the server.|
| [#3323](https://github.com/ISISComputingGroup/IBEX/issues/3323) | Patch| Made it more obvious when changes in the DAE have not been applied. |
| [#3143](https://github.com/ISISComputingGroup/IBEX/issues/3143) | Patch | Added option to load one of the last five loaded configurations. |

### Interfaces

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3048](https://github.com/ISISComputingGroup/IBEX/issues/3048) | Patch| DataWeb: Accessing the SECI webpage can now redirect to an IBEX webpage if it is more relevant. |

### Performance

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#1188](https://github.com/ISISComputingGroup/IBEX/issues/1188) | Minor | Redirect error from PV disconnect to genie_python log |
| [#3020](https://github.com/ISISComputingGroup/IBEX/issues/3020) | Patch | Allow float values in waitfor_time() |
| [#3232](https://github.com/ISISComputingGroup/IBEX/issues/3232) | Patch | Add switch TCB tables from python. | 
| [#3098](https://github.com/ISISComputingGroup/IBEX/issues/3098) | Patch | Pass through original exceptions from scripts. |
| [#3033](https://github.com/ISISComputingGroup/IBEX/issues/3033) | Patch | genie_python: Check the current run state before sending run state commands to DAE (e.g. do not allow `g.pause()` if already paused). |
| [#3350](https://github.com/ISISComputingGroup/IBEX/issues/3350) | Patch | Fix keyboard interrupt sometimes being ignored in genie_python |
| [#3217](https://github.com/ISISComputingGroup/IBEX/issues/3217) | Patch | Fixed importing between instrument scripts. |
| [#3443](https://github.com/ISISComputingGroup/IBEX/issues/3443) | Patch| Fixed genie_python `CTRL-C` interrupt when using scipy. |

### IBEX Server

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3089](https://github.com/ISISComputingGroup/IBEX/issues/3089) | Minor | On config change, only restart GWBLOCK if needed |
| [#3137](https://github.com/ISISComputingGroup/IBEX/issues/3137) | Minor | ArchiveEngine now uses archive rate rather than normal monitor rate. |
| [#1315](https://github.com/ISISComputingGroup/IBEX/issues/1315) | Minor | IBEX server will now restart if the computer reboots. |
| [#3272](https://github.com/ISISComputingGroup/IBEX/issues/3272) | Patch | Blockserver rechecks if settings branch is allowed each time  |
| [#3263](https://github.com/ISISComputingGroup/IBEX/issues/3263) | Patch | Eurotherm OPI now displays ramp rate units.|
| [#3194](https://github.com/ISISComputingGroup/IBEX/issues/3194) | Patch | Added machine resources checks to installs and upgrades of IBEX. |


### Development process

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2936](https://github.com/ISISComputingGroup/IBEX/issues/2936) | Patch | ZOOM: Employ the collision detection system to the baffle and detector trolley axes. |
| [#3212](https://github.com/ISISComputingGroup/IBEX/issues/3212) | Patch | Analogue fermi chopper working on MAPS. |
| [#3195](https://github.com/ISISComputingGroup/IBEX/issues/3195) | Patch | Make IOC test framework stop IOCs better and not print CA exceptions.  |
| [#3363](https://github.com/ISISComputingGroup/IBEX/issues/3363) | Minor | Added new argument to IOCTestFramework test runner to call specific tests. |
| [#3321](https://github.com/ISISComputingGroup/IBEX/issues/3321) | Patch | Added LICENCE file to IOC-generator. |


### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3253](https://github.com/ISISComputingGroup/IBEX/issues/3253) | Patch | Log key PV values before and after deployment. |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

what | version | where | last updated/checked
---- | ------- | ----- | --------------------
`MySQL` | 5.7.22 | system | 2018-06-01
`MySQL connector/j` | 5.1.46 | gui databases plugin and EPICS\ISIS\IocLogServer | 2018-06-01
`Java JRE` | 1.8.0 update 171 | system | 	2018-06-01
`ActiveMQ` | 5.15.4 | GUI, server | 2018-06-01
`EPICS` | 3.15.5 | server | 2018-06-01 (latest stable)
`joda-time` | 2.10 | GUI, sever | 2018-06-01
`commons-codec`  | 1.11  | GUI, sever | 2018-06-01
`log4j` | 2.3 | GUI | 2018-06-01
`jeromq` | 0.4.2 | GUI | 2018-06-01 0.4.3 is unreleased
`opal` | 1.0.0 | GUI | see ticket  #3270
`pydev` | ? (6.3.1 for E4) | GUI as target | out of date (7/3/2014 for e4)
`pydev` in E4 | 6.3.1 | GUI as target | 7/3/2014
`target platform` | various | GUI | not updated because getting E4 out
`genie_python` packages | various | genie_python\package_builder\build_python.bat | 9/2017
`genie_python_3` packages | various | genie_python\package_builder\build_python_3.bat and requirements.txt | 9/2017

