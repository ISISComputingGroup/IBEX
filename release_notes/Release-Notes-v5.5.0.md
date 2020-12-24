- [Instrument specific changes](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#instrument-specific-changes)
- [Devices](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#devices)
  * [Newly supported devices](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#newly-supported-devices)
  * [Modified devices](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#modified-devices)
  * [Reflectometry server](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#reflectometry-server)
- [Client](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#ibex-client)
  * [Configuration menus](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#configurations)
  * [Other client changes](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#other)
- [genie_python](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#genie_python)
- [Other changes](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#other-1)
- [Dependencies](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0/_edit#dependencies)
  * [Server dependencies](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#server-dependencies)
  * [Client dependencies](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#gui-dependencies)
  * [genie_python dependencies](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v5.5.0#genie_python-dependencies)

***

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| Polaris | [#4079](https://github.com/ISISComputingGroup/IBEX/issues/4079)| Patch | Move configurations to Mk3 Chopper |
| Nimrod | [#4112](https://github.com/ISISComputingGroup/IBEX/issues/4112)| Minor | Added support for NIMROD jaws manager |
| Imat | [#4111](https://github.com/ISISComputingGroup/IBEX/issues/4111)| Patch | Correct OPI for T0 chopper. |
| Emma | [#3751](https://github.com/ISISComputingGroup/IBEX/issues/3751)| Minor | Fermi Chopper Lift OPI: lift movement disabled when chopper levitation complete. |
| Muon front end | [#4160](https://github.com/ISISComputingGroup/IBEX/issues/4160) | Patch | Muon Separator: Prevent stability always reading 5s |
| Muon front end | [#4333](https://github.com/ISISComputingGroup/IBEX/issues/4333) | Minor | Updated overview OPI for new power supplies |

# Devices

### Newly supported devices

| Ticket | Device |
| ------ | ------|
|[#3484](https://github.com/ISISComputingGroup/IBEX/issues/3484)| TPG36X pressure readout |
|[#3720](https://github.com/ISISComputingGroup/IBEX/issues/3720)| Danfysik model 8500 power supply |
| [#3739](https://github.com/ISISComputingGroup/IBEX/issues/3739) |Oxford Instruments Mercury Heliox He3 Fridge |
|[#3787](https://github.com/ISISComputingGroup/IBEX/issues/3787)| Aladdin 1000 Syringe Pump |
|[#3745](https://github.com/ISISComputingGroup/IBEX/issues/3745)| Keyence LK-G positioning sensor |
|[#4038](https://github.com/ISISComputingGroup/IBEX/issues/4038)| Coherent OBIS Laser controller |
| [#3786](https://github.com/ISISComputingGroup/IBEX/issues/3786) | Watson-Marlow 323 Peristaltic pump |
| [#3784](https://github.com/ISISComputingGroup/IBEX/issues/3784) | Thurlby TTI355 power supply |

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
|[#4355](https://github.com/ISISComputingGroup/IBEX/issues/4355)| Minor | Danfysik (calibrated) | Various small bug fixes for calibrated Danfysiks |
|[#4365](https://github.com/ISISComputingGroup/IBEX/issues/4365)| Patch | DAE | Fix deadlock when ending a run. |
|[#4033](https://github.com/ISISComputingGroup/IBEX/issues/4033)| Patch | Oxford Instruments ITC503 | Corrected voltage setpoint to heater percentage setpoint. |
|[#4426](https://github.com/ISISComputingGroup/IBEX/issues/4426)| Patch | Oxford Instruments IPS | Added warning message to OPI if running in non-persistent mode. |
| [#3134](https://github.com/ISISComputingGroup/IBEX/issues/3134) | Minor | Eurotherm | Fix potential issues possibly leading to an accidental ramp. |
| [#3964](https://github.com/ISISComputingGroup/IBEX/issues/3964) | Minor | Eurotherm | OPI redesign to clarify ramp & temperature set-points |
| [#3881](https://github.com/ISISComputingGroup/IBEX/issues/3881) | Minor | Knauer 1050 | Can now pump for a set time/volume or continuously |
| [#3991](https://github.com/ISISComputingGroup/IBEX/issues/3991) | Minor | Beckhoff motors | Added integration tests for beckhoff motion controllers. |
|[#4029](https://github.com/ISISComputingGroup/IBEX/issues/4029)| Minor | JASCO | Explicitly specify calculation method for pump duration/volume in timed mode |


### Reflectometry server

| Ticket | Change |
| ------ | ------------- |
| [#4306](https://github.com/ISISComputingGroup/IBEX/issues/4306) | Theta readback works when there is a detector offset |
| [#4541](https://github.com/ISISComputingGroup/IBEX/issues/4541) | Backlash is now taken into account when calculating move duration |
| [#3533](https://github.com/ISISComputingGroup/IBEX/issues/3533) | Add reflectometry server to IBEX |
| [#3466](https://github.com/ISISComputingGroup/IBEX/issues/3466) | beamline now configures using a python script in root config directory |
| [#3586](https://github.com/ISISComputingGroup/IBEX/issues/3586) | server appears to start and stop, with parameters that are interesting and archived |
| [#4295](https://github.com/ISISComputingGroup/IBEX/issues/4295) | Parameters now have `CHANGING` to indicate their changing status and `RBV:AT_SP` to confirm if a set point target has been reached within tolerance. Support for a visual representation of this has been added to the GUI. |
|[#4045](https://github.com/ISISComputingGroup/IBEX/issues/4045)| Revert motor velocities after move to original values. |
|[#4394](https://github.com/ISISComputingGroup/IBEX/issues/4394)| Do not move parameters not in mode |
|[#4310](https://github.com/ISISComputingGroup/IBEX/issues/4310)| Stop synchronising some axes (Piezo motor speeds) |
|[#3542](https://github.com/ISISComputingGroup/IBEX/issues/3542)| initialise parameter setpoints on IOC startup |
| [#3890](https://github.com/ISISComputingGroup/IBEX/issues/3890) | Disable mode added to unlink components |
| [#3889](https://github.com/ISISComputingGroup/IBEX/issues/3889) | Place components in and out of the beam in the reflectometry server |
|[#4264](https://github.com/ISISComputingGroup/IBEX/issues/4264)| Parameters now displayed in the same order as specified in the config, parameters in mode have an M marker displayed. |
|[#4603](https://github.com/ISISComputingGroup/IBEX/issues/4603)| Cache the velocity to restore in the reflectometry server instead of reading it each time. |
|[#4252](https://github.com/ISISComputingGroup/IBEX/issues/4252)| Setpoint changes on the Jaws IOC do not propagate up to reflectometry parameters. |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|[#3708](https://github.com/ISISComputingGroup/IBEX/issues/3708)| Minor | IBEX GUI: Component IOCs now listed as "in config" in start/stop IOC dialog. |
|[#3778](https://github.com/ISISComputingGroup/IBEX/issues/3778)| Patch | IBEX GUI: Fixed bug where block tool-tips incorrectly displayed "disconnected". |
|[#4414](https://github.com/ISISComputingGroup/IBEX/issues/4414)| Minor | IBEX GUI: Added ability to view configs and components without edit access. |
|[#4346](https://github.com/ISISComputingGroup/IBEX/issues/4346)| Minor | OPI macros now have defaults defined. |
|[#4345](https://github.com/ISISComputingGroup/IBEX/issues/4345)| Minor | Macros in device screens are now editable in the table. |
| [#4202](https://github.com/ISISComputingGroup/IBEX/issues/4202) | Minor | Warning given if an action would result in duplicate IOCs in a configuration. |
| [#4605](https://github.com/ISISComputingGroup/IBEX/issues/4605) | Minor | Switching to a new configuration upon saving it for the first time now works correctly |

### Other client changes

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|[#4406](https://github.com/ISISComputingGroup/IBEX/issues/4406)| Patch | Correct time zone used by log plotter in GUI. |
|[#3416](https://github.com/ISISComputingGroup/IBEX/issues/3416)| Minor | Made two home buttons into one in motor OPI. |
|[#3511](https://github.com/ISISComputingGroup/IBEX/issues/3511)| Minor | Fixed bug with disabled more details button in motor OPI. |
|[#4138](https://github.com/ISISComputingGroup/IBEX/issues/4138)| Minor | IBEX GUI: Made dialogue to display help information and resized About dialogue to fit Java Path. |
|[#4297](https://github.com/ISISComputingGroup/IBEX/issues/4297)| Minor | IBEX GUI: Add TS1 TS2 Beam currents to graph view|
|[#3585](https://github.com/ISISComputingGroup/IBEX/issues/3585)| Minor | IBEX GUI: Graphs now auto-scale once when opened and then do not autoscale again. Blocks can be plotted on existing axes in right click menu. |
|[#2704](https://github.com/ISISComputingGroup/IBEX/issues/2704) and [#2705](https://github.com/ISISComputingGroup/IBEX/issues/2705)| Minor | Added the ability to filter and search the journal table. |
| [#4146](https://github.com/ISISComputingGroup/IBEX/issues/4146) | Patch | Python scripting in GUI: limit output in scripting console to prevent excessive memory use. |
| [#3172](https://github.com/ISISComputingGroup/IBEX/issues/3172) | Minor | Add heartbeat to remaining XYGraphs  |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#3895](https://github.com/ISISComputingGroup/IBEX/issues/3895)| Minor | Added `waitfor_pv` command in `genie_python.advanced` module |
|[#4391](https://github.com/ISISComputingGroup/IBEX/issues/4391)| Patch | Fixed broken autocomplete for load_script method. |
| [#3960](https://github.com/ISISComputingGroup/IBEX/issues/3960) | Minor | `cset`/`cget` issue a warning if block is in alarm |
| [#3688](https://github.com/ISISComputingGroup/IBEX/issues/3688) | Minor | `change_tables` now confirms files exist and have all written correctly, new get_<file_type>_table methods for detector/spectra/wiring |
|[#4308](https://github.com/ISISComputingGroup/IBEX/issues/4308)| Minor | Matplotlib: Old plots are closed when over the limit. |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#4116](https://github.com/ISISComputingGroup/IBEX/issues/4116)| Patch | Asking an IOC to stop twice quickly now actually stops it rather than restarting |
|[#4402](https://github.com/ISISComputingGroup/IBEX/issues/4402)| Minor | Fixed RB number populator pushing to database|
|[#4435](https://github.com/ISISComputingGroup/IBEX/issues/4435)| Minor | Add serial port test tool |
|[#4435](https://github.com/ISISComputingGroup/IBEX/issues/4435)| Minor | Fix an infrequent issue with MOXA ports becoming "stuck" causing devices to no longer communicate. |
| [#2669](https://github.com/ISISComputingGroup/IBEX/issues/2669) | Major | Centralised the way data is pushed to the instrument experiment users database. |
| [#2788](https://github.com/ISISComputingGroup/IBEX/issues/2788) | Patch | Fixed logging IOC messages to have correct time |
| [#4347](https://github.com/ISISComputingGroup/IBEX/issues/4347) | Patch | Only forward neutron data to kafka on real instruments |
| [#4408](https://github.com/ISISComputingGroup/IBEX/issues/4408) | Minor | Experiment database populator: reduced calls to BusApps. |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### Server dependencies

what | version | where | last updated/checked
---- | ------- | ----- | --------------------
| `EPICS` | 3.15.5 | server | 2018-06-01 (latest stable)
| `git` | 2.19.1-64 | system | -
| `MySQL` | 8.0.15.0 | system | 2019-03-18
| `MySQL connector/j` | 5.1.46 | EPICS\ISIS\IocLogServer | 2018-06-01
| `Java (OpenJDK) JRE` | 1.8 update 212 | system | 2019-08-09
| `ActiveMQ` | 5.15.7 | server | 2019-03-18
| `joda-time` | 2.10 | server | 2018-06-01
| `commons-codec`  | 1.11  | server | 2018-06-01
| `seq` epics support module | 2.1.21 | EPICS | out of date there is at least 2.2.5 | - 
| `csm` epics support module | 4-3 | EPICS | out of date there is at least 4-4 | - 

### GUI Dependencies

Dependency | Version | last updated/checked
---- | ------- | --------------------
| `Java` | OpenJDK version 1.8.0_202 | March 2019 |
| `Eclipse RCP` | 4.8 | March 2019 |
| `CS-Studio` | 4.6 | March 2019 |
| `MySQL connector/j` | 5.1.46 | March 2019 |
| `py4j` | 0.10.8 | March 2019 |
| `tycho` | 1.2 | March 2019 |
| `jeroMQ` | 0.5.0 | March 2019 |
| `jacoco` | 0.8.2 | March 2019 |
| `pydev` | 6.5.0 | March 2019 |
| `opal` | 1.0.0 | see ticket  #3270 |
| `log4j` | 2.3 | 2018-06-01 |
| `ActiveMQ` | 5.15.7 | March 2019 |
| `joda-time` | 2.10 | 2018-06-01 |
| `commons-codec` | 1.11 | 2018-06-01 |

### genie_python Dependencies

This list can be generated by running `python -m pip freeze`.

```
argh==0.26.2
backport-ipaddress==0.1
backports-abc==0.5
backports.functools-lru-cache==1.5
backports.shutil-get-terminal-size==1.0.0
CaChannel==3.0.4
certifi==2019.6.16
chardet==3.0.4
colorama==0.4.1
contextlib2==0.5.5
coverage==4.5.3
cycler==0.10.0
decorator==4.4.0
docopt==0.6.2
docutils==0.14
enum34==1.1.6
funcsigs==1.0.2
futures==3.2.0
gitdb2==2.0.5
GitPython==2.1.11
h5py==2.9.0
idna==2.7
ipython==5.8.0
ipython-genutils==0.2.0
Jinja2==2.10.1
json-rpc==1.12.1
kafka-python==1.4.6
kiwisolver==1.1.0
ldap3==2.6
lewis==1.2.0
lxml==4.3.4
MarkupSafe==1.1.1
matplotlib==2.2.3
mock==3.0.5
mysql-connector==2.2.9
mysql-connector-python==8.0.16
nicos-pyctl==1.0
numpy==1.16.2
ode==0.15.2
parameterized==0.6.1
pathlib2==2.3.3
pathtools==0.1.2
pcaspy==0.7.1
pdfrw==0.4
pickleshare==0.7.5
Pillow==6.0.0
ply==3.11
prompt-toolkit==1.0.16
protobuf==3.8.0
psutil==5.6.3
py4j==0.10.8.1
pyasn1==0.4.5
pyepics==3.4.0
pyfits==3.5
pygame==1.9.6
Pygments==2.4.2
PyHamcrest==1.9.0
PyOpenGL==3.1.0
pyparsing==2.4.0
PyQt4==4.11.4
pyreadline==2.1
pyserial==3.4
python-dateutil==2.8.0
python-redmine==2.2.1
pytz==2019.1
pywin32==218
PyYAML==5.1.1
pyzmq==18.0.1
reportlab==3.5.23
requests==2.20.1
rsa==4.0
rst2pdf==0.94.1
scandir==1.10.0
scanf==1.5.2
scipy==1.2.1
semantic-version==2.6.0
simplegeneric==0.8.1
singledispatch==3.4.0.3
six==1.12.0
smartypants==2.0.1
smmap2==2.0.5
stomp.py==4.1.21
tornado==5.1.1
traitlets==4.3.2
Unidecode==1.1.1
unittest-xml-reporting==2.5.1
urllib3==1.24.3
watchdog==0.9.0
wcwidth==0.1.7
win-unicode-console==0.5
```
