# Release notes v5.3.0

### Instrument Specific Changes
Changes made for a particular instrument

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| MUONFE | [#3975](https://github.com/ISISComputingGroup/IBEX/issues/3975) | Patch | Add aliases to the Muon front end separator and NGPS iocs for compatibility with the labview wrapper (note: this was patched on MUONFE Feb 2019) |
| LET | [#3738](https://github.com/ISISComputingGroup/IBEX/issues/3738)| Minor | Add support for Mezei spin flipper (note: this was patched on LET Mar 2019). |
| LET | [#3995](https://github.com/ISISComputingGroup/IBEX/issues/3995)| Minor | IPS driver will now report either the persistent or supplied field automatically depending on it's mode (note: this was patched on LET Mar 2019). |
| POLARIS | [#4042](https://github.com/ISISComputingGroup/IBEX/issues/4042)| Minor | Induction furnace: add options to select sample holder and read thermocouple faults (note: this was patched on POLARIS Mar 2019) |

### Devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
|[#3969](https://github.com/ISISComputingGroup/IBEX/issues/3969)|Minor| Moxa ioLogik 12XX | Scaling factor for units is available |
|[#4034](https://github.com/ISISComputingGroup/IBEX/issues/4034)| Minor | Galil motors | Added a De-Energise switch to Motor Details page |
|[#3923](https://github.com/ISISComputingGroup/IBEX/issues/3923)| Minor | JASCO PU-4180 | Added support for JASCO PU-4180 HPLC Pump |
|[#3971](https://github.com/ISISComputingGroup/IBEX/issues/3971)| Patch | Julabo water baths | Add options for hardware & software flow control to be enabled (default is off) |
|[#3781](https://github.com/ISISComputingGroup/IBEX/issues/3781)| Minor | Knauer K-6 | Added support for Knauer Electric Valve Drive K-6 |
|[#4063](https://github.com/ISISComputingGroup/IBEX/issues/4063)| Patch | Keithley 2400 | Minor improvements to user interface. |
|[#4124](https://github.com/ISISComputingGroup/IBEX/issues/4124)| Patch | Spin flipper | Limit amplitude to 3A, and delta T to less than zero. |
| [#2994](https://github.com/ISISComputingGroup/IBEX/issues/2994) | Minor | Keithley 2700| Calculate temperature and drift values |
|[#4028](https://github.com/ISISComputingGroup/IBEX/issues/4028)| Patch | GEM/HRPD/POLARIS sample changer | Add code to recover from dropped sample and sample changer power-cycle. |
|[#3992](https://github.com/ISISComputingGroup/IBEX/issues/3992)| Minor | Lakeshore 340 | Add support for Lakeshore 340 temperature controller. |
|[#4073](https://github.com/ISISComputingGroup/IBEX/issues/4073)| Patch | CAEN HV | Make communications to the CAEN more reliable |

###  IBEX Client

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|[#3986](https://github.com/ISISComputingGroup/IBEX/issues/3986)| Patch | Add beam energy, bunch length and extract delay parameters to beam status view. |
|[#2281](https://github.com/ISISComputingGroup/IBEX/issues/2281)| Minor | Add ability to zoom and set custom scales on detector spectra plots |
|[#3605](https://github.com/ISISComputingGroup/IBEX/issues/3605)| Minor | IOC's auto-start/restart by default when added to a configuration. |
|[#4059](https://github.com/ISISComputingGroup/IBEX/issues/4059)| Minor | Added duplicate PV Values button. |

### Performance

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#3859](https://github.com/ISISComputingGroup/IBEX/issues/3859)| Patch | Adds appropriate memory usage limits to Java processes |
|[#3764](https://github.com/ISISComputingGroup/IBEX/issues/3764)| Minor | IBEX GUI: Fixed bug that resulted slowdown of jaws OPI |
|[#3606](https://github.com/ISISComputingGroup/IBEX/issues/3606)| Minor | Can now view CPU and memory usage of the GUI remotely for debugging purposes |
|[#3877](https://github.com/ISISComputingGroup/IBEX/issues/3877)| Patch | Client will now generate better diagnostic information if it crashes in native code. |

### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#3974](https://github.com/ISISComputingGroup/IBEX/issues/3974)| Patch | Fixed bug where scripts directory was not getting appended to load_script |
|[#3998](https://github.com/ISISComputingGroup/IBEX/issues/3998)| Minor | Send TCPIP command added to genie python |
|[#3953](https://github.com/ISISComputingGroup/IBEX/issues/3953)|Minor| IBEX GUI: During Python console start-up the location of instrument scripts is displayed |
|[#4070](https://github.com/ISISComputingGroup/IBEX/issues/4070)| Patch | Fix issue with keyboard interrupts in python console. |
|[#4152](https://github.com/ISISComputingGroup/IBEX/issues/4152)| Patch | Fix exception when using `g.cset` with keyword arguments. |

### Development & Deployment process

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#3862](https://github.com/ISISComputingGroup/IBEX/issues/3862)| Minor | System Tests: New tests to determine if memory limits reached for large configuration |
|[#4201](https://github.com/ISISComputingGroup/IBEX/issues/4201)| Patch | Fix build failure when `sh.exe` is on the system path |
|[#4248](https://github.com/ISISComputingGroup/IBEX/issues/4248)| Minor | GUI: Fixed build due to CSS repositories becoming incompatible |

### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#3506](https://github.com/ISISComputingGroup/IBEX/issues/3506)| Minor | Update dependencies (`MySQL 8`, `Eclipse 4.8`, `ActiveMQ 5.15.7`, `Tycho 1.2`, `Jacoco 0.8.2`, `JeroMQ 0.5.0`, `PyDev 6.5.0`, `Py4j 0.10.8`, `CS-Studio 4.6`)  |
|[#4070](https://github.com/ISISComputingGroup/IBEX/issues/4070)| Patch | Update various python dependencies: `numpy 1.16.2`, `scipy 1.2.1`, `pcaspy 0.7.1`, `cachannel 3.0.4`, `ipython 5.8`, `watchdog 0.9.0`, `gitpython 2.1.11`, `requests 2.20.1`, `stomp.py 4.1.21` |
|[#3987](https://github.com/ISISComputingGroup/IBEX/issues/3987)| Patch | Beckhoff PLC code build pipeline in Jenkins |
|[3539](https://github.com/ISISComputingGroup/IBEX/issues/3539)| Minor | Reflectometry: When issuing a move, unchanged components will not move. |

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
| `Java JRE` | 1.8.0 update 171 | system | 2018-06-01
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
atomicwrites==1.3.0
attrs==19.1.0
backports-abc==0.5
backports.functools-lru-cache==1.5
backports.shutil-get-terminal-size==1.0.0
CaChannel==3.0.4
certifi==2019.3.9
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
idna==2.7
ipython==5.8.0
ipython-genutils==0.2.0
Jinja2==2.10
json-rpc==1.12.1
kiwisolver==1.0.1
ldap3==2.5.2
lewis==1.2.0
lxml==4.3.2
MarkupSafe==1.1.1
matplotlib==2.2.3
mock==2.0.0
more-itertools==5.0.0
mysql-connector==2.1.6
mysql-connector-python==8.0.15
nicos-pyctl==1.0
numpy==1.16.2
ode==0.15.2
parameterized==0.6.1
pathlib2==2.3.3
pathtools==0.1.2
pbr==5.1.3
pcaspy==0.7.1
pdfrw==0.4
pickleshare==0.7.5
Pillow==5.4.1
pluggy==0.9.0
ply==3.11
prompt-toolkit==1.0.15
protobuf==3.7.0
psutil==5.6.1
py==1.8.0
py4j==0.10.8.1
pyasn1==0.4.5
pyepics==3.3.3
pyfits==3.5
pygame==1.9.4
Pygments==2.3.1
PyHamcrest==1.9.0
PyOpenGL==3.1.0
pyparsing==2.3.1
PyQt4==4.11.4
pyreadline==2.1
pyserial==3.4
pytest==4.3.1
python-dateutil==2.8.0
python-redmine==2.2.1
pytz==2018.9
pywin32==218
PyYAML==5.1
pyzmq==18.0.1
reportlab==3.5.13
requests==2.20.1
rsa==4.0
rst2pdf==0.94
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
Unidecode==1.0.23
unittest-xml-reporting==2.5.0
urllib3==1.24.1
watchdog==0.9.0
wcwidth==0.1.7
win-unicode-console==0.5
```