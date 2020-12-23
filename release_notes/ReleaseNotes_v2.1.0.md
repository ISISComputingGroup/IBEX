# TODO as part of this release

## MUON FRONT END 

* For ticket 1138: 
    1. Copy `...\EPICS\support\barndoors\master\settings\*.cmd` to `C:\Instrument\Settings\config\NDEMUONFE\configurations\galil`.
    1. Run the motor configuration script [Config file](../../IBEX.wiki/release/MUONFE%20Galil%20Config.txt)
* For ticket 1210:
    1. Add EXCLUSIVE1=:MFE to globals.txt
    1. Create gwext.acf and gwext.pvlist files in Settings\config\NDEMUONFE\AccessSecurity with the contents of [ACF](../../IBEX.wiki/release/MFE.acf) and [PVLIST](../../IBEX.wiki/release/MFE.pvlist) respectively

## LARMOR

* For ticket 1208:
    1. Set the Macro DFKPS_01__BAUD to 115200
    1. Remove the block for SETIRAW in blocks.xml in configurations\components\ISISSTAT
* For ticket 1414: the LAKESHORE218 IOC was renamed to LKSH218. As of 1/8/2016 there are no files needing updating in config/ but more recent files should be checked
* For ticket 1455:
    1. Go to the synoptics folder in the settings and do a search to replace "DANFSYIK" with "DANFYSIK". Then look for any synoptic using the TPG300, and replace the macro "N" (which has no value) with a macro called "TPG300" with value "TPG300_01"

## IMAT
* For ticket 1414: the LAKESHORE218 IOC was renamed to LKSH218. As of 1/8/2016 there are no files needing updating in config/ but more recent files should be checked
* For ticket 1455:
   1. Go to the synoptics folder in the settings and do a search to replace "DANFSYIK" with "DANFYSIK". Then look for any synoptic using the TPG300, and replace the macro "N" (which has no value) with a macro called "TPG300" with value "TPG300_01"
* For ticket 1210:
   1. Create a gwext.pvlist file in Settings\config\NDXIMAT\AccessSecurity with the contents of [PVLIST](../../IBEX.wiki/release/IMAT.pvlist)

## DEMO
* For ticket 1210:
    1. Add ACF_PV=ANYBODY to globals.txt

## ALL INSTRUMENTS

* For ticket 1425:
    1. Clone the common calibrations git repository to settings
        1. `cd /c/Instrument/Settings/config`
        1. `git clone http://control-svcs.isis.cclrc.ac.uk/gitroot/instconfigs/common.git`
    1. Ensure that all calibration files on the system are now located in this directory (check c/Instrument/Settings/calib and c/Instrument/Settings/configuration/calib). If there are file in here make sure they are the same or add them.
    1. If any configurations have eurotherms in them then edit them and add the eurotherm addresses and port to the a macros. The macros `ADDR_1` should be set to 1, `ADDR_2` = 2 and `ADDR_3` = 3.
* For ticket 1421 - the _base component in Settings/config/NDXXX/configurations/components/_base/  does not match the schema for IOCS, Blocks, Groups etc.:
    1. Check out _base from master and copy it to the appropriate instrument directory on all the instrument machines (NDX)
    1. These changes then need to be checked back into the instrument branches

