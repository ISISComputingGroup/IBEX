# Dependencies

what | version | where | last updated/checked
---- | ------- | ----- | --------------------
MySQL | 5.7.19 | system | 	24-01-2018
Java JRE | 1.8.0 update 161 | system | 	24-01-2018
ActiveMQ | 5.10.0 | EPICS\ISIS\ActiveMQ | out of date
EPICS | 3.15.5 | EPICS\base | ?
genie_python packages | various | genie_python\package_builder\build_python.bat | 9/2017
genie_python_3 packages | various | genie_python\package_builder\build_python_3.bat and requirements.txt | 9/2017
pydev | ? (6.3.1 for E4) | GUI as target | out of date (7/3/2014 for e4)
pydev in E4 | 6.3.1 | GUI as target | 7/3/2014

## Changes to make on specific instruments when releasing

## All instruments

### IMAT

Apply hotfix as per https://github.com/ISISComputingGroup/EPICS-ioc/pull/267 which was missed from [#3037](https://github.com/ISISComputingGroup/IBEX/issues/3037)

## IBEX changes

### Features

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2904](https://github.com/ISISComputingGroup/IBEX/issues/2904) | Minor | Journal viewer: pagination |
| [#2905](https://github.com/ISISComputingGroup/IBEX/issues/2905) | Minor | Put journal viewer data into tabular form |
| [#2541](https://github.com/ISISComputingGroup/IBEX/issues/2541) | Minor | Show the NICOS output in the IBEX GUI |
| [#2869](https://github.com/ISISComputingGroup/IBEX/issues/2542) | Minor | Can send pause/resume/stop commands to NICOS from GUI |

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2914](https://github.com/ISISComputingGroup/IBEX/issues/2914) | Minor | Add PID table to triton |
| [#3005](https://github.com/ISISComputingGroup/IBEX/issues/3005) | Minor | Add third KEPCO IOC |
| [#2961](https://github.com/ISISComputingGroup/IBEX/issues/2961) | Minor | Galil homing routines now use the same acceleration as normal moves |
| [#2642](https://github.com/ISISComputingGroup/IBEX/issues/2642) | Minor | Add Gamry |
| [#2915](https://github.com/ISISComputingGroup/IBEX/issues/2915) | Minor | Create Triton IOC |
| [#2943](https://github.com/ISISComputingGroup/IBEX/issues/2943) | Minor | MK3Chopper communication reconnect |
| [#3037](https://github.com/ISISComputingGroup/IBEX/issues/3037) | Minor | BKHOFF non integer steps sent |

### UI

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2222](https://github.com/ISISComputingGroup/IBEX/issues/2222) | Minor | Fix issue where IOC macro values were appearing in the GUI when they shouldn't. |
| [#2889](https://github.com/ISISComputingGroup/IBEX/issues/2889) | Patch | Display units in log plotter perspective. |
| [#2869](https://github.com/ISISComputingGroup/IBEX/issues/2869) | Patch | Make DAE simulation mode even more obvious |
| [#2646](https://github.com/ISISComputingGroup/IBEX/issues/2646) | Minor | Eurotherm OPI: Prevent autofocus on toggle ramp button |

### Interfaces

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Performance

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Back end

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2971](https://github.com/ISISComputingGroup/IBEX/issues/2971) | Patch | Fix disconnected monitor blocks |
| [#2750](https://github.com/ISISComputingGroup/IBEX/issues/2750) | Minor | Exception support in DAE |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
