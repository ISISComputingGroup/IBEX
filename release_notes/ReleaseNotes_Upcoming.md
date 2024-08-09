Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#6049](https://github.com/ISISComputingGroup/IBEX/issues/6049) | PEARL Thermometry Device | Support for 16 channel cDAQ thermocouple device used on PEARL |
| [7951](https://github.com/ISISComputingGroup/IBEX/issues/7951) | Stanford PS300 | Support for all Stanford PS300 Series powersupplies|
| [#8210](https://github.com/ISISComputingGroup/IBEX/issues/8210) | LINDY ISWITCH | IOC for LINDY ISwitch device|
| [#8264](https://github.com/ISISComputingGroup/IBEX/issues/8264) | ISIS Remote Labview Services| Support for talking remotley to Labview VI's using the remote Services. |
| [#6211](https://github.com/ISISComputingGroup/IBEX/issues/6211) | Tektronix DMM4040/4050 Multimeters | OPIs and IOC fixes for Tektronix DMM4040/4050 Multimeters |
| [#8345](https://github.com/ISISComputingGroup/IBEX/issues/8345) | PEARL BFSPGR16SC2 Camera | Support for new pearl camera with smaller ccd |
| [#6214](https://github.com/ISISComputingGroup/IBEX/issues/6214) | Stanford SR400 Photon Counter | Add device to support CHIPIR migration |
| [#6218](https://github.com/ISISComputingGroup/IBEX/issues/6218) | CHIPIR collimator | Support for CHIPIR collimator and jaws |
| [#6029](https://github.com/ISISComputingGroup/IBEX/issues/6029) | WISH SR850 Lock-In Amplifier | Support for Stanford RS SR850 Lock-In Amplifier |
| [#8265](https://github.com/ISISComputingGroup/IBEX/issues/8265) | SXD Tensile stress rig | Add IBEX support |
| [#6210](https://github.com/ISISComputingGroup/IBEX/issues/6210) | Hameg HM8123 | Support for Hameg HM8123 programmable counter |
| [#8130](https://github.com/ISISComputingGroup/IBEX/issues/8130) | ISIS Environment Monitor | Support for new ISIS Environment Monitor device |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8160](https://github.com/ISISComputingGroup/IBEX/issues/8160) | minor | Beckhoff/TwinCAT | Allow 2 instances of the TC IOC, for portable beckhoffs |
| [#8104](https://github.com/ISISComputingGroup/IBEX/issues/8104) | minor | PACE5000 | Various PACE5000 snags - set units to bar, slew mode to lin, display source pressure, fix vent status |
| [#8218](https://github.com/ISISComputingGroup/IBEX/issues/8218) | minor | GALIL |  allow COM in GALILADDR macro |
| [#7677](https://github.com/ISISComputingGroup/IBEX/issues/7677) | minor | Tektronix AFG3XXX | Channel 1 and 2 are configurable in IOC macros, by default both are enabled just like so far. |
| [#8248](https://github.com/ISISComputingGroup/IBEX/issues/8248) | minor | Lakeshore 340 | Lakeshore no longer sets excitiation threshold with potentially invalid values on startup. |
| [#6854](https://github.com/ISISComputingGroup/IBEX/issues/6854) | major | Beckhoff/TwinCAT | Remove old CRISP course jaw tcioc motor record code |
| [#8175](https://github.com/ISISComputingGroup/IBEX/issues/8175) | minor | needlevalve | Add macro to govern wriet mode toggle. |
| [#8262](https://github.com/ISISComputingGroup/IBEX/issues/8262) | minor | Keithley 2400 | Add input fields for compliance voltage and current. |
| [#8284](https://github.com/ISISComputingGroup/IBEX/issues/8284)| minor | McLennan | Add macro to set access group of JVEL, HLM, LLM to allow setting of those fields without restart of IOC |
| [#8322](https://github.com/ISISComputingGroup/IBEX/issues/8322)| minor | HVCAEN | Fix issue with write records not getting created | 
| [#7778](https://github.com/ISISComputingGroup/IBEX/issues/7778)| minor | Muon zerofield, Kepco | performance improvements to fix MUSR zerofiel issues | 
| [#8253](https://github.com/ISISComputingGroup/IBEX/issues/8253)| minor | McLennan | Make paramters last a powercycle. Parameters are now saved on homing of device |
| [#8335](https://github.com/ISISComputingGroup/IBEX/issues/8335)| minor | Beckhoff/TwinCAT | Fix issue with table of motors advanced view with energised icon not working | 
| [#8137](https://github.com/ISISComputingGroup/IBEX/issues/8137) | major | ALDN1000 | The IOC now supports daisy chained devices which means the same IOC can control multiple devices on the same COM port. The PVs now carry extra information which is the number of the pump (1-4). Their IDs can be changed in the IOC config but PVs will always reference then from 1-4. |
| [#8353](https://github.com/ISISComputingGroup/IBEX/issues/8353) | major | Tektronix DMM4040/4050 Multimeters | Remove now-obselete (as of #6211) LVDCOM support modules for Tektronix DMM4040/4050 Multimeters |
| [#8357](https://github.com/ISISComputingGroup/IBEX/issues/8357)| minor | Allow configurable number of crates + cards per IOC |
| [#8341](https://github.com/ISISComputingGroup/IBEX/issues/8341)| minor | Allow setting the alarm severity of underrange pressure channels via IOC macro |
| [#8379](https://github.com/ISISComputingGroup/IBEX/issues/8379)| minor | Allow automatic scanning of nputs, add second IOC |
| [#7618](https://github.com/ISISComputingGroup/IBEX/issues/7618)| minor | Beckhoff/TwinCAT | Fix issue with TC creating huge log files on disconnect | 
| [#8342](https://github.com/ISISComputingGroup/IBEX/issues/8342)| minor | Danfysik PSU | Added Current PV to alarm tree | 
| [#7319](https://github.com/ISISComputingGroup/IBEX/issues/7319)| minor | Beckhoff/TwinCAT | Fix issue with TC overwriting autosave values if beckhoff cannot be reached on startup | 
| [#8461](https://github.com/ISISComputingGroup/IBEX/issues/8461)| major | Stanford Research SR400/PS350 | Remove old LVDCOM (labview) IOCs for the SR400 photon counter and PS350 power supplies | 
| [7755da0](https://github.com/ISISComputingGroup/EPICS/commit/7755da05d596d72b20a55c075464429c191c9aa9)| major | Rotbench | Remove old ROTBENCH IOC | 






### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#4631](https://github.com/ISISComputingGroup/IBEX/issues/4631) | Minor | Prevent tracked moves that will clash against soft limits for motors - warn in error log |
| [#8063](https://github.com/ISISComputingGroup/IBEX/issues/8063) | minor | Add a way to apply an engineering correction to a directparameter (ie. INTER's DET_BENCH_ANGLE) |
| [#8218](https://github.com/ISISComputingGroup/IBEX/issues/8218) | minor | GALIL: allow COM in GALILADDR macro |
| [#8227](https://github.com/ISISComputingGroup/IBEX/issues/8227) | minor | Fix string constants not being displayed properly in the constants tab |
| [#8225](https://github.com/ISISComputingGroup/IBEX/issues/8225) | Minor | Revert #5607 (Set velocity on all axes before moving, which should help with synchronised moves) | 
| [#7533](https://github.com/ISISComputingGroup/IBEX/issues/7533) | Minor | Add FOM in beam to SURF front panel | 


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7642](https://github.com/ISISComputingGroup/IBEX/issues/7642) | Major | Added the abillity to set blocks on config change. |
| [#8346](https://github.com/ISISComputingGroup/IBEX/issues/8346) | Minor | The table of IOCs and table of Blocks displayed when viewing/editing a config now displays which component an IOC or Block is added by. |

### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8185](https://github.com/ISISComputingGroup/IBEX/issues/8185) | Patch | Retain Moxa view display state after refresh |
| [#5880](https://github.com/ISISComputingGroup/IBEX/issues/5880) | Minor | Added OPI for CHRONUS Magnet Status |
| [#8106](https://github.com/ISISComputingGroup/IBEX/issues/8106)| Minor | Created a button builder class to better manage creation of buttons in perspectives | 
| [#7813](https://github.com/ISISComputingGroup/IBEX/issues/7813) | Minor | Standardized some common macros like PORT and BAUD |
| [#8281](https://github.com/ISISComputingGroup/IBEX/issues/8281) | Minor | Warn user  on client close about processes that may still be running |
| [#8299](https://github.com/ISISComputingGroup/IBEX/issues/8299) | Minor | Add option to add a PV name to the clipboard |
| [#8285](https://github.com/ISISComputingGroup/IBEX/issues/8285) | Minor | Show warning on adanced motor view if the user can change a MCLENNAN motor's settings but they won't persists. |
| [#8421](https://github.com/ISISComputingGroup/IBEX/issues/8421) | Minor | Added identifying motor controller to oscillating collimator OPI |
| [#8278](https://github.com/ISISComputingGroup/IBEX/issues/8278) | Patch | Ensure OPIs cannot cause a gradual CPU leakage issue |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8148](https://github.com/ISISComputingGroup/IBEX/issues/8148) | Minor | Update pylint package to 3.1.0 |
| [#8351](https://github.com/ISISComputingGroup/IBEX/issues/8351) | Minor | Add the packages needed for the scans library |
| [#8358](https://github.com/ISISComputingGroup/IBEX/issues/8358) | Minor | Add p4p for use with pva |
| [#8382](https://github.com/ISISComputingGroup/IBEX/issues/8382) | Minor | Fix error message running genie_python.bat caused by ipython update  |
| [#8372](https://github.com/ISISComputingGroup/IBEX/issues/8372) | Patch | Reduce memory use for long-running scripts using matplotlib's interactive mode (`pyplot.ion()`). In particular, this addresses a memory leak in Muon background plots. |
| [no ticket](https://github.com/ISISComputingGroup/genie_python/pull/414) | Patch | Allow passing `use_numpy` to `g.get_pv` to return `numpy` arrays for EPICS waveform data. |
|[#8411](https://github.com/ISISComputingGroup/IBEX/issues/8411) | Minor | Adds support for redefining motor positions via CLI |

extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Bluesky

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8439](https://github.com/ISISComputingGroup/IBEX/issues/8439) | Minor | Initial repository structure & minimal set of functionality |
| [#1](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/1) | Minor | Create CI for Bluesky repositroy |
| [ibex_bluesky_core#2](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/2) | Minor | Define & export a bluesky run engine configured for IBEX |
| [ibex_bluesky_core#6](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/6) | Minor | Add a callback which logs all prodcued documents from BlueSky |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8140](https://github.com/ISISComputingGroup/IBEX/issues/8140) | Minor | Fixed runcontrol causing DAE stuck WAITING after adding a block with "suspend if invalid" enabled | 
| [#8298](https://github.com/ISISComputingGroup/IBEX/issues/8298) | Minor | Add PVAccess to every IOC |
| [#8371](https://github.com/ISISComputingGroup/IBEX/issues/8371) | Minor | gateway: refactor startup to try and avoid possible race condition |
| [#8339](https://github.com/ISISComputingGroup/IBEX/issues/8339) | Patch | ConfiChecker: assert all beckhoff axes have non-zero `.DLY` setting, to ensure fast consecutive moves on virtual axes are reliable |
| [#8309](https://github.com/ISISComputingGroup/IBEX/issues/8309) | Minor | gateway: add PVAccess instrument external gateway |
| [#8360](https://github.com/ISISComputingGroup/IBEX/issues/8360) | Minor | Logs: automatically rotate logs |


# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [8056](https://github.com/ISISComputingGroup/IBEX/issues/8056) | Minor | Created a new Jenkins pipeline to check for uncomitted and commits not pushed on inst EPICS repos |
| [#8289](https://github.com/ISISComputingGroup/IBEX/issues/8289)| Minor | Added ability to close command-line emulators within the test framework. |
| [#8362](https://github.com/ISISComputingGroup/IBEX/issues/8362)| Patch | Conserver Log: start a new logfile each day |
| [#8366](https://github.com/ISISComputingGroup/IBEX/issues/8366)| Major | Create new IBEX device generator python package. |
| [#8389](https://github.com/ISISComputingGroup/IBEX/issues/8389)| Minor | Make restore motor positions script easier to use by making most options optional besides time, also prompt to reset power check for galil |
| [#8378](https://github.com/ISISComputingGroup/IBEX/issues/8378)| Minor | Enforce Compliance with our python standards |


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
| MySQL | 8.0.35 | ibex_install_utils | 11/2023 |
| Make | 4.4 | utils_win32 | 11/2023 |
| ActiveMQ | 5.18.3 | ISIS\ActiveMQ | 12/2023 |
| Nicos | 23 | ScriptServer | 11/2023 |
| Cygwin | 3.4.9 | ICP_Binaries |	12/2023 |
| MySql-connector J | 8.0.33 | IOCLogServer | 12/2023 |

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Gson | 2.10.1 | 11/2023 |
| MySql-connector J | 8.0.33 | 12/2023 |
| commons-codec | 1.16.0 | 12/2023 |
| Maven | 3.9.5 | 11/2023 |
| ActiveMQ (different to server version) | 5.17.6 | 12/2023 |
| Nicos | 23 | 11/2023 |
| Jakarta Activation API | 2.1.2 | 12/2023 |
| Jakarta Mail API | 2.1.1 | 12/2023 |
| Jakarta XML Binding API | 4.0.1 | 12/2023 |
| JavaX Activation | 1.1.1 | 12/2023 |
| joda time | 2.12.5 | 12/2023 |
| py4j | 0.10.9.7 | 12/2023 |
| log4j | 2.22.0 | 12/2023 |
| JAXB Runtime | 4.0.4 | 12/2023 |
| Tyrus | 2.1.4 | 12/2023 |
| JacORB OMG API | 3.9 | 12/2023 |
| Mockito Core | 5.7.0 | 12/2023 |
| Mockito Inline | 5.2.0 | 12/2023 |
| JeroMQ | 0.5.4 | 12/2023 |
| Nebula | 3.0.0 | 12/2023 |
| CS-Studio | 12/2023 | 12/2023 |
| Pydev | 11.0.3 | 12/2023 |
| Eclipse | 2024-03 | 04/2024 |
| Eclipse Updates| 4.26 | 12/2023 |

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Python | 3.11.6 | 11/2023 |
| ode |	0.16.4 | 11/2023 |
| Lewis | 11/2023 | 11/2023 |
| matplotlib | 3.8.2 | 12/2023 |
