# Highlights and Breaking Changes

### IBEX User Forum

The IBEX user forum is for IBEX users to discuss hints and tips about how to use the system. You can join it on [Teams](https://teams.microsoft.com/l/team/19%3a926e5e961a364c15ba0d56e97e188e2f%40thread.skype/conversations?groupId=b20b0859-14eb-4fa7-b221-c96ac1027927&tenantId=3f66361c-a87e-4158-8f61-99e82db3cac8).

### `genie_python` now uses Python 3

[Ticket #5175](https://github.com/ISISComputingGroup/IBEX/issues/5175): `genie_python` will now run under Python 3.8 as opposed to 2.7. There are differences between python 2 and 3 which may mean that some scripts which worked under python 2 will no longer work under python 3. See [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Python-3) for further details.

### `genie_python` now has a `b.` module containing block names.

[Ticket #5401](https://github.com/ISISComputingGroup/IBEX/issues/5401): `genie_python` now has a shortcut to block names `b.<blockname>`. This can be used wherever you would have used the name of a block - for example in a call to `g.cset`. It will also autocomplete in the scripting window. See post on forum [here](https://teams.microsoft.com/l/message/19:7a45f6d4e99d4a31b441e46a82fb33c1@thread.skype/1592484373224?tenantId=3f66361c-a87e-4158-8f61-99e82db3cac8&groupId=b20b0859-14eb-4fa7-b221-c96ac1027927&parentMessageId=1592484373224&teamName=IBEX%20Users&channelName=Scripting&createdTime=1592484373224)

### Alarms on blocks are now recorded in nexus files

[Ticket #4936](https://github.com/ISISComputingGroup/IBEX/issues/4936): Alarm status of blocks is now put into the Nexus file and can be filtered by Mantid

### The import mechanism for the `inst` module has changed

[Ticket #5262](https://github.com/ISISComputingGroup/IBEX/issues/5262): A new import mechanism for the `inst` module. We no longer try to do the equivalent of `import * from *`, instead functions need to be imported explicitly into the inst module. 

This means that if you want a new function to be available in `inst.` you will need to update `inst\__init__.py`. 

Instruments with very simple scripts now only have a single inst.py file instead of a module. 

See [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Python-3#changes-with-instrument-scripts-due-to-python-3) for further details.

### Removal of the `dummy` argument from `g.load_script`

[Ticket #5451](https://github.com/ISISComputingGroup/IBEX/issues/5451): Remove the dummy argument from `g.load_script`. This will cause an error message if an old GUI runs with a new `genie_python`. It will break any user scripts where you have called `load_script` with more than one argument in a positional way. 

Examples: 
- `g.load_script("my_script.py", None, False, True)` will be broken. 
- `g.load_script("my_script.py")` or `g.load_script("my_script.py", check_script=False, warnings_as_error=True)` will both be fine.

### Removal of deprecated `genie_python` functions

[Ticket #5457](https://github.com/ISISComputingGroup/IBEX/issues/5457): The following functions have been removed from genie_python in favour of their `change_` equivalents: 
- `set_title` (use `change_title` instead)
- `set_script_dir` (use `change_script_dir` instead)
- `set_number_soft_periods` (use `change_number_soft_periods` instead)
- `set_sample_par` (use `change_sample_par` instead)
- `set_beamline_par` (use `change_beamline_par` instead)
- `set_period` (use `change_period` instead)

The following functions have been removed entirely:
- `check_lowlimit_against_highlimit`
- `get_absolute_path`
- `is_absolute` 
- `get_instrument_py_name`. 

The following functions have been moved into `g.adv`:
- `get_instrument` (use `g.adv.get_instrument` instead) 
- `set_messages_verbosity` (use `g.adv.set_messages_verbosity` instead) 

`send_tcpip` has been moved into the shared InstrumentScripts repository.

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| EMU | [#5222](https://github.com/ISISComputingGroup/IBEX/issues/5222) | Minor | Refactor script generator definitions |
| EMU | [#5133](https://github.com/ISISComputingGroup/IBEX/issues/5133) | Minor | Add booster heater scripts |
| SANS2D | [#4555](https://github.com/ISISComputingGroup/IBEX/issues/4555) | Minor | Added support for SANS2D FINS vacuum PLC |
| CRISP | [#4303](https://github.com/ISISComputingGroup/IBEX/issues/4303) | Minor | Added support for CRISP coarse jaws | |

# Devices

### Newly supported devices

| Ticket | Device |
| ------ | ------|
| [#5103](https://github.com/ISISComputingGroup/IBEX/issues/5103) | Lakeshore 372 |
| [#4918](https://github.com/ISISComputingGroup/IBEX/issues/4918) | LSI correlator |
| [#5378](https://github.com/ISISComputingGroup/IBEX/issues/5378) | CRISP Flipper |

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#4831](https://github.com/ISISComputingGroup/IBEX/issues/4831) | Minor | SMS series PSU | Added startup checks to Cryogenic ltd. SMS series cryomagnet PSU IOC. |
| [#5057](https://github.com/ISISComputingGroup/IBEX/issues/5057) | Minor | SMS series PSU | Added a simple queued state machine to IOC for SMS series PSU |
| [#4871](https://github.com/ISISComputingGroup/IBEX/issues/4871) | Minor | Mezei Flipper | Modify MEZFLIPR ioc to talk to new-style software (for LET) |
| [#4488](https://github.com/ISISComputingGroup/IBEX/issues/4488) | Minor | Attocube ANC350 | Removed unused IOC for Attocube ANC350 |
| [#5190](https://github.com/ISISComputingGroup/IBEX/issues/5190) | Minor | Zero Field Controller | Change STABILITY PV to AT_SETPOINT and modified logic to give N/A when in manual mode
| [#4925](https://github.com/ISISComputingGroup/IBEX/issues/4925) | Minor | SM300 | Add missing return and param update in driver, minor improvements |
| [#5266](https://github.com/ISISComputingGroup/IBEX/issues/5266) | Minor | DaqMX (NI DAQ) |  Automatically reconnects the DAQmx if there is a transient communications fault. |
| [#5382](https://github.com/ISISComputingGroup/IBEX/issues/5382) | Minor | Keithley 2700 | Fix device stop processing after 1 day |
| [#4287](https://github.com/ISISComputingGroup/IBEX/issues/4287) | Minor | Rotating Sample Changer (POLARIS, GEM, HRPD) | Added error checking and recovery on rotating sample changer |
| [#5332](https://github.com/ISISComputingGroup/IBEX/issues/5332) | Minor | FINS PLC | Added ability to specify PLC node |
| [#4999](https://github.com/ISISComputingGroup/IBEX/issues/4999) | Minor | LSI Correlator | Added ability to save to vendor format. |
| [#5412](https://github.com/ISISComputingGroup/IBEX/issues/5412) | Minor | Danfysik | Investigate startup after crash sending wrong setpoints (due to auto-on-off which is now correct). As part of the ticket added more logging to IOC db. |
| [#5381](https://github.com/ISISComputingGroup/IBEX/issues/5381) | Minor | Beckhoff & Oercone | Fixed lua scripting bug occurring in IOCs for Beckhoff and oercone
| [#5268](https://github.com/ISISComputingGroup/IBEX/issues/5268) | Minor | Danfysik PSU | Allow disabling Danfysik PSU auto on/off settings
| [#4948](https://github.com/ISISComputingGroup/IBEX/issues/4948) | Minor | DMA4500M | Bring IOC up to ISIS standards and add tests |

### Reflectometry server

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#4331](https://github.com/ISISComputingGroup/IBEX/issues/4331) | Minor | Expose beamline constants as PVs |
| [#3555](https://github.com/ISISComputingGroup/IBEX/issues/3555) | Minor | Implement global error handler and better feedback |
| [#3535](https://github.com/ISISComputingGroup/IBEX/issues/3535) | Minor | Improved logging (log all moves) and minor bug fixes|
| [#3897](https://github.com/ISISComputingGroup/IBEX/issues/3897) | Minor | Autosave and restore incoming beam paths in disable mode |
| [#4309](https://github.com/ISISComputingGroup/IBEX/issues/4309) | Minor | Allow multiple out of beam positions per component dependent on the incoming beam
| [#5387](https://github.com/ISISComputingGroup/IBEX/issues/5387) | Patch | fix bug preventing CTRL-C from killing a script when using the reflectometry perspective.
| [#4967](https://github.com/ISISComputingGroup/IBEX/issues/4967) | Patch | Improved the overall look and consistency of the reflectometry OPI.

#  IBEX Client

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5155](https://github.com/ISISComputingGroup/IBEX/issues/5155) | Patch | Edit Configuration dialog: the default synoptic config is now automatically selected |
| [#5136](https://github.com/ISISComputingGroup/IBEX/issues/5136) | Patch | Remove a memory leak that happened every time the configuration dialogue was opened. |
| [#4648](https://github.com/ISISComputingGroup/IBEX/issues/4648) | Patch | Improved the speed of searching for PVs to connect blocks to |
| [#5030](https://github.com/ISISComputingGroup/IBEX/issues/5030) | Minor | Loading config after saving it from `Edit configuration` window
| [#4958](https://github.com/ISISComputingGroup/IBEX/issues/4958) | Minor | Fixed a bug where blocks with Deadbands less than `1e-4` or of the form `Xe-X` can not be saved
| [#5116](https://github.com/ISISComputingGroup/IBEX/issues/5116) | Minor | DAE spectra plots display counts/nanosecond for Muons and counts/microsecond for neutrons
| [#5104](https://github.com/ISISComputingGroup/IBEX/issues/5104) | Minor | Voltage limits can now be set via the zero field controller for the Kepco PSUs it is using. |
| [#4951](https://github.com/ISISComputingGroup/IBEX/issues/4951) | Minor | Fixes GUI bug that tick or untick multiple checkboxes when clicking on one after you sort the table |
| [#4291](https://github.com/ISISComputingGroup/IBEX/issues/4291) | Minor | Created Reflectometry Front Panel Perspective |
| [#5063](https://github.com/ISISComputingGroup/IBEX/issues/5063) | Minor | Advanced table of motors can now be shown, includes more information about the motors. |
| [#4732](https://github.com/ISISComputingGroup/IBEX/issues/4732) | Minor | GEM Jaws OPI aspect ratio fix plus limit of travel indicators
| [#5314](https://github.com/ISISComputingGroup/IBEX/issues/5314) | Minor | Indicate on RIKEN front-end when there is a connection problem with the DAQmx.
| [#5084](https://github.com/ISISComputingGroup/IBEX/issues/5084) | Minor | Scripting perspective now gives a confirmation dialog if you are opening multiple scripting windows.
| [#5391](https://github.com/ISISComputingGroup/IBEX/issues/5391) | Patch | Fixed autocomplete for script names in `g.load_script` in the scripting perspective
| [#5146](https://github.com/ISISComputingGroup/IBEX/issues/5146) | Minor | Nicos current script window auto-scrolls to highlighted line |

# Script generator

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#5114](https://github.com/ISISComputingGroup/IBEX/issues/5114) | Minor | Show help string as defined in the script definition.
| [#5166](https://github.com/ISISComputingGroup/IBEX/issues/5166) | Minor | Add link to user manual page.
| [#5118](https://github.com/ISISComputingGroup/IBEX/issues/5118) | Minor | Allow scripts to be saved with given name |
| [#5107](https://github.com/ISISComputingGroup/IBEX/issues/5107) | Minor | Allow saving of parameters file, parameters files are also saved alongside any generated script |
| [#5312](https://github.com/ISISComputingGroup/IBEX/issues/5312) | Minor | Add "Clear All" button |
| [#4907](https://github.com/ISISComputingGroup/IBEX/issues/4907) | Minor | Provide default values for new actions in the table |
| [#5090](https://github.com/ISISComputingGroup/IBEX/issues/5090) | Minor | Added tests for the script generator GUI |
| [#5121](https://github.com/ISISComputingGroup/IBEX/issues/5121) | Minor | Can now use TAB to move around the script generator table |
| [#5425](https://github.com/ISISComputingGroup/IBEX/issues/5425) | Minor | Script generator: Can now select where generated scripts are saved |


# genie_python

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5142](https://github.com/ISISComputingGroup/IBEX/issues/5142) | Minor | Add "immediate" option to END and PAUSE commands |
| [#5210](https://github.com/ISISComputingGroup/IBEX/issues/5210) | Patch | Improve the performance of the linter when repeatedly calling `g.load_script()`
| [#5378](https://github.com/ISISComputingGroup/IBEX/issues/5378) | Minor | Added warning if running genie_python in incorrect python version
| [#5431](https://github.com/ISISComputingGroup/IBEX/issues/5431) | Minor | cset has been tidied up internally and no longer queries blockserver for blocknames, meaning there is less to go wrong and potentially giving a speed increase
| [#5401](https://github.com/ISISComputingGroup/IBEX/issues/5401) | Minor | Added the `b` namespace that contains blocknames for autocomplete. See [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Block-names-helper) for how to use.
| [#5141](https://github.com/ISISComputingGroup/IBEX/issues/5141) | Minor | Add the ability to prevent a run from beginning by setting begin_precmd with a function that returns a string explaining why not to begin the run. See documentation [here](https://github.com/ISISComputingGroup/ibex_user_manual/wiki/Pre-and-Post-Command-Hooks)
| [#5380](https://github.com/ISISComputingGroup/IBEX/issues/5380) | Minor | Genie python now warns you if you're using cset to wait and you could be waiting for ever. |
| [#5214](https://github.com/ISISComputingGroup/IBEX/issues/5214) | Minor | Script Checker: make shared instrument scripts lintable |
| [#5209](https://github.com/ISISComputingGroup/IBEX/issues/5209) | Minor | Script Checker: improve support for Python assignments |
| [#4992](https://github.com/ISISComputingGroup/IBEX/issues/4992) | Minor | Genie Python console now shows exceptions if it can not change the number of periods or the period number. Also added system tests for change_period and change_num_soft_periods. |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#4934](https://github.com/ISISComputingGroup/IBEX/issues/4934) | Minor | IBEX can now save load config with characters longer than 60 characters |
| [#4887](https://github.com/ISISComputingGroup/IBEX/issues/4887) | Minor | Convert ScriptServer to Python 3 |
| [#5254](https://github.com/ISISComputingGroup/IBEX/issues/5254) | Minor | Fixed issue causing instruments to be running using the python on the share. |
| [#5164](https://github.com/ISISComputingGroup/IBEX/issues/5164) | Minor | Added check for MUONFE hotfix to install script |
| [#5334](https://github.com/ISISComputingGroup/IBEX/issues/5334) | Minor | Cap the maximum number of threads used by genie_python while waiting for a caput in the channel wrapper used in pycaspy IOCs e.g. the blockserver, reflectometry ioc |
| [#4136](https://github.com/ISISComputingGroup/IBEX/issues/4136) | Minor | Removed the block cache. This required a number of changes to how cget/cshow work which should have resulted in a speed up |
| [#5331](https://github.com/ISISComputingGroup/IBEX/issues/5331) | Minor | Disable quick edit in windows in IBEX startup. Should mean that during startup the user can no longer accidentally click in a window which would pauses its execution. |
| [#5207](https://github.com/ISISComputingGroup/IBEX/issues/5207) | Patch | Run Control: rename SUSPEND_ON_INVALID PV to SOI |
| [#5275](https://github.com/ISISComputingGroup/IBEX/issues/5275) | Minor | Upgrade script: automatically rename updated PVs in synoptic config files |

# Internal changes

Note: these changes are to tools or workflows used by developers only.

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#5127](https://github.com/ISISComputingGroup/IBEX/issues/5127) | Minor | Wiki Checker: add test for special characters in file names |
| [#5339](https://github.com/ISISComputingGroup/IBEX/issues/5339) | Minor | Make off site backup for development files |
| [#5176](https://github.com/ISISComputingGroup/IBEX/issues/5176) | Minor | Fixes for instrument deploy script |
| [#4892](https://github.com/ISISComputingGroup/IBEX/issues/4892) | Minor | Convert ConfigChecker to Python 3 |
| [#4036](https://github.com/ISISComputingGroup/IBEX/issues/4036) | Minor | Move web dashboard machine to latest Windows version |
| [#4891](https://github.com/ISISComputingGroup/IBEX/issues/4891) | Minor | Convert GUI build scripts to Python 3 |
| [#5344](https://github.com/ISISComputingGroup/IBEX/issues/5344) | Patch | Jenkins build status reported on MS Teams |
| [#5173](https://github.com/ISISComputingGroup/IBEX/issues/5173) | Minor | Support latest Visual Studio version |
| [#5286](https://github.com/ISISComputingGroup/IBEX/issues/5286) | Minor | Fix KYNCTM3K IOC tests |
| [#5109](https://github.com/ISISComputingGroup/IBEX/issues/5109) | Minor | Added ability to run individually system tests locally |