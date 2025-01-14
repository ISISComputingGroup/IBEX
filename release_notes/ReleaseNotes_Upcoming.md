Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8415](https://github.com/ISISComputingGroup/IBEX/issues/8415) | Minor | `g.load_script` will now apply argument type-checking, via `pyright`, by default. This means that some errors which would previously have been runtime errors will now be caught during the `g.load_script` call. See [Error Checking Troubleshooting](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Error-Checking-Troubleshooting) for more details. Also adds type hinting to public genie-python API functions.|
| [#8588](https://github.com/ISISComputingGroup/IBEX/issues/8588) | Minor | Previously ibex created many `procServ` processes in the background that managed start/stop and logging of each IOC, including ones fro IOCs that were never used. These are now created on demand which shoudld reduce the overall ibex memory footprint |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Minor | The `genie_python` library has been split out into a [pip-installable package](https://pypi.org/project/genie-python/). There are no direct user-facing changes to `genie_python` as a result of this change, but it is now possible to depend on `genie_python` in downstream libraries and to install the `genie_python` library into environments other than IBEX via `pip`. |
| [#6510](https://github.com/ISISComputingGroup/IBEX/issues/6510) | Minor | Remove `genie_mantid` script in favour of `pip install`ing the above `genie` package. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| CHIPIR | [Ticket6217](https://github.com/ISISComputingGroup/IBEX/issues/6217#issue-805738735) | Minor | Added OPI support for CHIPIR Filter Set |
| CHIPIR | [Ticket6216](https://github.com/ISISComputingGroup/IBEX/issues/6216) | Minor | Added device screen for CHIPIR XYZ table |
| Muons | [Ticket6232](https://github.com/ISISComputingGroup/IBEX/issues/6232) | Minor | Added muon tpar file text editor/viewer |
| HiFi | [Ticket6086](https://github.com/ISISComputingGroup/IBEX/issues/6086) | Minor | Added an OPI for the Hifi Magnet powersupplies |
| HiFi | [Ticket8332](https://github.com/ISISComputingGroup/IBEX/issues/8332) | Minor | Added an OPI for the Hifi Litron Laser Front Panel VI |
| HiFi | [Ticket6090](https://github.com/ISISComputingGroup/IBEX/issues/6090) | Minor | Added an OPI for Hifi Litron Laser Timing Control & extended DG645 IOC | 
| HiFI | [Ticket8403](https://github.com/ISISComputingGroup/IBEX/issues/8403) | Patch | Increase minimum precision that the cryosms driver can send to the power supply. |
# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#8502](https://github.com/ISISComputingGroup/IBEX/issues/8502) | Danfysik model 8500 | Use `WA` command rather than `DA 0` as per equipment safety note from Danfysik. |
| [#6085](https://github.com/ISISComputingGroup/IBEX/issues/6085) | Thorlabs FW102C | Six position filter wheel controller |
| [#8400](https://github.com/ISISComputingGroup/IBEX/issues/8400) | Group3 Hall probe | Hall probe used by zero-field system on HIFI |
| [#8331](https://github.com/ISISComputingGroup/IBEX/issues/8331) | New Focus Intelligent Picometer | Motor used to control Litron Laser Power on HIFI. |
| [#8413](https://github.com/ISISComputingGroup/IBEX/issues/8413) | Anton-Paar L-DENS 3300 Density sensor | Density meter used by reflectometry instruments. | 
| [#8403](https://github.com/ISISComputingGroup/IBEX/issues/8403) | HIFI Zero-field system | Zero-field system used on HIFI. | 


### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [inst_servers#400](https://github.com/ISISComputingGroup/EPICS-inst_servers/pull/400) | Collision Avoidance Monitor | Remove the collision avoidance monitor. |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8160](https://github.com/ISISComputingGroup/IBEX/issues/8160) | minor | Beckhoff/TwinCAT | Allow 2 instances of the TC IOC, for portable beckhoffs |
| [#8104](https://github.com/ISISComputingGroup/IBEX/issues/8104) | minor | PACE5000 | Various PACE5000 snags - set units to bar, slew mode to lin, display source pressure, fix vent status |
| [#8218](https://github.com/ISISComputingGroup/IBEX/issues/8218) | minor | GALIL |  allow COM in GALILADDR macro |
| [#7677](https://github.com/ISISComputingGroup/IBEX/issues/7677) | minor | Tektronix AFG3XXX | Channel 1 and 2 are configurable in IOC macros, by default both are enabled just like so far. |
| [#8248](https://github.com/ISISComputingGroup/IBEX/issues/8248) | minor | Lakeshore 340 | Lakeshore no longer sets excitiation threshold with potentially invalid values on startup. |
| [#6854](https://github.com/ISISComputingGroup/IBEX/issues/6854) | major | Beckhoff/TwinCAT | Remove old CRISP course jaw tcioc motor record code |
| [#8175](https://github.com/ISISComputingGroup/IBEX/issues/8175) | minor | needlevalve | Add macro to govern wriet mode toggle. |
| [#8262](https://github.com/ISISComputingGroup/IBEX/issues/8262) | minor | Keithley 2400 | Add input fields for compliance voltage and current. |
| [#8284](https://github.com/ISISComputingGroup/IBEX/issues/8284)| minor | McLennan | Add macro to set access group of JVEL, HLM, LLM to allow setting of those fields without restart of IOC |
| [#8322](https://github.com/ISISComputingGroup/IBEX/issues/8322)| minor | HVCAEN | Fix issue with write records not getting created | 
| [#8253](https://github.com/ISISComputingGroup/IBEX/issues/8253)| minor | McLennan | Make paramters last a powercycle. Parameters are now saved on homing of device |
| [#8335](https://github.com/ISISComputingGroup/IBEX/issues/8335)| minor | Beckhoff/TwinCAT | Fix issue with table of motors advanced view with energised icon not working | 
| [#8310](https://github.com/ISISComputingGroup/IBEX/issues/8310)| minor | Eurotherm | Fix issue where disconnected/missing Eurotherm causes other Eurotherms to fail to be read |
| [#8427](https://github.com/ISISComputingGroup/IBEX/issues/8427) | Minor | Motion controllers | The settings for motor controllers (Galil, Beckhoff, Mclennan, Linmot, SMC100, SM300) have been moved from `c:\instrument\settings\config\<instrument>\configurations\<motor_type>` to `c:\instrument\apps\epics\support\motorExtensions\master\settings\<instrument>\<motor_type>`. This does not affect settings for `motionSetpoints`, which remain in the configurations directory. Settings have been migrated. |
| [Ticket8504](https://github.com/ISISComputingGroup/IBEX/issues/8504) | Motors | Minor | Fix home button showing as disconnected for aliased axes ie. sample changer axes | 
| [Ticket8516](https://github.com/ISISComputingGroup/IBEX/issues/8516) | Lindy IPower Switch | Minor | Add 4 more LNDYISW IOCs | 
| https://github.com/ISISComputingGroup/EPICS-Tektronix_AFG3XXX/pull/4 | Tektronix AFG3XXX | Minor | Add ramp symmetry functionality | 
| [Ticket8551](https://github.com/ISISComputingGroup/IBEX/issues/8551) | Galil | Minor | (new galil driver) set homing to be allowed in both directions by default | 
| [Ticket8524](https://github.com/ISISComputingGroup/IBEX/issues/8524) | Galil | Minor | (new galil driver) notify users of disconnection at startup and during running | 

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
| [#8181](https://github.com/ISISComputingGroup/IBEX/issues/8181) | Minor | Added purge functioanlity (buttons, LEDs, etc) to PEARLPC OPI |

# Python

### `genie_python`

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [genie python#8501](https://github.com/ISISComputingGroup/IBEX/issues/8501) | minor | Added optional parameter to wait_for_runstate() to be in agreement with genie_simulate_impl.wait_for_runstate() on the number of positional parameters |
| [#8359](https://github.com/ISISComputingGroup/IBEX/issues/8359)| Minor | Added wrapper for P4P to allow use of pv access as well as channel access in genie python. |
| [#8409](https://github.com/ISISComputingGroup/IBEX/issues/8409) | Minor | Add commands to quickly read and sum event mode spectrum data. |
| [#8579](https://github.com/ISISComputingGroup/IBEX/issues/8579) | Patch | Hide messages of the form `CAERROR: ...` which could show up in console. |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Minor | The back-end mechanism for sending sms/email/slack alerts via `g.send_sms` and `g.send_email` was updated to share a mechanism with other IBEX alerting mechanisms. These functions will no longer work on machines outside the ISIS network, or on IBEX installations which have not been configured to send alerts (all instrument machines have been configured to send alerts). |

### Bluesky

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [ibex_bluesky_core#15](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/15) | Minor | Make `ibex_bluesky_core` available as a dependency, and add automated & manual system tests for bluesky. |
| [ibex_bluesky_core#10](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/10) | Minor | Add block read & write functionality - this allows using an arbitrary block as either a "motor" or "detector" in a scan. |
| [ibex_bluesky_core#8](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/8) | Minor | Expose & document bluesky's plotting functionality. |
| [ibex_bluesky_core#21](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/21) | Minor | Generate & publish uncertainties from DAE Counts data |
| [ibex_bluesky_core#19](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/19) | Major | Introduces fitting for scans in a user friendly way with dynamic guessing functions & new fitting models. |

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8453](https://github.com/ISISComputingGroup/IBEX/issues/8453) | Patch | Build and execute all python-epics wrappers against `epicscorelibs`-provided libraries. No user-facing change. |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Patch | Python bindings to the Open Dynamics Engine (`pyode`) were removed. A deprecated version of `pyreadline` bindings were removed. |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8438](https://github.com/ISISComputingGroup/IBEX/issues/8438) | minor | Containerised Archiver Appliance and associated new EPICS gateway for local containers |


# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8437](https://github.com/orgs/ISISComputingGroup/projects/20/views/8?pane=issue&itemId=72604908) | Patch | Create a network independant Python venv |
| [#8593](https://github.com/ISISComputingGroup/IBEX/issues/8593)) | Patch | Stop log file output getting garbled if ioc restarted via console command |


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
