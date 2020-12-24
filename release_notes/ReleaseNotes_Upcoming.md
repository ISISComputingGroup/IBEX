Changes merged into master but not in an official release yet.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#4792](https://github.com/ISISComputingGroup/IBEX/issues/4792) | Minor | Print error details when ICP run fails with g.begin(); but does not continue to next line of script. This has caused lost time before because users have assumed that it is setting up and left it. Fix the problem in the error and begin the run and the script will continue. |
| [#5717](https://github.com/ISISComputingGroup/IBEX/issues/5717) | Patch | An issue causing IOCs to hang on all instruments every 49.7 days, requiring an IBEX restart to recover, has been fixed. |
| [#5380](https://github.com/ISISComputingGroup/IBEX/issues/5380) | Minor | genie_python: Added an easy way to switch on/off simulation mode so that you can easily test scripts, see [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Simulating-Scripts) |
| [#5410](https://github.com/ISISComputingGroup/IBEX/issues/5410) | Minor | Allow users to define arbitrary python functions against user PVs and hence run a script from an OPI or the banner. |
| [#4573](https://github.com/ISISComputingGroup/IBEX/issues/4573) | Major | Added the ability to set motion set points for >2 dimensions and so implemented preset positions for the SANS2D waveguides and apertures. Required major re-write of motion set points in general. | Requires changes to anywhere motionSetPoints are currently used, see [wiki](https://github.com/ISISComputingGroup/ibex_developers_manual/wiki/Motion-Set-points#upgrading-from-720)
| [#3185](https://github.com/ISISComputingGroup/IBEX/issues/3185) | Minor | On the KEPCO an ability to set device into remote mode through reset and reapplying setpoints. Whether this happens depends on configuration can be don't, if firmware <2 and always; default is don't, request us to do this if wanted. Also a button on the OPI. |
| [#5296](https://github.com/ISISComputingGroup/IBEX/issues/5296) | Minor | On a Danfysik the polarity is set by using a negative set point not by setting the polarity except for the Riken power supply chains. |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| NIMROD | [#5622](https://github.com/ISISComputingGroup/IBEX/issues/5622) | Patch | Fix can't see data files |
| POLREF | [#5465](https://github.com/ISISComputingGroup/IBEX/issues/5465) | Patch | Install IBEX on POLREF |
| SANS2D | [#5602](https://github.com/ISISComputingGroup/IBEX/issues/5602) | Minor | Migrate galil homing routines from SECI |
| SANS2D | [#4587](https://github.com/ISISComputingGroup/IBEX/issues/4587) | Minor | Collision avoidance for components in the vacuum tank has been added. Motors will be stopped if any component is too close and getting closer. There is an override. |
| MARI | [#5741](https://github.com/ISISComputingGroup/IBEX/issues/5741) | Patch | Fix sample changer positions, 2 and 4 swapped. Custom homing routine script created. Ticket [#5729](https://github.com/ISISComputingGroup/IBEX/issues/5729) will make a permanent fix. |
| SANS2D | [#5968](https://github.com/ISISComputingGroup/IBEX/issues/5698) | Minor | Migrate instrument scripts |
| SANS2D | [#5735](https://github.com/ISISComputingGroup/IBEX/issues/5735) | Minor | Decelerate faster for collision avoidance |
| NIMROD | [#5494](https://github.com/ISISComputingGroup/IBEX/issues/5494) | Minor | Add ability to limit temperature of TiZr cell based on pressure |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#5546](https://github.com/ISISComputingGroup/IBEX/issues/5546) | Little blue cryostat | Mercury now supports the little blue cryostat in flow mode. The pressure is controlled by temperature and temperature set point. |
| [#5688](https://github.com/ISISComputingGroup/IBEX/issues/5688) | Newport XPS | Motor controller for use on Larmor |

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#5609](https://github.com/ISISComputingGroup/IBEX/issues/5609) | Minor | Caen V895 | Fix an issue with sending saved threshold values on IOC start |
| [#4711](https://github.com/ISISComputingGroup/IBEX/issues/4711) | Minor | Separator | Separator stability reads with text labels instead of int |
| [#5752](https://github.com/ISISComputingGroup/IBEX/issues/5752) | Minor | DAQmx | Now reconnects if network is lost whilst in monster mode |
| [#5782](https://github.com/ISISComputingGroup/IBEX/issues/5782) | Minor | ITC502 | Add set point for heater voltage maximum |
| [#5624](https://github.com/ISISComputingGroup/IBEX/issues/5624) | Minor | CAENv895 | Initialisation done through vme config load from a defaults file. Race condition in autosave has been removed by using config menu explicitly. |
| [#5720](https://github.com/ISISComputingGroup/IBEX/issues/5720) | Minor | SampleChanger | Modified the sample changer to allow selecting which sample changer you have and then building up a set of positions for it. This is in preparation for harmonising the sample changer across SANS instruments. |
| [#5336](https://github.com/ISISComputingGroup/IBEX/issues/5336) | Minor | LSI Correlator | Added macros and tests for the LSI correlator. |
| [#3185](https://github.com/ISISComputingGroup/IBEX/issues/3185) | Minor | KEPCO | Ability to set device into remote mode through reset and reapplying setpoints. Whether this happens depends on configuration can be don't, if firmware <2 and always; default is don't, request us to do this if wanted. Also a button on the OPI. |
| [#5661](https://github.com/ISISComputingGroup/IBEX/issues/5661) | Minor | KEPCO | Added ramping capability in KEPCO IOC |
| [#5259](https://github.com/ISISComputingGroup/IBEX/issues/5259) | Minor | CRYOSMS | Ramps field using steps from the config file |
| [#5662](https://github.com/ISISComputingGroup/IBEX/issues/5662) | Minor | KEPCO | Add ability to use calibration files with KEPCO for magnetic fields |
| [#5839](https://github.com/ISISComputingGroup/IBEX/issues/5839) | Minor | ILM200 | Correct alarms on RATE:ASSERT, LEVEL and VERSION |
| [#5840](https://github.com/ISISComputingGroup/IBEX/issues/5840) | Minor | ILM200 | Up reply and other timeouts to reduce zero readings and flickering alarms |
| [#4704](https://github.com/ISISComputingGroup/IBEX/issues/4704) | Minor | EDNEXT | Remove/disable EDNEXT, EDITC is the ioc to use |


### Reflectometry server

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#5477](https://github.com/ISISComputingGroup/IBEX/issues/5477) | Minor | Update OPI to display more parameters because of the number on POLREF |
| [#5541](https://github.com/ISISComputingGroup/IBEX/issues/5541) | Minor | Limit bench slide position based on min/max bench angle |
| [#5742](https://github.com/ISISComputingGroup/IBEX/issues/5742) | Minor | On parameter change just see if update is needed to parameter PVs thus speeding up the IOC. |
| [#5798](https://github.com/ISISComputingGroup/IBEX/issues/5798) | Minor | Split up OPI to increase performance |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#4800](https://github.com/ISISComputingGroup/IBEX/issues/4800) | Minor | Added description column to config/component dialog lists |
| [#5841](https://github.com/ISISComputingGroup/IBEX/issues/5841) | Patch | Matplotlib plots will automatically periodically reload to avoid an issue with the display freezing. |
| [#4334](https://github.com/ISISComputingGroup/IBEX/issues/4334) | Minor | Removal of config description length limiter |

### Script Generator
| Ticket | Type  | Change |
| ------ | ---- | ----------- |
|[#5968](https://github.com/ISISComputingGroup/IBEX/issues/5968)| Minor  | New lines can now inherit default values from the previous line |
|[#5998](https://github.com/ISISComputingGroup/IBEX/issues/5998)| Minor  | Lines now have line numbers |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5591](https://github.com/ISISComputingGroup/IBEX/issues/5591) | Patch | Update python scripting path so it only using python3. |
| [#5625](https://github.com/ISISComputingGroup/IBEX/issues/5625) | Minor | Motor disconnected Scraper Aperture fixed, Pillar OPI in Vacuum Tank unit changed from mm to degree, Vacuum status on Scraper Aperture removed, All the apertures and guides fits into the OPI without scrolling, minor typos fixed SANS2D Opi
| [#4479](https://github.com/ISISComputingGroup/IBEX/issues/4479) | Minor | Improved the Journal Viewer page control by replacing the spinner with more intuitive navigation elements|
| [#5924](https://github.com/ISISComputingGroup/IBEX/issues/5924) | Minor | Made gateway more intelligently filter incoming PV requests |
| [#5062](https://github.com/ISISComputingGroup/IBEX/issues/5062) | Minor | Hide load config warning message when no protected config |
| [#5488](https://github.com/ISISComputingGroup/IBEX/issues/5488) | Minor | Made setting bump stop up more configurable |

# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5674](https://github.com/ISISComputingGroup/IBEX/issues/5674) | Minor | Raise an error when attempting to set a PV which has `DISP` set, as these sets will not work and previously failed silently. |
| [#5776](https://github.com/ISISComputingGroup/IBEX/issues/5776) | Minor | Added ability to set initial values of blocks when entering simulation mode. |
| [#3012](https://github.com/ISISComputingGroup/IBEX/issues/3012) | Minor | Abort command now tells you how to recover. |
| [#5863](https://github.com/ISISComputingGroup/IBEX/issues/5863) | Minor | Improved reliability of `g.change_users`. |
| [#5620](https://github.com/ISISComputingGroup/IBEX/issues/5620) | Minor | Added block units to genie python cget |

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5785](https://github.com/ISISComputingGroup/IBEX/issues/5785) | Minor | Allow users to ctrl-c out of scans loop |
| [#3989](https://github.com/ISISComputingGroup/IBEX/issues/3989) | Minor | Tidy up motion setpoint pvs |
| [#4689](https://github.com/ISISComputingGroup/IBEX/issues/4689) | Minor | Motion setpoints copy units from underlying motor |
| [#5995](https://github.com/ISISComputingGroup/IBEX/issues/5995) | Minor | Allow user to open device screens with no blockserver running |
| [#3243](https://github.com/ISISComputingGroup/IBEX/issues/3243) | Minor | Web Dashboard: flag an error if instrument time and webserver time are different |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5600](https://github.com/ISISComputingGroup/IBEX/issues/5600) | Patch | Change BusApps address |
| [#5598](https://github.com/ISISComputingGroup/IBEX/issues/5598) | Patch | ICP crashing on begin run |
| [#5522](https://github.com/ISISComputingGroup/IBEX/issues/5522) | Minor | check opi_info.xml as part of build |
| [#3209](https://github.com/ISISComputingGroup/IBEX/issues/3209) | Minor | Stop rcptt_ test synoptics from being committed to git |
| [#5412](https://github.com/ISISComputingGroup/IBEX/issues/5412) | Minor | Added tests to confirm that Danfysik retains settings after IOC restart |
| [#5591](https://github.com/ISISComputingGroup/IBEX/issues/5591) | Minor | Update python scripting path so it only using python3 |
| [#5906](https://github.com/ISISComputingGroup/IBEX/issues/5906) | Minor | Use tempfile instead of specific filename when running an admin command |
| [#4886](https://github.com/ISISComputingGroup/IBEX/issues/4886) | Minor | Journal parser used for migration from SECI now uses python3 |
| [#5978](https://github.com/ISISComputingGroup/IBEX/issues/5978) | Minor | Use importlib instead of imp |
| [#4880](https://github.com/ISISComputingGroup/IBEX/issues/4880) | Minor | Convert ArchiverAccess to python 3 |

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
