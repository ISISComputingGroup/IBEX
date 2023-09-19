Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| INTER | [#7979](https://github.com/ISISComputingGroup/IBEX/issues/7979) | Patch | Add arbritary fields from/to INTER tank beckhoff | 

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#6048](https://github.com/ISISComputingGroup/IBEX/issues/6048) | PEARL Sample Alignment Motor OPI | Used on PEARL |
| [#7820](https://github.com/ISISComputingGroup/IBEX/issues/7820) | Fermi Chopper Condition monitoring box | Add IOC for PRE4500/Fermi chopper condition monitoring box | 

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#7890](https://github.com/ISISComputingGroup/IBEX/issues/7890) | Patch | DG645 | Fix delay width readback to correctly represent the time difference between leading and trailing edge |
| [#7889](https://github.com/ISISComputingGroup/IBEX/issues/7889) | Patch | DG645 | Plots x axes update if needed. |
| [#7863](https://github.com/ISISComputingGroup/IBEX/issues/7863) | Minor | Fermichopper | Changed fault colour of the LEDs to a brighter hue of red | 
| [#7892](https://github.com/ISISComputingGroup/IBEX/issues/7892) | Minor | DG645 | Labels added to readback delays on OPI | 
| [#8000](https://github.com/ISISComputingGroup/IBEX/issues/8000) | Minor | FINS PLC | Added support for the remote control of the SANDALS V2 Valve | 


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |


### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7985](https://github.com/ISISComputingGroup/IBEX/issues/7985) | patch | Adding a block from the beam status perspective context menu now correctly unchecks "is local" by default. |
| [#7699](https://github.com/ISISComputingGroup/IBEX/issues/7699) | Minor | Added a combined spectra plot to the DAE |
| [#7921](https://github.com/ISISComputingGroup/IBEX/issues/7921) | Minor | Added "Show Title and Users in Dataweb Dashboard Page" to dashboard |
| [#7896](https://github.com/ISISComputingGroup/IBEX/issues/7896) | Minor | Show IOC - COM port mapping on Moxa Ports perspective. |

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
| [#7961](https://github.com/ISISComputingGroup/IBEX/issues/7961) | Minor | New script for standardising colours and fonts used in OPIs |
| [#7982](https://github.com/ISISComputingGroup/IBEX/issues/7982) | Minor | Modified Galil install step to be automated based upon the previous deploy's Galil decision |
| [#7987](https://github.com/ISISComputingGroup/IBEX/issues/7987) | Minor | Improve upgrade script to check MySQL, Java, Git versions automatically, add git status step, check backup directory space, and some other minor changes |

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

