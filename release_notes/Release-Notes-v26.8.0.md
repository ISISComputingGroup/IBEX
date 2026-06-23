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
| [#8919](https://github.com/ISISComputingGroup/IBEX/issues/8919) | Moxa ioLogik E1213 | Added Support for new device|
| [5885](https://github.com/ISISComputingGroup/IBEX/issues/5885) | QuantumNorthwest NeutronIQ | Added support. |


### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [8798](https://github.com/ISISComputingGroup/IBEX/issues/8798) | Major | Coherent OBIS Laser Remote | Support multiple lasers on a single IOC & add support for switching lasers on/off and setting output power. Previous PV names have changed, e.g. `CHTOBISR_01:some_pv` will now be `CHTOBISR_01:1:some_pv` (where `1` is the laser number). |
| [TwinCat #4](https://github.com/ISISComputingGroup/EPICS-TwincatMotor/pull/4) | Patch | TC/Beckhoff | Send reset just before any moves to clear errors if possible |
| [GUI #1840](https://github.com/ISISComputingGroup/ibex_gui/pull/1840) | Patch | Motors | Show a warning if motor has been left in SET mode |
| [#8688](https://github.com/ISISComputingGroup/IBEX/issues/8688) | Minor | Eurotherm | Added additional Eurotherm attributes.|
| [2196](https://github.com/ISISComputingGroup/IBEX/issues/2196) & [8959](https://github.com/isisComputingGroup/ibex/issues/8959) | Minor | Nanodac | Add OPI, fix IOC, add control of "advanced loop". |
| [8955](https://github.com/ISISComputingGroup/IBEX/issues/8955) | Patch | Mercury ITC | Allow Ethernet comms in addition to existing serial comms |
| [8971](https://github.com/ISISComputingGroup/IBEX/issues/8971) | Patch | Knauer K-6 | Increase number of available IOCs from 2 to 4 |
| [8969](https://github.com/ISISComputingGroup/IBEX/issues/8969) | Minor | Keithley 6517B | Add set/read "zero check" and current autorange modes |
| [8464](https://github.com/ISISComputingGroup/IBEX/issues/8464) | Minor | TC/Beckhoff | Allow sending a frozen offset to beckhoffs in order to set position |
| [6839](https://github.com/ISISComputingGroup/IBEX/issues/6839)  | Minor | TC/Beckhoff | Implement setting auto-energise to controller |


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
| [PR](https://github.com/ISISComputingGroup/ibex_gui/pull/1846) | Patch | Display Moxas in a predictable order in the Moxa perspective |



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
|[8885](https://github.com/isisComputingGroup/ibex/issues/8885) | Patch | Dependency version updates. No user-facing behaviour changes expected. |
|[8947](https://github.com/ISISComputingGroup/IBEX/issues/8947) | Minor | Update EPICS SNMP driver and net-snmp support library to latest upstream (1.1.0.6 and 5.9.5.2) |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

what | version | where | last updated/checked
|---- | ------- | ----- | --------------------|
| MySQL | 8.4.9 | ibex_install_utils | 05/2026 |
| ActiveMQ | 5.19.6 | ISIS\ActiveMQ | 05/2026 |
| MySql-connector J | 8.4.0 | IOCLogServer | 05/2026 |

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Gson | 2.14.0 | 05/2026 |
| Guava | 33.6.0 | 05/2026 |
| MySql-connector J | 8.4.0 | 05/2026 |
| commons-codec | 1.22.0 | 05/2026 |
| Maven | 3.9.15 | 05/2026 |
| ActiveMQ (different to server version) | 5.19.0 | 05/2026 |
| Jakarta Mail API | 2.2.0 | 05/2026 |
| joda time | 2.14.2 | 05/2026 |
| py4j | 0.10.9.9 | 05/2026 |
| log4j | 2.26.0 | 05/2026 |
| JAXB | 4.0.6 | 05/2026 |
| Tyrus | 2.2.2 | 05/2026 |
| JacORB OMG API | 3.9 | 05/2026 |
| Mockito Core | 5.23.0 | 05/2026 |
| JeroMQ | 0.6.0 | 05/2026 |
| Eclipse | 2026-03 | 05/2026 |

### Uktena dependencies

```
python -m pip freeze (on the release build when release is created)
```
