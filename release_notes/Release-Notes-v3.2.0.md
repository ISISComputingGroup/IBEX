# Dependencies

- MySQL 5.6.34
- JRE 1.8.0 update 121

## Changes to make on specific instruments when releasing

- POLARIS - Ticket 2082/2083:
   Ensure that the jaws.cmd for Polaris is the same as in https://github.com/ISISComputingGroup/ibex_gui/pull/475/ (note: the motor numbers in that PR are just dummies; they will need changing to the actual motor numbers)

- IRIS - Ticket 2176
IRIS specifically asked for a single chopper (Mk3) OPI. Now that this is available, their synoptics should be changed to use the single chopper OPI rather than the "standard" multi-chopper OPI

- IMAT - Ticket 2110
Get the latest version of the Instron Stress Rig VI, which should be updated to have newline characters removed from all its labels (specifically, "Waveform Running", "Cross Sectional Area (mm^2)", "Going to setpoint")

- ALF - Ticket 2071
Check that synoptics and device screens containing the goniometer still work (check that the OPI opens correctly). You will need to remove the "old" goniometer and then add in the "new" goniometer to synoptics.


- HRPD - Ticket 2219
Follow the test procedure when setting up the Jaws.

### All instruments

- Ticket 2004:
   Update the installed version of MySQL using the instructions on the [deployment page](https://github.com/ISISComputingGroup/ibex_developers_manual/wiki/Deployment-on-an-Instrument-Control-PC).

- Ticket 1749:
    Genie python should now be imported as `g` by default. Existing scripts can have `from genie_python import genie as g` removed, but check that they still work after this change.

- General:
    Check the settings directory (`c:\Instrument\Settings` and children) to ensure it contains only 1 copy of `globals.txt` and that this is in `C:\Instrument\Settings\config\<INST NAME>\configurations`. If you find any other copies of `globals.txt`, copy the content into the genuine `globals.txt` file and comment it out.  Then delete the redundant copies of `globals.txt`.

- Ticket 1875:
    Applies mostly to IRIS. Configurations containing McLennans need updating to the new macros. Specifically, `MRES` has been replaced by `MSTP`. The relation will typically be `MSTP=1/MRES`. `MSTP` is often the denominator in the encoder ratio, though not always (the `ERES` fraction may have been simplified). If the value can't be derived elsewhere, check the original VI settings.

## Summary of all changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|  [#1814](https://github.com/ISISComputingGroup/IBEX/issues/1814) | Patch | Corrected a bug where the upper/lower limit icons in the motors perspective were highlighted the wrong way around (e.g. upper limit icon highlighted when motor at lower limit) |
|  [#1238](https://github.com/ISISComputingGroup/IBEX/issues/1238) | Minor | Add GUI for the ZOOM sample stack |
|  [#1804](https://github.com/ISISComputingGroup/IBEX/issues/1804) | Minor | Overhauled IOC adding/editing process |
|  [#2044](https://github.com/ISISComputingGroup/IBEX/issues/2044) | Patch | Updated McLennan velocity macro description so that the units are in "units/s" rather than "mm/s" since the length unit is variable depending on the other macros |
|  [#2056](https://github.com/ISISComputingGroup/IBEX/issues/2056) | Patch | Monitor spectrum numbers up to 1 million can now be set via the client. The previous limit was 100. |
|  [#2007](https://github.com/ISISComputingGroup/IBEX/issues/2007) | Patch | Component dependencies update correctly when component is added to multiple configs |
|  [#2006](https://github.com/ISISComputingGroup/IBEX/issues/2006) | Minor | Added component details to config editing backend |
|  [#2031](https://github.com/ISISComputingGroup/IBEX/issues/2031) | Patch | Fixed bug where component names were not being copied to save dialog. |
|  [#1756](https://github.com/ISISComputingGroup/IBEX/issues/1756) | Minor | Connected NICOS to the GUI backend. |
|  [#2049](https://github.com/ISISComputingGroup/IBEX/issues/2049) | Minor | Removed the selection of default synoptic for components in the GUI |
|  [#2077](https://github.com/ISISComputingGroup/IBEX/issues/2077) | Patch| Add missing activemq and nicos plugins | |
|  [#1229](https://github.com/ISISComputingGroup/IBEX/issues/1229) | Patch | Updated GUI to CS-Studio 3.3.11 |
|  [#1987](https://github.com/ISISComputingGroup/IBEX/issues/1987) | Patch | Fixed an issue where the motor details view didn't get scrollbars. |
|  [#1749](https://github.com/ISISComputingGroup/IBEX/issues/1749) | Minor | Make genie python's `g` available by default. |
|  [#1666](https://github.com/ISISComputingGroup/IBEX/issues/1666) | Patch | Edit default instrument script to be in line with #1749. |
|  [#1827](https://github.com/ISISComputingGroup/IBEX/issues/1827) | Minor | Added support for CCD100 |
|  [#2075](https://github.com/ISISComputingGroup/IBEX/issues/2075) | Minor| Add TS1 only option to genie_python. |
|  [#2091](https://github.com/ISISComputingGroup/IBEX/issues/2091) | Minor| Update epics seq to 2.1.21. |
|  [#2050](https://github.com/ISISComputingGroup/IBEX/issues/2050) | Minor| Update epics asyn to 4.30. |
|  [#2092](https://github.com/ISISComputingGroup/IBEX/issues/2092) | Minor| Update Stream Device to 2.7.7. |
|  [#2076](https://github.com/ISISComputingGroup/IBEX/issues/2076) | Minor | Add option for ts1 only timing source to GUI. |
|  [#2063](https://github.com/ISISComputingGroup/IBEX/issues/2063) | Patch | Fixed a bug which meant TPG300 02 and 03 wouldn't start. |
|  [#2003](https://github.com/ISISComputingGroup/IBEX/issues/2003) | Minor | Add OpenSSL for curl. |
|  [#2100](https://github.com/ISISComputingGroup/IBEX/issues/2100) | Minor | Add AreaDetector for DAE. |
|  [#1961](https://github.com/ISISComputingGroup/IBEX/issues/1961) | Minor | Fixed a bug which caused the coloured borders around blocks to slip out of place |
|  [#2079](https://github.com/ISISComputingGroup/IBEX/issues/2079) | Minor | CA Channel error messages will no longer be printed in the console when trying to connect to a PV that does not exist. The genie_python error `ERROR: PV MY_PV does not exist` will still be printed as before. |
|  [#2059](https://github.com/ISISComputingGroup/IBEX/issues/2059) | Minor | Added a title to the PV selector dialog. |
|  [#1973](https://github.com/ISISComputingGroup/IBEX/issues/1973) | Minor | When sorting a list of device screens, the sort is now case insensitive (e.g. `a` comes before `B`) |
|  [#2057](https://github.com/ISISComputingGroup/IBEX/issues/2057) | Patch | Make error messages when naming configs/pvs etc more intuitive |
|  [#1979](https://github.com/ISISComputingGroup/IBEX/issues/1979) | Minor | Allow LVDCOM Options to be set on 3D magnet |
|  [#1854](https://github.com/ISISComputingGroup/IBEX/issues/1854) | Patch | GUI icon is now transparent |
|  [#1952](https://github.com/ISISComputingGroup/IBEX/issues/1952) | Minor | lvDCOM flag to wait for labview. |
|  [#2048](https://github.com/ISISComputingGroup/IBEX/issues/2048) | Minor | Descriptions now accompany each of the IOCs in the IOC and configuration editor dialogs. |
|  [#1985](https://github.com/ISISComputingGroup/IBEX/issues/1985) | Minor | Fix a GUI freeze during log message searches |
|  [#2135](https://github.com/ISISComputingGroup/IBEX/issues/2135) | Patch | Fix a resource leak causing one thread to use an entire core's worth of CPU |
|  [#2096](https://github.com/ISISComputingGroup/IBEX/issues/2096) | Minor | Allow multiple build architectures in same source tree. |
|  [#2087](https://github.com/ISISComputingGroup/IBEX/issues/2087) | Patch | Fix an issue where the log messages did not switch when the instrument is switched |
|  [#2074](https://github.com/ISISComputingGroup/IBEX/issues/2074) | Patch | Refactored synoptic code to try and fix a number of errors. Already included as part of release 3.1.1 |
|  [#1695](https://github.com/ISISComputingGroup/IBEX/issues/1695) | Minor | Auto-generate lvDCOM files from SECI blocks. |
|  [#2016](https://github.com/ISISComputingGroup/IBEX/issues/2016) | Minor | Java path in about dialog now wraps |
|  [#1752](https://github.com/ISISComputingGroup/IBEX/issues/1752) | Minor | Add ability to store device screens locally as well as remotely. |
|  [#1949](https://github.com/ISISComputingGroup/IBEX/issues/1949) | Patch | Fix typos in startup scripts. |
|  [#2026](https://github.com/ISISComputingGroup/IBEX/issues/2026) | Minor | Add DAE3 parallel running. |
|  [#2150](https://github.com/ISISComputingGroup/IBEX/issues/2150) | Patch | Fixed bug where IOC macros could not be edited. |
|  [#2175](https://github.com/ISISComputingGroup/IBEX/issues/2175) | Minor | Change published install kit root. |
|  [#1946](https://github.com/ISISComputingGroup/IBEX/issues/1946) | Patch | Fixed a potential deadlock during startup |
|  [#2125](https://github.com/ISISComputingGroup/IBEX/issues/2125) | Patch | Removed redundant message on the save synoptic and save config dialogs. |
|  [#1875](https://github.com/ISISComputingGroup/IBEX/issues/1875) | Minor | Fixed the McLennan IOC so that it can support multiple axes on the same crate |
|  [#1875](https://github.com/ISISComputingGroup/IBEX/issues/1875) | Minor | Replaced McLennan `MRES` macro with `MSTP`. The latter is the number of motor pulses per real-world unit. The relation will typically be `MSTP=1/MRES` |
|  [#2000](https://github.com/ISISComputingGroup/IBEX/issues/2000) | Patch | Fixed a bug where if one McLennan axis was set to open loop mode then it would apply to all axes on that controller |
|  [#2000](https://github.com/ISISComputingGroup/IBEX/issues/2000) | Minor | Added the ability to select from a number of homing modes |
|  [#2071](https://github.com/ISISComputingGroup/IBEX/issues/2071) | Minor | Rewrite ALF's goniometer OPI in CSS. |
|  [#2156](https://github.com/ISISComputingGroup/IBEX/issues/2156) | Patch | Fixed bug where IOC macros could not be set |
|  [#2021](https://github.com/ISISComputingGroup/IBEX/issues/2021) | Minor | The jog buttons in the motor OPI are now toggles |
|  [#1758](https://github.com/ISISComputingGroup/IBEX/issues/1758) | Minor | Convert lakeshore 336 OPI to new style |
|  [#2045](https://github.com/ISISComputingGroup/IBEX/issues/2045) | Minor | Allow Keithley 2400 general input reads/writes to function independently. |
|  [#2193](https://github.com/ISISComputingGroup/IBEX/issues/2193) | Minor| Build EPICS_UTILS with Jenkins |
|  [#1843](https://github.com/ISISComputingGroup/IBEX/issues/1843) | Minor | Added support for a NANODAC device |
|  [#2161](https://github.com/ISISComputingGroup/IBEX/issues/2161) | Patch | Add logging to PVManager to try to catch the cause of the blank IOC list |
|  [#2001](https://github.com/ISISComputingGroup/IBEX/issues/2001) | Minor | Improved feedback when attempting to delete components that are used in configurations. |
|  [#1364](https://github.com/ISISComputingGroup/IBEX/issues/1364) | Patch | Script Server: Send a script to NICOS from the GUI |
|  [#1846](https://github.com/ISISComputingGroup/IBEX/issues/1846) | Minor | Add run diagnostics 2 IOC support |
|  [#2124](https://github.com/ISISComputingGroup/IBEX/issues/2124) | Minor| Allowed multiple devices to be deleted in the device screens |
|  [#1766](https://github.com/ISISComputingGroup/IBEX/issues/1766) | Patch | Ampersands can now be set to the DAE title/users |
|  [#2210](https://github.com/ISISComputingGroup/IBEX/issues/2210) | Minor | Add stubs for the PLC so that it is easier to update post-release. |
|  [#2098](https://github.com/ISISComputingGroup/IBEX/issues/1846) [#2219](https://github.com/ISISComputingGroup/IBEX/issues/2219) | Minor | Add LinMot motor support |
|  [#2083](https://github.com/ISISComputingGroup/IBEX/issues/2083) | Minor | Add support for the jaw set on polaris |
|  [#2082](https://github.com/ISISComputingGroup/IBEX/issues/2082) | Major | Add support for access security |
|  [#2130](https://github.com/ISISComputingGroup/IBEX/issues/2130) | Minor | Add MK2 chopper support |
|  [#2172](https://github.com/ISISComputingGroup/IBEX/issues/2172) | Minor | IOC macro text now updates better |
|  [#2176](https://github.com/ISISComputingGroup/IBEX/issues/2176) | Minor | Create an OPI for a single Mk3 chopper |
|  [#2052](https://github.com/ISISComputingGroup/IBEX/issues/2052) | Minor | Change controls for selecting spectra number/period from text field to spinner |
|  [#2227](https://github.com/ISISComputingGroup/IBEX/issues/2227) | Patch | Sort configs list case insensitively |
|  [#1884](https://github.com/ISISComputingGroup/IBEX/issues/1884) | Minor | Added a check for duplicate blocks when adding components to a config |
|  [#2144](https://github.com/ISISComputingGroup/IBEX/issues/2144) | Patch | Fixed bug where disconnected runtime PV was crashing website |
|  [#1996](https://github.com/ISISComputingGroup/IBEX/issues/1996) | Patch | Updated genie_python to Lewis 1.0.2 |
|  [#1698](https://github.com/ISISComputingGroup/IBEX/issues/1698) | Minor | Updated the script checker to check for 'g' and 'inst' on genie_python on the IBEX GUI |
|  [#2104](https://github.com/ISISComputingGroup/IBEX/issues/2104) | Minor | Restart stuck block archiver on BEGIN |
|  [#2232](https://github.com/ISISComputingGroup/IBEX/issues/2232) | Patch | Ensure that scripting and alarms perspectives close and reopen on instrument switch |
|  [#2221](https://github.com/ISISComputingGroup/IBEX/issues/2221) | Patch | Add interest field to eurotherm autotune |
|  [#2110](https://github.com/ISISComputingGroup/IBEX/issues/2110) | Minor | lvDCOM IOC wrapper for Stress Rig vi |
|  [#2109](https://github.com/ISISComputingGroup/IBEX/issues/2109) | Minor | lvDCOM OPI |
|  [#1828](https://github.com/ISISComputingGroup/IBEX/issues/1828) | Minor | Add Neocera LTC21 device support |
|  [#1235](https://github.com/ISISComputingGroup/IBEX/issues/1235) | Minor | Add DAE areaDetector support for ZOOM |
|  [#2238](https://github.com/ISISComputingGroup/IBEX/issues/1235) | Minor | Add ad_kafka_interface for data streaming |
|  [#2023](https://github.com/ISISComputingGroup/IBEX/issues/2023) | Patch | Fix an infrequent crash of the DAE perspective |
|  [#2173](https://github.com/ISISComputingGroup/IBEX/issues/2173) | Minor | Added device support for rotating sample changer |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
