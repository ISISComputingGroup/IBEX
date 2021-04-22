Minor release for MuSR migration.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| MUSR | [#6379](https://github.com/ISISComputingGroup/IBEX/issues/6379) | Minor | Buttons to turn set of CAEN HV PSUs on and off |
| MUSR | [#6133](https://github.com/ISISComputingGroup/IBEX/issues/6133) | Minor | Buttons to save and load steering magnet defaults |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6221](https://github.com/ISISComputingGroup/IBEX/issues/6221) | Patch | HIFIMAGS (HiFi Cryomagnet) | Corrected units of max field. Provide feedback on OPI when controls are disabled. Use a cryomagnet icon. |
| [#6286](https://github.com/ISISComputingGroup/IBEX/issues/6286) | Minor | MercuryITC | Fixed timeout issues giving transient invalid blocks. |

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

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6350](https://github.com/ISISComputingGroup/IBEX/issues/6350) | Minor | Added option to reduce logging on IOCs that do ramping, particularly added this to the Kepcos used on MUSR |
| [#6333](https://github.com/ISISComputingGroup/IBEX/issues/6333) | Minor | Added test coverage report option for IOC system tests |

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
