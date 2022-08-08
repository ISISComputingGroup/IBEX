Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7022](https://github.com/ISISComputingGroup/IBEX/issues/7022) | Minor| Passing `prepost=False` to begin, pause commands etc will now skip ioc/server pre/post commands. However client side pre/post command will now need to be modified to accept a prepost argument so they can decide what to do|
| [#7135](https://github.com/ISISComputingGroup/IBEX/issues/7135) | Minor| The NICOS script server daemon (`NICOSDAEMON`) is no longer started by default, and instead should be added to appropriate configurations or components if it is required - for example, on instruments using the script generator. |
| [#7181](https://github.com/ISISComputingGroup/IBEX/issues/7181) | Minor| There should be no longer be many brief flashes of windwos during ibex startup|
| [#6769](https://github.com/ISISComputingGroup/IBEX/issues/6769) | Minor| Genie Python will no longer print an exception trace if you enable handleing exceptions yourself (This is not the default case).|

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#7253](https://github.com/ISISComputingGroup/IBEX/issues/7253) | Temperature Jump Apparatus | Add support for SANS Temperature Jump Apparatus RS232 |
| [6942](https://github.com/ISISComputingGroup/IBEX/issues/6942) | Transtechnik PSU | Add support for Transtechnik PSU (for RIKEN) |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6861](https://github.com/ISISComputingGroup/IBEX/issues/6861) | Patch | TC/Beckhoff | Get velocity from ADS rather than setting to 1 by default | 
| [#7198](https://github.com/ISISComputingGroup/IBEX/issues/7198) | Patch | TC/Beckhoff | Fix moving/done flip-flop from 1 to 0 inversely. | 


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#3736](https://github.com/ISISComputingGroup/IBEX/issues/3736) | Minor | Added navigation to run control settings via block right click menu; Clarified run control settings in block configuration window are default.  |


### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6425](https://github.com/ISISComputingGroup/IBEX/issues/6425) | Minor | Added file name and error message to Motion Setpoints OPIs |


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
| [#6425](https://github.com/ISISComputingGroup/IBEX/issues/6425) | Minor | Added error messages for common issues when processing a motionsetpoints file |


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
