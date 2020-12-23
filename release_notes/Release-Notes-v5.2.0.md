### Instrument Specific Changes
Changes made for a particular instrument

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| Muon FE |[#3409](https://github.com/ISISComputingGroup/IBEX/issues/3409) | Minor | Add Muon separator stability logic |
| LOQ | [#3623](https://github.com/ISISComputingGroup/IBEX/issues/3623) | Minor | Added motorExtension for the LOQ Aperture|
| LARMOR/SURF| [#3262](https://github.com/ISISComputingGroup/IBEX/issues/3262) | Minor | Added IOC and OPI for Knauer 1050 HPLC pump|
| LOQ | [#3622](https://github.com/ISISComputingGroup/IBEX/issues/3622) | Minor | LOQ Added IOC and OPI for Water Bath Valve|

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3667](https://github.com/ISISComputingGroup/IBEX/issues/3667) | Minor | GENESYS address changed from float to integer.|
| [#3679](https://github.com/ISISComputingGroup/IBEX/issues/3679) | Minor | Better logging of transient errors for the Fermi Choppers|
| [#3776](https://github.com/ISISComputingGroup/IBEX/issues/3776) | Minor | Modifications to Mercury OPI |
| [#3621](https://github.com/ISISComputingGroup/IBEX/issues/3621) | Minor | Make Julabo communications more configurable to cope with different models. |
| [#2133](https://github.com/ISISComputingGroup/IBEX/issues/2133) | Minor | Eurotherm and Danfysik IOCs allow setting local calibration directory via macro |
| [#3386](https://github.com/ISISComputingGroup/IBEX/issues/3386) | Minor | Added IOC and OPI for Ocean Optics DH2000 shutter|
| [#3469](https://github.com/ISISComputingGroup/IBEX/issues/3469) | Minor | McLennan homing mode 3 changed, reapplies offset after home |
| [#3578](https://github.com/ISISComputingGroup/IBEX/issues/3578) | Minor |Added Alarm PV to Reflectometry IOC |
|[#3770](https://github.com/ISISComputingGroup/IBEX/issues/3770)| Minor | Eurotherm: Display when a reading is out of range for the calibration file |
| [#3476](https://github.com/ISISComputingGroup/IBEX/issues/3476) | Minor | IRIS: Add support for the Keithley 2001 digital multimeter.|
| [#3740](https://github.com/ISISComputingGroup/IBEX/issues/3740) | Minor | LET: Add support for Astrium Choppers |

###  IBEX Client

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#3439](https://github.com/ISISComputingGroup/IBEX/issues/3439) | Minor | Replaced all IBEX GUI icons and icon licensing information |
| [#3641](https://github.com/ISISComputingGroup/IBEX/issues/3641) | Minor | Danfysik has a new Choice Button power and polarity toggle |
| [#3550](https://github.com/ISISComputingGroup/IBEX/issues/3550) | Minor | MK3 Chopper OPI now provides clearer indication of local/remote modes |
|[#3677](https://github.com/ISISComputingGroup/IBEX/issues/3677) | Minor | Allow scrolling of macros and PVs within IOC view for IOCs in a component when remote |
| [#3656](https://github.com/ISISComputingGroup/IBEX/issues/3656) | Minor | Jaws motion is now more clearly highlighted on the Jaws/Jaws Manager views. |
| [#3577](https://github.com/ISISComputingGroup/IBEX/issues/3577) | Minor | Added "in position" LEDs for each individual position on the Motion Set Points (few) OPI |
| [#3699](https://github.com/ISISComputingGroup/IBEX/issues/3699) | Minor | Convert Lakeshore 218 to new opi style.|
|[#3274](https://github.com/ISISComputingGroup/IBEX/issues/3274)| Minor | Edit scripts in script server queue |

### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3335](https://github.com/ISISComputingGroup/IBEX/issues/3335) | Minor | Make cache thread safe (should mean alarm server restarts more consistently but it is hard to prove this) |
|[#3824](https://github.com/ISISComputingGroup/genie_python/pull/148)| Minor | Genie python: Users can now return the pv name for a given block |


### IBEX Server

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3580](https://github.com/ISISComputingGroup/IBEX/issues/3580) | Minor | Axis record preserves units from underlying motor record  |
|[#3829](https://github.com/ISISComputingGroup/IBEX/issues/3829)| Minor | Failed communication with danfysiks now causes alarm |

### Development & Deployment process

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#3836](https://github.com/ISISComputingGroup/IBEX/issues/3836) | Minor | IOC system tests can use the latest clean build |
|[#2809](https://github.com/ISISComputingGroup/IBEX/issues/2809)| Patch| OPI Checker: Does not check tabbed containers correctly |
|[#3908](https://github.com/ISISComputingGroup/IBEX/issues/3908)| Minor | Inst Servers: Add test coverage |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality