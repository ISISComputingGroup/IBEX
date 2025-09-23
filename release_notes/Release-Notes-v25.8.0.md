See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |
| [8739](https://github.com/isiscomputinggroup/ibex/issues/8739) | Patch | The user manual has been moved to [a new location](https://isiscomputinggroup.github.io/ibex_user_manual/) with more user-friendly structured navigation. |


# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| CHIPIR | [PR](https://github.com/ISISComputingGroup/ibex_gui/pull/1785) | Minor | Put filters on CHIPIR collimator screen |
| INTER | [#8675](https://github.com/isiscomputinggroup/ibex/issues/8675) | Patch | Gracefully stop galil motors when safety system is tripped. |
| HIFI | [#8704](https://github.com/ISISComputingGroup/IBEX/issues/8704) | Minor | Inhibit taking reading within two seconds of field measurement range change |
| INTER | [#7814](https://github.com/isiscomputinggroup/ibex/issues/7814) | Patch | Add Inclinometer variable for INTER Beckhoff. |
| MAPS | [#8586](https://github.com/isiscomputinggroup/ibex/issues/8586) | Minor | Add OPC UA IOC for MAPS Vacuum System upgrade. |
| SXD | [#6056](https://github.com/ISISComputingGroup/IBEX/issues/6056) | Minor | Added support for SXD Attocube |


# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#8586](https://github.com/isiscomputinggroup/ibex/issues/8586) | OPC UA Server | Add OPC UA general IOC, and for MAPS Vacuum System upgrade. |


### Removed devices

| Ticket | Device | Notes|
| ------ | ------ | -----|


### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#8673](https://github.com/ISISComputingGroup/IBEX/issues/8673) | Patch | TC/Beckhoff | Make poll rate configurable |
| [#8660](https://github.com/ISISComputingGroup/IBEX/issues/8660) | Patch | HV Caen | Increase number of available channels to 16 cards x 24 channels. |
| [#8666](https://github.com/ISISComputingGroup/IBEX/issues/8666) | Major | DDS STRESS RIG | Replaced internal logic with Statemachine to properly reflect state of VI |
| [#8682](https://github.com/ISISComputingGroup/IBEX/issues/8682) | Patch | ISISDAE | Add string-formatted run duration and period run duration PVs. |
| [#8682](https://github.com/ISISComputingGroup/IBEX/issues/8692) | Patch | DG645 | Limit OPI (user interface) graph update to 1Hz, to avoid excessive CPU usage. |
| [#8704](https://github.com/ISISComputingGroup/IBEX/issues/8704) | Minor | G3HALLPROBE | Inhibit taking reading within two seconds of field measurement range change |
| [#8706](https://github.com/ISISComputingGroup/IBEX/issues/8706) | Patch | TPG300 | archive relay status PVs |
| [#8720](https://github.com/ISISComputingGroup/IBEX/issues/8720) | Patch | ISISDAE | Improve begin/end speeds by optimising archiver restarts |
| [#8687](https://github.com/ISISComputingGroup/IBEX/issues/8687) | Minor | LITRON | Added a stale indicator to allow detection of VI disconnection from hardware. |
| [#8701](https://github.com/ISISComputingGroup/IBEX/issues/8701) | Minor | GALIL | Updated NEW Galil driver to latest upstream |
| [#8736](https://github.com/ISISComputingGroup/IBEX/issues/8736) | Minor | LNDYISW | Fixed race condition that caused back to back sets to outlets to overwrite eachother. |



### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |


#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8725](https://github.com/ISISComputingGroup/IBEX/issues/8725) | Minor | Added warning to dashboard if DAE is using test clock. |

### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |
| [#8697](https://github.com/ISISComputingGroup/IBEX/issues/8697) | Patch | Fix an issue where the enablement of the "Run" button in the script generator gets out of sync with NICOS. |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#8505](https://github.com/ISISComputingGroup/IBEX/issues/8505) | Minor | Jaws: enforce minimum and maximum gap values |
| [PR](https://github.com/ISISComputingGroup/ibex_gui/pull/1775) | Minor | Add muon and EPB1 beam current to beam status view |
| [#8578](https://github.com/ISISComputingGroup/IBEX/issues/8578) | Minor | Add defaults for font size and autolayout in a scripting console |
| [#8254](https://github.com/ISISComputingGroup/IBEX/issues/8254) | Minor | Update EPICS standard modules to later upstream versions  |


# Python

### `genie_python`

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [4338](https://github.com/ISISComputingGroup/IBEX/issues/4338) | Minor | Improve performance of `cget` function |
| [8671](https://github.com/ISISComputingGroup/IBEX/issues/8671) | Minor | Make error message from corrupt cache more verbose |
| [#8725](https://github.com/ISISComputingGroup/IBEX/issues/8725) | Minor | Added warning to to begin() if DAE is using test clock. |

### Bluesky

See https://github.com/ISISComputingGroup/ibex_bluesky_core/releases for bluesky release notes.

### Other python libraries

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [8597](https://github.com/ISISComputingGroup/IBEX/issues/8597) | Minor | Numpy version 2 will now be used. Some APIs are not backwards-compatible between numpy 1.x and 2.x. See [numpy 2 release notes](https://numpy.org/devdocs/release/2.0.0-notes.html) for further details. |
| [8597](https://github.com/ISISComputingGroup/IBEX/issues/8597) | Minor | Python version 3.12 will now be used. |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#8628](https://github.com/ISISComputingGroup/ibex/issues/8628) | Patch | Ensure experiment database populator can be installed on modern python versions |
| [#8631](https://github.com/ISISComputingGroup/IBEX/issues/8631) | Patch | Update experiment database populator auth scheme to REST rather than SOAP |
| [#8751](https://github.com/ISISComputingGroup/IBEX/issues/8751) | Minor | Update EPICS base to version 7.0.9 |

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
| Gson | 2.12.1 | 04/2025 |
| Guava | 33.4.0 | 04/2025 |
| MySql-connector J | 9.1.0 | 01/2025 |
| commons-codec | 1.18.0 | 04/2025 |
| Maven | 3.9.5 | 11/2023 |
| ActiveMQ (different to server version) | 5.19.0 | 04/2025 |
| Nicos | 23 | 11/2023 |
| Jakarta Activation API | 2.1.2 | 10/2024 |
| Jakarta Mail API | 2.1.3 | 10/2024 |
| Jakarta XML Binding API | 4.0.1 | 10/2024 |
| JavaX Activation | 1.1.1 | 10/2024 |
| joda time | 2.13.1 | 04/2025 |
| py4j | 0.10.9.9 | 04/2025 |
| log4j | 2.24.3 | 04/2025 |
| JAXB | 3.0.2 | 10/2024 |
| Tyrus | 2.2.0 | 10/2024 |
| JacORB OMG API | 3.9 | 10/2024 |
| Mockito Core | 5.16.1 | 04/2025 |
| JeroMQ | 0.6.0 | 10/2024 |
| Nebula | 3.0.0 | 10/2024 |
| CS-Studio | 04/2025 | 04/2025 |
| Pydev | 11.0.3 | 12/2023 |
| Eclipse | 2024-12 | 04/2025 |
| Eclipse Updates| 4.34 | 04/2025 |

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|
| Python | 3.12.9 | 4/2025 |
| matplotlib | 3.10.1 | 10/2024 |
| 2to3 | 1.0 | 21/08/2025 | 
 | aioca | 1.8.1 | 21/08/2025 | 
 | annotated-types | 0.7.0 | 21/08/2025 | 
 | argh | 0.31.3 | 21/08/2025 | 
 | asteval | 1.0.6 | 21/08/2025 | 
 | astroid | 3.3.11 | 21/08/2025 | 
 | astropy | 7.1.0 | 21/08/2025 | 
 | astropy-iers-data | 0.2025.8.4.0.42.59 | 21/08/2025 | 
 | asttokens | 3.0.0 | 21/08/2025 | 
 | attrs | 25.3.0 | 21/08/2025 | 
 | autobahn | 24.4.2 | 21/08/2025 | 
 | Automat | 25.4.16 | 21/08/2025 | 
 | backports-abc | 0.5 | 21/08/2025 | 
 | backports.functools-lru-cache | 2.0.0 | 21/08/2025 | 
 | backports.shutil-get-terminal-size | 1.0.0 | 21/08/2025 | 
 | bluesky | 1.14.2 | 21/08/2025 | 
 | CaChannel | git+https://github.com/ISISComputingGroup/CaChannel@ec1ae054419b09c62e5a750fed7518e8bdfa2753 | 21/08/2025 | 
 | certifi | 2025.8.3 | 21/08/2025 | 
 | cffi | 1.17.1 | 21/08/2025 | 
 | chardet | 5.2.0 | 21/08/2025 | 
 | charset-normalizer | 3.4.2 | 21/08/2025 | 
 | colorama | 0.4.6 | 21/08/2025 | 
 | colorlog | 6.9.0 | 21/08/2025 | 
 | compress-pickle | 2.1.0 | 21/08/2025 | 
 | constantly | 23.10.4 | 21/08/2025 | 
 | contextlib2 | 21.6.0 | 21/08/2025 | 
 | contourpy | 1.3.3 | 21/08/2025 | 
 | coverage | 7.10.2 | 21/08/2025 | 
 | cryptography | 45.0.5 | 21/08/2025 | 
 | cycler | 0.12.1 | 21/08/2025 | 
 | Cython | 3.1.2 | 21/08/2025 | 
 | decorator | 5.2.1 | 21/08/2025 | 
 | dill | 0.4.0 | 21/08/2025 | 
 | dnspython | 2.7.0 | 21/08/2025 | 
 | docopt | 0.6.2 | 21/08/2025 | 
 | docutils | 0.21.2 | 21/08/2025 | 
 | email_validator | 2.2.0 | 21/08/2025 | 
 | epicscorelibs | https://github.com/ISISComputingGroup/epicscorelibs/releases/download/epicscorelibs-7.0.7.99.1.2a1-isis/epicscorelibs-7.0.7.99.1.2a1-cp312-cp312-win_amd64.whl#sha256=9853977ac0c54cf9836446bc67bf4e15b817ed4e99be7dce8b35f65239e6a1f8 | 21/08/2025 | 
 | epicscorelibs_pcas | git+https://github.com/IsisComputingGroup/epicscorelibs_pcas@0f2d3b313372120d7621b546ac601287676e2c64 | 21/08/2025 | 
 | ess-streaming-data-types | 0.27.0 | 21/08/2025 | 
 | event-model | 1.23 | 21/08/2025 | 
 | executing | 2.2.0 | 21/08/2025 | 
 | flatbuffers | 25.2.10 | 21/08/2025 | 
 | fonttools | 4.59.0 | 21/08/2025 | 
 | funcsigs | 1.0.2 | 21/08/2025 | 
 | future | 1.0.0 | 21/08/2025 | 
 | genie_python | 25.8.0 | 21/08/2025 | 
 | gitdb | 4.0.12 | 21/08/2025 | 
 | gitdb2 | 4.0.2 | 21/08/2025 | 
 | GitPython | 3.1.45 | 21/08/2025 | 
 | graypy | 2.1.0 | 21/08/2025 | 
 | h5py | 3.14.0 | 21/08/2025 | 
 | historydict | 1.2.6 | 21/08/2025 | 
 | hyperlink | 21.0.0 | 21/08/2025 | 
 | ibex-bluesky-core | 1.0.0 | 21/08/2025 | 
 | idna | 3.10 | 21/08/2025 | 
 | importlib_metadata | 8.7.0 | 21/08/2025 | 
 | importlib_resources | 6.5.2 | 21/08/2025 | 
 | incremental | 24.7.2 | 21/08/2025 | 
 | iniconfig | 2.0.0 | 21/08/2025 | 
 | ipaddress | 1.0.23 | 21/08/2025 | 
 | ipython | 8.37.0 | 21/08/2025 | 
 | ipython-genutils | 0.2.0 | 21/08/2025 | 
 | isort | 6.0.1 | 21/08/2025 | 
 | jedi | 0.19.2 | 21/08/2025 | 
 | Jinja2 | 3.1.6 | 21/08/2025 | 
 | json-rpc | 1.15.0 | 21/08/2025 | 
 | jsonschema | 4.25.0 | 21/08/2025 | 
 | jsonschema-specifications | 2025.4.1 | 21/08/2025 | 
 | kafka-python | 2.2.15 | 21/08/2025 | 
 | kiwisolver | 1.4.8 | 21/08/2025 | 
 | lazy_loader | 0.4 | 21/08/2025 | 
 | ldap3 | 2.9.1 | 21/08/2025 | 
 | lewis | 1.3.5 | 21/08/2025 | 
 | lmfit | 1.3.4 | 21/08/2025 | 
 | lxml | 6.0.0 | 21/08/2025 | 
 | lz4 | 4.4.4 | 21/08/2025 | 
 | MarkupSafe | 3.0.2 | 21/08/2025 | 
 | matplotlib | 3.10.1 | 21/08/2025 | 
 | matplotlib-inline | 0.1.7 | 21/08/2025 | 
 | mccabe | 0.7.0 | 21/08/2025 | 
 | mock | 5.2.0 | 21/08/2025 | 
 | mpltoolbox | 25.5.0 | 21/08/2025 | 
 | msgpack | 1.1.1 | 21/08/2025 | 
 | msgpack-numpy | 0.4.8 | 21/08/2025 | 
 | mysql-connector-python | 8.4.0 | 21/08/2025 | 
 | nicos-pyctl | git+https://github.com/mlz-ictrl/nicos-pyctl@f9a017aeecf1da00f89069f35b381f0ac985ebb8 | 21/08/2025 | 
 | nodeenv | 1.9.1 | 21/08/2025 | 
 | nose2 | 0.15.1 | 21/08/2025 | 
 | numpy | 2.3.2 | 21/08/2025 | 
 | opentelemetry-api | 1.36.0 | 21/08/2025 | 
 | ophyd-async | 0.11 | 21/08/2025 | 
 | orjson | 3.11.1 | 21/08/2025 | 
 | p4p | 4.2.0 | 21/08/2025 | 
 | packaging | 24.1 | 21/08/2025 | 
 | parameterized | 0.9.0 | 21/08/2025 | 
 | parso | 0.8.4 | 21/08/2025 | 
 | pathlib2 | 2.3.7.post1 | 21/08/2025 | 
 | pcaspy @ git+https://github.com/ISISComputingGroup/pcaspy@62fea0811f3dd1427966cd58d6d64dfa53cdc0b0 | 21/08/2025 | 
 | pdfrw | 0.4 | 21/08/2025 | 
 | pickleshare | 0.7.5 | 21/08/2025 | 
 | pillow | 11.3.0 | 21/08/2025 | 
 | platformdirs | 4.3.8 | 21/08/2025 | 
 | plopp | 25.7.1 | 21/08/2025 | 
 | pluggy | 1.5.0 | 21/08/2025 | 
 | ply | 3.11 | 21/08/2025 | 
 | prompt_toolkit | 3.0.51 | 21/08/2025 | 
 | protobuf | 6.31.1 | 21/08/2025 | 
 | psutil | 7.0.0 | 21/08/2025 | 
 | pure_eval | 0.2.3 | 21/08/2025 | 
 | pvxslibs | 1.3.3 | 21/08/2025 | 
 | py4j | 0.10.9.9 | 21/08/2025 | 
 | pyasn1 | 0.6.0 | 21/08/2025 | 
 | pyasynchat | 1.0.4 | 21/08/2025 | 
 | pyasyncore | 1.0.4 | 21/08/2025 | 
 | pycparser | 2.22 | 21/08/2025 | 
 | pydantic | 2.11.7 | 21/08/2025 | 
 | pydantic_core | 2.33.2 | 21/08/2025 | 
 | pydantic_numpy | 8.0.1 | 21/08/2025 | 
 | pyerfa | 2.0.1.5 | 21/08/2025 | 
 | Pygments | 2.19.2 | 21/08/2025 | 
 | PyHamcrest | 2.1.0 | 21/08/2025 | 
 | pylint | 3.3.7 | 21/08/2025 | 
 | PyOpenGL | 3.1.9 | 21/08/2025 | 
 | pyparsing | 3.2.3 | 21/08/2025 | 
 | pyright | 1.1.403 | 21/08/2025 | 
 | pyserial | 3.5 | 21/08/2025 | 
 | pysmi-lextudio | 1.4.3 | 21/08/2025 | 
 | pysnmp | 7.1.21 | 21/08/2025 | 
 | pysnmp-lextudio | 5.0.34 | 21/08/2025 | 
 | pysnmpcrypto | 0.0.4 | 21/08/2025 | 
 | pytest | 8.3.3 | 21/08/2025 | 
 | python-dateutil | 2.9.0.post0 | 21/08/2025 | 
 | python-redmine | 2.5.0 | 21/08/2025 | 
 | pytz | 2025.2 | 21/08/2025 | 
 | pywin32 | 311 | 21/08/2025 | 
 | PyYAML | 6.0.2 | 21/08/2025 | 
 | pyzmq | 27.0.1 | 21/08/2025 | 
 | referencing | 0.36.2 | 21/08/2025 | 
 | reportlab | 4.4.3 | 21/08/2025 | 
 | requests | 2.32.4 | 21/08/2025 | 
 | rpds-py | 0.26.0 | 21/08/2025 | 
 | rsa | 4.9.1 | 21/08/2025 | 
 | rst2pdf | 0.103.1 | 21/08/2025 | 
 | ruamel.yaml | 0.18.14 | 21/08/2025 | 
 | ruamel.yaml.clib | 0.2.12 | 21/08/2025 | 
 | ruff | 0.12.7 | 21/08/2025 | 
 | scandir | 1.10.0 | 21/08/2025 | 
 | scanf | 1.5.2 | 21/08/2025 | 
 | scipp | 25.5.1 | 21/08/2025 | 
 | scippneutron | 25.7.0 | 21/08/2025 | 
 | scippnexus | 25.6.0 | 21/08/2025 | 
 | scipy | 1.16.1 | 21/08/2025 | 
 | semantic-version | 2.10.0 | 21/08/2025 | 
 | semver | 3.0.4 | 21/08/2025 | 
 | server_common | git+https://github.com/ISISComputingGroup/server_common@7fe5aedac83b7e95347a71679a2e97214bc85f0b | 21/08/2025 | 
 | setuptools | 80.9.0 | 21/08/2025 | 
 | setuptools_dso | 2.12.2 | 21/08/2025 | 
 | simplegeneric | 0.8.1 | 21/08/2025 | 
 | singledispatch | 4.1.2 | 21/08/2025 | 
 | six | 1.17.0 | 21/08/2025 | 
 | smartypants | 2.0.2 | 21/08/2025 | 
 | smmap | 5.0.2 | 21/08/2025 | 
 | smmap2 | 3.0.1 | 21/08/2025 | 
 | snmpsim-lextudio | 1.0.5 | 21/08/2025 | 
 | stack-data | 0.6.3 | 21/08/2025 | 
 | stomp.py | 8.2.0 | 21/08/2025 | 
 | swig | 4.3.1 | 21/08/2025 | 
 | toml | 0.10.2 | 21/08/2025 | 
 | tomlkit | 0.13.3 | 21/08/2025 | 
 | toolz | 1.0.0 | 21/08/2025 | 
 | tornado | 6.5.1 | 21/08/2025 | 
 | tqdm | 4.67.1 | 21/08/2025 | 
 | traitlets | 5.14.3 | 21/08/2025 | 
 | Twisted | 25.5.0 | 21/08/2025 | 
 | txaio | 25.6.1 | 21/08/2025 | 
 | typing-inspection | 0.4.1 | 21/08/2025 | 
 | typing_extensions | 4.14.1 | 21/08/2025 | 
 | tzdata | 2025.2 | 21/08/2025 | 
 | uncertainties | 3.2.3 | 21/08/2025 | 
 | Unidecode | 1.4.0 | 21/08/2025 | 
 | unittest-xml-reporting | 3.2.0 | 21/08/2025 | 
 | urllib3 | 2.5.0 | 21/08/2025 | 
 | watchdog | 6.0.0 | 21/08/2025 | 
 | wcwidth | 0.2.13 | 21/08/2025 | 
 | websocket-client | 1.8.0 | 21/08/2025 | 
 | wheel | 0.45.1 | 21/08/2025 | 
 | win_unicode_console | 0.5 | 21/08/2025 | 
 | zipp | 3.23.0 | 21/08/2025 | 
 | zope.interface | 7.2 | 21/08/2025 | 
