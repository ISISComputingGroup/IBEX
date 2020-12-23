## Changes to make on specific instruments when releasing

### All instruments

- Ticket 1289: Search through all the synoptics and replace the following (**IMPORTANT**: remember to commit and push changes to git, or the blockserver will just pull again from the repo and undo all your changes):
  - For synoptics containing components of type `ATTENUATOR`, the `Q` macro was deleted
    - in ATTENUATOR replace the section
    ```
<properties>
	<property>
		<key>Q</key>
		<value>some_value</value>
	</property>
</properties>
    ```
       with `<properties/>`
  - For synoptics containing components of type `MUON_FRONT_END`:
    - replace macro key `MM_MuSR` with `MM_MUSR`
    - replace macro key `MM_HiFi` with `MM_HIFI`
  - For synoptics containing components of type `MOVINGMONITOR`, the `CHANNUM` macro was deleted
    - in MOVINGMONITOR delete the section:
    ```
<property>
    <key>CHANNUM</key>
    <value>some_value</value>
</property>
    ```
  - For synoptics containing components of type `MONITOR` and target name `Monitor` (not the `Double Monitor`!), the `CHANNUM`, `MM` and `N` macros were deleted
    - in MONITOR delete the following sections:
    ```
<property>
	<key>CHANNUM</key>
	<value>some_value</value>
</property>

<property>
	<key>MM</key>
	<value>some_value</value>
</property>

<property>
	<key>N</key>
	<value>some_value</value>
</property>
     ```
  - For synoptics containing components of type `JAWS`: the `MM`, `JAWS` and `M` macros were deleted
    - in JAWS delete the following sections:
     ```
<property>
	<key>MM</key>
	<value>some_value</value>
</property>

<property>
	<key>JAWS</key>
	<value>some_value</value>
</property>

<property>
	<key>M</key>
	<value>some_value</value>
</property>
```

