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

### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [8798](https://github.com/ISISComputingGroup/IBEX/issues/8798) | Major | Coherent OBIS Laser Remote | Support multiple lasers on a single IOC & add support for switching lasers on/off and setting output power. Previous PV names have changed, e.g. `CHTOBISR_01:some_pv` will now be `CHTOBISR_01:1:some_pv` (where `1` is the laser number). |
| [TwinCat #4](https://github.com/ISISComputingGroup/EPICS-TwincatMotor/pull/4) | Patch | TC/Beckhoff | Send reset just before any moves to clear errors if possible |
| [GUI #1840](https://github.com/ISISComputingGroup/ibex_gui/pull/1840) | Patch | Motors | Show a warning if motor has been left in SET mode |



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



# Python

### `genie_python`

See https://github.com/ISISComputingGroup/genie/releases

### Bluesky

See https://github.com/ISISComputingGroup/ibex_bluesky_core/releases

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |



# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[8445](https://github.com/ISISComputingGroup/IBEX/issues/8445) | Minor | Change how we set macro default values on ioc's so that it uses the same source of truth as the gui, this will not affect existing configurations |

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

### `uktena` Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
