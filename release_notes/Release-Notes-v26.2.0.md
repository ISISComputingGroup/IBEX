See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8822](https://github.com/ISISComputingGroup/IBEX/issues/8822) | Major | Remove various SECI compatibility tools - `SECI2IBEX` IOC, SECI web dashboard, startup scripts etc. |
| [#7914](https://github.com/ISISComputingGroup/IBEX/issues/7914) | Minor | Add deploy script step to pull and merge master branch of instrument scripts into local |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| PEARL | [#8349](https://github.com/ISISComputingGroup/IBEX/issues/8349) | Patch | Add option for permanently-centred crosshair on Pearl camera |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#8691](https://github.com/ISISComputingGroup/IBEX/issues/8691) | Ambrell EasyHeat Induction Furnace PSU | Intended for ENGIN-X. | 
| [#8899](https://github.com/ISISComputingGroup/IBEX/issues/8899) | Knauer Valve Unifier VU4.1 | Support device, using KNRK6 IOC, which has new configuration options to allow communicating in IP mode. |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8614](https://github.com/ISISComputingGroup/IBEX/issues/8614) | Minor | Oxford Instruments - Mercury IPS| Added support for SCPI mode to use the full capabilities of the new Mercury IPS magnet supplies |
| [#8766](https://github.com/ISISComputingGroup/IBEX/issues/8766) | Minor | DELFTDCMAG IOC| Echo Coil RBV and SP now agree on units (Amps) |
| [#8680](https://github.com/ISISComputingGroup/IBEX/issues/8680) | Minor | HVCAEN | Number of summary channels is now configurable by macro. |
| [#8871](https://github.com/ISISComputingGroup/IBEX/issues/8871) | Minor | FZJ Fermi Choppers | Disable start button on OPIs when vacuum interlock is bad |
| [#8875](https://github.com/ISISComputingGroup/IBEX/issues/8875) | Minor | TC/Beckhoff | Remove problematic velocity monitors which sometimes causes the velocity to be set to 0 |


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8731](https://github.com/ISISComputingGroup/IBEX/issues/8731) | Major | Added new GUI dialog to configure Alerts. |
| [#8820](https://github.com/ISISComputingGroup/IBEX/issues/8820) | Minor | Added a 'Home' button to the 'Motors' tab within the Motion Set Point (Few) device screen |

### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |
| [#8826](https://github.com/ISISComputingGroup/IBEX/issues/8826) | Minor | Reorganised script generator buttons. |
| [#8697](https://github.com/ISISComputingGroup/IBEX/issues/8697) | Patch | Fix an issue where the enablement of the "Run" button in the script generator gets out of sync with NICOS. |
| [#8688](https://github.com/ISISComputingGroup/IBEX/issues/8688) | Minor | Added additional Eurotherm attributes.|

### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8699](https://github.com/ISISComputingGroup/IBEX/issues/8699) | Minor | Show current high/low limits for Alarm in tool-tip popup |
| [#8473](https://github.com/ISISComputingGroup/IBEX/issues/8473) | Minor | Made more obvious that jog is in progress on motor opi |

# Python

### `genie_python`

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#24](https://github.com/ISISComputingGroup/genie/issues/24) | Patch | Allow `g.begin()` when DBSVR is down |
| [#8724](https://github.com/ISISComputingGroup/IBEX/issues/8724) | Minor | Added `change_autosave` command to change autosave frequency. |
| [#8849](https://github.com/ISISComputingGroup/IBEX/issues/8849) | Minor | Fixed types on `g.change()` causing scripts calling it to fail type checking. |

### Bluesky

See https://github.com/ISISComputingGroup/ibex_bluesky_core/releases

# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|[5081](https://github.com/ISISComputingGroup/IBEX/issues/5081) | Minor | Functions that allow scientists to save known "good" states of their TPAR file directory and reload them at will. |
|[8788](https://github.com/ISISComputingGroup/IBEX/issues/8788) | Minor | Dependency updates (minor/patch versions). |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8681](https://github.com/ISISComputingGroup/IBEX/issues/8681) | Major | Move JDK install location to \instrument\apps\JDK\ |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### genie_python Dependencies

These are versions of Python libraries available for use in the IBEX Python environment. See individual packages' release notes for detailed release notes.

```
2to3==1.0
aioca==2.0
annotated-types==0.7.0
argh==0.31.3
asteval==1.0.8
astroid==4.0.3
astropy==7.2.0
astropy-iers-data==0.2026.1.12.0.42.13
asttokens==3.0.1
attrs==25.4.0
autobahn==25.12.2
Automat==25.4.16
backports-abc==0.5
backports.functools-lru-cache==2.0.0
backports.shutil-get-terminal-size==1.0.0
bluesky==1.14.6
CaChannel @ git+https://github.com/ISISComputingGroup/CaChannel.git@8f8895c9c60d4aa43214c8078924bb4f328178fd
cbor2==5.8.0
certifi==2026.1.4
cffi==2.0.0
chardet==5.2.0
charset-normalizer==3.4.4
click==8.3.1
colorama==0.4.6
colorlog==6.10.1
compress-pickle==2.1.0
confluent-kafka==2.13.0
constantly==23.10.4
contextlib2==21.6.0
contourpy==1.3.3
coverage==7.13.1
cryptography==46.0.3
cycler==0.12.1
Cython==3.2.4
decorator==5.2.1
dill==0.4.0
dnspython==2.8.0
docopt==0.6.2
docutils==0.22.4
email-validator==2.3.0
epicscorelibs @ https://github.com/ISISComputingGroup/epicscorelibs/releases/download/epicscorelibs-7.0.7.99.1.2-isis/epicscorelibs-7.0.7.99.1.2-cp313-cp313-win_amd64.whl#sha256=55ffd7b59aec2384301b85313d717e30767d9663157142a3bf456c5ca544711e
epicscorelibs_pcas @ git+https://github.com/IsisComputingGroup/epicscorelibs_pcas@0f2d3b313372120d7621b546ac601287676e2c64
ess-streaming-data-types==0.27.0
event-model==1.23.1
executing==2.2.1
flatbuffers==25.12.19
fonttools==4.61.1
funcsigs==1.0.2
future==1.0.0
genie_python==26.2.0
gitdb==4.0.12
gitdb2==4.0.2
GitPython==3.1.46
graypy==2.1.0
h5py==3.15.1
historydict==1.2.6
hyperlink==21.0.0
ibex-bluesky-core==1.2.0
idna==3.11
importlib_metadata==8.7.1
importlib_resources==6.5.2
Incremental==24.11.0
ipaddress==1.0.23
ipython==8.38.0
ipython-genutils==0.2.0
isort==7.0.0
jedi==0.19.2
Jinja2==3.1.6
json-rpc==1.15.0
jsonschema==4.26.0
jsonschema-specifications==2025.9.1
kafka-python==2.3.0
kiwisolver==1.4.9
lazy_loader==0.4
ldap3==2.9.1
lewis==1.3.5
lmfit==1.3.4
lxml==6.0.2
lz4==4.4.5
MarkupSafe==3.0.3
matplotlib==3.10.7
matplotlib-inline==0.2.1
mccabe==0.7.0
mock==5.2.0
mpltoolbox==25.10.0
msgpack==1.1.2
msgpack-numpy==0.4.8
mysql-connector-python==8.4.0
nicos-pyctl @ git+https://github.com/mlz-ictrl/nicos-pyctl@f9a017aeecf1da00f89069f35b381f0ac985ebb8
nodeenv==1.10.0
nose2==0.15.1
numpy==2.3.5
opentelemetry-api==1.39.1
ophyd-async==0.14.2
orjson==3.11.5
p4p==4.2.1
packaging==25.0
parameterized==0.9.0
parso==0.8.5
pathlib2==2.3.7.post1
pcaspy @ git+https://github.com/ISISComputingGroup/pcaspy.git@62fea0811f3dd1427966cd58d6d64dfa53cdc0b0
pdfrw==0.4
pickleshare==0.7.5
pillow==12.1.0
platformdirs==4.5.1
plopp==25.11.0
ply==3.11
prompt_toolkit==3.0.52
protobuf==6.33.4
psutil==7.2.1
pure_eval==0.2.3
pvxslibs==1.4.1
py-ubjson==0.16.1
py4j==0.10.9.9
pyasn1==0.6.0
pyasynchat==1.0.5
pyasyncore==1.0.5
pycparser==2.23
pydantic==2.12.5
pydantic-numpy==9.0.1
pydantic_core==2.41.5
pyerfa==2.0.1.5
Pygments==2.19.2
PyHamcrest==2.1.0
pylint==4.0.4
PyOpenGL==3.1.10
pyparsing==3.3.1
pyright==1.1.408
pyserial==3.5
pysmi-lextudio==1.4.3
pysnmp==7.1.22
pysnmp-lextudio==5.0.34
pysnmpcrypto==0.0.4
python-dateutil==2.9.0.post0
python-redmine==2.5.0
pytz==2025.2
pywin32==311
PyYAML==6.0.3
pyzmq==27.1.0
referencing==0.37.0
reportlab==4.4.7
requests==2.32.5
rpds-py==0.30.0
rsa==4.9.1
rst2pdf==0.104
ruamel.yaml==0.18.0
ruff==0.14.11
scandir==1.10.0
scanf==1.5.2
scanspec==0.9.0
scipp==25.12.0
scippneutron==25.11.2
scippnexus==25.11.0
scipy==1.17.0
semantic-version==2.10.0
semver==3.0.4
server_common @ git+https://github.com/ISISComputingGroup/server_common@8805dc6854389004b81ce83a0884793f1d65200f
setuptools==80.9.0
setuptools_dso==2.12.2
simplegeneric==0.8.1
singledispatch==4.1.2
six==1.17.0
smartypants==2.0.2
smmap==5.0.2
smmap2==3.0.1
snmpsim-lextudio==1.0.5
stack-data==0.6.3
stamina==25.2.0
stomp.py==8.2.0
swig==4.4.1
telnetlib3==2.0.8
tenacity==9.1.2
toml==0.10.2
tomlkit==0.14.0
toolz==1.1.0
tornado==6.5.4
tqdm==4.67.1
traitlets==5.14.3
Twisted==25.5.0
txaio==25.12.2
typing-inspection==0.4.2
typing_extensions==4.15.0
tzdata==2025.3
ujson==5.11.0
uncertainties==3.2.4
Unidecode==1.4.0
unittest-xml-reporting==4.0.0
urllib3==2.6.3
velocity-profile==1.0.0
watchdog==6.0.0
wcwidth==0.2.14
websocket-client==1.9.0
wheel==0.45.1
win_unicode_console==0.5
zipp==3.23.0
zope.interface==8.2
```


