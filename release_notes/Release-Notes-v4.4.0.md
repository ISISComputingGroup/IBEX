# Changes to make on specific instruments

## LARMOR

(3010) In `configurations/banner.xml`, add a local PV called "Bump strip" pointing at `MOT:BUMP_STOP`. Check this appears in the spangle banner.

## ZOOM

(3010) Copy the files from `motorextensions\master\settings\zoom_bump_strip` into `configurations\galil`

(3010) In `configurations/banner.xml`, add a local PV called "Bump strips" pointing at `MOT:BUMPSTRIP:ANY`. Check this appears in the spangle banner.

## All instruments

## IBEX changes

### Features

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2927](https://github.com/ISISComputingGroup/IBEX/issues/2927) | Minor | Genie_python command to set DAE simulation mode |
| [#3052](https://github.com/ISISComputingGroup/IBEX/issues/3052) | Minor | Add `get_instrument_name` and `get_instrument_py_name` to genie python |
| [#3010](https://github.com/ISISComputingGroup/IBEX/issues/3010) | Minor | Make spangle banner configurable and add bump strip statuses for zoom |

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2992](https://github.com/ISISComputingGroup/IBEX/issues/2992) | Minor | Fix SANDALS SM300 (no flow control). |
| [#2838](https://github.com/ISISComputingGroup/IBEX/issues/2838) | Minor | Individual interlocks for danfysik 8000 |
| [#3003](https://github.com/ISISComputingGroup/IBEX/issues/3003) | Patch | Add IP macro to HVCAEN |
| [#2642](https://github.com/ISISComputingGroup/IBEX/issues/2642) | Minor | Add Gamry. |
| [#2887](https://github.com/ISISComputingGroup/IBEX/issues/2887) | Minor | Display raw readback values in Lakeshore460 |
| [#2983](https://github.com/ISISComputingGroup/IBEX/issues/2983) | Minor | Improve motionsetpoints |
| [#2998](https://github.com/ISISComputingGroup/IBEX/issues/2998) | Minor | Removed flow control for LINMOT, added polling |
| [#3086](https://github.com/ISISComputingGroup/IBEX/issues/3086) | Minor | Gem beamscraper jaw limits are now configurable |
| [#2202](https://github.com/ISISComputingGroup/IBEX/issues/2202) | Minor | Added polling for the mclennan's position |
| [#647](https://github.com/ISISComputingGroup/IBEX/issues/647) | Minor | Keithley 2700 IOC/emulator/OPI/tests |
| [#3105](https://github.com/ISISComputingGroup/IBEX/issues/3105) | Minor | Couette cell IOC |
| [#3074](https://github.com/ISISComputingGroup/IBEX/issues/3074) | Patch | Add aliases for external temperature setpoint on julabo |
| [#3095](https://github.com/ISISComputingGroup/IBEX/issues/3095) | Patch | Allow Beckhoff motor to define an axis and other motor extras. |
| [#3097](https://github.com/ISISComputingGroup/IBEX/issues/3097) | Patch | Add ability to set control mode on Julabo |
| [#3121](https://github.com/ISISComputingGroup/IBEX/issues/3121) | Patch | Add ability to stop and show motion in the Beckhoff axes |
| [#3130](https://github.com/ISISComputingGroup/IBEX/issues/3130) | Minor | Add additional event mode information PVs |
| [#3103](https://github.com/ISISComputingGroup/IBEX/issues/3103) | Patch | Fix memory leak in MK3 Chopper IOC |
| [#3192](https://github.com/ISISComputingGroup/IBEX/issues/3192) | Patch | Fixed a bug where stop commands would not work with McLennan motors |
| [#3077](https://github.com/ISISComputingGroup/IBEX/issues/3077) | Minor | Add homing mode for McLennan motors: constant velocity move and zero, mode 3 |
| [#3139](https://github.com/ISISComputingGroup/IBEX/issues/3139) | Patch | Verified flow control settings on existing IOCs where it is defined (Gamry, Kepco, LinMot, PIMot Schneider, SM300, SMC100) |
| [#3191](https://github.com/ISISComputingGroup/IBEX/issues/3191) | Minor | Beckhoff now autosaves parameters. |
| [#3127](https://github.com/ISISComputingGroup/IBEX/issues/3127) | Minor | Beckhoff now archives values like other motors. |

### UI

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#1306](https://github.com/ISISComputingGroup/IBEX/issues/1306) | Patch | PyDev Console keeps history across sessions |
| [#2922](https://github.com/ISISComputingGroup/IBEX/issues/2922) | Patch | Synoptics with only one component can show beam |
| [#3001](https://github.com/ISISComputingGroup/IBEX/issues/3001) | Minor | Add additional logging on setting specific environment variable to analyse the behaviour of unexpected greyed out buttons |
| [#2730](https://github.com/ISISComputingGroup/IBEX/issues/2730) | Minor | Allow option to either add to existing plot or create a new plot when right clicking a block |
| [#2730](https://github.com/ISISComputingGroup/IBEX/issues/2730) | Minor | Allow plotting multiple PVs |
| [#2878](https://github.com/ISISComputingGroup/IBEX/issues/2878) | Patch | Fix E4 beam status graph |
| [#2882](https://github.com/ISISComputingGroup/IBEX/issues/2882) | Patch | Fix E4 scripting console reporting `CA_ADDR_LIST` as `null` |
| [#3030](https://github.com/ISISComputingGroup/IBEX/issues/3030) | Patch | Changes for new triton software |
| [#3087](https://github.com/ISISComputingGroup/IBEX/issues/3087) | Patch | Update E4 prototype to use Eclipse 4.6 (Oxygen) and CSS 4.5 |
| [#2306](https://github.com/ISISComputingGroup/IBEX/issues/2306) | Patch | Fix synoptic greyed out on startup bug |
| [#2540](https://github.com/ISISComputingGroup/IBEX/issues/2540) | Minor | Allowed NICOS queue to be viewed in UI |
| [#2877](https://github.com/ISISComputingGroup/IBEX/issues/2877) | Minor | E4 - perspective switcher gets current perspective |
| [#3133](https://github.com/ISISComputingGroup/IBEX/issues/3133) | Patch | Improved error message when beginning whilst running. |
| [#2892](https://github.com/ISISComputingGroup/IBEX/issues/2892) | Minor | E4 - Added tooltips to perspective buttons |
| [#2874](https://github.com/ISISComputingGroup/IBEX/issues/2874) | Minor | Right click log plotter from OPIs. |
| [#2875](https://github.com/ISISComputingGroup/IBEX/issues/2875) | Minor | E4 - Fix OPIs |
| [#2884](https://github.com/ISISComputingGroup/IBEX/issues/2884) | Patch | Restore detector diagnostics enabling behaviour in E4 prototype |
| [#1320](https://github.com/ISISComputingGroup/IBEX/issues/1320) | Minor | Added column sorting on most tables in the GUI. |
| [#3100](https://github.com/ISISComputingGroup/IBEX/issues/3100) | Minor | TPG300 and JulaboFP50 OPI graphs update on heartbeat, updated TPG300 layout |
| [#3002](https://github.com/ISISComputingGroup/IBEX/issues/3002) | Minor | The number of crates, slots and channels supported by the HV Caen OPI are now configurable via OPI macros. |

### Interfaces

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Performance

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3129](https://github.com/ISISComputingGroup/IBEX/issues/3129) | Minor | Improve update time for DAE parameters |

### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### IBEX Server

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2916](https://github.com/ISISComputingGroup/IBEX/issues/2916) | Patch | Reduced logging for repeated messages on stream devices |
| [#2750](https://github.com/ISISComputingGroup/IBEX/issues/2750) | Minor | Fix spectra freeze |
| [#3064](https://github.com/ISISComputingGroup/IBEX/issues/3064) | Minor | Allow Galil recsim mode |
| [#3036](https://github.com/ISISComputingGroup/IBEX/issues/3036) | Minor | Use interruptible sleep command in genie_python for nicos |
| [#3138](https://github.com/ISISComputingGroup/IBEX/issues/3138) | Minor | reflect setting low level motor values in higher level |
| [#3157](https://github.com/ISISComputingGroup/IBEX/issues/3157) | Patch | Fix for spectra updating issue |
| [#2916](https://github.com/ISISComputingGroup/IBEX/issues/2916) | Minor | Reduce logging when disconnected |

### Development process

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2939](https://github.com/ISISComputingGroup/IBEX/issues/2939) | Minor | Add a script for installing a release on a new instrument |
| [#2870](https://github.com/ISISComputingGroup/IBEX/issues/2870) | Minor | Add tests for motion set points |
| [#2959](https://github.com/ISISComputingGroup/IBEX/issues/2959) | Minor | Add checking & warning for simulation mode in config and globals |
| [#2942](https://github.com/ISISComputingGroup/IBEX/issues/2942) | Minor | Add a script which detects changes to DB files. |
| [#2386](https://github.com/ISISComputingGroup/IBEX/issues/2386) | Minor | Upgrade Lewis. |
| [#3084](https://github.com/ISISComputingGroup/IBEX/issues/3084) | Minor | Additional COM port diagnostics |
| [#3046](https://github.com/ISISComputingGroup/IBEX/issues/3046) | Minor | New development workflow for genie python. |
| [#3016](https://github.com/ISISComputingGroup/IBEX/issues/3016) | Patch | Created a script to push changes to the calibration files to all instruments |
| [#3081](https://github.com/ISISComputingGroup/IBEX/issues/3081) | Patch | Shared python area: git hook to check committer is not spudulike |
| [#3188](https://github.com/ISISComputingGroup/IBEX/issues/3188) | Patch | Running genie python build deleted newly created site-packages/genie-python files not added to git. |

### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2990](https://github.com/ISISComputingGroup/IBEX/issues/2990) | Minor | Windows control characters in `genie_python` paths no longer prevent DAE tables from loading |
| [#3029](https://github.com/ISISComputingGroup/IBEX/issues/3029) | Minor | Add script for monitoring EPICS archive rates |
| [#2716](https://github.com/ISISComputingGroup/IBEX/issues/2716) | Minor | Ideas for sharing code between instrument scientists |
| [#2678](https://github.com/ISISComputingGroup/IBEX/issues/2678) | Minor | Inform the user that load() may not be the function they were expecting |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

what | version | where | last updated/checked
---- | ------- | ----- | --------------------
MySQL | 5.7.21 | system | 	24-01-2018
Java JRE | 1.8.0 update 161 | system | 	24-01-2018
ActiveMQ | 5.10.0 | EPICS\ISIS\ActiveMQ | out of date
EPICS | 3.15.5 | EPICS\base | ?
genie_python packages | various | genie_python\package_builder\build_python.bat | 9/2017
genie_python_3 packages | various | genie_python\package_builder\build_python_3.bat and requirements.txt | 9/2017
pydev | ? (6.3.1 for E4) | GUI as target | out of date (7/3/2014 for e4)
pydev in E4 | 6.3.1 | GUI as target | 7/3/2014
