This is a minor release and will only be deployed to certain instruments.

Please see [release notes for version 5.0.0](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.0.0) for the latest major changes.

### Instrument Specific Changes
Changes made for a particular instrument

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| Tosca | [#3455](https://github.com/ISISComputingGroup/IBEX/issues/3455) | Minor | Add support for Tosca sample positioner |
| Gem / Polaris | [#3296](https://github.com/ISISComputingGroup/IBEX/issues/3296) + [#3681](https://github.com/ISISComputingGroup/IBEX/issues/3681) | Minor | Added Induction furnace IOC |
| Osiris | [#3460](https://github.com/ISISComputingGroup/IBEX/issues/3460) | Minor | Added support for the OSIRIS beryllium filter |
| Rikenfe | [#3314](https://github.com/ISISComputingGroup/IBEX/issues/3314) | Minor | Update RIKENFE Power supplies to be the same as are working on the instrument |
| Rikenfe | [#3615](https://github.com/ISISComputingGroup/IBEX/issues/3615) | Minor | Add banner messages for RB3/RB4 on riken |
| Osiris | [#3629](https://github.com/ISISComputingGroup/IBEX/issues/3629) | Minor | OSIRIS: Be filter motor set points and Lakeshore IOC |
| Muonfe | [#3408](https://github.com/ISISComputingGroup/IBEX/issues/3408) | Minor | Added IOC to display Status of the Separator PSU |
| Ines | [#3577](https://github.com/ISISComputingGroup/IBEX/issues/3577)  | Minor | INES: Neutron Camera Positioner |
| Tosca |[#3696](https://github.com/ISISComputingGroup/IBEX/issues/3696) | Minor | TOSCA: Add support fourth Lakeshore 218 IOC |
| Loq |[#3479](https://github.com/ISISComputingGroup/IBEX/issues/3479) | Minor | Add support for LOQ integrating detector card to liveview |

### Features

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3551](https://github.com/ISISComputingGroup/IBEX/issues/3551) | Minor | Reflectometry server has different movement depending on move parameter and move beamline. |

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3468](https://github.com/ISISComputingGroup/IBEX/issues/3468) | Patch | Fix mclennan slow communications |
| [#3463](https://github.com/ISISComputingGroup/IBEX/issues/3463) | Minor | Added vertical-only jaws OPI |
| [#3524](https://github.com/ISISComputingGroup/IBEX/issues/3524) | Minor | Can set instrument prefix to non-local instrument on MK3 Chopper OPI |


###  IBEX Client

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#3341](https://github.com/ISISComputingGroup/IBEX/issues/3341) | Patch | Log plots are now closed when switching to a different instrument. |
| [#3207](https://github.com/ISISComputingGroup/IBEX/issues/3207) | Patch | DAE synoptic icon no longer points to DAE perspective, live view synoptic icon now works |
| [#3480](https://github.com/ISISComputingGroup/IBEX/issues/3480) | Patch | Allowed access to the motor details via the galil engineering screen, regardless of manager mode |
| [#3488](https://github.com/ISISComputingGroup/IBEX/issues/3488) | Patch | Fixed bug where synoptics could not be deleted |
| [#3504](https://github.com/ISISComputingGroup/IBEX/issues/3504) | Patch | Fixed bug where total uAh would display incorrectly on run information panel |
| [#3554](https://github.com/ISISComputingGroup/IBEX/issues/3554) | Patch | Fixed bug where block window would judder if at the wrong size |
| [#3515](https://github.com/ISISComputingGroup/IBEX/issues/3515) | Patch | Added OPI duplicate key test and removed existing duplicates |
| [#3427](https://github.com/ISISComputingGroup/IBEX/issues/3427) | Minor | Add XY Profile option for Detector Live View |
| [#3369](https://github.com/ISISComputingGroup/IBEX/issues/3369) | Minor | NICOS now displays the name of the script that is currently running. |
| [#3628](https://github.com/ISISComputingGroup/IBEX/issues/3628) | Minor | Add Instrument updating dialogue box when DAE busy |
| [#3631](https://github.com/ISISComputingGroup/IBEX/issues/3631) | Minor | Add ROI and configuration/settings to liveview |
| [#3545](https://github.com/ISISComputingGroup/IBEX/issues/3545) | Minor | Add TOF v Pixel liveview |
| [#3630](https://github.com/ISISComputingGroup/IBEX/issues/3630) | Minor | Add area detector stats plugin for liveview |
| [#3697](https://github.com/ISISComputingGroup/IBEX/issues/3697) | Patch | Fix a bug causing macros to be set incorrectly when copying synoptic components |

### Interfaces

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2777](https://github.com/ISISComputingGroup/IBEX/issues/2777) | Minor | Correct Group/Block ordering on Instrument Status web frontend |

### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2658](https://github.com/ISISComputingGroup/IBEX/issues/2658) | Minor | Warning message on `g.begin()` if DAE is in simulation mode  |

### IBEX Server

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3342](https://github.com/ISISComputingGroup/IBEX/issues/3342) | Patch | Fix inconsistent behaviour when using PV values |
| [#3422](https://github.com/ISISComputingGroup/IBEX/issues/3422) | Minor | looking for IOCs not only in master |
| [#3419](https://github.com/ISISComputingGroup/IBEX/issues/3419) | Patch | Fixed address list to allow clients to connect through a VPN |
| [#3627](https://github.com/ISISComputingGroup/IBEX/issues/3627) | Minor | Set STATETRANS (busy) variable during wiring table changes |


### Development & Deployment process

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3500](https://github.com/ISISComputingGroup/IBEX/issues/3500) | Patch | Fix deployment script dividing by zero when motor resolution is not set |


### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2448](https://github.com/ISISComputingGroup/IBEX/issues/2448) | Patch| Dataweb: Move run control PVs to block archiver |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
