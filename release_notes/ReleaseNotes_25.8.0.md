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
| [#8682](https://github.com/ISISComputingGroup/IBEX/issues/8682) | Patch | ISISDAE | Add string-formatted run duration and period run duration PVs. |
| [#8682](https://github.com/ISISComputingGroup/IBEX/issues/8692) | Patch | DG645 | Limit OPI (user interface) graph update to 1Hz, to avoid excessive CPU usage. |
| [#8704](https://github.com/ISISComputingGroup/IBEX/issues/8704) | Minor | G3HALLPROBE | Inhibit taking reading within two seconds of field measurement range change |
| [#8706](https://github.com/ISISComputingGroup/IBEX/issues/8706) | Patch | TPG300 | archive relay status PVs |
| [#8720](https://github.com/ISISComputingGroup/IBEX/issues/8720) | Patch | ISISDAE | Improve begin/end speeds by optimising archiver restarts |
| [#8687](https://github.com/ISISComputingGroup/IBEX/issues/8687) | Minor | LITRON | Added a stale indicator to allow detection of VI disconnection from hardware. |



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
| [4338](https://github.com/ISISComputingGroup/IBEX/issues/4338) | Minor | Improve performance of `cget` function |
| [8671](https://github.com/ISISComputingGroup/IBEX/issues/8671) | Minor | Make error message from corrupt cache more verbose |

### Bluesky

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [8597](https://github.com/ISISComputingGroup/IBEX/issues/8597) | Minor | Numpy version 2 will now be used. Some APIs are not backwards-compatible between numpy 1.x and 2.x. See [numpy 2 release notes](https://numpy.org/devdocs/release/2.0.0-notes.html) for further details. |
| [8597](https://github.com/ISISComputingGroup/IBEX/issues/8597) | Minor | Python version 3.12 will now be used. |


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
| Gson | 2.12.1 | 04/2025 |
| Guava | 33.4.0 | 04/2025 |
| MySql-connector J | 9.1.0 | 01/2025 |
| commons-codec | 1.18.0 | 04/2025 |
| Maven | 3.9.5 | 11/2023 |
| ActiveMQ (different to server version) | 5.19.0 | 04/2025 |
| Nicos | 23 | 11/2023 |
| Jakarta Activation API | 2.1.2 | 10/2024 |
| Jakarta Mail API | 2.1.3 | 10/2024 |
| Jakarta XML Binding API | 4.0.1 | 10/2024 |
| JavaX Activation | 1.1.1 | 10/2024 |
| joda time | 2.13.1 | 04/2025 |
| py4j | 0.10.9.9 | 04/2025 |
| log4j | 2.24.3 | 04/2025 |
| JAXB | 3.0.2 | 10/2024 |
| Tyrus | 2.2.0 | 10/2024 |
| JacORB OMG API | 3.9 | 10/2024 |
| Mockito Core | 5.16.1 | 04/2025 |
| JeroMQ | 0.6.0 | 10/2024 |
| Nebula | 3.0.0 | 10/2024 |
| CS-Studio | 04/2025 | 04/2025 |
| Pydev | 11.0.3 | 12/2023 |
| Eclipse | 2024-12 | 04/2025 |
| Eclipse Updates| 4.34 | 04/2025 |

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Python | 3.12.9 | 4/2025 |
| matplotlib | 3.10.1 | 10/2024 |
