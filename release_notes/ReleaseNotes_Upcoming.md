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
| [7951](https://github.com/ISISComputingGroup/IBEX/issues/7951) | Stanford PS300 | Support for all Stanford PS300 Series powersupplies|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8160](https://github.com/ISISComputingGroup/IBEX/issues/8160) | minor | Beckhoff/TwinCAT | Allow 2 instances of the TC IOC, for portable beckhoffs |
| [#8104](https://github.com/ISISComputingGroup/IBEX/issues/8104) | minor | PACE5000 | Various PACE5000 snags - set units to bar, slew mode to lin, display source pressure, fix vent status |
| [#8218](https://github.com/ISISComputingGroup/IBEX/issues/8218) | minor | GALIL |  allow COM in GALILADDR macro |
| [#7677](https://github.com/ISISComputingGroup/IBEX/issues/7677) | minor | Tektronix AFG3XXX | Channel 1 and 2 are configurable in IOC macros, by default both are enabled just like so far. |



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

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|

