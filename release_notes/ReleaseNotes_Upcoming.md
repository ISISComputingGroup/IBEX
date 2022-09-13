Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#7022](https://github.com/ISISComputingGroup/IBEX/issues/7022) | Minor| Passing `prepost=False` to begin, pause commands etc will now skip ioc/server pre/post commands. However client side pre/post command will now need to be modified to accept a prepost argument so they can decide what to do|
| [#7135](https://github.com/ISISComputingGroup/IBEX/issues/7135) | Minor| The NICOS script server daemon (`NICOSDAEMON`) is no longer started by default, and instead should be added to appropriate configurations or components if it is required - for example, on instruments using the script generator. |
| [#7181](https://github.com/ISISComputingGroup/IBEX/issues/7181) | Minor| There should be no longer be many brief flashes of windwos during ibex startup|
| [#6769](https://github.com/ISISComputingGroup/IBEX/issues/6769) | Minor| Genie Python will no longer print an exception trace if you enable handleing exceptions yourself (This is not the default case).|
| [#7237](https://github.com/ISISComputingGroup/IBEX/issues/7237) | Minor| The IOC descriptions have been updated to follow a convention of Manufacturer Model/Series (optional) Device/Description. This is not a breaking change, but things will appear differently in the IOC lists in the GUI. |

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
| [#5993](https://github.com/ISISComputingGroup/IBEX/issues/5993) | Minor | CRYOSMS | Added support for more complex ramp modes. |
| [#6861](https://github.com/ISISComputingGroup/IBEX/issues/6861) | Patch | TC/Beckhoff | Get velocity from ADS rather than setting to 1 by default | 
| [#7261](https://github.com/ISISComputingGroup/IBEX/issues/7261) | Minor | Lakeshore336 | Added support for output/loop 3 and 4 |
| [#7198](https://github.com/ISISComputingGroup/IBEX/issues/7198) | Patch | TC/Beckhoff | Fix moving/done flip-flop from 1 to 0 inversely. |
| [#7213](https://github.com/ISISComputingGroup/IBEX/issues/7213) | Minor | TTIPLP | Added overcurrent and overvolt trip warnings and reset functionality. |
| [#6283](https://github.com/ISISComputingGroup/IBEX/issues/6283) | Minor | MercuryiTC | Add a % of the volt limit used on pressure and temp cards | 
| [#7255](https://github.com/ISISComputingGroup/IBEX/issues/7255) | Minor | TPG300 | Fix previously added switching function and an error when setting units. |
| [#7315](https://github.com/ISISComputingGroup/IBEX/issues/7315) | Minor | DAE | Autosave run number so displayed correctly even if DAE is OFF | 
| [#7324](https://github.com/ISISComputingGroup/IBEX/issues/7324) | Minor | TC/Beckhoff | Fix motionsetpoints loading. |
| [#4318](https://github.com/ISISComputingGroup/IBEX/issues/4318) | Minor | JSCO4180 | Added JSCO4180_2 and JSCO4180_3 IOCs. |


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#7276](https://github.com/ISISComputingGroup/IBEX/issues/7276) | Minor | Various waveform PVs are now safely truncated. |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#3736](https://github.com/ISISComputingGroup/IBEX/issues/3736) | Minor | Added navigation to run control settings via block right click menu; Clarified run control settings in block configuration window are default.  |
| [#5743](https://github.com/ISISComputingGroup/IBEX/issues/5743) | Minor | Added script path macro to the Background Script IOC. |
| [#3647](https://github.com/ISISComputingGroup/IBEX/issues/3647) | Minor | New and existing block names limited to 25 characters. |


### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6425](https://github.com/ISISComputingGroup/IBEX/issues/6425) | Minor | Added file name and error message to Motion Setpoints OPIs |
| [#7261](https://github.com/ISISComputingGroup/IBEX/issues/7261) | Minor | Added support for output/loop 3 and 4 in the Lakeshore336 OPI |
| [#7212](https://github.com/ISISComputingGroup/IBEX/issues/7212) | Patch | Optimise the memory usage of very large/complex OPIs which have dynamic behaviour (e.g. the reflectometry OPI). This solves issues seen on INTER and POLREF with the client crashing or slowing down due to out-of-memory conditions. |
| [#6719](https://github.com/ISISComputingGroup/IBEX/issues/6719) | Minor | Implement a new matplotlib backend. This should significantly improve the stability of long-running and dynamically updating plots. |
| [#7224](https://github.com/ISISComputingGroup/IBEX/issues/7224) | Patch | Fixed "add block to a config" (not current config) option on right-click. |
| [#7133](https://github.com/ISISComputingGroup/IBEX/issues/7133) | Minor | Adding to the Log Plotter if the Log Plotter perspective is disabled will now show a warning. |
| [#4673](https://github.com/ISISComputingGroup/IBEX/issues/4673) | Minor | Added Eurotherm single temperature sensor OPI |
| [#5470](https://github.com/ISISComputingGroup/IBEX/issues/5470) | Minor | Added hide title and users checkbox to experiment details view; Adjusts its wording |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5470](https://github.com/ISISComputingGroup/IBEX/issues/5470) | Minor | Added command to hide an experiment's title and users |


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7291](https://github.com/ISISComputingGroup/IBEX/issues/7291) | Patch | The `restart_ioc_when_pv_in_alarm` script now returns a stoppable thread. | 


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6425](https://github.com/ISISComputingGroup/IBEX/issues/6425) | Minor | Added error messages for common issues when processing a motionsetpoints file |
| [#5764](https://github.com/ISISComputingGroup/IBEX/issues/5764) | Minor | fte not checked if mode is not 2 in splitCharWaveform |



# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7240](https://github.com/ISISComputingGroup/IBEX/issues/7240) | Minor | Schneider PLC IOC: Refactor to make generic |

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
