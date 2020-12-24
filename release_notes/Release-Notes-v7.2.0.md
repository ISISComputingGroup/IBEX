Mostly adding functionality for SANS2D, INTER and POLARIS

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| SANS2D  | [#4585](https://github.com/ISISComputingGroup/IBEX/issues/4585) | Patch | Baffle position controls |
| SANS2D  | [#4583](https://github.com/ISISComputingGroup/IBEX/issues/4583) | Minor | Rear detector beam stops |
| SANS2D  | [#4579](https://github.com/ISISComputingGroup/IBEX/issues/4579) | Minor | Added stop button for motion in vacuum tank |
| SANS2D  | [#4584](https://github.com/ISISComputingGroup/IBEX/issues/4584) | Minor | Rear detector strip beam stop |
| SANS2D  | [#4582](https://github.com/ISISComputingGroup/IBEX/issues/4582) | Minor | Front detector strip beam stop |
| POLARIS | [#5610](https://github.com/ISISComputingGroup/IBEX/issues/5610) | Minor | Fix VNC and clean up disc space |

# Devices

### Newly supported devices

| Ticket | Device |
| ------ | ------|

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#5590](https://github.com/ISISComputingGroup/IBEX/issues/5590) | Minor | CAENV895 | Reset values on config change |
| [#5497](https://github.com/ISISComputingGroup/IBEX/issues/5497) | Minor | MercuryITC | Test new IOC against hardware |

### Reflectometry server

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#5452](https://github.com/ISISComputingGroup/IBEX/issues/5452) | Minor | Add Macros to Reflectometry IOC |
| [#5453](https://github.com/ISISComputingGroup/IBEX/issues/5453) | Minor | Add select engineering correction based on mode |
| [#5455](https://github.com/ISISComputingGroup/IBEX/issues/5455) | Minor | In/out beam parameters can now be set on multiple axes not just position. E.g. Can set an out of beam position on the trans axis. |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5503](https://github.com/ISISComputingGroup/IBEX/issues/5503) | Patch | Add linux version of the ibex client |

### Script Generator
| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5026](https://github.com/ISISComputingGroup/IBEX/issues/5026) | Minor | Script definition saving and bundling |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|[#5509](https://github.com/ISISComputingGroup/IBEX/issues/5509) | Patch | Build and deploy client RPM |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5333](https://github.com/ISISComputingGroup/IBEX/issues/5333) | Helium recovery | Add FINS template specifically for Helium recovery |
| [#5575](https://github.com/ISISComputingGroup/IBEX/issues/5575) | Alerts | Set password and url on instruments |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5573](https://github.com/ISISComputingGroup/IBEX/issues/5573) | Install script | Blocks are now recorded on deploy |


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
| `py4j` | 0.10.9 | 2020-04 |
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
cffi==1.14.1
chardet==3.0.4
colorama==0.4.3
constantly==15.1.0
contextlib2==0.6.0.post1
coverage==5.2.1
cryptography==3.0
cycler==0.10.0
Cython==0.29.21
decorator==4.4.2
docopt==0.6.2
docutils==0.16
entrypoints==0.3
enum34==1.1.10
ess-streaming-data-types==0.9.1
flake8==3.7.9
flatbuffers==1.12
funcsigs==1.0.2
future==0.18.2
futures==3.1.1
gitdb==4.0.5
gitdb2==4.0.2
GitPython==3.1.7
h5py==2.10.0
hyperlink==20.0.1
idna==2.10
incremental==17.5.0
ipython==7.17.0
ipython-genutils==0.2.0
isort==4.3.21
jedi==0.17.2
Jinja2==2.11.2
json-rpc==1.13.0
kafka-python==2.0.1
kiwisolver==1.2.0
lazy-object-proxy==1.4.3
ldap3==2.8
lewis==1.2.2
lxml==4.5.2
MarkupSafe==1.1.1
matplotlib==3.2.2
mccabe==0.6.1
mock==4.0.2
mysql-connector-python==8.0.21
nicos-pyctl==1.1
numpy==1.19.1
ode==0.4.0
parameterized==0.7.4
parso==0.7.1
pathlib2==2.3.5
pathtools==0.1.2
pcaspy==0.7.2
pdfrw==0.4
pickleshare==0.7.5
Pillow==7.2.0
ply==3.11
prompt-toolkit==3.0.6
protobuf==3.6.1
psutil==5.7.2
py4j==0.10.9
pyasn1==0.4.8
pycodestyle==2.5.0
pycparser==2.20
pyepics==3.4.2
pyflakes==2.1.1
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
pyzmq==19.0.2
reportlab==3.5.47
requests==2.24.0
rsa==4.6
rst2pdf==0.97
scandir==1.10.0
scanf==1.4.1
scipy==1.5.2
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
urllib3==1.25.10
watchdog==0.10.3
wcwidth==0.2.5
win-unicode-console==0.5
wrapt==1.12.1
xmlrunner==1.7.7
zope.interface==5.1.0
```
