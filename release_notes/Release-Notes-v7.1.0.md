Note that this is a small release made for cycle 2020/02. Changes from [7.0.0](https://github.com/ISISComputingGroup/IBEX/wiki/Release-Notes-v7.0.0), a much bigger release, have also also been deployed since last cycle.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#5491](https://github.com/ISISComputingGroup/IBEX/issues/5491) | Minor | Add genie python commands to set email or SMS alerts when blocks go in/out of ranges, see [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Alerts-on-Blocks) on how to use |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| SANS2D | [#4559](https://github.com/ISISComputingGroup/IBEX/issues/4559) | Minor | Added gauge controls to Vacuum screen |
| SANS2D | [#4592](https://github.com/ISISComputingGroup/IBEX/issues/4592) | Minor | Added support for scraper aperture |
| SANS2D | [#4568](https://github.com/ISISComputingGroup/IBEX/issues/4568) | Minor | Added OPI for control of aperture and guides |
| SANS2D | [#4568](https://github.com/ISISComputingGroup/IBEX/issues/4577) | Minor | Added OPI for control of vacuum tank |
| SANS2D | [#4590](https://github.com/ISISComputingGroup/IBEX/issues/4590) | Minor | Adds post-begin and pre-end run commands for SANS2D auto-shutter. |

# Devices

### Newly supported devices

| Ticket | Device |
| ------ | ------|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#5326](https://github.com/ISISComputingGroup/IBEX/issues/5326) | Minor | Mezei spin flipper | Tidied up the way it communicates with the device |
| [#5519](https://github.com/ISISComputingGroup/IBEX/issues/5519) | Patch | Galil motion controllers | Reduce polling rate for axes which are not moving, to reduce CPU load. |
| [#5395](https://github.com/ISISComputingGroup/IBEX/issues/5395) | Patch | Jasco 4180 | Fixed issue where sending multiple setpoints in quick succession may not get through to the device |
| [#4594](https://github.com/ISISComputingGroup/IBEX/issues/4594) | Patch | Superlogics | allow disabling channels (for SANS2D detector temperatures) |
| [#1392](https://github.com/ISISComputingGroup/IBEX/issues/1392) | Minor | Mercury ITC | has been converted to a native EPICS driver. This improves the error reporting from the device as well as adding some missing options. The COM port and card locations for the mercury now need to be specified in the configuration (there is a new "system" tab to show which cards are currently present if you are unsure). |

### Reflectometry server

| Ticket | Type | Change |
| ------ | --- | ------------- |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5503](https://github.com/ISISComputingGroup/IBEX/issues/5503) | Patch | Add linux version of the ibex client |

### Script Generator
| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#4172](https://github.com/ISISComputingGroup/IBEX/issues/4172) | Minor | Added functionality for specifying the estimated time for a script (see [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Writing-Script-Definitions) for how to use. |
| [#5348](https://github.com/ISISComputingGroup/IBEX/issues/5348) | Minor | Can now overwrite as well as append parameters from a data file |
| [#5122](https://github.com/ISISComputingGroup/IBEX/issues/5122) | Minor | Allow selecting multiple lines and duplicating/moving/deleting |
| [#5418](https://github.com/ISISComputingGroup/IBEX/issues/5418) | Minor | Add Jenkins stand-alone release pipeline for the script generator|

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5463](https://github.com/ISISComputingGroup/IBEX/issues/5463) | Minor | GUI will now fallback to the bundled Python if the installed Python is not available, making it easier to install the GUI on machines that are not the NDX |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5087](https://github.com/ISISComputingGroup/IBEX/issues/5087) | Minor | Remove the genie_python SECI API |
| [#5555](https://github.com/ISISComputingGroup/IBEX/issues/5555) | Minor | The recommended way to send SMS messages from a script has changed to be in line with the general alert system, see [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Alerts-on-Blocks#sending-alerts-from-scripts) |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5201](https://github.com/ISISComputingGroup/IBEX/issues/5201) | Minor | Added alert on motor details screen if motor and encoder steps go out of sync |
| [#5298](https://github.com/ISISComputingGroup/IBEX/issues/5298) | Minor | Stream live view into Kafka to test ESS datastreaming software |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#4878](https://github.com/ISISComputingGroup/IBEX/issues/4878) | Patch | Run DBUnitChecker under python 3 |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

## Server dependencies

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

## GUI Dependencies

Dependency | Version | last updated/checked
---- | ------- | --------------------
| `Java` | OpenJDK version 11.0.4 | 2020-04 |
| `maven` | 3.6.3 | 2020-04 |
| `Eclipse RCP` | 4.14 | 2020-04 |
| `CS-Studio` | 4.6 | 2020-04 |
| `MySQL connector/j` | 8.0.19 | 2020-04 |
| `py4j` | 0.10.9 | 2020-04 |
| `tycho` | 1.6.0 | 2020-04 |
| `jeroMQ` | 0.5.2 | 2020-04 |
| `pydev` | 7.5.0 | 2020-04 |
| `opal` | 1.0.0 | See ticket [#3270](https://github.com/ISISComputingGroup/IBEX/issues/3270) |
| `log4j` | 2.13 | 2020-04 |
| `ActiveMQ` | 5.15.11 | 2020-04 |
| `joda-time` | 2.10.5 | 2020-04 |

## genie_python Dependencies

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
matplotlib==3.2.2
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

