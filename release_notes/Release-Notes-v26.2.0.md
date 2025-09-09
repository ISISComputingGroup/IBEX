Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8822](https://github.com/ISISComputingGroup/IBEX/issues/8822) | Major | Remove various SECI compatibility tools - `SECI2IBEX` IOC, SECI web dashboard, startup scripts etc. |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |

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
|[#8614](https://github.com/ISISComputingGroup/IBEX/issues/8614) | Major | Oxford Instruments - Mercury IPS| Added support for SCPI mode to use the full capabilities of the new Mercury IPS magnet supplies|


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


### Bluesky

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |



# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

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


