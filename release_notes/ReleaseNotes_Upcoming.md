Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8415](https://github.com/ISISComputingGroup/IBEX/issues/8415) | Minor | `g.load_script` will now apply argument type-checking, via `pyright`, by default. This means that some errors which would previously have been runtime errors will now be caught during the `g.load_script` call. See [Error Checking Troubleshooting](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Error-Checking-Troubleshooting) for more details. Also adds type hinting to public genie-python API functions.|


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| CHIPIR | [Ticket6217](https://github.com/ISISComputingGroup/IBEX/issues/6217#issue-805738735) | Minor | Added OPI support for CHIPIR Filter Set |
| CHIPIR | [Ticket6216](https://github.com/ISISComputingGroup/IBEX/issues/6216) | Minor | Added device screen for CHIPIR XYZ table |
| Muons | [Ticket6232](https://github.com/ISISComputingGroup/IBEX/issues/6232) | Minor | Added muon tpar file text editor/viewer |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#8502](https://github.com/ISISComputingGroup/IBEX/issues/8502) | Danfysik model 8500 | Use `WA` command rather than `DA 0` as per equipment safety note from Danfysik. |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8427](https://github.com/ISISComputingGroup/IBEX/issues/8427) | Minor | Motion controllers | The settings for motor controllers (Galil, Beckhoff, Mclennan, Linmot, SMC100, SM300) have been moved from `c:\instrument\settings\config\<instrument>\configurations\<motor_type>` to `c:\instrument\apps\epics\support\motorExtensions\master\settings\<instrument>\<motor_type>`. This does not affect settings for `motionSetpoints`, which remain in the configurations directory. Settings have been migrated. |
| [Ticket8504](https://github.com/ISISComputingGroup/IBEX/issues/8504) | Motors | Minor | Fix home button showing as disconnected for aliased axes ie. sample changer axes | 
| [Ticket8516](https://github.com/ISISComputingGroup/IBEX/issues/8516) | Lindy IPower Switch | Minor | Add 4 more LNDYISW IOCs | 
| https://github.com/ISISComputingGroup/EPICS-Tektronix_AFG3XXX/pull/4 | Tektronix AFG3XXX | Minor | Add ramp symmetry functionality | 


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
| #8438  | minor | Added Archiver Appliance container implementation and corresponding container gateway in start_gateways.bat |
| #8480  | minor | Added check for repository permissions in repository checks |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8453](https://github.com/ISISComputingGroup/IBEX/issues/8453) | Patch | Build and execute all python-epics wrappers against `epicscorelibs`-provided libraries. No user-facing change. |
| [genie python#8501](https://github.com/ISISComputingGroup/IBEX/issues/8501) | minor | Added optional parameter to wait_for_runstate() to be in agreement with genie_simulate_impl.wait_for_runstate() on the number of positional parameters |
| [ibex_bluesky_core#15](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/15) | Minor | Make `ibex_bluesky_core` available as a dependency, and add automated & manual system tests for bluesky. |
| [#8409](https://github.com/ISISComputingGroup/IBEX/issues/8409) | Minor | Add commands to quickly read and sum event mode spectrum data. |



# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Bluesky

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [ibex_bluesky_core#10](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/10) | Minor | Add block read & write functionality - this allows using an arbitrary block as either a "motor" or "detector" in a scan. |
| [bluesky#8](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/8) | Minor | Expose & document bluesky's plotting functionality. |
| [bluesky#21](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/21) | Minor | Generate & publish uncertainties from DAE Counts data |
| [ibex_bluesky_core#19](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/19) | Major | Introduces fitting for scans in a user friendly way with dynamic guessing functions & new fitting models. |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8438](https://github.com/ISISComputingGroup/IBEX/issues/8438) | minor | Containerised Archiver Appliance and associated new EPICS gateway for local containers |


# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8437](https://github.com/orgs/ISISComputingGroup/projects/20/views/8?pane=issue&itemId=72604908) | Patch | Create a network independant Python venv |


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
| MySql-connector J | 8.4.0 | 10/2024 |
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
| ode |	0.16.4 | 10/2024 |
| Lewis | git | 10/2024 |
| matplotlib | 3.9.2 | 10/2024 |
