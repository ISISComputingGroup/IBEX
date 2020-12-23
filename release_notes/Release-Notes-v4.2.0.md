# Dependencies

- MySQL 5.7.17
- JRE 1.8.0 update 161

## Changes to make on specific instruments when releasing

### Polaris

- [#2695](https://github.com/ISISComputingGroup/IBEX/issues/2695)
    * In the component keithley_voltage, set the IEOS and OEOS macros to be `\\r` (note the double backslash).

### MUONFE

- [Ticket 2334](https://github.com/ISISComputingGroup/IBEX/issues/2334): The muon_front_end OPI has been removed in favour of a single slit set OPI.
  * Remove the synoptic called "slits"
  * In the MuonFE synoptic, change the "momentum slits" item to refer to the new OPI

### IRIS

- Ticket 2605: Check that the MK3 Chopper IOC correctly identifies and displays in the GUI when the chopper is switched between remote and local mode.

## All instruments

- [#2477](https://github.com/ISISComputingGroup/IBEX/issues/2477)
   * This is make the dataweb stop working so you must release a new version of the dataweb. This means the roll out needs to be to all instruments that appear on the dataweb.
   * The dataweb fails when trying to get RUNDURATION_PD, if you fix this then block will be missing because the alarm signal has gone from OK to blank so the `block_raw.split(None, 3)` return 3 instead of 4 elements and the channel is ignored.

- Ticket 2787: The way the Galils load DBs has changed significantly. Make sure the configuration upgrade script is run and that any configurations with Galils correctly load the expected Galil. 

## Summary of all changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|  [#1672](https://github.com/ISISComputingGroup/IBEX/issues/1672) | Patch | Hide groups containing only hidden blocks |
| [#2522](https://github.com/ISISComputingGroup/IBEX/issues/2522)  | Minor | Added engin-x collimator continuous scan script |
| [#2334](https://github.com/ISISComputingGroup/IBEX/issues/2334)  | Minor | Add OPI for slit set with a single degree of freedom |
| [#2563](https://github.com/ISISComputingGroup/IBEX/issues/2563) | Patch | Fix dragging and dropping synoptic elements |
| [#2574](https://github.com/ISISComputingGroup/IBEX/issues/2574) | Patch | Improve handling of configuration version control |
| [#2508](https://github.com/ISISComputingGroup/IBEX/issues/2508)  | Patch | Set PVs by string in Genie Python  |
| [#2592](https://github.com/ISISComputingGroup/IBEX/issues/2592) | Minor | Fixed a bug in danfysik 8800 where power pv was incorrectly reporting |
| [#2437](https://github.com/ISISComputingGroup/IBEX/issues/2437)  | Minor | Add IOC for X-Y Beamstop |
| [#2292](https://github.com/ISISComputingGroup/IBEX/issues/2292)  | Minor | Moved edit screens button on Device Screens panel |
| [#2465](https://github.com/ISISComputingGroup/IBEX/issues/2465)  | Minor | Changed Eurotherm to ramp in Kelvin per minute |
| [#2564](https://github.com/ISISComputingGroup/IBEX/issues/2564)  | Minor | Load script now prints the time the script was last modified |
| [#2571](https://github.com/ISISComputingGroup/IBEX/issues/2571) | Minor | Fix drag and drop (remove hack) |
| [#2621](https://github.com/ISISComputingGroup/IBEX/issues/2621) | Minor | Remove warning on first access of block in scripting window |
| [#2629](https://github.com/ISISComputingGroup/IBEX/issues/2629) | Minor | Correct magnitude error in Fermi Chopper phase delay setpoint |
| [#2632](https://github.com/ISISComputingGroup/IBEX/issues/2632) | Minor | Update IEG errors |
| [#2621](https://github.com/ISISComputingGroup/IBEX/issues/2632) | Minor | Update variable precision in Fermi Chopper |
| [#2656](https://github.com/ISISComputingGroup/IBEX/issues/2656) | Minor | Allow setting fermi chopper veto from script |
| [#2665](https://github.com/ISISComputingGroup/IBEX/issues/2665) | Patch | Fix zoom plc writing |
| [#628](https://github.com/ISISComputingGroup/IBEX/issues/628) | Minor | DAE has PV for sim mode rather than modifying title |
| [#2672](https://github.com/ISISComputingGroup/IBEX/issues/2672) | Patch | Reduce number of times DB is polled to check that log file should be written |
| [#2594](https://github.com/ISISComputingGroup/IBEX/issues/2594) | Patch | Remove setpoint alarm from positioner |
| [#2624](https://github.com/ISISComputingGroup/IBEX/issues/2624) | Minor | Simplify version control on instrument config directories |
| [#2345](https://github.com/ISISComputingGroup/IBEX/issues/2345) | Minor | Compress added git directory (added in previous release)  |
| [#2586](https://github.com/ISISComputingGroup/IBEX/issues/2586) | Minor | Don't start iocs on mini inst |
| [#2577](https://github.com/ISISComputingGroup/IBEX/issues/2577) | Patch | Improve performance on configuration changes |
| [#2307](https://github.com/ISISComputingGroup/IBEX/issues/2307) | Minor | Make proper errors appear if gui doesn't understand configuration |
| [#1335](https://github.com/ISISComputingGroup/IBEX/issues/1335) | Patch | Error conditions on change commands not shown to user |
| [#2296](https://github.com/ISISComputingGroup/IBEX/issues/2296) | Minor | Table of motors now shows useful description for each axis |
| [#2604](https://github.com/ISISComputingGroup/IBEX/issues/2604) | Minor | Purple border around blocks when underlying PV is in INVALID state |
| [#2548](https://github.com/ISISComputingGroup/IBEX/issues/2548) | Patch | Updated genie_python dependencies |
| [#2580](https://github.com/ISISComputingGroup/IBEX/issues/2580) | Patch | Allow dashes in PV names |
| [#2660](https://github.com/ISISComputingGroup/IBEX/issues/2660) | Minor | Add missing fermi chopper parameters |
| [#2627](https://github.com/ISISComputingGroup/IBEX/issues/2627) | Minor | Added a configuration checker |
| [#2712](https://github.com/ISISComputingGroup/IBEX/issues/2712) | Patch | Allow passing parameters to genie_python.bat |
| [#2477](https://github.com/ISISComputingGroup/IBEX/issues/2477) | Minor | Update the archive engine to use Json |
| [#2695](https://github.com/ISISComputingGroup/IBEX/issues/2695) | Patch | Make Keithley 2400 terminator configurable |
| [#2639](https://github.com/ISISComputingGroup/IBEX/issues/2639) | Patch | Enhanced deployment script for instruments. Now prompts for SECI shortcut cleanup |
| [#2693](https://github.com/ISISComputingGroup/IBEX/issues/2693) | Patch | Prevent Keithley crash with disconnected sensors |
| [#2633](https://github.com/ISISComputingGroup/IBEX/issues/2633) | Patch | Prevent Mk3 chopper crash on error by fixing overflow |
| [#2758](https://github.com/ISISComputingGroup/IBEX/issues/2758) | Patch | Limit IEG pressure reading to be > 0 and tweak OPI |
| [#1704](https://github.com/ISISComputingGroup/IBEX/issues/1704) | Minor | Can disable FIFO veto via genie python |
| [#2535](https://github.com/ISISComputingGroup/IBEX/issues/2535) | Patch | Add support for Oscillating Collimator (LET) |
| [#1343](https://github.com/ISISComputingGroup/IBEX/issues/1343) | Minor | Fix send_sms and and send_email and send_alert (for slack) |
| [#2579](https://github.com/ISISComputingGroup/IBEX/issues/2579) | Minor | Make synoptic editor more user friendly |
| [#2778](https://github.com/ISISComputingGroup/IBEX/issues/2579) | Minor | Add MUONFE to web dashboard |
| [#2780](https://github.com/ISISComputingGroup/IBEX/issues/2780) | Minor | Added tooltips to icons in table of motors |
| [#2605](https://github.com/ISISComputingGroup/IBEX/issues/2605) | Minor | Remote/Local light for MK3Chopper |
| [#2734](https://github.com/ISISComputingGroup/IBEX/issues/2734) | Minor | Include a link to report bugs on the Webdashboard |
| [#2503](https://github.com/ISISComputingGroup/IBEX/issues/2503) | Patch | Fixed handling of attempts to name a group "Other" |
| [#2785](https://github.com/ISISComputingGroup/IBEX/issues/2785) | Minor | Added MISS and RCNT fields to archive |
| [#1197](https://github.com/ISISComputingGroup/IBEX/issues/1197) | Minor | Added generic sample stack OPI |
| [#2748](https://github.com/ISISComputingGroup/IBEX/issues/2748) | Patch | Fixed error in `genie_python` `plot_spectrum` |
| [#2653](https://github.com/ISISComputingGroup/IBEX/issues/2653) | Minor | Eurotherm: Ramp is disabled when no sensor is connected |
| [#2718](https://github.com/ISISComputingGroup/IBEX/issues/2718) | Minor | Add access security to Mk3 Chopper |
| [#2365](https://github.com/ISISComputingGroup/IBEX/issues/2365) | Minor | Add support for emma's fermi chopper lift |
| [#2776](https://github.com/ISISComputingGroup/IBEX/issues/2776) | Minor | Allow any number of user PVs. |
| [#2687](https://github.com/ISISComputingGroup/IBEX/issues/2687) | Minor | Allow selection of "absolute counts" Y axis in spectra plots. |
| [#2784](https://github.com/ISISComputingGroup/IBEX/issues/2784) | Patch | Fixed a bug in the oscillating collimator where velocities were not correctly set on the hardware |
| [#2787](https://github.com/ISISComputingGroup/IBEX#2787) | Minor | Galils now load dbs in a much more standard way. (This is not backward compatible in that the all configurations will need to be updated, it is backward compatible with old GUIs) |
| [#2607](https://github.com/ISISComputingGroup/IBEX#2607) | Minor | Created Galil specific OPI |
| [#2820](https://github.com/ISISComputingGroup/IBEX#2820) | Patch | Runcontrol periodically checks it is in the correct state |
| [#2086](https://github.com/ISISComputingGroup/IBEX#2086) | Patch | Read multiple bytes from serial |
| [#2643](https://github.com/ISISComputingGroup/IBEX/issues/2643) | Patch | Fix threading issue causing DAE buttons to be greyed out in setup. |
| [#2825](https://github.com/ISISComputingGroup/IBEX/issues/2825) | Minor | Message in drop down for DAE tables now points users to the correct location.  |
| [#2409](https://github.com/ISISComputingGroup/IBEX/issues/2409) | Minor | Add support for the GEM oscillating radial collimator |
| [#2789](https://github.com/ISISComputingGroup/IBEX/issues/2789) | Minor | Added ability to lock axes behind manager mode |
| [#2691](https://github.com/ISISComputingGroup/IBEX/issues/2691) | Minor | Add warning for lowlimit/highlimit swap |
| [#2663](https://github.com/ISISComputingGroup/IBEX/issues/2663) | Minor | Make E4 build run on maven+jenkins. |
| [#2663](https://github.com/ISISComputingGroup/IBEX/issues/2663) | Minor | Log Plotter Perspective E4 Migration |
| [#2149](https://github.com/ISISComputingGroup/IBEX/issues/2149) | Minor | Add ability to see currently executing script and line in NICOS scripting |
| [#2801](https://github.com/ISISComputingGroup/IBEX/issues/2801) | Minor | Script to support Keithley 2420 being used on Polaris |
| [#2803](https://github.com/ISISComputingGroup/IBEX#2803) | Minor | genie_python is now compatible with Python 2 and 3 |
| [#2723](https://github.com/ISISComputingGroup/IBEX#2723) | Minor | Add infrastructure to journal parser to put run information into IBEX database |
| [#2769](https://github.com/ISISComputingGroup/IBEX/issues/2769) | Minor | Shutter status is now on web dashboard |
| [#2397](https://github.com/ISISComputingGroup/IBEX/issues/2397) | Minor | Add support for SKF MB350 chopper |
| [#2755](https://github.com/ISISComputingGroup/IBEX/issues/2755) | Minor | Fixed bug where only 'other' blocks could be added to synoptics |
| [#2191](https://github.com/ISISComputingGroup/IBEX/issues/2191) | Minor | Galil will now reconnect in sync mode if Galil controller stops sending UDP DR packets |
| [#2843](https://github.com/ISISComputingGroup/IBEX/issues/2843) | Patch | The generic sample stack OPI no longer generates two of the same label for similarly named axes |
| [#2796](https://github.com/ISISComputingGroup/IBEX/issues/2796) | Minor | The unit tests for the database server now run without needing a database |
| [#2697](https://github.com/ISISComputingGroup/IBEX/issues/2697) | Minor | Added script to get all motor params |
| [#2845](https://github.com/ISISComputingGroup/IBEX/issues/2845) | Minor | `genie_python` no longer hangs on `None` input to `waitfor` commands |
| [#2760](https://github.com/ISISComputingGroup/IBEX/issues/2760) | Minor | Send reset before every move on McLennans |
| [#2839](https://github.com/ISISComputingGroup/IBEX/issues/2839) | Minor | Number of flows in CCD100 OPI changes depending on number of macros |
| [#2419](https://github.com/ISISComputingGroup/IBEX/issues/2419) | Minor | Display current PVPrefix in Help -> About |
| [#2657](https://github.com/ISISComputingGroup/IBEX/issues/2657) | Minor | Display simulation mode indicator in banner |
| [#2659](https://github.com/ISISComputingGroup/IBEX/issues/2659) | Minor | Add DAE simulation mode to dataweb. |
| [#2644](https://github.com/ISISComputingGroup/IBEX/issues/2644) | Patch | Add check for double colons in PVs to the PV Validator |
| [#2824](https://github.com/ISISComputingGroup/IBEX/issues/2824) | Patch | Fix blockserver crash when many synoptics |
| [#2844](https://github.com/ISISComputingGroup/IBEX/issues/2844) | Minor | Fixed script for upgrading galil macros |
| [#2762](https://github.com/ISISComputingGroup/IBEX/issues/2762) | patch | Graph of heater output on Eurotherm has correct number of points |
| [#2466](https://github.com/ISISComputingGroup/IBEX/issues/2466) | Patch | Add error message for nonexistent blocks in waitfor |
| [#1897](https://github.com/ISISComputingGroup/IBEX/issues/1897) | Patch | Open motor OPIs now close on changing instrument |
| [#2014](https://github.com/ISISComputingGroup/IBEX/issues/2014) | Patch | Default synoptics can now be deleted |
| [#2527](https://github.com/ISISComputingGroup/IBEX/issues/2527) | Patch | Default synoptic no longer says "(recommended)". There is a new button in the synoptic perspective for loading the default synoptic for the current configuration. The default synoptic for a configuration is also now `-- NONE --` if no default synoptic was selected at creation |
| [#2447](https://github.com/ISISComputingGroup/IBEX/issues/2447) | Patch | Removing IOCs from the active configuration stops them. |
| [#2667](https://github.com/ISISComputingGroup/IBEX/issues/2667) | Patch | Add alarms to instron IOC |
| [#1992](https://github.com/ISISComputingGroup/IBEX/issues/1992) | Patch | allow opening device screens on disconnected instrument |
| [#2749](https://github.com/ISISComputingGroup/IBEX/issues/2749) | Minor | Make MAX_OUPUT appear on medium interest PVs in GUI. |
| [#1332](https://github.com/ISISComputingGroup/IBEX/issues/1332) | Patch | Changes to run state are now validated before execution. Invalid changes (e.g. paused to beginning) are discarded prior to execution |
| [#2848](https://github.com/ISISComputingGroup/IBEX/issues/2848) | Patch | Fix IOC Tests and System Tests |
| [#1907](https://github.com/ISISComputingGroup/IBEX/issues/1907) | Patch | Fixed issue with activating tab on SKF G5 OPI |
| [#2812](https://github.com/ISISComputingGroup/IBEX/issues/2812) | Minor | E4: Added missing parts in Beam Status perspective |
| [#2812](https://github.com/ISISComputingGroup/IBEX/issues/2812) | Patch | E4: Fixed connection to Alarm Server |
| [#646](https://github.com/ISISComputingGroup/EPICS-ioc/pull/210) | Minor | Lakeshore460 IOC/Emulator/OPI/Test Files |
| [#2566](https://github.com/ISISComputingGroup/IBEX/issues/2566) | Minor | Logging produces a file continuously while logging is on |
| [#2812](https://github.com/ISISComputingGroup/IBEX/issues/2812) | Minor | E4: Added scrollbars to all DAE perspective views |
| [#2727](https://github.com/ISISComputingGroup/IBEX/issues/2727) | Minor | Add `waitfor_raw_frames` command to genie.py |
| [#2846](https://github.com/ISISComputingGroup/IBEX/issues/2846) | Patch | Allow large numbers (over 2**31) to be entered in waitfor commands |
| [#2683](https://github.com/ISISComputingGroup/IBEX/issues/2683) | Minor | Eurotherm: Setpoint can be sent that is the same as the previous value after a sensor change |
| [#2707](https://github.com/ISISComputingGroup/IBEX/issues/2707) | Minor | Add support for Sandals sample changer and SM300 motor |
| [#2802](https://github.com/ISISComputingGroup/IBEX/issues/2802) | Minor | Fix waveform generator for the stress rig |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
