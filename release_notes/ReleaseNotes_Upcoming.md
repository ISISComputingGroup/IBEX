Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#6032](https://github.com/ISISComputingGroup/IBEX/issues/6032) | Major | Updated ORC code to cater for WISH collimator - Note this may effect the behaviour of the LET/MERLIN collimators as they share some code. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
|[#6040](https://github.com/ISISComputingGroup/IBEX/issues/6040)|PEARLPC|Created IOC, tests, emulator and OPI for the PEARL pressure controller|
|[#5952](https://github.com/ISISComputingGroup/IBEX/issues/5952)|DFKPS|Correct bug where autoonoff was always a step behind|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#4815](https://github.com/ISISComputingGroup/IBEX/issues/4815) | Minor | Mclennan | Set creep sped to HVEL when sending an internal home |
| [#6754](https://github.com/ISISComputingGroup/IBEX/issues/6754) | Minor | Beckhoff| The Beckhoff IOC will now automatically pick up how many axes are on the controller. |
| [#6797](https://github.com/ISISComputingGroup/IBEX/issues/6797) | Minor | ZFCNTRL | The ZFCNTRL ioc write tolerance default has been changed from 0.0002 to 0.0012 to support a kepco running in the higher current range. |
| [#6797](https://github.com/ISISComputingGroup/IBEX/issues/6797) | Minor | KEPCO | Added the ability to set and get current ranges. |
| [#6027](https://github.com/ISISComputingGroup/IBEX/issues/6027) | Patch | LKSH336 | Made it clearer that the 336 IOC can be used to control the 350 model. |


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6586](https://github.com/ISISComputingGroup/IBEX/issues/6586) | Minor | Make it clearer that period 0 is the current period in the spectra plots |
| [#6831](https://github.com/ISISComputingGroup/IBEX/issues/6831) | Patch | Using built-in Java function rather than our own Converter class  |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#858](https://github.com/ISISComputingGroup/IBEX/issues/858) | Minor | Added validation for duplicate PVs on synoptic components |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6352](https://github.com/ISISComputingGroup/IBEX/issues/6352) | Minor | ReadASCII made more extendable to variable amount of columns |

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
