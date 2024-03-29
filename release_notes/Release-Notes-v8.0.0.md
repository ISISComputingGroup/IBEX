Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
|  [#6132](https://github.com/ISISComputingGroup/IBEX/issues/6132) | Major | Removed \Instrument\Apps\Python (Python 2) - Python 3 is now the default version of Python deployed. |
| [#6600](https://github.com/ISISComputingGroup/IBEX/issues/6600) | Major | Removed CHIPIR obselete LVDCOM IOCs | 
| [#6596](https://github.com/ISISComputingGroup/IBEX/issues/6596) | Major | Update stream device to 2.8.20 - reduces excess logging from devices  | 


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| MUSR | [#6360](https://github.com/ISISComputingGroup/IBEX/issues/6360) | Minor | Enabled autosave on ZFCTRL_01 auto-feedback mode so it stays the same despite a config change. |
| INTER | [#6357](https://github.com/ISISComputingGroup/IBEX/issues/6357) | Minor | Add mirror angle dependant correction for sample height |
| WISH | [#6034](https://github.com/ISISComputingGroup/IBEX/issues/6034) | Minor | Add Vacuum PLC OPI |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#6221](https://github.com/ISISComputingGroup/IBEX/issues/6221) | Patch | HIFIMAGS (HiFi Cryomagnet) | Corrected units of max field. Provide feedback on OPI when controls are disabled. Use a cryomagnet icon. |
| [#6286](https://github.com/ISISComputingGroup/IBEX/issues/6286) | Minor | MercuryITC | Fixed timeout issues giving transient invalid blocks. |
| [#6361](https://github.com/ISISComputingGroup/IBEX/issues/6361) | Minor | HIFIMAGS (HiFi Cryomagnet) | OPI created for main SMS cryomagnet. |
| [#6392](https://github.com/ISISComputingGroup/IBEX/issues/6392) | Minor | Sample Changer | Allowed rack name and sample suffix to be different. |
| [#6390](https://github.com/ISISComputingGroup/IBEX/issues/6390) | Minor | GALIL | Fixed race condition in poll() which only showed with new driver. |
| [#6381](https://github.com/ISISComputingGroup/IBEX/issues/6381) | Patch | CRYOSMS | Add option to put with notify to internal database. |
| [#6414](https://github.com/ISISComputingGroup/IBEX/issues/6414) | Minor | SANS Sample Changer | Allow setting arbitrary x/y co-ordinates. |
| [#6409](https://github.com/ISISComputingGroup/IBEX/issues/6409) | Minor | SANS Sample Changer | Allowed selecting positions not in current rack. |
| [#6328](https://github.com/ISISComputingGroup/IBEX/issues/6328) | Minor | ILM200 | Allow use of ILM200 without isobus by setting USE_ISOBUS to No. Defaults to Yes so any current setups of ILM200s are still correct. | 
| [#6403](https://github.com/ISISComputingGroup/IBEX/issues/6403) | Minor | HVCAENx527 | Fix issue with name read now terminating on empty slot |
| [#6442](https://github.com/ISISComputingGroup/IBEX/issues/6442) | Minor | HVCAENx527 | Handle return values from the new version of the CAENHVWrapper library correctly |
| [#6442](https://github.com/ISISComputingGroup/IBEX/issues/6442) | Minor | HVCAENA | Handle return values from the new version of the CAENHVWrapper library correctly |
| [#6484](https://github.com/ISISComputingGroup/IBEX/issues/6484) | Minor | TRITON | Change CHANNEL_POLL_RATE to "10 second" from "15 second" as "15 second" is not a valid value. This does not affect EMU as they have it set to "2 second" which is valid value in globals.txt. |
| [#6383](https://github.com/ISISComputingGroup/IBEX/issues/6383) | Patch | ZFCNTRL | Add macro for auto-saving the feedback mode so if the IOC restarts it will bring the zf system back to whatever mode it was previously in. The default will not do this so will not affect EMU's zero field controller, but will allow MUSR to achieve this via setting the macro to YES. |
| [#5739](https://github.com/ISISComputingGroup/IBEX/issues/5739) | Minor | Mclennan | Fix homing to limits occassionally failing. |
| [#6551](https://github.com/ISISComputingGroup/IBEX/issues/6551) | Minor | Jasco | Do not allow pumping if the concentrations do not equal 100% |
| [#5093](https://github.com/ISISComputingGroup/IBEX/issues/5093) | Minor | Jasco | Add description to the OPI about whether you are pumping |
| [#4681](https://github.com/ISISComputingGroup/IBEX/issues/4681) | Minor | Jasco | Add estimated time/volume for pumping |
| [#4404](https://github.com/ISISComputingGroup/IBEX/issues/4404) | Minor | Jasco | Separate controls into user/advanced on the OPI |
| [#6255](https://github.com/ISISComputingGroup/IBEX/issues/6255) | Minor | GALIL | Preparetary work for updating to new Galil driver |


### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#6393](https://github.com/ISISComputingGroup/IBEX/issues/6393) | Minor | Added virtual "soft" parameters |
| [#6455](https://github.com/ISISComputingGroup/IBEX/issues/6455) | Minor | Fix issue where theta would be in alarm if a long axis was not defined. |
| [#6472](https://github.com/ISISComputingGroup/IBEX/issues/6472) | Minor | Server is less strict about enforcing Z coordinates | 

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6359](https://github.com/ISISComputingGroup/IBEX/issues/6359) | Patch | Enable Scrollbar in components list |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |
| [#6434](https://github.com/ISISComputingGroup/IBEX/issues/6434) | Patch | Renamed "Line" to "Action" in script generator for consistency with buttons |
| [#6402](https://github.com/ISISComputingGroup/IBEX/issues/6402) | Patch | Correct version number for script generator produced by build. |
| [#6478](https://github.com/ISISComputingGroup/IBEX/issues/6478) | Minor | Get script generator version number in standalone UI. |
| [#5616](https://github.com/ISISComputingGroup/IBEX/issues/5616) | Minor | Added abillity to set global parameters on generated scripts. |
| [#4169](https://github.com/ISISComputingGroup/IBEX/issues/4169) | Minor | Queue scripts in the script server directly in the script generator. |
| [#6493](https://github.com/ISISComputingGroup/IBEX/issues/6493) | Minor | Added time & date of last generated script. |
| [#6492](https://github.com/ISISComputingGroup/IBEX/issues/6492) | Minor | Tied together the workflow of generating and loading scripts, removing the confusion of parameters files from the user. |
| [#4170](https://github.com/ISISComputingGroup/IBEX/issues/4170) | Minor | Added ability to preview scripts before sending them to the script server | 
| [#6663](https://github.com/ISISComputingGroup/IBEX/issues/6663) | Patch | Fix script generator build i.e. maven and eclipse |
| [#6593](https://github.com/ISISComputingGroup/IBEX/issues/6593) | Patch | Fix cell focus. |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6450](https://github.com/ISISComputingGroup/IBEX/issues/6450) | Minor | Updated Emma chopper lifter OPI for new chopper |
| [#6486](https://github.com/ISISComputingGroup/IBEX/issues/6486) | Patch | Fix stationary LEDs on motion setpoints and sample changer OPIs |
| [#6506](https://github.com/ISISComputingGroup/IBEX/issues/6506) | Minor | Add default value display to steering magnet OPI  |
| [#6451](https://github.com/ISISComputingGroup/IBEX/issues/6451) | Patch | Fix RB number search by removing GROUP BY statement in query |
| [#6542](https://github.com/ISISComputingGroup/IBEX/issues/6542) | Patch | Fix flashing nicos window |
| [#6202](https://github.com/ISISComputingGroup/IBEX/issues/6202) | Minor | Add OPI and trigger ability for Tektronix AFG3000 series |
| [#6351](https://github.com/ISISComputingGroup/IBEX/issues/6351) | Minor | Stops a Python graphing window from popping up in random perspectives in the GUI |
| [#6573](https://github.com/ISISComputingGroup/IBEX/issues/6573) | Patch | Fix GUI console logs going blank over time |
| [#6488](https://github.com/ISISComputingGroup/IBEX/issues/6488) | Patch | Added message indicating that changes made in run control window can be overwritten by config |
| [#6308](https://github.com/ISISComputingGroup/IBEX/issues/6308) | Minor | Added options to select which config/component a new block gets added to from OPI menu  |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5447](https://github.com/ISISComputingGroup/IBEX/issues/5447) | Minor | Converted genie python to use python built-in logging library and added graylog logger, this should help the dev team to track errors in genie_python across beamlines. |

# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6499](https://github.com/ISISComputingGroup/IBEX/issues/6499) | Minor | Modified set_height functions so that they set the correct height for INTER's naming conventions (but unchanged for other instruments) |
| [#5867](https://github.com/ISISComputingGroup/IBEX/issues/5867) | Minor | Added functionality to execute a scan and write it to a folder that has not been created, they can either create the folder or abort the scan.

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6464](https://github.com/ISISComputingGroup/IBEX/issues/6464) | Minor | Make web dashboard more reliable by adding default unknown options to instrument pvs |
| [#6465](https://github.com/ISISComputingGroup/IBEX/issues/6465) | Patch | Impoved error for no data in database populator, and prevented cyptography failure error |
| [#6511](https://github.com/ISISComputingGroup/IBEX/issues/6511) | Minor | Changed web dashboard to read configuration using EPICS |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#6396](https://github.com/ISISComputingGroup/IBEX/issues/6396) | Patch | Hotfix HRPD, ENGINX and ALF for using :MON: DAE PVs. |
| [#6333](https://github.com/ISISComputingGroup/IBEX/issues/6333) | Patch | Check for IOCs that are not tested in IOC test framework |
| [#6410](https://github.com/ISISComputingGroup/IBEX/issues/6410) | Patch | Accelerator PVs are now read only |
| [#2745](https://github.com/ISISComputingGroup/IBEX/issues/2745) | Patch | Combined DbUnitChecker into DbChecker |
| [#5148](https://github.com/ISISComputingGroup/IBEX/issues/5148) | Patch | Removed ExperimentalDatabase IOC in favour for centrally hosted populator |
| [#4900](https://github.com/ISISComputingGroup/IBEX/issues/4900) | Patch | Converted squish tests to Python 3 |
| [#6256](https://github.com/ISISComputingGroup/IBEX/issues/6256) | Minor | Fix IOC system tests hanging by using the old method of the lewis backdoor |
| [#6560](https://github.com/ISISComputingGroup/IBEX/issues/6560) | Minor | Use separate asyn scan loop for DAE spectra |

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
| `MySQL` | 8.0.25 | system (`C:\Instrument\Apps\MySQL`) | 2021-06
| `MySQL connector/j` | 8.0.25 | server (`EPICS\ISIS\IocLogServer\master`) | 2021-06
| `Java (OpenJDK) JRE` | 11.0.11 | system (`C:\Program Files\AdoptOpenJDK`) | 2021-06
| `ActiveMQ` | 5.16.2 | server (`EPICS\ISIS\ActiveMQ\master`) | 2021-06
| `joda-time` | 2.10.10 | server (`EPICS\ISIS\IocLogServer\master`) | 2021-06
| `seq` epics support module | 2.1.21 | EPICS | out of date there is at least 2.2.5 | - 
| `csm` epics support module | 4-3 | EPICS | out of date there is at least 4-4 | - 
| `asyn` epics support module | 4-38 | EPICS | 2020-02  
| `areaDetector` epics support module | 3-8 | EPICS | 2020-02  
| `sscan` epics support module | 2-11-3 | EPICS | 2020-02  
| `sequencer` epics support module | 2-2-8 | EPICS | 2020-02  

### GUI Dependencies

Dependency | Version | last updated/checked
---- | ------- | --------------------
| `Java` | OpenJDK version 11.0.11 | 2021-06 |
| `maven` | 3.8.1 | 2021-06 |
| `Eclipse RCP` | 4.14 | 2020-04 |
| `CS-Studio` | 4.6 | 2021-06 |
| `MySQL connector/j` | 8.0.21 | 2021-06 |
| `py4j` | 0.10.9.2 | 2021-03-01 |
| `tycho` | 2.3.0 | 2021-06 |
| `jeroMQ` | 0.5.2 | 2020-04 |
| `pydev` | 8.3.0 | 2021-06 |
| `opal` | 1.0.0 | See ticket [#3270](https://github.com/ISISComputingGroup/IBEX/issues/3270) |
| `log4j` | 2.13.3 | 2021-06 |
| `ActiveMQ` | 5.16.2 | 2021-06 |
| `joda-time` | 2.10.6 | 2021-06 |
| `Eclipse SDK` | 4.19 | 2021-06 |

### genie_python Dependencies

Python version: 3.9.5
This list can be generated by running `python -m pip freeze`.

```
astroid==1.6.6
atomicwrites==1.4.0
attrs==20.3.0
backports-abc==0.5
backports.functools-lru-cache==1.6.1
backports.shutil-get-terminal-size==1.0.0
CaChannel==3.1.3
certifi==2020.11.8
chardet==3.0.4
colorama==0.4.4
configparser==4.0.2
contextlib2==0.6.0.post1
coverage==5.3
cycler==0.10.0
decorator==4.4.2
docopt==0.6.2
docutils==0.16
enum34==1.1.10
funcsigs==1.0.2
future==0.18.2
futures==3.3.0
gitdb2==2.0.6
GitPython==2.1.15
h5py==2.10.0
idna==2.10
importlib-metadata==2.1.1
ipython==5.9.0
ipython-genutils==0.2.0
isort==4.3.21
Jinja2==2.11.2
json-rpc==1.13.0
kafka-python==2.0.2
kiwisolver==1.1.0
lazy-object-proxy==1.5.1
ldap3==2.8.1
lewis==1.2.2
lxml==4.6.1
MarkupSafe==1.1.1
matplotlib==2.2.5
mccabe==0.6.1
mock==3.0.5
more-itertools==5.0.0
mysql-connector==2.2.9
mysql-connector-python==8.0.22
nicos-pyctl==1.1
numpy==1.16.6
packaging==20.8
parameterized==0.7.4
pathlib2==2.3.5
pathtools==0.1.2
pcaspy==0.7.3
pdfrw==0.4
pickleshare==0.7.5
Pillow==6.2.2
pluggy==0.13.1
ply==3.11
prompt-toolkit==1.0.18
protobuf==3.14.0
psutil==5.7.3
py==1.10.0
py4j==0.10.9.1
pyasn1==0.4.8
pyepics==3.4.3
pyfits==3.5
pygame==2.0.0
Pygments==2.5.2
PyHamcrest==1.10.1
pylint==1.9.5
PyOpenGL==3.1.5
pyparsing==2.4.7
PyQt4 @ file:///P:/Kits%24/CompGroup/ICP/genie_python_dependencies/PyQt4-4.11.4-cp27-cp27m-win_amd64.whl
pyreadline==2.1
pyserial==3.4
pytest==4.6.11
python-dateutil==2.8.1
python-redmine==2.3.0
pytz==2020.4
pywin32==218
PyYAML==5.3.1
pyzmq==19.0.2
reportlab==3.5.55
requests==2.24.0
rsa==4.5
rst2pdf==0.97
scandir==1.10.0
scanf==1.4.1
scipy==1.2.3
semantic-version==2.8.5
simplegeneric==0.8.1
singledispatch==3.4.0.3
six==1.15.0
smartypants==2.0.1
smmap==3.0.4
smmap2==3.0.1
stomp.py==4.1.23
tornado==5.1.1
traitlets==4.3.3
Unidecode==1.1.1
unittest-xml-reporting==2.5.2
urllib3==1.25.11
watchdog==0.10.3
wcwidth==0.2.5
win-unicode-console==0.5
wrapt==1.12.1
zipp==1.2.0
```
