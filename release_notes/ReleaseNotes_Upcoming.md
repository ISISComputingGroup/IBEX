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
| [#8210](https://github.com/ISISComputingGroup/IBEX/issues/8210) | LINDY ISWITCH | IOC for LINDY ISwitch device|


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
| [#8284](https://github.com/ISISComputingGroup/IBEX/issues/8284)| minor | McLennan | Add macro to set access group of JVEL, HLM, LLM to allow setting of those fields without restart of IOC |

### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#4631](https://github.com/ISISComputingGroup/IBEX/issues/4631) | Minor | Prevent tracked moves that will clash against soft limits for motors - warn in error log |
| [#8063](https://github.com/ISISComputingGroup/IBEX/issues/8063) | minor | Add a way to apply an engineering correction to a directparameter (ie. INTER's DET_BENCH_ANGLE) |
| [#8218](https://github.com/ISISComputingGroup/IBEX/issues/8218) | minor | GALIL: allow COM in GALILADDR macro |
| [#8227](https://github.com/ISISComputingGroup/IBEX/issues/8227) | minor | Fix string constants not being displayed properly in the constants tab |
| [#8225](https://github.com/ISISComputingGroup/IBEX/issues/8225) | Minor | Revert #5607 (Set velocity on all axes before moving, which should help with synchronised moves) | 


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7642](https://github.com/ISISComputingGroup/IBEX/issues/7642) | Major | Added the abillity to set blocks on config change. |

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


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |



extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |



# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8140](https://github.com/ISISComputingGroup/IBEX/issues/8140)| Minor | Fixed runcontrol causing DAE stuck WAITING after adding a block with "suspend if invalid" enabled | 


# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [8056](https://github.com/ISISComputingGroup/IBEX/issues/8056) | Minor | Created a new Jenkins pipeline to check for uncomitted and commits not pushed on inst EPICS repos |


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
| Eclipse | 2023-03 | 12/2023 |
| Eclipse Updates| 4.26 | 12/2023 |

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Python | 3.11.6 | 11/2023 |
| ode |	0.16.4 | 11/2023 |
| Lewis | 11/2023 | 11/2023 |
| matplotlib | 3.8.2 | 12/2023 |
