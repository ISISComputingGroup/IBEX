# Version 5.4.0

### Instrument Specific Changes
Changes made for a particular instrument

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| POLARIS | [#3958](https://github.com/ISISComputingGroup/IBEX/issues/3958) | Minor | IBEX GUI : Polaris: Consolidate GUI into one page, the Jaws Manager. |
| LET | [#4123](https://github.com/ISISComputingGroup/IBEX/issues/4123) | Patch | Astrium Chopper: Mitigated hardware bug in choppers causing chopper phase to be incorrect in some cases. |
| LET | [#4102](https://github.com/ISISComputingGroup/IBEX/issues/4102) | Patch | Fixed Python interpreter crash when `park_choppers` is called |
| RIKENFE | [#4091](https://github.com/ISISComputingGroup/IBEX/issues/4091)| Patch | RIKEN power supplies: Read individual interlocks |
| RIKENFE | [#3490](https://github.com/ISISComputingGroup/IBEX/issues/3490)| Patch | RIKEN power supplies: Read state of RB2 and port 3/4 changeover switches (states now published as `RKNPS_01:RB2:MODE` and `RKNPS_01:PORT3_4:MODE`) |
| LET/MERLIN | [#4027](https://github.com/ISISComputingGroup/IBEX/issues/4027)| Patch | Oscillating collimator does not stop on IOC restarts |

### Devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#3783](https://github.com/ISISComputingGroup/IBEX/issues/3783)| Minor | NIMA Trough | Support added. |
| [#4198](https://github.com/ISISComputingGroup/IBEX/issues/4198) | Minor | JASCO 4180 | Create "User" and "Advanced" panels |
| [#4199](https://github.com/ISISComputingGroup/IBEX/issues/4199) | Minor | JASCO 4180 | Can reset device state remotely |
| [#4284](https://github.com/ISISComputingGroup/IBEX/issues/4284) | Minor | JASCO 4180 | Descriptive string for device status |
|[#4227](https://github.com/ISISComputingGroup/IBEX/issues/4227)| Minor | ITC503 & IPS | Remove "locked" control mode from user interface. |
|[#4103](https://github.com/ISISComputingGroup/IBEX/issues/4103)| Patch | Triton dilution fridge | Now automatically turns closed loop on when sending a temperature setpoint. Add ability to save PID table as part of configuration. |


### genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#4281](https://github.com/ISISComputingGroup/IBEX/issues/4281)| Minor | Genie_python: h5py package added so HDF5 binary data format are readable |


### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[#4266](https://github.com/ISISComputingGroup/IBEX/issues/4266)| Minor | Utilities: error_setter.template remove unused alias |
| [#4279](https://github.com/ISISComputingGroup/IBEX/issues/4279) | Minor | ISISDAE: Added tests for sample parameters |
| [#4083](https://github.com/ISISComputingGroup/IBEX/issues/4083) | Minor | ISISDAE: Changed mechanism for sending sample parameters |
| [#4302](https://github.com/ISISComputingGroup/IBEX/issues/4302) | Minor | `config_env` does not quit if it fails to find programs. |
| [#4110](https://github.com/ISISComputingGroup/IBEX/issues/4110) | Minor | Fixed various bugs where things were not being correctly restarted on config change |
| [#4218](https://github.com/ISISComputingGroup/IBEX/issues/4218) | Patch | Start a limited number of procserv processes on mini-instruments (i.e. instruments that use IBEX iocs under SECI). |
| [#4237](https://github.com/ISISComputingGroup/IBEX/issues/4237) | Minor | Start datastreaming software by default. |

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
h5py==2.9.0
idna==2.7
ipython==5.8.0
ipython-genutils==0.2.0
Jinja2==2.10.1
json-rpc==1.12.1
kafka==1.3.5
kiwisolver==1.1.0
ldap3==2.6
lewis==1.2.0
lxml==4.3.3
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
protobuf==3.7.1
psutil==5.6.2
py4j==0.10.8.1
pyasn1==0.4.5
pyepics==3.3.3
pyfits==3.5
pygame==1.9.6
Pygments==2.4.0
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
PyYAML==5.1
pyzmq==18.0.1
reportlab==3.5.21
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
unittest-xml-reporting==2.5.1
urllib3==1.24.3
watchdog==0.9.0
wcwidth==0.1.7
win-unicode-console==0.5
```