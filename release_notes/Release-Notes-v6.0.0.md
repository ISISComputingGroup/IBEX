- [Instrument specific changes](Release-Notes-v6.0.0#instrument-specific-changes)
- [Devices](Release-Notes-v6.0.0#devices)
  * [Newly supported devices](Release-Notes-v6.0.0#newly-supported-devices)
  * [Modified devices](Release-Notes-v6.0.0#modified-devices)
  * [Reflectometry server](Release-Notes-v6.0.0#reflectometry-server)
- [Client](Release-Notes-v6.0.0#ibex-client)
  * [Configuration menus](Release-Notes-v6.0.0#configurations)
  * [Other client changes](Release-Notes-v6.0.0#other)
- [genie_python](Release-Notes-v6.0.0#genie_python)
- [Other changes](Release-Notes-v6.0.0#other-1)
- [Dependencies](Release-Notes-v6.0.0#dependencies)
  * [Server dependencies](Release-Notes-v6.0.0#server-dependencies)
  * [Client dependencies](Release-Notes-v6.0.0#gui-dependencies)
  * [genie_python dependencies](Release-Notes-v6.0.0#genie_python-dependencies)

***

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| LARMOR | [#4770](https://github.com/ISISComputingGroup/IBEX/issues/4770) | Patch | Remove code for X-Y beamstop, as this design is no longer in use. |
| GEM | [#4731](https://github.com/ISISComputingGroup/IBEX/issues/4731) | Patch  | Fix bug preventing beamscraper jaws from being set from jaws manager screen |
| HIFI | [#651](https://github.com/ISISComputingGroup/IBEX/issues/651) | Minor | HIFI Cryomag skeleton of IOC/emulator/OPI/tests |
| NIMROD | [#4672](https://github.com/ISISComputingGroup/IBEX/issues/4672) | Patch | NIMROD Jaws Manager - Fixed a number of minor usability issues |

# Devices

### Newly supported devices

| Ticket | Device |
| ------ | ------|
| [#4056](https://github.com/ISISComputingGroup/IBEX/issues/4056) | MKS PR4000B gas panel |
| [#4115](https://github.com/ISISComputingGroup/IBEX/issues/4115) | Oerlikon centre-one pressure gauge |
| [#4011](https://github.com/ISISComputingGroup/IBEX/issues/4011) | Edwards turbo instrument controller |
| [#4680](https://github.com/ISISComputingGroup/IBEX/issues/4680) | TPG361 Single Gauge Pump |
| [#3876](https://github.com/ISISComputingGroup/IBEX/issues/3876) | ICE Dilution fridge |
| [#4838](https://github.com/ISISComputingGroup/IBEX/issues/4838) | Muon zero field system: NI-DAQ magnetometer |
| [#4855](https://github.com/ISISComputingGroup/IBEX/issues/4855) | Muon zero field system: Zero field controller |
| [#5009](https://github.com/ISISComputingGroup/IBEX/issues/5009) | Muon Jaws |

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#4533](https://github.com/ISISComputingGroup/IBEX/issues/4533) | Minor | Jaws | Split jaws so that they could be run across motors |
| [#4636](https://github.com/ISISComputingGroup/IBEX/issues/4636) | Patch | Twincat IOC | Now has standard prefixes for PVs |
| [#4618](https://github.com/ISISComputingGroup/IBEX/issues/4618) | Patch | Attocube | Correctly reports connection errors |
| [#4695](https://github.com/ISISComputingGroup/IBEX/issues/4695) | Patch | Jaws | Copy archive deadbands from underlying motors to jaws. This is necessary to prevent excessive logging on jaw sets with noisy encoders. |
| [#4184](https://github.com/ISISComputingGroup/IBEX/issues/4184) | Patch | HV CAEN | Allow a read-only option for remote monitoring of CAEN crates. |
| [#4348](https://github.com/ISISComputingGroup/IBEX/issues/4348) | Minor | Danfysik | Allow scientists to reset Danfysik interlocks on normal Danfysiks exactly the way it can be done on Riken Danfysik. |
| [#4267](https://github.com/ISISComputingGroup/IBEX/issues/4267) | Minor | Danfysik | Text on the Danfysik OPI now reads "interlock tripped" rather than "interlock" when the interlocks are bad. |
| [#3583](https://github.com/ISISComputingGroup/IBEX/issues/3583) | Minor | Danfysik | Made power indicator more obvious. |
| [#5042](https://github.com/ISISComputingGroup/IBEX/issues/5042) | Minor | Danfysik | Various minor improvements |
| [#4452](https://github.com/ISISComputingGroup/IBEX/issues/4452) | Minor | IPS and ITC503 | Send remote and unlocked before write commands. IPS warns user if in "clamped" state. |
| [#4921](https://github.com/ISISComputingGroup/IBEX/issues/4921) | Minor | Motors | Prevent motor positions being written on IOC init. |
| [#4864](https://github.com/ISISComputingGroup/IBEX/issues/4864) | Minor | Keyence LKG | Hotfixes after testing |
| [#4665](https://github.com/ISISComputingGroup/IBEX/issues/4665) | Minor | LinMot | Create emulator and tests |
| [#4908](https://github.com/ISISComputingGroup/IBEX/issues/4908) | Patch | McLennan | Prevent McLennan motors from redefining position if the motion stops for a reason other than hitting a limit switch |
| [#5028](https://github.com/ISISComputingGroup/IBEX/issues/5028) | Minor | Cryo Valve | Added alarm to pv |
| [#4872](https://github.com/ISISComputingGroup/IBEX/issues/4872) | Minor | Jasco 4180 | Fixed bug when you did not set the flowrate and then started to pump for a given time or volume, the calculation was wrong because of invalid setpoint. Changed it so now the calculation uses the setpoint RBV. |
| [#1286](https://github.com/ISISComputingGroup/IBEX/issues/1286) | Minor | Mercury ITC | Add support for pressure cards. |
| [#5043](https://github.com/ISISComputingGroup/IBEX/issues/5043) | Minor | TDK Lambda Genesys PSU | Power supply can now be calibrated to display field in Gauss. Explicit maximum fields & currents can be provided via configuration macros. |
| [#3850](https://github.com/ISISComputingGroup/IBEX/issues/3850) | Minor | DAQmx (affects muon separator and zero field magnetometer) | Alarms on device are now forwarded to blocks/OPI |
| [#4926](https://github.com/ISISComputingGroup/IBEX/issues/4926) | Patch | Muon ICE fridge | Minor changes to the ICE dilution fridge to fix problems found while testing the IOC on the real hardware. |
| [#4288](https://github.com/ISISComputingGroup/IBEX/issues/4288) | Minor | Oercone | Partial conversion of the oercone ioc to a lua boot script |
| [#4623](https://github.com/ISISComputingGroup/IBEX/issues/4623) | Minor | Attocube | Axis are now powered on when moved and so can recover from hardware reset. |

### Reflectometry server

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#4310](https://github.com/ISISComputingGroup/IBEX/issues/4310) | Minor | Reflectometry: Add option for non-synchronized motor axes |
| [#4322](https://github.com/ISISComputingGroup/IBEX/issues/4322) | Minor | Reflectometry: Changed "MOVE" in PV names to "ACTION" |
| [#4899](https://github.com/ISISComputingGroup/IBEX/issues/4899) | Minor | Remove crash when components start out of the beam |
| [#4588](https://github.com/ISISComputingGroup/IBEX/issues/4588) | Minor | Prevent IOC crash on connection loss |
| [#4127](https://github.com/ISISComputingGroup/IBEX/issues/4127) | Minor | Reflectometry: Server waits for motor IOCs on startup |
| [#4190](https://github.com/ISISComputingGroup/IBEX/issues/4190) | Minor | Reflectometry: beamline message PV changed from string to char array, increasing max message length |
| [#3906](https://github.com/ISISComputingGroup/IBEX/issues/3906) | Minor | Reflectometry: Improved beamline tests |
| [#3892](https://github.com/ISISComputingGroup/IBEX/issues/3892) | Minor | Reflectometry parameters reflect alarms of underlying motors. |
| [#4975](https://github.com/ISISComputingGroup/IBEX/issues/4975) | Minor | Reflectometry: PV Wrapper sets a minimum motor velocity to prevent stalling. |
| [#3904](https://github.com/ISISComputingGroup/IBEX/issues/3904) | Minor | Add put log to Reflectometry IOC. |


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#4239](https://github.com/ISISComputingGroup/IBEX/issues/4239) | Patch | Fix increasing memory usage when repeatedly editing configurations |
| [#2911](https://github.com/ISISComputingGroup/IBEX/issues/2911) | Minor | Changes the text displayed when no blocks in config to instruct users on how to add blocks |
| [#4624](https://github.com/ISISComputingGroup/IBEX/issues/4624) | Minor | Add default values to IOC dialog, if available |
| [#4794](https://github.com/ISISComputingGroup/IBEX/issues/4794) | Minor | Allow configurations and components to be marked as "protected". |
| [#3687](https://github.com/ISISComputingGroup/IBEX/issues/3687) | Minor | Synoptic editor now displays which synoptic is being edited |
| [#4619](https://github.com/ISISComputingGroup/IBEX/issues/4624) | Minor | IBEX GUI: Added coloured border around PVs in the synoptic to indicate alarms |
| [#4904](https://github.com/ISISComputingGroup/IBEX/issues/4904) | Minor | Can save configs with IOC macros set to default  |
| [#4796](https://github.com/ISISComputingGroup/IBEX/issues/4796) | Minor | When in manager mode can edit and delete protected configs. When not in manager mode cannot edit and delete protected configs but can "save as" a new unprotected config based on an old config with a new name. |
| [#5014](https://github.com/ISISComputingGroup/IBEX/issues/5014) | Minor | Banner information is now configurable, slight changes in layout of banner for neutron instruments, muon instruments have different information displayed by default. |
| [#4703](https://github.com/ISISComputingGroup/IBEX/issues/4703) | Minor | When a block goes into alarm run control now stops data collection if last-known-good-value was within run control limits, else it is suspended. There is a new option to suspend data collection for alarmed values, regardless of the last known value. cget returns alarm status of block/pv and prints a warning if in alarm. cshow now prints alarm. Web dashboard blocks display INVALID/LINK_ALARM with link to explanation. GUI now displays invalid blocks with a purple border and the text is "invalid". In an OPI a readback field displays last know good value and has a purple border. Hovering over a readback field will now also display the alarm status. |
| [#4647](https://github.com/ISISComputingGroup/IBEX/issues/4647) | Patch | Fixed bug with reordering blocks in groups |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#3562](https://github.com/ISISComputingGroup/IBEX/issues/3562) | Minor | Added customisable buttons to the GUI banner. |
| [#4140](https://github.com/ISISComputingGroup/IBEX/issues/4140) | Minor | Adding `@block_name@` to a title will automatically fill in the block value. See [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Add-blocks-to-run-title) |
| [#3905](https://github.com/ISISComputingGroup/IBEX/issues/3905) | Minor | When a script is being run on the script server, the script server button on the perspective switcher shows either a pause or play button based on whether or not it is paused, and either flashes green or is highlighted with a steady green when script server is unfocussed, respectively. |
| [#4550](https://github.com/ISISComputingGroup/IBEX/issues/4550) | Minor | Warning when searching to and from dates if to and from inputs are in wrong order |
| [#4668](https://github.com/ISISComputingGroup/IBEX/issues/4668) | Patch | Make OPIs which rely on embedded scripts open significantly faster |
| [#4755](https://github.com/ISISComputingGroup/IBEX/issues/4755) | Minor | Added week view in the IBEX GUI Beam log |
| [#3359](https://github.com/ISISComputingGroup/IBEX/issues/3359) | Minor | Scripts in the script server queue can be dragged and dropped |
| [#4335](https://github.com/ISISComputingGroup/IBEX/issues/4335) | Minor | Added a button to collapse and expand the perspective switcher sidebar to make more space |
| [#4513](https://github.com/ISISComputingGroup/IBEX/issues/4513) | Minor | Fixed bug where trying to connect to a disconnected NICOS script server would cause handle leaks |
| [#4786](https://github.com/ISISComputingGroup/IBEX/issues/4786) | Minor | Adds a git hook which creates a dummy button in all the OPIS to stop them from moving focus. Dummy buttons created on all opis. |
| [#4757](https://github.com/ISISComputingGroup/IBEX/issues/4757) | Minor | Clarify how to set Xpress run RB numbers. |
| [#4166](https://github.com/ISISComputingGroup/IBEX/issues/4166) | Minor | Added data table to script generator and related actions, as well as the ability to drop and rebuild a table for a different action in the code (not the gui). |
| [#4722](https://github.com/ISISComputingGroup/IBEX/issues/4722) | Patch | Fixed deadlock in log plotter after zooming out quickly, which meant that no historic data could be loaded |
| [#4165](https://github.com/ISISComputingGroup/IBEX/issues/4165) | Minor | Script generator now loads it's config from file |
| [#4736](https://github.com/ISISComputingGroup/IBEX/issues/4736) | Patch | Fix CTRL-C no longer killing a script correctly after pressing the reset layout button. |
| [#3773](https://github.com/ISISComputingGroup/IBEX/issues/3773) | Patch | Scripting window no longer appears in non-scripting perspectives when switching rapidly. |
| [#4910](https://github.com/ISISComputingGroup/IBEX/issues/4910) | Minor | Script Generator: Bundle python with GUI |
| [#4168](https://github.com/ISISComputingGroup/IBEX/issues/4168) | Minor | Script generator now checks if parameters are valid and displays to the user if not. Structure also created for script generation in java classes |
| [#4168](https://github.com/ISISComputingGroup/IBEX/issues/4168) | Minor | Script generator is now able to generate python scripts for use in the scripting window |
| [#4774](https://github.com/ISISComputingGroup/IBEX/issues/4774) | Minor | Included tests for blocks panel so that they are run automatically. |
| [#5106](https://github.com/ISISComputingGroup/IBEX/issues/5106) | Minor | Scripting matplotlib window now appears normal on start up, rather than being minimized on the right side.|
| [#5114](https://github.com/ISISComputingGroup/IBEX/issues/5114) | Minor | Script generator now shows help string |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#4547](https://github.com/ISISComputingGroup/IBEX/issues/4547) | Minor | genie_python: `waitfor` checks for completion more frequently, pause, resume and abort no longer wait for state switch, connect to PV uses a different underlying operation to make it faster but no longer processes background tasks in epics.  |
| [#4911](https://github.com/ISISComputingGroup/IBEX/issues/4911) | Minor | Retry indefinitely with error message on cget, cshow, cset, get_sample_pars, set_sample_pars, get_beamline_pars and set_beamline_pars so that if PV does not exist in blockserver command will pause until it is available and contains sensible data. |
| [#4497](https://github.com/ISISComputingGroup/IBEX/issues/4497) | Minor | Genie python waitfor no longer aborts under channel access, prints information to the user when necessary |
| [#4419](https://github.com/ISISComputingGroup/IBEX/issues/4419) | Minor | Split user/developer python. Developer python is now Python 3, and is used by the database server. |
| [#4874](https://github.com/ISISComputingGroup/IBEX/issues/4874) | Patch | Fig bug preventing scripts from being loaded using `g.load_script` after using `from __future__ import unicode literals` in a python session. |
| [#4014](https://github.com/ISISComputingGroup/IBEX/issues/4014) | Minor | genie_python: always return a distribution when getting spectrum data|
| [#4630](https://github.com/ISISComputingGroup/IBEX/issues/4630) | Minor | Lint user scripts on load_script |
| [#4914](https://github.com/ISISComputingGroup/IBEX/issues/4914) | Minor | New waitfor functionality: waitfor_mevent where millions of events are waited for |
| [#4895](https://github.com/ISISComputingGroup/IBEX/issues/4896) | Minor | Genie Python now py2/3 compatible |
| [#4913](https://github.com/ISISComputingGroup/IBEX/issues/4913) | Minor | Refactored how to add hooks in for begin, end etc. See [docs](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Pre-and-Post-Command-Hooks) for details. |
| [#4630](https://github.com/ISISComputingGroup/IBEX/issues/4630) | Minor | Genie python Script Checker Uses pylint to lint a script upon loading
| [#5102](https://github.com/ISISComputingGroup/IBEX/issues/5102) | Minor | Add `quiet` argument to `end()` command

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#4255](https://github.com/ISISComputingGroup/IBEX/issues/4255) | Minor | Update various dependencies for security, performance and functionality patches. Full dependency versions are listed below. |
| [#4599](https://github.com/ISISComputingGroup/IBEX/issues/4599) | Patch | Change build rules to be compatible with a future EPICS 7 migration. |
| [#4694](https://github.com/ISISComputingGroup/IBEX/issues/4694) | Patch | Added tests to confirm that access security on PVs works |
| [#4799](https://github.com/ISISComputingGroup/IBEX/issues/4799) | Minor | Made Beckhoff IOC tests fails with IOError if AutomationTools binary has not been built |
| [#4797](https://github.com/ISISComputingGroup/IBEX/issues/4797) | Minor | Changed DB Server so that now it also creates a PV with information about all LOW Interesting PVs of that instrument, just as it did for high, medium or facility pvs. |
| [#4655](https://github.com/ISISComputingGroup/IBEX/issues/4655) | Minor | Added config checker tests that check how many non interesting PVs have a block on them in any component/configuration of an instrument. |
| [#3125](https://github.com/ISISComputingGroup/IBEX/issues/3125) | Major | Start of remote IOC server, allow IOCs to be run on remote machines but controlled as if they are on an instrument machine. |
| [#4983](https://github.com/ISISComputingGroup/IBEX/issues/4983) | Patch | Update name of EPICS timezone record to be E7 compatible |
| [#5073](https://github.com/ISISComputingGroup/IBEX/issues/5073) | Minor | Alarm Server console level logging is set to INFO instead of FINE so that excessive logging does not fill up disk space on EMU. |
| [#4896](https://github.com/ISISComputingGroup/IBEX/issues/4896) | Minor | Convert JSON bourne (the service responsible for the web dashboard) to Python 3 |
| [#5052](https://github.com/ISISComputingGroup/IBEX/issues/5052) | Minor | Refactor Beckhoff test runner code to be more generic |
| [#5112](https://github.com/ISISComputingGroup/IBEX/issues/5112) | Minor | Changed all links in the GUI to point to internal pages and changed IE on instrument machines to only view internal pages |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### Server dependencies

what | version | where | last updated/checked
---- | ------- | ----- | --------------------
| `EPICS` | 3.15.5 | server (`EPICS\base\master`) | 2018-06-01 (latest stable)
| `git` | 2.19.1-64 | system | -
| `MySQL` | 8.0.19 | system (`C:\Instrument\Apps\MySQL`) | 2020-01
| `MySQL connector/j` | 8.0.17 | server (`EPICS\ISIS\IocLogServer\master`) | 2019-09
| `Java (OpenJDK) JRE` | 1.8 update 222 | system (`C:\Program Files\AdoptOpenJDK`) | 2019-09
| `ActiveMQ` | 5.15.9 | server (`EPICS\ISIS\ActiveMQ\master`) | 2019-09
| `joda-time` | 2.10.3 | server (`EPICS\ISIS\IocLogServer\master`) | 2019-09
| `seq` epics support module | 2.1.21 | EPICS | out of date there is at least 2.2.5 | - 
| `csm` epics support module | 4-3 | EPICS | out of date there is at least 4-4 | - 

### GUI Dependencies

Dependency | Version | last updated/checked
---- | ------- | --------------------
| `Java` | OpenJDK version 11.0.4 | 2019-09 |
| `maven` | 3.6.2 | 2019-09 |
| `Eclipse RCP` | 4.12 | 2019-09 |
| `CS-Studio` | 4.6 | 2019-09 |
| `MySQL connector/j` | 8.0.17 | 2019-09 |
| `py4j` | 0.10.8 | 2019-09 |
| `tycho` | 1.4 | 2019-09 |
| `jeroMQ` | 0.5.1 | 2019-09 |
| `pydev` | 5.9.2 | 2019-09 |
| `opal` | 1.0.0 | See ticket [#3270](https://github.com/ISISComputingGroup/IBEX/issues/3270) |
| `log4j` | 2.3 | 2019-09 |
| `ActiveMQ` | 5.15.9 | 2019-09 |
| `joda-time` | 2.10.3 | 2019-09 |

### genie_python Dependencies

This list can be generated by running `python -m pip freeze`.

```
argh==0.26.2
astroid==1.6.6
backports-abc==0.5
backports.functools-lru-cache==1.6.1
backports.shutil-get-terminal-size==1.0.0
CaChannel==3.1.2
certifi==2019.11.28
chardet==3.0.4
colorama==0.4.3
configparser==4.0.2
contextlib2==0.6.0.post1
coverage==5.0.3
cycler==0.10.0
decorator==4.4.1
dnspython==1.16.0
docopt==0.6.2
docutils==0.16
enum34==1.1.6
funcsigs==1.0.2
future==0.18.2
futures==3.3.0
gitdb2==2.0.6
GitPython==2.1.14
h5py==2.10.0
idna==2.8
ipython==5.8.0
ipython-genutils==0.2.0
isort==4.3.21
Jinja2==2.11.0
json-rpc==1.13.0
kafka-python==1.4.7
kiwisolver==1.1.0
lazy-object-proxy==1.4.3
ldap3==2.6.1
lewis==1.2.1
lxml==4.4.2
MarkupSafe==1.1.1
matplotlib==2.2.4
mccabe==0.6.1
mock==3.0.5
mysql-connector==2.2.9
mysql-connector-python==8.0.19
nicos-pyctl==1.0
numpy==1.16.5
ode==0.15.2
parameterized==0.7.0
pathlib2==2.3.5
pathtools==0.1.2
pcaspy==0.7.2
pdfrw==0.4
pickleshare==0.7.5
Pillow==6.2.2
ply==3.11
prompt-toolkit==1.0.18
protobuf==3.11.2
psutil==5.6.7
py4j==0.10.9
pyasn1==0.4.8
pyepics==3.4.1
pyfits==3.5
pygame==1.9.6
Pygments==2.5.2
PyHamcrest==1.10.1
pylint==1.9.5
PyOpenGL==3.1.5
pyparsing==2.4.6
PyQt4==4.11.4
pyreadline==2.1
pyserial==3.4
python-dateutil==2.8.1
python-redmine==2.2.1
pytz==2019.3
pywin32==218
PyYAML==5.3
pyzmq==18.1.1
reportlab==3.5.34
requests==2.22.0
rsa==4.0
rst2pdf==0.96
scandir==1.10.0
scanf==1.5.2
scipy==1.2.2
semantic-version==2.8.4
simplegeneric==0.8.1
singledispatch==3.4.0.3
six==1.14.0
smartypants==2.0.1
smmap2==2.0.5
stomp.py==4.1.22
tornado==5.1.1
traitlets==4.3.3
Unidecode==1.1.1
unittest-xml-reporting==2.5.2
urllib3==1.25.8
watchdog==0.9.0
wcwidth==0.1.8
win-unicode-console==0.5
wrapt==1.11.2
```