- Ticket 1728: Axes configurations and IOC macros for instruments using McLennans will need updating. I think this is currently just Iris but this needs confirmation. In the folder `C:\Instrument\Settings\config\NDX[INST]\mclennan` any files that use the macros `IFPORT#` need updating to `IFAXIS#`. For Iris in particular, the `axes.cmd` file should be updated so that the stretching rig configuration is called for `IFMTRCTRL2` and the sample changer with `IFMTRCTRL1`. Please see the [McLennan wiki page](https://github.com/ISISComputingGroup/IBEX/wiki/McLennan-motors) for more details.
- Ticket 1751: Existing device screens configurations need to be moved from `/[instrument name]/configurations/configurations/[config name]/screens.xml` and merged into the new location `/[instrument name]/configurations/devices/screens.xml`. Once once commit and push changes.
- Ticket 1644 (IMPORTANT: this is actually part of release 3.0.0) 
    - Review the configurations, components and synoptics for all instruments and adjust references to `EUROTHERM_nn` IOCs to `EUROTHRM_nn`, and PVs from `EUROTHERMn` to `EUROTHERM_0n`.
    - Update EUROTHERM to EUROTHRM for autosave files to preserve persisted behaviour.
    - Check user and instrument scripts for instances of EUROTHERM that need converting to EUROTHRM
    - Remember to check for and update macros defined in `globals.txt`
- Ticket 1895 (IMPORTANT: this is actually part of release 3.0.0) 
    - As above for MK3CHOPPER renamed to MK3CHOPR
    - Pay particular note to updates to `globals.txt` as this is where the MK3 chopper is configured.
- Ticket 1541: Pay particular attention to the period tab when comparing DAE settings before/after deployment as it has undergone some significant changes.
- Ticket 1446: Confirm that the instrument configurations are being stored in a remote repository. See [here](https://github.com/ISISComputingGroup/ibex_developers_manual/wiki/First-time-installing-and-building-(Windows)#setting-up-a-configurations-directory) for how to set this up.
- Ticket 1567: All instruments intending to use the script generator need to make slight changes to the dosans_normal/dotrans_normal python methods: rename "uamps" parameter to "waitfor" and add "change_period" parameter. This is based on genie python code as seen on LARMOR, check if other instruments deviate.
Current method signature: 
```
def dosans_normal(position="",title="",uamps=10.0,thickness=1.0,width="",height="",geometry="",waitfortype="uamps",rtype=0,delayed=0):
```
Desired method signature:
```
def dosans_normal(position="",title="",waitfor=10.0,thickness=1.0,width="",height="",geometry="",waitfortype="uamps",rtype=0,delayed=0, change_period=1.0):
```
- Changes have been made to the web dashboard code, follow the deployment instructions described in https://github.com/ISISComputingGroup/ibex_developers_manual/wiki/Web-Dashboard#deployment

- Ticket 1904: For synoptics containing components of type `KEPCO`: the `IOC_NUM' macro has been replaced by the 'KEPCO' macro. The Kepco macro now expects a full PV name (e.g. KEPCO_01) rather than it's numeric identifier (e.g. 01). Search through synoptic for any synoptics containing a kepco and replace the IOC_NUM macro with the new KEPCO macro.


- Ticket 1875: The IOC macros for McLennan motors have been changed so that each IOC takes a single baud rate, stop bits etc. Update those instruments that use McLennans (currently Iris, Vesuvio) so that the configurations use the new IOC macros.

### NDXIRIS

- Push config to git repository `git push --set-upstream origin NDXIRIS`
- Delete configurations_to_delete folder in config

### NDXIMAT

- Check that the FINS attentuator is working correctly. E.g. `camonitor IN:IMAT:ATTEN:OPEN` returns no errors.

### NDXZOOM

- Ticket 1236: to use the DMS OPI, create a file in the config folder at NDXZOOM\configurations\galil\axes.cmd, with the following content:
```
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=DISK:BEAMSTOP1:X,mAXIS=MTR0101")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=DISK:BEAMSTOP1:Y,mAXIS=MTR0102")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=DISK:BEAMSTOP2:X,mAXIS=MTR0103")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=DISK:BEAMSTOP2:Y,mAXIS=MTR0104")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STRIP:BEAMSTOP,mAXIS=MTR0105")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=DETECTORS,mAXIS=MTR0106")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=BAFFLE,mAXIS=MTR0107")
```

### MUON Front End

- Ticket 1840: Ensure that the muon front end synoptic opi works. I.e. that macros work correctly with the OPI and IOC; correct if not as per suggestions.

The `IFDMC01` macro and the `MTR0x0x` need to be changed to the appropriate value of the motors in use in the DMS.

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|  [#1595](https://github.com/ISISComputingGroup/IBEX/issues/1595) | Patch | Fixed a bug whereby new IOC macro values were not immediately being applied to their respective IOCs when the current configuration is edited.  |
|  [#1717](https://github.com/ISISComputingGroup/IBEX/issues/1717) | Patch | Add precision for TPG readback |
|  [#1593](https://github.com/ISISComputingGroup/IBEX/issues/1593) | Minor | The SDTest OPI macro `DEV` can now be set from the synoptic editor in the client. |
|  [#1768](https://github.com/ISISComputingGroup/IBEX/issues/1768) | Patch | RB number selector not coping with accents |
|  [#1667](https://github.com/ISISComputingGroup/IBEX/issues/1667) | Minor | Can now view config on read-only instruments. |
|  [#1410](https://github.com/ISISComputingGroup/IBEX/issues/1410) | Minor | Can no longer appear to edit blocks on read-only instruments. |
|  [#1541](https://github.com/ISISComputingGroup/IBEX/issues/1541) | Minor | Modified the layout of the "periods"-tab in experiment setup, so that the window only displays settings relevant to the selected period type / period source (following the layout of the "time channels"-tab) |
|  [#1551](https://github.com/ISISComputingGroup/IBEX/issues/1551) | Minor | Added labels to the file/table selection controls in experiment setup, to clarify which file is currently loaded and which is selected to change to |
|  [#1770](https://github.com/ISISComputingGroup/IBEX/issues/1724) | Patch | Fixed a bug which sometimes caused a crash in the Blockserver whilst restarting |
|  [#1728](https://github.com/ISISComputingGroup/IBEX/issues/1728) | Minor | Updated the McLennan macros and available environment variables to make configuration of axes with multiple controllers easier. |
|  [#1564](https://github.com/ISISComputingGroup/IBEX/issues/1564) | Minor | Can save a file to disk from the script generator. |
|  [#1820](https://github.com/ISISComputingGroup/IBEX/issues/1820) | Minor | Runcontrol manger should not hang if run controller does not start. |
|  [#1655](https://github.com/ISISComputingGroup/IBEX/issues/1655) | Minor | Add units to various values. |
|  [#1503](https://github.com/ISISComputingGroup/IBEX/issues/1503) | Patch | Create calibrated and uncalibrated Danfysik OPIs. |
|  [#1692](https://github.com/ISISComputingGroup/IBEX/issues/1692) | Minor | Added extra TEMP and TEMP:SP PVs in Lakeshore336 so blocks work correctly |
|  [#1410](https://github.com/ISISComputingGroup/IBEX/issues/1410) | Minor | Can no longer appear to edit blocks on read-only instruments. |
|  [#1725](https://github.com/ISISComputingGroup/IBEX/issues/1725) | Patch | Added underlying infrastructure to support custom McLennan homing routines. |
|  [#1547](https://github.com/ISISComputingGroup/IBEX/issues/1547) | Patch | Add script server proxy to pickle JSON for NICOS. |
|  [#1446](https://github.com/ISISComputingGroup/IBEX/issues/1446) | Minor | Configurations are not pushed to git if you are looking at the wrong branch |
|  [#1603](https://github.com/ISISComputingGroup/IBEX/issues/1603) | Minor | Perspective does not switch to IOC log when configuration is changed. |
|  [#1727](https://github.com/ISISComputingGroup/IBEX/issues/1727) | Minor | A confirmation dialog will appear if you try and save a configuration with the name of a pre-existing configuration |
|  [#1727](https://github.com/ISISComputingGroup/IBEX/issues/1727) | Minor | When creating a new configuration, or editing a current one, the configuration cannot be saved with the name of the current configuration. The current configuration can only be modified from the `Edit current configuration` dialog. |
|  [#1712](https://github.com/ISISComputingGroup/IBEX/issues/1712) | Minor | The client will no longer let you save configs when there are spaces at the end of the name. |
|  [#1793](https://github.com/ISISComputingGroup/IBEX/issues/1793) | Patch | IOCs are now (re)started in parallel when loading/updating a configuration. This should improve performance, especially for configurations with lots of IOCs. |
|  [#1812](https://github.com/ISISComputingGroup/IBEX/issues/1812) | Patch| Removed SVN from ConfigVersioncontrol - should have no affect on users |
|  [#1855](https://github.com/ISISComputingGroup/IBEX/issues/1855) | Patch | Avoid NPE on no PVPrefix set in instrument info. |
|  [#1847](https://github.com/ISISComputingGroup/IBEX/issues/1847) | Patch | Do not log when motor moves. |
|  [#1801](https://github.com/ISISComputingGroup/IBEX/issues/1801) | Patch | FINS attenuator read status is a single read to reduce the load on the FINS. |
|  [#1384](https://github.com/ISISComputingGroup/IBEX/issues/1384) | Patch | Exception message on closing run-control dialog eliminated. |
|  [#1850](https://github.com/ISISComputingGroup/IBEX/issues/1850) | Patch | When Log messages are no longer overloading the GUI the GUI does not continue to redraw the log table as fast as it can (reduces CPU load). |
|  [#1356](https://github.com/ISISComputingGroup/IBEX/issues/1356) | Minor | Tidied up validation of description on config dialog. |
|  [#873](https://github.com/ISISComputingGroup/IBEX/issues/873) | Minor | The show/hide blocks menu now also appears when right clicking on a block and group. |
|  [#1751](https://github.com/ISISComputingGroup/IBEX/issues/1751) | Minor | Device screens are saved per instrument rather than per configuration |
|  [#1750](https://github.com/ISISComputingGroup/IBEX/issues/1750) | Minor | The instrument time at the latest data update will now be displayed on the dataweb. |
|  [#1667](https://github.com/ISISComputingGroup/IBEX/issues/1667) | Minor | Can now view config on read-only instruments. |
|  [#1344](https://github.com/ISISComputingGroup/IBEX/issues/1344) | Patch | "Help about" version number is resized to match size of number |
|  [#1738](https://github.com/ISISComputingGroup/IBEX/issues/1738) | Patch | Tidy SFKChopper IOC boot scripts.. |
|  [#1807](https://github.com/ISISComputingGroup/IBEX/issues/1807) | Minor | Fixed a bug whereby spurious dialogs were created after selecting `Edit block` from the block dashboard on the main view. |
|  [#1434](https://github.com/ISISComputingGroup/IBEX/issues/1434) | Minor | Changed colour scheme of traces on beam status graph to high contrast colours more suitable for colour blind users. |
|  [#1618](https://github.com/ISISComputingGroup/IBEX/issues/1618) | Minor | Fixed a bug whereby an IOC wasn't restarted with the block server when the simulation level was changed. |
|  [#1816](https://github.com/ISISComputingGroup/IBEX/issues/1816) | Minor | Made the component tab the first tab in the edit configuration dialog and moved IOC macros tab directly to the right of the IOCs tab. |
|  [#1644](https://github.com/ISISComputingGroup/IBEX/issues/1644) | Major | IMPORTANT: this is actually part of release 3.0.0. `EUROTHERM` IOCs have been renamed to `EUROTHRM` for consistency with EPICS 8-character naming to help prevent PV overflow. Eurotherm PVs have been adjusted to the standard format such that `EUROTHERMn` would now be `EUROTHRM_0n`. |
|  [#1432](https://github.com/ISISComputingGroup/IBEX/issues/1432) | Minor | Made table of motors more suitable for colour-blind users. |
|  [#1891](https://github.com/ISISComputingGroup/IBEX/issues/1891) | Minor | Simulated motors now respect limits when they are changed during a move. |
|  [#1856](https://github.com/ISISComputingGroup/IBEX/issues/1856) | Minor | Converted Eurotherm OPI to new format. Added error messages for the calibration and ramp files in case they're not found |
|  [#1567](https://github.com/ISISComputingGroup/IBEX/issues/1567) | Minor | ScriptGenerator creates actual meaningful genie_python scripts. |
|  [#1236](https://github.com/ISISComputingGroup/IBEX/issues/1236) | Minor | Added OPI for the ZOOM DMS (detector motion system) |
|  [#1839](https://github.com/ISISComputingGroup/IBEX/issues/1839) | Minor | Added links to user manual & genie python documentation to weblinks perspective. Added link to user manual to Help menu. |
|  [#1902](https://github.com/ISISComputingGroup/IBEX/issues/1902) | Minor | Fixed a problem with the way motors were displayed in the motors perspective. |
|  [#1777](https://github.com/ISISComputingGroup/IBEX/issues/1777) | Patch | Fixed bug where PV values would be deleted when any key was pressed |
|  [#1862](https://github.com/ISISComputingGroup/IBEX/issues/1862) | Minor | Added keyboard shortcuts for the perspectives. |
|  [#1578](https://github.com/ISISComputingGroup/IBEX/issues/1578) | Minor | Added method to genie python to get pv prefix, also additional parameter in get/set pv |
|  [#1233](https://github.com/ISISComputingGroup/IBEX/issues/1233) | Minor | Add OPI for MuonFE polariser, guide and collimisation device. |
|  [#1917](https://github.com/ISISComputingGroup/IBEX/issues/1917) | Minor | The Pixelman OPI is now accessible from the client and the OPI has been updated to the current style guidelines. |
|  [#1925](https://github.com/ISISComputingGroup/IBEX/issues/1925) | Patch | Fixed an internal exception caused by saving a synoptic before the synoptic perspective has been opened. |
|  [#1836](https://github.com/ISISComputingGroup/IBEX/issues/1836) | Minor | Moved Active MQ into it's own repository. |
|  [#1870](https://github.com/ISISComputingGroup/IBEX/issues/1870) | Minor | Fixed bug in synoptic editor where READ/WRITE option was not being properly selected |
|  [#1878](https://github.com/ISISComputingGroup/IBEX/issues/1878) | Minor | The device screens perspective will pop up an error if the user tries to open a device screen without a target. |
|  [#1872](https://github.com/ISISComputingGroup/IBEX/issues/1806) | Patch | Create a sensible error page for the web interface when it is unable to connect. |
|  [#1895](https://github.com/ISISComputingGroup/IBEX/issues/1895) | Major | IMPORTANT: this is actually part of release 3.0.0. The `MK3CHOPPER_01` IOC has been renamed to `MK3CHOPR_01` for consistency with EPICS 8-character naming to help prevent PV overflow. |
|  [#1358](https://github.com/ISISComputingGroup/IBEX/issues/1358) | Minor | Minor refactor of instrument switching code, should cause no behaviour change. |
|  [#1930](https://github.com/ISISComputingGroup/IBEX/issues/1930) | Minor | Make device screens available by default. |
|  [#1806](https://github.com/ISISComputingGroup/IBEX/issues/1806) | Patch | Close activeMQ connection to instrument in alarm perspective on switch instruments. |
|  [#1932](https://github.com/ISISComputingGroup/IBEX/issues/1932) | Patch | Fixed a bug where synoptic menu items were not being disabled at startup. |
|  [#1933](https://github.com/ISISComputingGroup/IBEX/issues/1933) | Patch | Removed some console messages in GUI startup. |
|  [#1530](https://github.com/ISISComputingGroup/IBEX/issues/1530) | Minor | Added a function for finding a free port and added it to the Julabo. |
|  [#1938](https://github.com/ISISComputingGroup/IBEX/issues/1938) | Minor | Fix a bug where the Kepco IOC wouldn't start in recsim mode. |
|  [#1939](https://github.com/ISISComputingGroup/IBEX/issues/1939) | Patch | Fix a units error in the Kepco IOC. |
|  [#1263](https://github.com/ISISComputingGroup/IBEX/issues/1263) | Minor | Add a get_version() command to genie python and display the current version on startup. |
|  [#1904](https://github.com/ISISComputingGroup/IBEX/issues/1904) | Major | Changed the Kepco OPI to the new style and modified it's macro to take the full IOC name (e.g. KEPCO_01) rather than just it's numeric identifier (e.g. 01). |
|  [#1810](https://github.com/ISISComputingGroup/IBEX/issues/1810) | Patch | Fixed a bug allowing users to save device screens with a blank (non-existent) target OPI. |
|  [#1289](https://github.com/ISISComputingGroup/IBEX/issues/1289) | Minor | Tidied up OPIs macros and descriptions that can be set via the synoptic. |
|  [#1903](https://github.com/ISISComputingGroup/IBEX/issues/1903) | Minor | Added a throttle to the Eurotherm IOC read PVs so that using extra sensors does not result in timeouts. |
|  [#1903](https://github.com/ISISComputingGroup/IBEX/issues/1903) | Minor | Eurotherm set points can now be  greater than 99.99 |
|  [#1903](https://github.com/ISISComputingGroup/IBEX/issues/1903) | Minor | Fixed an issue with the Eurotherm IOC whereby small negative values were not read correctly |
|  [#1967](https://github.com/ISISComputingGroup/IBEX/issues/1967) | Minor | Fixed bug in getting local PV in genie python |
|  [#1934](https://github.com/ISISComputingGroup/IBEX/issues/1934) | Patch | Fixed a bug where ampersands were appearing on perspective buttons. |
|  [#1944](https://github.com/ISISComputingGroup/IBEX/issues/1944) | Minor | Fixed bug where a git lock can stop the device screens PVs being populated. |
|  [#1881](https://github.com/ISISComputingGroup/IBEX/issues/1881) | Minor | Added volumetric rig emulator, added lewis to genie_python, and removed plankton from sub modules |
|  [#1611](https://github.com/ISISComputingGroup/IBEX/issues/1611) | Minor | Duplicate component names in synoptic editor gives a better error message |
|  [#1840](https://github.com/ISISComputingGroup/IBEX/issues/1840) | Patch | Update OPI for muon front end. |
|  [#1940](https://github.com/ISISComputingGroup/IBEX/issues/1940) | Minor | Added java version and path to the Help->About menu |
|  [#1941](https://github.com/ISISComputingGroup/IBEX/issues/1941) | Minor | The JRE is now bundled with the client |
|  [#1981](https://github.com/ISISComputingGroup/IBEX/issues/1981) | Minor | Fixed a bug where the syntax `cset("block_name", value, wait=True)` wasn't allowed by genie_python |
|  [#1906](https://github.com/ISISComputingGroup/IBEX/issues/1905) | Patch | Made a script to check formatting of new OPIs. |
|  [#1969](https://github.com/ISISComputingGroup/IBEX/issues/1969) | Patch | Minor rework of the ordering of queries sent to the Eurotherm |
|  [#1826](https://github.com/ISISComputingGroup/IBEX/issues/1826) | Minor | Added Keithley 2400 Source Meter IOC, OPI and emulator |
|  [#1990](https://github.com/ISISComputingGroup/IBEX/issues/1990) | Minor | Add galil special move command for MUONFE |
|  [#2011](https://github.com/ISISComputingGroup/IBEX/issues/2011) | Minor | Rename Keithley |


# What components have been changed

1. TPG
1. SDTEST
1. Experiment Details (RB Numbers)
1. Blockserver
1. McLennan
1. Eurotherm
1. IOC started in parallel on load
1. Motor logging
1. FINS
1. SKFChopper
1. ActiveMQ (Logging and alarms)
1. Instrument Switching
1. Kepco
