## Changes to make on specific instruments when releasing

## All instruments

## IBEX changes

### Features

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3189](https://github.com/ISISComputingGroup/IBEX/issues/3189) | Minor | Add Oxford Instruments ITC IOC. |
| [#2593](https://github.com/ISISComputingGroup/IBEX/issues/2593) | Minor | Add support for Cryomagnet IPS |
| [#2856](https://github.com/ISISComputingGroup/IBEX/issues/2856) | Minor | Update the FZJ DD Fermi Chopper based on hardware testing |


### UI

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#2814](https://github.com/ISISComputingGroup/IBEX/issues/2814) | Minor | Add OPI for FZJ DD Fermi Chopper. |

### Interfaces

| Ticket | Type  | Change |
| ------ | ------| ------------- |


### Performance

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |


### IBEX Server

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Development process

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

what | version | where | last updated/checked
---- | ------- | ----- | --------------------
MySQL | 5.7.21 | system | 	24-01-2018
Java JRE | 1.8.0 update 161 | system | 	24-01-2018
ActiveMQ | 5.10.0 | EPICS\ISIS\ActiveMQ | out of date
EPICS | 3.15.5 | EPICS\base | ?
genie_python packages | various | genie_python\package_builder\build_python.bat | 9/2017
genie_python_3 packages | various | genie_python\package_builder\build_python_3.bat and requirements.txt | 9/2017
pydev | ? (6.3.1 for E4) | GUI as target | out of date (7/3/2014 for e4)
pydev in E4 | 6.3.1 | GUI as target | 7/3/2014
