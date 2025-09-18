Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8822](https://github.com/ISISComputingGroup/IBEX/issues/8822) | Major | Remove various SECI compatibility tools - `SECI2IBEX` IOC, SECI web dashboard, startup scripts etc. |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| PEARL | [#8349](https://github.com/ISISComputingGroup/IBEX/issues/8349) | Patch | Add option for permanently-centred crosshair on Pearl camera |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#8691](https://github.com/ISISComputingGroup/IBEX/issues/8691) | Ambrell EasyHeat Induction Furnace PSU | Intended for ENGIN-X. | 

### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
|[#8614](https://github.com/ISISComputingGroup/IBEX/issues/8614) | Minor | Oxford Instruments - Mercury IPS| Added support for SCPI mode to use the full capabilities of the new Mercury IPS magnet supplies|
|[#8680](https://github.com/ISISComputingGroup/IBEX/issues/8680) | Minor | HVCAEN | Number of summary channels is now configurable by macro. |


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8731](https://github.com/ISISComputingGroup/IBEX/issues/8731) | Major | Added new GUI dialog to configure Alerts. |
| [#8820](https://github.com/ISISComputingGroup/IBEX/issues/8820) | Minor | Added a 'Home' button to the 'Motors' tab within the Motion Set Point (Few) device screen |

### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8699](https://github.com/ISISComputingGroup/IBEX/issues/8699) | Minor | Show current high/low limits for Alarm in tool-tip popup |



# Python

### `genie_python`

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#24](https://github.com/ISISComputingGroup/genie/issues/24) | Patch | Allow `g.begin()` when DBSVR is down |
| [#8724](https://github.com/ISISComputingGroup/IBEX/issues/8724) | Minor | Added `change_autosave` command to change autosave frequency. |


### Bluesky

See https://github.com/ISISComputingGroup/ibex_bluesky_core/releases

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |



# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[5081](https://github.com/ISISComputingGroup/IBEX/issues/5081) | Minor | Functions that allow scientists to save known "good" states of their TPAR file directory and reload them at will. |

# Internal changes

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
