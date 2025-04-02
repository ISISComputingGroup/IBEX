Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| CHIPIR | [PR](https://github.com/ISISComputingGroup/ibex_gui/pull/1785) | Minor | Put filters on CHIPIR collimator screen |
| INTER | [#8675](https://github.com/isiscomputinggroup/ibex/issues/8675) | Patch | Gracefully stop galil motors when safety system is tripped. |
| HIFI | [#8704](https://github.com/ISISComputingGroup/IBEX/issues/8704) | Minor | Inhibit taking reading within two seconds of field measurement range change |
| INTER | [#7814](https://github.com/isiscomputinggroup/ibex/issues/7814) | Patch | Add Inclinometer variable for INTER Beckhoff. |


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
| [#8673](https://github.com/ISISComputingGroup/IBEX/issues/8673) | Patch | TC/Beckhoff | Make poll rate configurable |
| [#8660](https://github.com/ISISComputingGroup/IBEX/issues/8660) | Patch | HV Caen | Increase number of available channels to 16 cards x 24 channels. |
| [#8682](https://github.com/ISISComputingGroup/IBEX/issues/8682) | Patch | ISISDAE IOC | Add string-formatted run duration and period run duration PVs. |
| [#8682](https://github.com/ISISComputingGroup/IBEX/issues/8692) | Patch | DG645 | Limit OPI (user interface) graph update to 1Hz, to avoid excessive CPU usage. |
| [#8704](https://github.com/ISISComputingGroup/IBEX/issues/8704) | Minor | G3HALLPROBE | Inhibit taking reading within two seconds of field measurement range change |


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
| [#8505](https://github.com/ISISComputingGroup/IBEX/issues/8505) | Minor | Jaws: enforce minimum and maximum gap values |
| [PR](https://github.com/ISISComputingGroup/ibex_gui/pull/1775) | Minor | Add muon and EPB1 beam current to beam status view |
| [#8578](https://github.com/ISISComputingGroup/IBEX/issues/8578) | Minor | Add defaults for font size and autolayout in a scripting console |



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
| [#8628](https://github.com/ISISComputingGroup/ibex/issues/8628) | Patch | Ensure experiment database populator can be installed on modern python versions |
| [#8631](https://github.com/ISISComputingGroup/IBEX/issues/8631) | Patch | Update experiment database populator auth scheme to REST rather than SOAP |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### Server dependencies

what | version | where | last updated/checked
|---- | ------- | ----- | --------------------|
| MySQL | 8.4.2 | ibex_install_utils | 10/2024 |
| Make | 4.4 | utils_win32 | 11/2023 |
| ActiveMQ | 5.18.3 | ISIS\ActiveMQ | 12/2023 |
| Nicos | 23 | ScriptServer | 11/2023 |
| Cygwin | 3.4.9 | ICP_Binaries |	12/2023 |
| MySql-connector J | 8.4.0 | IOCLogServer | 10/2024 |

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Gson | 2.11 | 10/2024 |
| Guava | 33.3.1 | 10/2024 |
| MySql-connector J | 9.1.0 | 01/2025 |
| commons-codec | 1.17.1 | 10/2024 |
| Maven | 3.9.5 | 11/2023 |
| ActiveMQ (different to server version) | 5.18.6 | 10/2024 |
| Nicos | 23 | 11/2023 |
| Jakarta Activation API | 2.1.2 | 10/2024 |
| Jakarta Mail API | 2.1.3 | 10/2024 |
| Jakarta XML Binding API | 4.0.1 | 10/2024 |
| JavaX Activation | 1.1.1 | 10/2024 |
| joda time | 2.13 | 10/2024 |
| py4j | 0.10.9.7 | 10/2024 |
| log4j | 2.24 | 10/2024 |
| JAXB | 3.0.2 | 10/2024 |
| Tyrus | 2.2.0 | 10/2024 |
| JacORB OMG API | 3.9 | 10/2024 |
| Mockito Core | 5.14.0 | 10/2024 |
| JeroMQ | 0.6.0 | 10/2024 |
| Nebula | 3.0.0 | 10/2024 |
| CS-Studio | 12/2023 | 12/2023 |
| Pydev | 11.0.3 | 12/2023 |
| Eclipse | 2024-09 | 04/2024 |
| Eclipse Updates| 4.33 | 10/2024 |

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Python | 3.11.9 | 10/2024 |
| Lewis | git | 10/2024 |
| matplotlib | 3.9.2 | 10/2024 |
