Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8415](https://github.com/ISISComputingGroup/IBEX/issues/8415) | Minor | `g.load_script` will now apply argument type-checking, via `pyright`, by default. This means that some errors which would previously have been runtime errors will now be caught during the `g.load_script` call. See [Error Checking Troubleshooting](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Error-Checking-Troubleshooting) for more details. Also adds type hinting to public genie-python API functions.|

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |


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


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Bluesky

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
| MySQL | 8.0.35 | ibex_install_utils | 11/2023 |
| Make | 4.4 | utils_win32 | 11/2023 |
| ActiveMQ | 5.18.3 | ISIS\ActiveMQ | 12/2023 |
| Nicos | 23 | ScriptServer | 11/2023 |
| Cygwin | 3.4.9 | ICP_Binaries |	12/2023 |
| MySql-connector J | 8.0.33 | IOCLogServer | 12/2023 |

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Gson | 2.10.1 | 11/2023 |
| MySql-connector J | 8.0.33 | 12/2023 |
| commons-codec | 1.16.0 | 12/2023 |
| Maven | 3.9.5 | 11/2023 |
| ActiveMQ (different to server version) | 5.17.6 | 12/2023 |
| Nicos | 23 | 11/2023 |
| Jakarta Activation API | 2.1.2 | 12/2023 |
| Jakarta Mail API | 2.1.1 | 12/2023 |
| Jakarta XML Binding API | 4.0.1 | 12/2023 |
| JavaX Activation | 1.1.1 | 12/2023 |
| joda time | 2.12.5 | 12/2023 |
| py4j | 0.10.9.7 | 12/2023 |
| log4j | 2.22.0 | 12/2023 |
| JAXB Runtime | 4.0.4 | 12/2023 |
| Tyrus | 2.1.4 | 12/2023 |
| JacORB OMG API | 3.9 | 12/2023 |
| Mockito Core | 5.7.0 | 12/2023 |
| Mockito Inline | 5.2.0 | 12/2023 |
| JeroMQ | 0.5.4 | 12/2023 |
| Nebula | 3.0.0 | 12/2023 |
| CS-Studio | 12/2023 | 12/2023 |
| Pydev | 11.0.3 | 12/2023 |
| Eclipse | 2024-03 | 04/2024 |
| Eclipse Updates| 4.26 | 12/2023 |

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Python | 3.11.6 | 11/2023 |
| ode |	0.16.4 | 11/2023 |
| Lewis | 11/2023 | 11/2023 |
| matplotlib | 3.8.2 | 12/2023 |
