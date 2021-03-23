Changes merged into master but not in an official release yet.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#1557](https://github.com/ISISComputingGroup/IBEX/issues/1557) | Minor | genie_python can be switched to a mode where it throw exception instead of just printing them. The user can then choose to catch them in their script. Most of the exceptions thrown are of type Exception, how important is it that this become more targeted? |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| MUSR | [#5955](https://github.com/ISISComputingGroup/IBEX/issues/5955) | Minor | Added CAEN HV power supply status in MuSR rotation OPI and IBEX banner.|
| MUSR | [#5956](https://github.com/ISISComputingGroup/IBEX/issues/5956) | Minor | King Fridge (uDR2) Configuration.|
| MUSR | [#5971](https://github.com/ISISComputingGroup/IBEX/issues/5971) | Minor | Migrating to IBEX |
| DETMON | [#5069](https://github.com/ISISComputingGroup/IBEX/issues/5069) | Minor | Configuration can specify a gwblock.pvlist and block_config.xml, blockserver will start the block gateway and block archiver accordingly |
| HRPD | [#5788](https://github.com/ISISComputingGroup/IBEX/issues/5788) | Minor | Install IBEX on HRPD_SETUP |
| MUSR | [#6112](https://github.com/ISISComputingGroup/IBEX/issues/6112) | Minor | Testing IBEX on MUSR |
| HIFI | [#653](https://github.com/ISISComputingGroup/IBEX/issues/653) | Minor | Addition of Cromagnet Systems IOC (HIFIMAGS) |
| MUSR | [#5957](https://github.com/ISISComputingGroup/IBEX/issues/5957) | Minor | uDR3 and uDR4 Fridge Configurations |
| HIFI | [#6224](https://github.com/ISISComputingGroup/IBEX/issues/6224) | Minor | Label change in HIFIMAGS and adaptations for integration to HIFI |
| MUSR | [#6285](https://github.com/ISISComputingGroup/IBEX/issues/6285) | Minor | Zero field system stability increase (new averaging method) | 

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#6241](https://github.com/ISISComputingGroup/IBEX/issues/6241) | Minor | New IOC to control ITC503 based Heliox |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#5950](https://github.com/ISISComputingGroup/IBEX/issues/5950) | Minor | LKSH340 | Add ability to set excitations on channel A and define temperature setpoint thresholds with corresponding excitation values to set. |
| [#6151](https://github.com/ISISComputingGroup/IBEX/issues/6151) | Minor | KEPCO | Fixed bug where negative currents could not be set. |
| [#6152](https://github.com/ISISComputingGroup/IBEX/issues/6152) | Minor | KEPCO | Fixed bug where two setpoints were sent to the device when a setpoint was set |
| [#6254](https://github.com/ISISComputingGroup/IBEX/issues/6254) | Minor | GALIL | Additional log messages if position redefined |
| [#6314](https://github.com/ISISComputingGroup/IBEX/issues/6314) | Minor | AFG3XXX | Convert to allow testing. |
| [#6198](https://github.com/ISISComputingGroup/IBEX/issues/6198) | Minor | TRITON | Added a set-able poll rate and channel poll rate for the Triton IOC |
| [#6294](https://github.com/ISISComputingGroup/IBEX/issues/6294) | Minor | Rework communications to control ITC503 based Heliox |
| [#6318](https://github.com/ISISComputingGroup/IBEX/issues/6318) | Minor | ICEFRIDGE | Removed support for the ICE dilution fridge, as the hardware is broken long-term. |
| [#6240](https://github.com/ISISComputingGroup/IBEX/issues/6240) | Minor | HLX503 | Add recondensing and other cryogenic control logic. |

### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#5814](https://github.com/ISISComputingGroup/IBEX/issues/5814) | Minor | When starting the server if the component is out of the beam the parameters with no autosave will be set to 0 and a warning will be issued. |
| [#4956](https://github.com/ISISComputingGroup/IBEX/issues/4956) | Minor | Documentation for reflectometry view |
| [#5930](https://github.com/ISISComputingGroup/IBEX/issues/5930) | Minor | Add auto height function in shared scripts |
| [#5899](https://github.com/ISISComputingGroup/IBEX/issues/5899) | Minor | Characteristic values can be defined for a parameter and value of pv is shown in OPI. |
| [#5900](https://github.com/ISISComputingGroup/IBEX/issues/5900) | Minor | Disable axis parameters for components out of beam |
| [#6273](https://github.com/ISISComputingGroup/IBEX/issues/6273) | Minor | Parameter can be configured so that its set point mirrors its readback value; Initial use case is long axis on INTER. |


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5848](https://github.com/ISISComputingGroup/IBEX/issues/5848) | Minor | Matplotlib plot window appears quicker on scan |
| [#5302](https://github.com/ISISComputingGroup/IBEX/issues/5302) | Patch | Prevent error messages from OPIs showing up in a BOY console within the scripting view. |
| [#6244](https://github.com/ISISComputingGroup/IBEX/issues/6244) | Patch | Add device screen for HLX503. |
| [#1478](https://github.com/ISISComputingGroup/IBEX/issues/1478) | Minor | Adding IBEX server status |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |
|[#5968](https://github.com/ISISComputingGroup/IBEX/issues/5968)| Minor | New lines can now inherit default values from the previous line |
|[#5998](https://github.com/ISISComputingGroup/IBEX/issues/5998)| Minor | Lines now have line numbers |
|[#5966](https://github.com/ISISComputingGroup/IBEX/issues/5966)| Minor | New lines can now be inserted part way through the script. Buttons have been reworded to improve clarity. |
|[#6017](https://github.com/ISISComputingGroup/IBEX/issues/6017)| Patch | Bug fix for CopyPreviousRow behaviour when inserting a row. |
|[#5965](https://github.com/ISISComputingGroup/IBEX/issues/5965)| Minor | Allow users to copy and paste rows in script generator, including copying from and to other programs such as Excel.|
|[#5371](https://github.com/ISISComputingGroup/IBEX/issues/5371) | Minor | Rename parameter file extension |
|[#5969](https://github.com/ISISComputingGroup/IBEX/issues/5969) | Minor | Display name of script parameters file being edited |
|[#5970](https://github.com/ISISComputingGroup/IBEX/issues/5970) | Minor | Show a `(*)` next to the script parameters filename if it has unsaved changes |
|[#5938](https://github.com/ISISComputingGroup/IBEX/issues/5938) | Minor | Script generator will first try to load script definitions from `c:\instrument\settings\...`, if that is not present it will fall back to storing definitions next to the executable. |
|[#6204](https://github.com/ISISComputingGroup/IBEX/issues/6204) | Minor | Fix bug where tabbing or copy and pasting when selecting certain cells causes out of bounds exception |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6233](https://github.com/ISISComputingGroup/IBEX/issues/6233) | Minor | Log plotter no longer averages data |
| [#2177](https://github.com/ISISComputingGroup/IBEX/issues/2177) | Minor | Plotting values from an OPI now works without having to modify anything |
| [#5597](https://github.com/ISISComputingGroup/IBEX/issues/5597) | Minor | Scripting toolbar: display active console count when multiple consoles |
| [#2582](https://github.com/ISISComputingGroup/IBEX/issues/2582) | Minor | Blocks can now be added by right clicking on an OPI value |
| [#6296](https://github.com/ISISComputingGroup/IBEX/issues/6296) | Minor | Correct the expected version of the NICOS script server protocol (this stops periodically flashing windows from appearing) |
| [#5373](https://github.com/ISISComputingGroup/IBEX/issues/5373) | Minor | Build MSI install kit |
| [#6305](https://github.com/ISISComputingGroup/IBEX/issues/6305) | Minor | Slit scan in the scans library |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5520](https://github.com/ISISComputingGroup/IBEX/issues/5520) | Minor | Created a linux build for genie_python |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#4897](https://github.com/ISISComputingGroup/IBEX/issues/4897) | Minor | Convert VmsJournalFileConverter to Python3 |
| [#6169](https://github.com/ISISComputingGroup/IBEX/issues/6169) | Minor | Utility script to restore motor positions from the archive |
| [#6121](https://github.com/ISISComputingGroup/IBEX/issues/6121) | Minor | VHDs: get a basic windows installation working and config on git |
| [#5765](https://github.com/ISISComputingGroup/IBEX/issues/5765) | Minor | Web dashboard: remove EMU unneeded alarms, hide empty ("N/A") blocks |
| [#5907](https://github.com/ISISComputingGroup/IBEX/issues/5907) | Minor | Added script to check whether instrument scripts are up to date with remote master |
| [#5373](https://github.com/ISISComputingGroup/IBEX/issues/5373) | Minor | Build MSI install kit |
| [#4646](https://github.com/ISISComputingGroup/IBEX/issues/4646) | Minor | Detect and report unknown/missing default macro values for IOCs |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6162](https://github.com/ISISComputingGroup/IBEX/issues/6162) | Minor | Fix python 2/3 str/bytes bug in blockserver synoptic_manager |
| [#6177](https://github.com/ISISComputingGroup/IBEX/issues/6177) | Minor | Fix system tests for devices with binary interfaces |
| [#5975](https://github.com/ISISComputingGroup/IBEX/issues/5975) | Minor | Muons: Ask Instrument Scientists to Document Tracebacks |
| [#5892](https://github.com/ISISComputingGroup/IBEX/issues/5892) | Minor | Fix slow searching when adding pvs to block |
| [#6165](https://github.com/ISISComputingGroup/IBEX/issues/6165) | Patch | Clean old system test DAE files |
| [#6268](https://github.com/ISISComputingGroup/IBEX/issues/6268) | Patch | GALILMUL: reference code in GALIL to avoid duplication |
| [#5984](https://github.com/ISISComputingGroup/IBEX/issues/5984) | Patch | Upgrade nagios server |
| [#5990](https://github.com/ISISComputingGroup/IBEX/issues/5990) | Minor | Add system tests for danfysik 8500 slew rate |
| [#5414](https://github.com/ISISComputingGroup/IBEX/issues/5414) | Minor | Speed up config checker tests |
| [#4883](https://github.com/ISISComputingGroup/IBEX/issues/4883) | Minor | Convert the collision avoidance monitor into Python 3 |
| [#6289](https://github.com/ISISComputingGroup/IBEX/issues/6289) | Patch | Use local version of Py4J |

# Support Issues Solved

| Ticket | Type  | Change |
| ------ | ------| ------------- |


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
| `Java (OpenJDK) JRE` | 1.8 update 242 | system (`C:\Program Files\AdoptOpenJDK`) | 2020-02
| `ActiveMQ` | 5.15.9 | server (`EPICS\ISIS\ActiveMQ\master`) | 2019-09
| `joda-time` | 2.10.3 | server (`EPICS\ISIS\IocLogServer\master`) | 2019-09
| `seq` epics support module | 2.1.21 | EPICS | out of date there is at least 2.2.5 | - 
| `csm` epics support module | 4-3 | EPICS | out of date there is at least 4-4 | - 
| `asyn` epics support module | 4-38 | EPICS | 2020-02  
| `areaDetector` epics support module | 3-8 | EPICS | 2020-02  
| `sscan` epics support module | 2-11-3 | EPICS | 2020-02  
| `sequencer` epics support module | 2-2-8 | EPICS | 2020-02  

### GUI Dependencies

Dependency | Version | last updated/checked
---- | ------- | --------------------
| `Java` | OpenJDK version 11.0.4 | 2020-04 |
| `maven` | 3.6.3 | 2020-04 |
| `Eclipse RCP` | 4.14 | 2020-04 |
| `CS-Studio` | 4.6 | 2020-04 |
| `MySQL connector/j` | 8.0.19 | 2020-04 |
| `py4j` | 0.10.9.2 | 2021-03-01 |
| `tycho` | 1.6.0 | 2020-04 |
| `jeroMQ` | 0.5.2 | 2020-04 |
| `pydev` | 7.5.0 | 2020-04 |
| `opal` | 1.0.0 | See ticket [#3270](https://github.com/ISISComputingGroup/IBEX/issues/3270) |
| `log4j` | 2.13 | 2020-04 |
| `ActiveMQ` | 5.15.11 | 2020-04 |
| `joda-time` | 2.10.5 | 2020-04 |

### genie_python Dependencies

This list can be generated by running `python -m pip freeze`.

```
2to3==1.0
argh==0.26.2
astroid==2.4.2
astropy==4.0.1.post1
attrs==19.3.0
autobahn==20.7.1
Automat==20.2.0
backcall==0.2.0
backport-ipaddress==0.1
backports-abc==0.5
backports.functools-lru-cache==1.6.1
backports.shutil-get-terminal-size==1.0.0
CaChannel==3.1.2
certifi==2020.6.20
cffi==1.14.0
chardet==3.0.4
colorama==0.4.3
constantly==15.1.0
contextlib2==0.6.0.post1
coverage==5.2
cryptography==2.9.2
cycler==0.10.0
Cython==0.29.21
decorator==4.4.2
docopt==0.6.2
docutils==0.16
enum34==1.1.10
funcsigs==1.0.2
future==0.18.2
futures==3.1.1
gitdb==4.0.5
gitdb2==4.0.2
GitPython==3.1.7
h5py==2.10.0
hyperlink==19.0.0
idna==2.10
incremental==17.5.0
ipython==7.16.1
ipython-genutils==0.2.0
isort==4.3.21
jedi==0.17.2
Jinja2==2.11.2
json-rpc==1.13.0
kafka-python==2.0.1
kiwisolver==1.2.0
lazy-object-proxy==1.4.3
ldap3==2.7
lewis==1.2.2
lxml==4.5.2
MarkupSafe==1.1.1
matplotlib==3.3.0
mccabe==0.6.1
mock==4.0.2
mysql-connector-python==8.0.21
nicos-pyctl==1.1
numpy==1.19.0
ode==0.4.0
parameterized==0.7.4
parso==0.7.0
pathlib2==2.3.5
pathtools==0.1.2
pcaspy==0.7.2
pdfrw==0.4
pickleshare==0.7.5
Pillow==7.2.0
ply==3.11
prompt-toolkit==3.0.5
protobuf==3.6.1
psutil==5.7.2
py4j==0.10.9
pyasn1==0.4.8
pycparser==2.20
pyepics==3.4.2
pygame==1.9.6
Pygments==2.6.1
PyHamcrest==2.0.2
pylint==2.5.3
PyOpenGL==3.1.5
pyparsing==2.4.7
pyreadline==2.1
pyserial==3.4
python-dateutil==2.8.1
python-redmine==2.3.0
pytz==2020.1
pywin32==228
PyYAML==5.3.1
pyzmq==19.0.1
reportlab==3.5.44
requests==2.24.0
rsa==4.6
rst2pdf==0.97
scandir==1.10.0
scanf==1.4.1
scipy==1.5.1
semantic-version==2.8.5
simplegeneric==0.8.1
singledispatch==3.4.0.3
six==1.15.0
smartypants==2.0.1
smmap==3.0.4
smmap2==3.0.1
stomp.py==6.1.0
toml==0.10.1
tornado==6.0.4
traitlets==4.3.3
Twisted==20.3.0
txaio==20.4.1
Unidecode==1.1.1
unittest-xml-reporting==3.0.2
urllib3==1.25.9
watchdog==0.10.3
wcwidth==0.2.5
win-unicode-console==0.5
wrapt==1.12.1
xmlrunner==1.7.7
zope.interface==5.1.0
```
