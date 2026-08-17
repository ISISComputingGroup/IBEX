Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8780](https://github.com/ISISComputingGroup/IBEX/issues/8780) | Medium | Added block level alarm config |
| [#8990](https://github.com/ISISComputingGroup/IBEX/issues/8990) | Major/breaking | Reworked the built-in Muon TPAR editor to use `current.tpar` as the user-editable copy of the "master" TPAR files so they can't be overwritten. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| MERLIN | [8726](https://github.com/ISISComputingGroup/IBEX/issues/8726) | MAJOR| Added Support for Vacuum PLC via OPCUA |
| MAPS | [9008](https://github.com/ISISComputingGroup/IBEX/issues/9008) | MINOR | Change to use new Vacuum interface deployed to MERLIN |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [8919](https://github.com/ISISComputingGroup/IBEX/issues/8919) | Moxa ioLogik E1213 | Added Support for new device|
| [5885](https://github.com/ISISComputingGroup/IBEX/issues/5885) | QuantumNorthwest NeutronIQ | Added support. |
| [#8934](https://github.com/ISISComputingGroup/IBEX/issues/8934) | Sefram DAS240 | Added support. |


### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [8995](https://github.com/ISISComputingGroup/IBEX/issues/8995) | Major  | Remove ISIS MK2 chopper IOC    |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [8979](https://github.com/ISISComputingGroup/IBEX/issues/8979) | Minor  | Galil | Update 'new' Galil driver from v3 to v4. |
| [8798](https://github.com/ISISComputingGroup/IBEX/issues/8798) | Major | Coherent OBIS Laser Remote | Support multiple lasers on a single IOC & add support for switching lasers on/off and setting output power. Previous PV names have changed, e.g. `CHTOBISR_01:some_pv` will now be `CHTOBISR_01:1:some_pv` (where `1` is the laser number). |
| [TwinCat #4](https://github.com/ISISComputingGroup/EPICS-TwincatMotor/pull/4) | Patch | TC/Beckhoff | Send reset just before any moves to clear errors if possible |
| [GUI #1840](https://github.com/ISISComputingGroup/ibex_gui/pull/1840) | Patch | Motors | Show a warning if motor has been left in SET mode |
| [8688](https://github.com/ISISComputingGroup/IBEX/issues/8688) | Minor | Eurotherm | Added additional Eurotherm attributes.|
| [2196](https://github.com/ISISComputingGroup/IBEX/issues/2196) & [8959](https://github.com/isisComputingGroup/ibex/issues/8959) | Minor | Nanodac | Add OPI, fix IOC, add control of "advanced loop". |
| [8955](https://github.com/ISISComputingGroup/IBEX/issues/8955) | Patch | Mercury ITC | Allow Ethernet comms in addition to existing serial comms |
| [8971](https://github.com/ISISComputingGroup/IBEX/issues/8971) | Patch | Knauer K-6 | Increase number of available IOCs from 2 to 4 |
| [8969](https://github.com/ISISComputingGroup/IBEX/issues/8969) | Minor | Keithley 6517B | Add set/read "zero check" and current autorange modes |
| [8464](https://github.com/ISISComputingGroup/IBEX/issues/8464) | Minor | TC/Beckhoff | Allow sending a frozen offset to beckhoffs in order to set position |
| [6839](https://github.com/ISISComputingGroup/IBEX/issues/6839)  | Minor | TC/Beckhoff | Implement setting auto-energise to controller |
| [8901](https://github.com/ISISComputingGroup/IBEX/issues/8901)  | Minor | OPCUA | Support reading MUONFE vacuum values from PLC  |
| [8957](https://github.com/ISISComputingGroup/IBEX/issues/8957) | Patch | Mezei Flipper | Add explicit reconnection to device and increase reconnection timeout to improve comms stability. |
| [8992](https://github.com/ISISComputingGroup/IBEX/issues/8992)  | Minor | OPCUA | Supports certificate based authentication to PLC |
| [8470](https://github.com/ISISComputingGroup/IBEX/issues/8470)  | Minor | PS300 | Support GPIB control of Stanford PS300 series power supplies |
| [8222](https://github.com/ISISComputingGroup/IBEX/issues/8222)  | Minor | Tekronics OSC | Add option to use MEASURE functionality |

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [3396](https://github.com/ISISComputingGroup/IBEX/issues/3396) | Minor | Added a tab to show globals settings in the edit/view configuration screen |
| [8764](https://github.com/ISISComputingGroup/IBEX/issues/8764) | Minor | Added block level alarm config in Add/Edit Block screen |

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [PR](https://github.com/ISISComputingGroup/ibex_gui/pull/1846) | Patch | Display Moxas in a predictable order in the Moxa perspective |

# Python

### `genie_python`

See https://github.com/ISISComputingGroup/genie/releases

### Bluesky

See https://github.com/ISISComputingGroup/ibex_bluesky_core/releases

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[8445](https://github.com/ISISComputingGroup/IBEX/issues/8445) | Minor | Change how we set macro default values on ioc's so that it uses the same source of truth as the gui, this will not affect existing configurations |
|[8885](https://github.com/isisComputingGroup/ibex/issues/8885) | Patch | Dependency version updates. No user-facing behaviour changes expected. |
|[8947](https://github.com/ISISComputingGroup/IBEX/issues/8947) | Minor | Update EPICS SNMP driver and net-snmp support library to latest upstream (1.1.0.6 and 5.9.5.2) |
|[8989](https://github.com/isisComputingGroup/ibex/issues/8989) | Patch | Update dependencies for old galil driver. |

Change Types: 

* Major - Backward incompatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

what | version | where | last updated/checked
|---- | ------- | ----- | --------------------|
| MySQL | 8.4.9 | ibex_install_utils | 05/2026 |
| ActiveMQ | 5.19.6 | ISIS\ActiveMQ | 05/2026 |
| MySql-connector J | 8.4.0 | IOCLogServer | 05/2026 |

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Gson | 2.14.0 | 05/2026 |
| Guava | 33.6.0 | 05/2026 |
| MySql-connector J | 8.4.0 | 05/2026 |
| commons-codec | 1.22.0 | 05/2026 |
| Maven | 3.9.15 | 05/2026 |
| ActiveMQ (different to server version) | 5.19.0 | 05/2026 |
| Jakarta Mail API | 2.2.0 | 05/2026 |
| joda time | 2.14.2 | 05/2026 |
| py4j | 0.10.9.9 | 05/2026 |
| log4j | 2.26.0 | 05/2026 |
| JAXB | 4.0.6 | 05/2026 |
| Tyrus | 2.2.2 | 05/2026 |
| JacORB OMG API | 3.9 | 05/2026 |
| Mockito Core | 5.23.0 | 05/2026 |
| JeroMQ | 0.6.0 | 05/2026 |
| Eclipse | 2026-03 | 05/2026 |

### Uktena dependencies

If you use the libraries below in user code, you should also review the release notes of those libraries.

```
2to3==1.0
aioca==2.1
annotated-types==0.8.0
ansicon==1.89.0
argh==0.31.3
asteval==1.0.9
astroid==4.0.4
astropy==8.0.1
astropy-iers-data==0.2026.8.10.0.32.39
asttokens==3.0.2
attrs==26.1.0
autobahn==26.7.1
Automat==25.4.16
backports-abc==0.5
backports.functools-lru-cache==2.0.0
backports.shutil-get-terminal-size==1.0.0
blessed==1.48.0
bluesky==1.15.1
CaChannel @ git+https://github.com/ISISComputingGroup/CaChannel.git@8f8895c9c60d4aa43214c8078924bb4f328178fd
cbor2==6.1.4
certifi==2026.7.22
cffi==2.1.1
chardet==7.5.1
charset-normalizer==3.4.9
click==8.4.2
colorama==0.4.6
colorlog==6.12.0
compress-pickle==2.1.0
confluent-kafka==2.15.0
constantly==23.10.4
contextlib2==21.6.0
contourpy==1.3.3
coverage==7.15.4
cryptography==50.0.0
cycler==0.12.1
Cython==3.2.9
decorator==5.3.1
dill==0.4.1
dnspython==2.8.0
docopt-ng==0.9.0
docutils==0.23
email-validator==2.3.0
epicscorelibs @ https://github.com/ISISComputingGroup/epicscorelibs/releases/download/epicscorelibs-7.0.7.99.1.2-isis/epicscorelibs-7.0.7.99.1.2-cp313-cp313-win_amd64.whl#sha256=55ffd7b59aec2384301b85313d717e30767d9663157142a3bf456c5ca544711e
epicscorelibs_pcas @ git+https://github.com/IsisComputingGroup/epicscorelibs_pcas@fd06898e0ec6c807981315d9d1765669efb66159
ess-streaming-data-types==0.27.0
event-model==1.24.0
executing==2.2.1
flatbuffers==25.12.19
fonttools==4.63.0
funcsigs==1.0.2
future==1.0.0
genie_python==26.8.0
gitdb==4.0.12
gitdb2==4.0.2
GitPython==3.1.59
graypy==2.1.0
h5py==3.16.0
historydict==1.2.6
hyperlink==21.0.0
ibex-bluesky-core==1.3.0
ibex-non-ca-helpers==0.1.0
idna==3.18
Incremental==24.11.0
ipaddress==1.0.23
ipython==8.39.0
ipython-genutils==0.2.0
isort==8.0.1
jedi==0.20.0
Jinja2==3.1.6
jinxed==2.1.0
json-rpc==1.15.0
jsonschema==4.26.0
jsonschema-specifications==2025.9.1
kafka-python==3.0.10
kiwisolver==1.5.0
lazy-loader==0.5
ldap3==2.9.1
lewis==1.3.5
lmfit==1.3.4
lxml==6.1.1
lz4==4.4.5
MarkupSafe==3.0.3
matplotlib==3.10.9
matplotlib-inline==0.2.2
mccabe==0.7.0
mock==5.2.0
mpltoolbox==26.2.0
msgpack==1.2.1
msgpack-numpy==0.4.8
mysql-connector-python==8.4.0
nicos-pyctl @ git+https://github.com/mlz-ictrl/nicos-pyctl@f9a017aeecf1da00f89069f35b381f0ac985ebb8
nodeenv==1.10.0
nose2==0.16.0
numpy==2.5.2
opentelemetry-api==1.44.0
ophyd-async==0.21.1
orjson==3.11.9
p4p==4.2.1
packaging==26.3
parameterized==0.9.0
parso==0.8.7
pathlib2==2.3.7.post1
pcaspy @ git+https://github.com/ISISComputingGroup/pcaspy.git@62fea0811f3dd1427966cd58d6d64dfa53cdc0b0
pdfrw==0.4
pickleshare==0.7.5
pillow==12.3.0
platformdirs==4.11.2
plopp==26.7.0
ply==3.11
prompt_toolkit==3.0.53
protobuf==7.35.1
psutil==7.2.2
pure_eval==0.2.3
pvxslibs==1.4.1
py4j==0.10.9.9
pyasn1==0.6.0
pyasynchat==1.0.5
pyasyncore==1.0.5
pycparser==3.0
pydantic==2.12.5
pydantic-numpy==9.0.2
pydantic_core==2.41.5
pyerfa==2.0.1.5
Pygments==2.20.0
PyHamcrest==2.1.0
pylint==4.0.7
PyOpenGL==3.1.10
pyparsing==3.3.2
PyQt6==6.11.0
PyQt6-Qt6==6.11.1
PyQt6_sip==13.12.0
pyright==1.1.411
pyserial==3.5
pysmi-lextudio==1.4.3
pysnmp==7.1.22
pysnmp-lextudio==5.0.34
pysnmpcrypto==0.0.4
python-dateutil==2.9.0.post0
python-redmine==2.5.0
pytz==2026.3.post1
pywin32==312
PyYAML==6.0.3
pyzmq==27.1.0
referencing==0.37.0
reportlab==4.5.1
requests==2.34.2
rpds-py==2026.6.3
rsa==4.9.1
rst2pdf==0.105
ruamel.yaml==0.18.0
ruff==0.16.2
scandir==1.10.0
scanf==1.5.2
scanspec==1.0.0
scipp==26.8.0
scippneutron==26.7.0
scippnexus==26.1.1
scipy==1.18.0
semantic-version==2.10.0
semver==3.0.4
server_common @ git+https://github.com/ISISComputingGroup/server_common@b56f75b93d9b4c84e0d540b0df344043dbacbed4
setuptools==84.0.0
setuptools_dso==2.12.3
simplegeneric==0.8.1
singledispatch==4.1.2
six==1.17.0
smartypants==2.0.2
smmap==5.0.3
smmap2==3.0.1
snmpsim-lextudio==1.0.5
stack-data==0.6.3
stamina==26.1.0
stomp.py==9.0.0
swig==4.4.1
telnetlib3==5.0.0
tenacity==9.1.4
toml==0.10.2
tomlkit==0.15.1
toolz==1.1.0
tornado==6.5.8
tqdm==4.70.0
traitlets==5.16.1
Twisted==26.4.0
txaio==26.6.1
typing-inspection==0.4.3
typing_extensions==4.16.0
tzdata==2026.3
ujson==5.13.0
uncertainties==3.2.3
Unidecode==1.4.0
unittest-xml-reporting==4.0.0
urllib3==2.7.0
velocity-profile==1.0.0
watchdog==6.0.0
wcwidth==0.8.2
websocket-client==1.9.0
wheel==0.47.0
win_unicode_console==0.5
zope.interface==8.5
```
