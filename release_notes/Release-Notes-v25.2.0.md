# Release numbering

The release numbering for IBEX has changed to a calendar-version scheme. This is the first release in that new scheme, release `25.2`, corresponding to Feburary 2025. The last release on the old scheme was release `15.0.0`, released August 2024.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [#8415](https://github.com/ISISComputingGroup/IBEX/issues/8415) | Major | `g.load_script` will now apply argument type-checking, via [`pyright`](https://github.com/microsoft/pyright?tab=readme-ov-file#static-type-checker-for-python), by default. This means that some errors which would previously have caused runtime exceptions will now be caught during `g.load_script`. See [Error Checking Troubleshooting](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Error-Checking-Troubleshooting#new-pyright) for more details. Also adds type hinting to public genie-python API functions.<br /><br />**In some cases this may mean that scripts which previously loaded are now rejected by `load_script`.** We would strongly encourage instruments to check key scripts early and to contact experiment controls for assistance if needed.<br /><br />Script checking can be entirely disabled by passing `check_script=False` to `load_script` if needed, but we would encourage instruments to instead fix the errors reported by the type-checker and to ask for assistance if needed. |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Minor | The `genie_python` library has been split out into a [pip-installable package](https://pypi.org/project/genie-python/).<br /><br />There are no direct user-facing changes to `genie_python`'s API as a result of this change, but it is now possible to depend on `genie_python` in downstream libraries and to install the `genie_python` library into environments other than IBEX via `pip`. |
| [#6510](https://github.com/ISISComputingGroup/IBEX/issues/6510) | Minor | Remove `genie_mantid` script in favour of `pip install`ing the above `genie` package. |
| [#8588](https://github.com/ISISComputingGroup/IBEX/issues/8588) | Minor | Previously ibex created many `procServ` processes in the background that managed start/stop and logging of each IOC, including ones fro IOCs that were never used. These are now created on demand which shoudld reduce the overall ibex memory footprint |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| CHIPIR | [Ticket6217](https://github.com/ISISComputingGroup/IBEX/issues/6217#issue-805738735) | Minor | Added OPI support for CHIPIR Filter Set |
| CHIPIR | [Ticket6216](https://github.com/ISISComputingGroup/IBEX/issues/6216) | Minor | Added device screen for CHIPIR XYZ table |
| Muons | [Ticket6232](https://github.com/ISISComputingGroup/IBEX/issues/6232) | Minor | Added muon tpar file text editor/viewer |
| HiFi | [Ticket6086](https://github.com/ISISComputingGroup/IBEX/issues/6086) | Minor | Added an OPI for the Hifi Magnet powersupplies |
| HiFi | [Ticket8332](https://github.com/ISISComputingGroup/IBEX/issues/8332) | Minor | Added an OPI for the Hifi Litron Laser Front Panel VI |
| HiFi | [Ticket6090](https://github.com/ISISComputingGroup/IBEX/issues/6090) | Minor | Added an OPI for Hifi Litron Laser Timing Control & extended DG645 IOC | 
| HiFI | [Ticket8403](https://github.com/ISISComputingGroup/IBEX/issues/8403) | Patch | Increase minimum precision that the cryosms driver can send to the power supply. |
# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#6085](https://github.com/ISISComputingGroup/IBEX/issues/6085) | Thorlabs FW102C | Six position filter wheel controller |
| [#8400](https://github.com/ISISComputingGroup/IBEX/issues/8400) | Group3 Hall probe | Hall probe used by zero-field system on HIFI |
| [#8331](https://github.com/ISISComputingGroup/IBEX/issues/8331) | New Focus Intelligent Picometer | Motor used to control Litron Laser Power on HIFI. |
| [#8413](https://github.com/ISISComputingGroup/IBEX/issues/8413) | Anton-Paar L-DENS 3300 Density sensor | Density meter used by reflectometry instruments. | 
| [#8403](https://github.com/ISISComputingGroup/IBEX/issues/8403) | HIFI Zero-field system | Zero-field system used on HIFI. | 


### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [inst_servers#400](https://github.com/ISISComputingGroup/EPICS-inst_servers/pull/400) | Collision Avoidance Monitor | Remove the collision avoidance monitor. |


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8502](https://github.com/ISISComputingGroup/IBEX/issues/8502) | Minor | Danfysik model 8500 | Use `WA` command rather than `DA 0` as per equipment safety note from Danfysik. |
| [#8160](https://github.com/ISISComputingGroup/IBEX/issues/8160) | Minor | Beckhoff/TwinCAT | Allow 2 instances of the TC IOC, for portable beckhoffs |
| [#8104](https://github.com/ISISComputingGroup/IBEX/issues/8104) | Minor | PACE5000 | Various PACE5000 snags - set units to bar, slew mode to lin, display source pressure, fix vent status |
| [#8218](https://github.com/ISISComputingGroup/IBEX/issues/8218) | Minor | GALIL |  allow COM in GALILADDR macro |
| [#7677](https://github.com/ISISComputingGroup/IBEX/issues/7677) | Minor | Tektronix AFG3XXX | Channel 1 and 2 are configurable in IOC macros, by default both are enabled just like so far. |
| [#8248](https://github.com/ISISComputingGroup/IBEX/issues/8248) | Minor | Lakeshore 340 | Lakeshore no longer sets excitiation threshold with potentially invalid values on startup. |
| [#6854](https://github.com/ISISComputingGroup/IBEX/issues/6854) | Minor | Beckhoff/TwinCAT | Remove old CRISP coarse jaw tcioc motor record code |
| [#8175](https://github.com/ISISComputingGroup/IBEX/issues/8175) | Minor | needlevalve | Add macro to govern wriet mode toggle. |
| [#8262](https://github.com/ISISComputingGroup/IBEX/issues/8262) | Minor | Keithley 2400 | Add input fields for compliance voltage and current. |
| [#8284](https://github.com/ISISComputingGroup/IBEX/issues/8284)| Minor | McLennan | Add macro to set access group of JVEL, HLM, LLM to allow setting of those fields without restart of IOC |
| [#8322](https://github.com/ISISComputingGroup/IBEX/issues/8322)| Minor | HVCAEN | Fix issue with write records not getting created | 
| [#8253](https://github.com/ISISComputingGroup/IBEX/issues/8253)| Minor | McLennan | Make paramters last a powercycle. Parameters are now saved on homing of device |
| [#8335](https://github.com/ISISComputingGroup/IBEX/issues/8335)| Minor | Beckhoff/TwinCAT | Fix issue with table of motors advanced view with energised icon not working | 
| [#8310](https://github.com/ISISComputingGroup/IBEX/issues/8310)| Minor | Eurotherm | Fix issue where disconnected/missing Eurotherm causes other Eurotherms to fail to be read |
| [#8427](https://github.com/ISISComputingGroup/IBEX/issues/8427) | Minor | Motion controllers | The settings for motor controllers (Galil, Beckhoff, Mclennan, Linmot, SMC100, SM300) have been moved from <br /> `c:\instrument\settings\config\<instrument>\configurations` <br /> to <br /> `c:\instrument\apps\epics\support\motorExtensions\master\settings\<instrument>`. <br /> This does not affect settings for `motionSetpoints`, which remain in the configurations directory. Settings have been migrated. |
| [Ticket8504](https://github.com/ISISComputingGroup/IBEX/issues/8504) | Minor | Motors | Fix home button showing as disconnected for aliased axes ie. sample changer axes | 
| [Ticket8516](https://github.com/ISISComputingGroup/IBEX/issues/8516) | Minor | Lindy IPower Switch | Add 4 more LNDYISW IOCs | 
| [Tektronix#4](https://github.com/ISISComputingGroup/EPICS-Tektronix_AFG3XXX/pull/4) | Minor | Tektronix AFG3XXX | Add ramp symmetry functionality | 
| [Ticket8551](https://github.com/ISISComputingGroup/IBEX/issues/8551) | Minor | Galil | (new galil driver) set homing to be allowed in both directions by default | 
| [Ticket8524](https://github.com/ISISComputingGroup/IBEX/issues/8524) | Minor | Galil | (new galil driver) notify users of disconnection at startup and during running | 
| [#8181](https://github.com/ISISComputingGroup/IBEX/issues/8181) | Minor | PearlPC | Added purge functioanlity (buttons, LEDs, etc) to PEARLPC OPI |

# Python

### `genie_python`

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [genie python#8501](https://github.com/ISISComputingGroup/IBEX/issues/8501) | Minor | Added optional parameter to `wait_for_runstate()` to be in agreement with `genie_simulate_impl.wait_for_runstate()` on the number of positional parameters |
| [#8359](https://github.com/ISISComputingGroup/IBEX/issues/8359)| Minor | Added wrapper for P4P to allow use of pv access as well as channel access in genie python. |
| [#8409](https://github.com/ISISComputingGroup/IBEX/issues/8409) | Minor | Add commands to quickly read and sum event mode spectrum data. |
| [#8579](https://github.com/ISISComputingGroup/IBEX/issues/8579) | Patch | Hide messages of the form `CAERROR: ...` which could show up in console. |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Minor | The back-end mechanism for sending sms/email/slack alerts via `g.send_sms` and `g.send_email` was updated to share a mechanism with other IBEX alerting mechanisms. These functions will no longer work on machines outside the ISIS network, or on IBEX installations which have not been configured to send alerts (all instrument machines have been configured to send alerts). |

### Bluesky

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [ibex_bluesky_core#15](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/15) | Minor | Make `ibex_bluesky_core` available as a dependency, and add automated & manual system tests for bluesky. |
| [ibex_bluesky_core#10](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/10) | Minor | Add block read & write functionality - this allows using an arbitrary block as either a "motor" or "detector" in a scan. |
| [ibex_bluesky_core#8](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/8) | Minor | Expose & document bluesky's plotting functionality. |
| [ibex_bluesky_core#21](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/21) | Minor | Generate & publish uncertainties from DAE Counts data |
| [ibex_bluesky_core#19](https://github.com/ISISComputingGroup/ibex_bluesky_core/issues/19) | Major | Introduces fitting for scans in a user friendly way with dynamic guessing functions & new fitting models. |

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8453](https://github.com/ISISComputingGroup/IBEX/issues/8453) | Patch | Build and execute all python-epics wrappers against `epicscorelibs`-provided libraries. No user-facing change. |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Patch | Python bindings to the Open Dynamics Engine (`pyode`) were removed.  |
| [#8381](https://github.com/ISISComputingGroup/IBEX/issues/8381) | Patch | A deprecated version of `pyreadline` bindings were removed. |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8438](https://github.com/ISISComputingGroup/IBEX/issues/8438) | Minor | Containerised Archiver Appliance and associated new EPICS gateway for local containers |
| [#8480](https://github.com/ISISComputingGroup/IBEX/issues/8430) | Minor | Added check for repository permissions in repository checks |
| [#8437](https://github.com/orgs/ISISComputingGroup/projects/20/views/8?pane=issue&itemId=72604908) | Patch | Create a network independant Python venv |
| [#8593](https://github.com/ISISComputingGroup/IBEX/issues/8593) | Patch | Stop log file output getting garbled if ioc restarted via console command |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### Server dependencies

what | version | where | last updated/checked
|---- | ------- | ----- | --------------------|
| MySQL | 8.4.2 | ibex_install_utils | 10/2024 |
| Make | 4.4 | utils_win32 | 11/2023 |
| ActiveMQ | 5.18.3 | ISIS\ActiveMQ | 12/2023 |
| Nicos | 23 | ScriptServer | 11/2023 |
| Cygwin | 3.4.9 | ICP_Binaries |	12/2023 |
| MySql-connector J | 8.4.0 | IOCLogServer | 10/2024 |

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Gson | 2.11 | 10/2024 |
| Guava | 33.3.1 | 10/2024 |
| MySql-connector J | 9.1.0 | 01/2025 |
| commons-codec | 1.17.1 | 10/2024 |
| Maven | 3.9.5 | 11/2023 |
| ActiveMQ (different to server version) | 5.18.6 | 10/2024 |
| Nicos | 23 | 11/2023 |
| Jakarta Activation API | 2.1.2 | 10/2024 |
| Jakarta Mail API | 2.1.3 | 10/2024 |
| Jakarta XML Binding API | 4.0.1 | 10/2024 |
| JavaX Activation | 1.1.1 | 10/2024 |
| joda time | 2.13 | 10/2024 |
| py4j | 0.10.9.7 | 10/2024 |
| log4j | 2.24 | 10/2024 |
| JAXB | 3.0.2 | 10/2024 |
| Tyrus | 2.2.0 | 10/2024 |
| JacORB OMG API | 3.9 | 10/2024 |
| Mockito Core | 5.14.0 | 10/2024 |
| JeroMQ | 0.6.0 | 10/2024 |
| Nebula | 3.0.0 | 10/2024 |
| CS-Studio | 12/2023 | 12/2023 |
| Pydev | 11.0.3 | 12/2023 |
| Eclipse | 2024-09 | 04/2024 |
| Eclipse Updates| 4.33 | 10/2024 |

### Python Dependencies

```
2to3==1.0
aioca==1.8.1
annotated-types==0.7.0
argh==0.31.3
asteval==1.0.5
astroid==3.3.8
astropy==7.0.0
astropy-iers-data==0.2025.1.13.0.34.51
asttokens==3.0.0
attrs==24.3.0
autobahn==24.4.2
Automat==24.8.1
backports-abc==0.5
backports.functools-lru-cache==2.0.0
backports.shutil-get-terminal-size==1.0.0
bluesky==1.13
CaChannel @ git+https://github.com/ISISComputingGroup/CaChannel@ac400e92bf24c7ee5d714d826e2d035f3a4423af
certifi==2024.12.14
cffi==1.17.1
chardet==5.2.0
charset-normalizer==3.4.1
colorama==0.4.6
colorlog==6.9.0
compress-pickle==2.1.0
constantly==23.10.4
contextlib2==21.6.0
contourpy==1.3.1
coverage==7.6.10
cryptography==44.0.0
cycler==0.12.1
Cython==3.0.11
decorator==5.1.1
Deprecated==1.2.15
dill==0.3.9
docopt==0.6.2
docutils==0.21.2
epicscorelibs==7.0.7.99.1.1a3
epicscorelibs_pcas @ git+https://github.com/IsisComputingGroup/epicscorelibs_pcas@7f77a10f649571814c58f4000391951b77113ac8
ess-streaming-data-types==0.27.0
event-model==1.22.3
executing==2.1.0
flatbuffers==24.12.23
flexcache==0.3
flexparser==0.4
fonttools==4.55.3
funcsigs==1.0.2
future==1.0.0
genie_python==25.2.1
gitdb==4.0.12
gitdb2==4.0.2
GitPython==3.1.44
graypy==2.1.0
h5py==3.12.1
HeapDict==1.0.1
historydict==1.2.6
hyperlink==21.0.0
ibex-bluesky-core==0.1.3
idna==3.10
importlib_metadata==8.5.0
importlib_resources==6.5.2
incremental==24.7.2
ipaddress==1.0.23
ipython==8.31.0
ipython-genutils==0.2.0
isort==5.13.2
jedi==0.19.2
Jinja2==3.1.5
json-rpc==1.15.0
jsonschema==4.23.0
jsonschema-specifications==2024.10.1
kafka-python==2.0.2
kiwisolver==1.4.8
ldap3==2.9.1
lewis==1.3.4
lmfit==1.3.2
lxml==5.3.0
lz4==4.3.3
MarkupSafe==3.0.2
matplotlib==3.9.2
matplotlib-inline==0.1.7
mccabe==0.7.0
mock==5.1.0
mpltoolbox==24.5.1
msgpack==1.1.0
msgpack-numpy==0.4.8
mysql-connector-python==8.4.0
networkx==3.4.2
nicos-pyctl==1.3
nodeenv==1.9.1
nose2==0.15.1
numpy==1.26.4
opentelemetry-api==1.29.0
ophyd-async==0.8.0
p4p==4.2.0a3
packaging==24.2
parameterized==0.9.0
parso==0.8.4
pathlib2==2.3.7.post1
pathtools==0.1.2
pcaspy @ git+https://github.com/ISISComputingGroup/pcaspy@ddb652651e0fe47537270af6c33f49b0a426888e
pdfrw==0.4
pickleshare==0.7.5
pillow==11.1.0
Pint==0.24.4
platformdirs==4.3.6
plopp==24.10.0
ply==3.11
prompt_toolkit==3.0.48
protobuf==5.29.3
psutil==6.1.1
pure_eval==0.2.3
pvxslibs==1.3.2a2
py4j==0.10.9.9
pyasn1==0.6.0
pycparser==2.22
pydantic==2.10.5
pydantic_core==2.27.2
pydantic_numpy==5.0.2
pyerfa==2.0.1.5
Pygments==2.19.1
PyHamcrest==2.1.0
pylint==3.3.3
PyOpenGL==3.1.7
pyparsing==3.2.1
pyright==1.1.392.post0
pyserial==3.5
pysmi-lextudio==1.4.3
pysnmp-lextudio==5.0.34
pysnmpcrypto==0.0.4
python-dateutil==2.9.0.post0
python-redmine==2.5.0
pytz==2024.2
pywin32==308
PyYAML==6.0.2
pyzmq==26.2.0
referencing==0.36.1
reportlab==4.2.5
requests==2.32.3
rpds-py==0.22.3
rsa==4.9
rst2pdf==0.103.1
ruamel.yaml==0.18.10
ruamel.yaml.clib==0.2.12
ruff==0.9.2
scandir==1.10.0
scanf==1.5.2
scipp==24.11.2
scippneutron==24.12.0
scippnexus==24.11.1
scipy==1.15.1
semantic-version==2.10.0
semver==3.0.2
setuptools-dso==2.11
simplegeneric==0.8.1
singledispatch==4.1.0
six==1.17.0
smartypants==2.0.1
smmap==5.0.2
smmap2==3.0.1
snmpsim-lextudio==1.0.5
stack-data==0.6.3
stomp.py==8.2.0
swig==4.3.0
toml==0.10.2
tomlkit==0.13.2
toolz==1.0.0
tornado==6.4.2
tqdm==4.67.1
traitlets==5.14.3
Twisted==24.11.0
txaio==23.1.1
typing_extensions==4.12.2
tzdata==2024.2
uncertainties==3.2.2
Unidecode==1.3.8
unittest-xml-reporting==3.2.0
urllib3==2.3.0
watchdog==6.0.0
wcwidth==0.2.13
websocket-client==1.8.0
win_unicode_console==0.5
wrapt==1.17.2
xmlrunner==1.7.7
zict==2.2.0
zipp==3.21.0
zope.interface==7.2
```