(Alternatively you can clone the config repository from scratch in a temporary directory somewhere outside the instrument, and then just copy the relevant files from there. Don't forget to commit. Instructions on what to clone are in the Backend Getting Started page, section "Setting up a configurations directory")
* Start_inst has been renamed to start_ibex_server for clarity
* For tickets 1209 and 1334:
     1. Update genie_python
* For ticket 1471:
    - The IOC DB schema has been updated to include an IOC description and details fields. There are two possible update methods depending on instrument type.
        1. Reform the DB schema. Note that this will completely reset the instrument database and so historical data may be lost. This is recommended for new or test instruments only.
            - To use this workflow, go to `C:\Instrument\Apps\EPICS\SystemSetup` and run `config_mysql.bat`. Then start the server as normal
        1. Add the new columns into the DB without disturbing the existing data
            1. Open a MySql terminal (go to command line and run "C:\Program Files\MySQL\MySQL Server 5.6\bin\mysql.exe" -u root -p, assuming its not in your PATH variables). As a reminder, the password can be found in `C:\Instrument\Apps\EPICS\CSS\master\ArchiveEngine\setup_mysql_database.txt`
            1. Run the following commands:
                - `Use iocdb;`
                - `Alter table iocs add column descr VARCHAR(100) COMMENT 'IOC full name/brief description';`
                - `Alter table iocs add column details TEXT COMMENT 'IOC details';`
            1. Start the IBEX server
* For ticket 1242:
    1. Verify that the DAE graphs are behaving as expected. We have updated the Nebula Visualization Widget plugin version in the GUI which may affect the behaviour of these components. Please report any issues through the usual channel.

# Changes since previous version

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|  [#1218](https://github.com/ISISComputingGroup/IBEX/issues/1218) | Minor | Custom instrument name must start with ND instead of NDW  |
| [#1374](https://github.com/ISISComputingGroup/IBEX/issues/1374) | Minor | Added functionality to show/hide experiment title on external displays (for future applications) |
|  [#1285](https://github.com/ISISComputingGroup/IBEX/issues/1285) | Minor | Add SIM records and OPI for Mercury iTC |
|  [#1362](https://github.com/ISISComputingGroup/IBEX/issues/1362) | Minor | NICOS Script Server starts as part of the instrument on development machines. It does not start on real instruments, but a message is displayed. |
|  [#1138](https://github.com/ISISComputingGroup/IBEX/issues/1138) | Minor | Muon front end: Barndoors and momentum slits |
|  [#1124](https://github.com/ISISComputingGroup/IBEX/issues/1124) | Minor | Device screens list in the GUI |
|  [#1325](https://github.com/ISISComputingGroup/IBEX/issues/1325) | Minor | Empty log plotter view gives sensible message |
|  [#1208](https://github.com/ISISComputingGroup/IBEX/issues/1208) | Minor | Improvements to the Danfysik IOC, including support for different models |
|  [#1274](https://github.com/ISISComputingGroup/IBEX/issues/1274) | Minor | Calculation Method and Time Channel File to DAE tab |
|  [#1411](https://github.com/ISISComputingGroup/IBEX/issues/1411) | Minor | Added TPG26x (ISIS Vacuum System) IOC and OPI |
|  [#1405](https://github.com/ISISComputingGroup/IBEX/issues/1405) | Minor | Added Iris cryo valve IOC and OPI |
|  [#1414](https://github.com/ISISComputingGroup/IBEX/issues/1414) | Minor | Renamed LAKESHORE218 IOC to LKSH218 |
|  [#1421](https://github.com/ISISComputingGroup/IBEX/issues/1421)  | Minor | IDE unit tests |
|  [#1406](https://github.com/ISISComputingGroup/IBEX/issues/1406) | Minor | Add MKS PDR 2000 pressure transducer |
|  [#1455](https://github.com/ISISComputingGroup/IBEX/issues/1455) | Minor | Correct spelling of Danfysik in synoptic view. Update Danfysik and TPG300 macros to use full PV names. This may require updates to Danfysik and TPG300 synoptic components currently in use |
|  [#1407](https://github.com/ISISComputingGroup/IBEX/issues/1407) | Minor | Modify sample changer to support Iris 1D version |
|  [#1253](https://github.com/ISISComputingGroup/IBEX/issues/1253) | Minor | Changed banner to display items from blockserver BANNER_DESCRIPTION PV (previously hardcoded) |
|  [#1485](https://github.com/ISISComputingGroup/IBEX/issues/1485) | Minor | Update build to explicitly make iocs (no wildcard) and tidy support makefile |
|  [#1445](https://github.com/ISISComputingGroup/IBEX/issues/1445) | Minor | Date created / modified labels in configuration summary tab now hidden if blank |
|  [#1404](https://github.com/ISISComputingGroup/IBEX/issues/1404) | Minor | Support for Lakeshore336 Temperature Controller |
|  [#1464](https://github.com/ISISComputingGroup/IBEX/issues/1464) | Minor | Added blank option to DAE table selection drop down menus to ensure changes are registered if only one file in list |
|  [#1403](https://github.com/ISISComputingGroup/IBEX/issues/1403) | Minor | Update for Eurotherm allowing more eurotherms |
|  [#1314](https://github.com/ISISComputingGroup/IBEX/issues/1314) | Minor | Mk3Chopper will automatically adjust to the number of choppers found on startup |
|  [#1209](https://github.com/ISISComputingGroup/IBEX/issues/1209) | Minor| TDK Lambda Genesys and Danfysik setpoints are autosaved and can be pushed to instrument at startup depending on a macro. Also, there is a genie_python command to reload the current configuration |
|  [#1322](https://github.com/ISISComputingGroup/IBEX/issues/1322) | Minor | Allowed user to remove user details individually |
|  [#1425](https://github.com/ISISComputingGroup/IBEX/issues/1425) | Minor | Calibration files are now in common directory |
|  [#1471](https://github.com/ISISComputingGroup/IBEX/issues/1471) | Minor | Added description and details to IOC database for future use in GUI |
|  [#1512](https://github.com/ISISComputingGroup/IBEX/issues/1512) | Minor | Added IOCs for Danfysiks 10 and 11 |
|  [#1210](https://github.com/ISISComputingGroup/IBEX/issues/1210) | Minor | Changes to provide more control over access security |
|  [#1398](https://github.com/ISISComputingGroup/IBEX/issues/1398) | Minor | Add 3D Magnet IOC |
|  [#1099](https://github.com/ISISComputingGroup/IBEX/issues/1099) | Minor | Introduce McLennan motor IOC |
|  [#1100](https://github.com/ISISComputingGroup/IBEX/issues/1100) | Minor | Widen motor record OPI to accommodate longer McLennan motor description |
|  [#1493](https://github.com/ISISComputingGroup/IBEX/issues/1493) | Minor | Added separate readback labels for currently set DAE tables / time channel & period files. |
|  [#1469](https://github.com/ISISComputingGroup/IBEX/issues/1469) | Minor | Add motor status PVs to motor-based IOCs other than Galils that provide human-readable motor status |
| [#1372](https://github.com/ISISComputingGroup/IBEX/issues/1372) | Patch | Perspectives can be hidden in preferences |
| [#1376](https://github.com/ISISComputingGroup/IBEX/issues/1376) | Patch | Install script bug fixed |
| [#1350](https://github.com/ISISComputingGroup/IBEX/issues/1350) | Patch | Allow deletion of multiple configuration and synoptics |
| [#1122](https://github.com/ISISComputingGroup/IBEX/issues/1122) | Patch (will not be available to users) | Device screens write xml to blockserver |
| [#1123](https://github.com/ISISComputingGroup/IBEX/issues/1123) | Patch (will not be available to users) | Factor out OPI display code from synoptics and device screens |
|  [#1165](https://github.com/ISISComputingGroup/IBEX/issues/1165) | Patch | RCPTT system test restart the block server |
|  [#1345](https://github.com/ISISComputingGroup/IBEX/issues/1345) | Patch | Turn off Genie python script checking |
|  [#1064](https://github.com/ISISComputingGroup/IBEX/issues/1064) | Patch | Factor out run control and synoptic manager |
|  [#1396](https://github.com/ISISComputingGroup/IBEX/issues/1396) | Patch | Fixed NoneType error when calling get_sample_pars and get_beamline_pars in genie_python |
|  [#1428](https://github.com/ISISComputingGroup/IBEX/issues/1428) | Patch | Empty log plotter view now works with plots from OPIs |
|  [#1438](https://github.com/ISISComputingGroup/IBEX/issues/1438) | Patch | Synoptic macro values can be edited even if OPI resources definition changes |
|  [#1462](https://github.com/ISISComputingGroup/IBEX/issues/1462)  | Patch | Fixed historic bug whereby the simlevel was saved as "None" instead of "none" in configurations. Currently blockserver patched to accept both versions on load |
| [#1394] (https://github.com/ISISComputingGroup/IBEX/issues/1394) | Patch | Fixed long config names not being visible on remote systems |
|  [#1467](https://github.com/ISISComputingGroup/IBEX/issues/1467) | Patch | Fixed a bug where changes made to IOCs in the edit config dialog would persist after cancelling |
|  [#1463](https://github.com/ISISComputingGroup/IBEX/issues/1463) | Patch | Fixed spelling mistake in spectra drop-down |
|  [#1501](https://github.com/ISISComputingGroup/IBEX/issues/1501) | Patch | Fixed usage of self.blockserver in genie_epics_api |
|  [#1498](https://github.com/ISISComputingGroup/IBEX/issues/1498) | Patch | Fixed blockserver unit tests for banner |
|  [#1480](https://github.com/ISISComputingGroup/IBEX/issues/1480) | Patch | Numbering of controller numbers in motors perspective has been corrected in the 8-16 and 17-24 tabs |
|  [#1477](https://github.com/ISISComputingGroup/IBEX/issues/1477) | Patch | Linkam95 IOC pump status PV fixed |
|  [#1513](https://github.com/ISISComputingGroup/IBEX/issues/1513) | Patch | Fixed GUI dependencies |
|  [#1334](https://github.com/ISISComputingGroup/IBEX/issues/1334) | Patch | Fixed a bug in load_script command which stopped it working on Windows |
|  [#1492](https://github.com/ISISComputingGroup/IBEX/issues/1492) | Patch | Icons now correctly show on tycho build |
|  [#1386](https://github.com/ISISComputingGroup/IBEX/issues/1386) | Patch | Fixed an non-critical exception on opening the beam status view |
|  [#1519](https://github.com/ISISComputingGroup/IBEX/issues/1519) | Patch | Fix RECSIM and DISABLE macros for cryo valve so it can be started in the requested mode from the GUI |
|  [#1468](https://github.com/ISISComputingGroup/IBEX/issues/1468) | Patch | Updated the sample changer IOC to fix an error message that was occurring with more than 10 motion set points  |
|  [#1509](https://github.com/ISISComputingGroup/IBEX/issues/1509) | Patch | Linkam95 IOC now sends initial T command before trying to set the pump to auto mode at startup |
|  [#1514](https://github.com/ISISComputingGroup/IBEX/issues/1514) | Patch | The Experimental Database does not go into a restart loop if no RB numbers file is found |
|  [#1420](https://github.com/ISISComputingGroup/IBEX/issues/1420) | Patch | The Experimental Database source folder has been renamed |
|  [#1402](https://github.com/ISISComputingGroup/IBEX/issues/1402) | Patch | Fixed a bug where spectra plots would not refresh properly after switching |
|  [#1100](https://github.com/ISISComputingGroup/IBEX/issues/1100) | Patch | The width of the motor OPI was increased to accommodate longer descriptions |
|  [#1488](https://github.com/ISISComputingGroup/IBEX/issues/1488) | Patch | Fixed a bug in Lakeshore336 IOC and made db unit checker error message more explicit |
|  [#1242](https://github.com/ISISComputingGroup/IBEX/issues/1242) | Patch | The GUI has been updated to use the Nebula Visualization widget v1.0.0  |
|  [#1571](https://github.com/ISISComputingGroup/IBEX/issues/1571) | Patch | If getting the error on a blocks has an error mark it as in error as opposed to setting the value to error  |
|  [#1576](https://github.com/ISISComputingGroup/IBEX/issues/1576) | Patch | Allow field on PV addresses |
|  [#1574](https://github.com/ISISComputingGroup/IBEX/issues/1574) | Patch | Alias the PVs of a PV with fields not the PV with field in the epics gateway from the blockserver |
|  [#1584](https://github.com/ISISComputingGroup/IBEX/issues/1584) | Patch | Expand macro regex for the McLenan to allow broader values. |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality