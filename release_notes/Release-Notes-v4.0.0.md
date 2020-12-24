# Dependencies

- MySQL 5.7.17
- JRE 1.8.0 update 144

# Changes to make on specific instruments when releasing

## All instruments

## POLARIS

- [Ticket 2314](https://github.com/ISISComputingGroup/IBEX/issues/2314): The PV names on the rotating sample changer have been updated. 
  * In Polaris' configurations, replace the block which points at `ROTSC_01:MOVE_TO_POSN` to point at `ROTSC_01:POSN:SP`

## HRPD

- [Ticket 2314](https://github.com/ISISComputingGroup/IBEX/issues/2314): The PV names on the rotating sample changer have been updated. 
  * In HRPD's configurations, look for any block which points at `ROTSC_01:MOVE_TO_POSN` and change it to point at `ROTSC_01:POSN:SP`
  * In HRPD's configurations, look for any block which points at `ROTSC_01:MOVE_TO_POSN:NO_LOWER` and change it to point at `ROTSC_01:POSN:NO_LOWER:SP`

## ALF

- [Ticket 2288](https://github.com/ISISComputingGroup/IBEX/issues/2288): One of Alf's goniometer axes has been renamed from THETA to RROT. 
  * In the following file: `\\NDXALF\c$\Instrument\Settings\config\NDXALF\configurations\galil\axes.cmd`, edit line 2 to contain `AXIS=RROT` instead of `AXIS=THETA`
  * In the "Jaws and Goniometer" component, change the block that points at "THETA" to point at "RROT"

## LARMOR

- Update following synoptics making the target of the rotating bench the rotating bench, M macro is 0401:
    - Larmor
    - Larmor_Base_Changer_Julabo
- require CAEN hotfix https://github.com/ISISComputingGroup/IBEX/issues/2603

## Engin-X

- Ensure your local version of `C:\Instrument\Apps\EPICS\support\motorExtensions\master` is up to date (`git pull`, `make clean uninstall && make`) with the latest master
- Copy `C:\Instrument\Apps\EPICS\support\motorExtensions\master\db\enginxjawset.db` into the equivalent location on NDXENGINX
- Remember to document this hotfix on the page at https://github.com/ISISComputingGroup/IBEX/wiki once deployed

## MuonFE

- Upgrade db password
- hotfix https://github.com/ISISComputingGroup/EPICS-ioc/commit/4454ecf8f3f1d0bc324af6cf134c45ef5ef39ad0
- hotfix https://github.com/ISISComputingGroup/IBEX/issues/2770

## Sans2D

- Add start_ibex_inst.bat to startup on windows start menu
- require CAEN hotfix https://github.com/ISISComputingGroup/IBEX/issues/2603

# All instruments

## Ticket 2990
The McLennan macro `MODE` has been replaced with `CMOD`, which is less generic. Make sure that any McLennans have their macros migrated. This is especially relevant for **IRIS** and **VESUVIO**

# Summary of all changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|  [#2070](https://github.com/ISISComputingGroup/IBEX/issues/2070) | Minor | Added code to show run control values on Web dashboard |
|  [#2265](https://github.com/ISISComputingGroup/IBEX/issues/2265) | Minor | change_users now works as expected in genie_python |
|  [#2248](https://github.com/ISISComputingGroup/IBEX/issues/2248) | Minor | Add HRPD to the standard instrument list |
|  [#2249](https://github.com/ISISComputingGroup/IBEX/issues/2249) | Patch | Fix install genie python |
|  [#2168](https://github.com/ISISComputingGroup/IBEX/issues/2168) | Patch | Updates to the Julabo IOC to enable record simulation and the record simulation framework itself |
|  [#2182](https://github.com/ISISComputingGroup/IBEX/issues/2182) | Patch | Fix bugs in the synoptic regarding how it handles groups and the DAE |
|  [#2195](https://github.com/ISISComputingGroup/IBEX/issues/2195) | Patch | Added fix in genie python to allow relative imports of loaded scripts |
|  [#2291](https://github.com/ISISComputingGroup/IBEX/issues/2291) | Minor | Removed weird border around device screens table |
|  [#1865](https://github.com/ISISComputingGroup/IBEX/issues/1865) | Minor | Add an inhibitor IOC with fixed PV targets |
|  [#2287](https://github.com/ISISComputingGroup/IBEX/issues/2287) | Minor | IOC description is now there when adding a new IOC. |
|  [#2236](https://github.com/ISISComputingGroup/IBEX/issues/2236) | Minor | Various minor changes to Polaris Jawset OPI & IOC |
|  [#2300](https://github.com/ISISComputingGroup/IBEX/issues/2300) | Patch | Exclude unmatched values from diagnostic returned count  |
|  [#2266](https://github.com/ISISComputingGroup/IBEX/issues/2266) | Minor | "Selected" text box in IOC tab when editing a configuration is cleared when no IOCs are selected. |
|  [#2226](https://github.com/ISISComputingGroup/IBEX/issues/2226) | Patch | When editing a configuration and the final IOC is deleted, it will no longer be shown in the "Selected" box |
|  [#2209](https://github.com/ISISComputingGroup/IBEX/issues/2209) | Minor | genie_python no longer hangs when zero or negative times are given to `waitfor_time`. Zero times have no wait, negative times result in an exception |
|  [#2298](https://github.com/ISISComputingGroup/IBEX/issues/2298) | Patch | Add exceptions for cases where Ibex tries to write to a read-only PV |
|  [#2236](https://github.com/ISISComputingGroup/IBEX/issues/2236) | Patch | Add missing configuration file for IOC BKHOFF_02 |
|  [#2272](https://github.com/ISISComputingGroup/IBEX/issues/2272) | Patch | Merged interlock group boxes on the Mk2 Chopper OPI |
|  [#2326](https://github.com/ISISComputingGroup/IBEX/issues/2326) | Patch | Fixed a bug in getting readings from the CCD100 with unexpected white space |
|  [#2208](https://github.com/ISISComputingGroup/IBEX/issues/2208) | Patch | Correct initialisation of startup script when scripting window launched on non-Instrument PC |
|  [#2289](https://github.com/ISISComputingGroup/IBEX/issues/2289) | Patch | Fix bug in McLennan homing mode 2 where it was not homing and zeroing |
|  [#2115](https://github.com/ISISComputingGroup/IBEX/issues/2115) | Minor | Add emulator for instron stress rig |
|  [#2299](https://github.com/ISISComputingGroup/IBEX/issues/2299) | Patch | McLennan and LinMot motors will now respond correctly to collective motor commands (e.g. genie_python `waitfor_move(...)` and Ibex client bump strip diagnostics |
|  [#2299](https://github.com/ISISComputingGroup/IBEX/issues/2299) | Patch | genie_python `waitfor_move` command now works with specified blocks |
|  [#2254](https://github.com/ISISComputingGroup/IBEX/issues/2254) | Minor | Fixed some bugs in the device screens properties table |
|  [#2264](https://github.com/ISISComputingGroup/IBEX/issues/2264) | Patch | Can edit a component block by right clicking in the blocks bar. Previously it would complain of it being a duplicate. |
|  [#2290](https://github.com/ISISComputingGroup/IBEX/issues/2290) | Minor | A macro is now available to set custom names for Linmots and McLennans |
|  [#2259](https://github.com/ISISComputingGroup/IBEX/issues/2259) | Minor | Minor alterations to the config/component editor Dialog |
|  [#2270](https://github.com/ISISComputingGroup/IBEX/issues/2270) | Minor | Add an AMINT2L device; IOC, Emulator and OPI  |
|  [#2265](https://github.com/ISISComputingGroup/IBEX/issues/2265) | Minor | Add change rb number to genie_python |
|  [#1936](https://github.com/ISISComputingGroup/IBEX/issues/1936) | Minor | Added pv address errors to synoptic title bar. |
|  [#2369](https://github.com/ISISComputingGroup/IBEX/issues/2369) | Minor | Automatically add trailing colon to `PVPREFIX` |
|  [#2134](https://github.com/ISISComputingGroup/IBEX/issues/2134) | Patch | Put all the files in the configurations directory under git |
|  [#2233](https://github.com/ISISComputingGroup/IBEX/issues/2233) | Minor | New device screens are now autoselected. |
|  [#2066](https://github.com/ISISComputingGroup/IBEX/issues/2066) | Minor | Add Visa serial device support. |
|  [#2155](https://github.com/ISISComputingGroup/IBEX/issues/2155) | Minor| Nagios Check for inst archive DAE pvs |
|  [#1355](https://github.com/ISISComputingGroup/IBEX/issues/1355) | Minor | IOCs from component are added to config when component is added |
|  [#2252](https://github.com/ISISComputingGroup/IBEX/issues/2252) | Minor | Add POLARIS to the standard instrument list |
|  [#2295](https://github.com/ISISComputingGroup/IBEX/issues/2295) | Minor | Web dashboard gives sensible error when IBEX is not running |
|  [#2308](https://github.com/ISISComputingGroup/IBEX/issues/2308) | Patch | GUI fails to build due to missing managermode plugin |
|  [#2111](https://github.com/ISISComputingGroup/IBEX/issues/2111) | Minor | Add IOC for Instron stress rig (part 1) |
|  [#1968](https://github.com/ISISComputingGroup/IBEX/issues/1968) | Patch | Handling of spectra by the client and server have been modified to significantly reduce traffic |
|  [#2412](https://github.com/ISISComputingGroup/IBEX/issues/2412) | Minor | Added some missing descriptions to the rotating sample changer |
|  [#2273](https://github.com/ISISComputingGroup/IBEX/issues/2273) | Minor | Groups from components can now be ordered within configurations that contain them. |
|  [#2379](https://github.com/ISISComputingGroup/IBEX/issues/2379) | Minor | Add test cases and emulator for TPG26x |
|  [#2054](https://github.com/ISISComputingGroup/IBEX/issues/2054) | Minor | Add run diagnostics GUI |
|  [#2288](https://github.com/ISISComputingGroup/IBEX/issues/2288) | Minor | Rename Alf's goniometer axis from theta to rrot. Add new goniometer icon |
|  [#2361](https://github.com/ISISComputingGroup/IBEX/issues/2361) | Minor | Add access security to the Mk2 chopper |
|  [#1723](https://github.com/ISISComputingGroup/IBEX/issues/1723) | Patch | Fix issues which caused alarm view to not update |
|  [#2242](https://github.com/ISISComputingGroup/IBEX/issues/2242) | Minor | Patch motors so that limit switch is preserved regardless of motion direction |
|  [#2347](https://github.com/ISISComputingGroup/IBEX/issues/2347) | Minor | Switch on and off detector diagnostics when viewed |
| [#2343](https://github.com/ISISComputingGroup/IBEX/issues/2343)  | Minor | Make interesting `calc` records readonly |
| [#2441](https://github.com/ISISComputingGroup/IBEX/issues/2441)  | Minor | Changed all pressure gauge graphs to be logarithmic |
| [#2381](https://github.com/ISISComputingGroup/IBEX/issues/2381)  | Minor | Mk3 and Mk2 choppers only allow specific frequencies |
| [#2263](https://github.com/ISISComputingGroup/IBEX/issues/2263)  | Minor | Run information PVs on the web dashboard are now ordered the same as in SECI |
| [#2378](https://github.com/ISISComputingGroup/IBEX/issues/2378)  | Minor | Add IOC for Superlogics device   |
| [#2385](https://github.com/ISISComputingGroup/IBEX/issues/2385)  | Minor | Install built files as READONLY   |
| [#2321](https://github.com/ISISComputingGroup/IBEX/issues/2321)  | Minor | Generate linker MAP file |
| [#2420](https://github.com/ISISComputingGroup/IBEX/issues/2420)  | Patch | Bug that stopped device screens being written to the server has been fixed |
| [#2315](https://github.com/ISISComputingGroup/IBEX/issues/2315)  | Major | Changed ActiveMQ port |
| [#2461](https://github.com/ISISComputingGroup/IBEX/issues/2461)  | Minor | Add mark and space parity options |
| [#2416](https://github.com/ISISComputingGroup/IBEX/issues/2416)  | Minor | VISAdrv additional options |
| [#2103](https://github.com/ISISComputingGroup/IBEX/issues/2103)  | Minor | FINS PLC auto reconnect and less logging on disconnect |
|  [#2314](https://github.com/ISISComputingGroup/IBEX/issues/2314) | Minor | Update PV names on the rotating sample changer so that they don't throw errors from scripts. |
|  [#2169](https://github.com/ISISComputingGroup/IBEX/issues/2169) | Minor| Nagios check for web dashboard |
| [#2413](https://github.com/ISISComputingGroup/IBEX/issues/2413)  | Patch | Fixed bug where view would crash if the GUI started pointing at a PROCESSING DAE |
| [#2355](https://github.com/ISISComputingGroup/IBEX/issues/2355)  | Minor | Add IOC/OPI/Emulator/Tests for fermi chopper |
| [#2389](https://github.com/ISISComputingGroup/IBEX/issues/2389)  | Patch | Make default error level MINOR |
| [#2159](https://github.com/ISISComputingGroup/IBEX/issues/2159)  | Patch | Fixed some non-visible html errors in the dataweb |
| [#2458](https://github.com/ISISComputingGroup/IBEX/issues/2458)  | Minor | Add Emulator/Tests for TDK Lambda Genesys |
|  [#2342](https://github.com/ISISComputingGroup/IBEX/issues/2342) | Minor | Added change_rb command to genie_python |
|  [#2112](https://github.com/ISISComputingGroup/IBEX/issues/2112) | Minor | Added support for the Instron Stress rig's channel commands. |
| [#2275](https://github.com/ISISComputingGroup/IBEX/issues/2275)  | Minor | Add an "overview" opi for the muon front end |
|  [#2237](https://github.com/ISISComputingGroup/IBEX/issues/2237) | Patch | Handle mm^2 etc in build server units check |
| [#2348](https://github.com/ISISComputingGroup/IBEX/issues/2348)  | Patch | Added timeout to IOC system tests |
| [#2456](https://github.com/ISISComputingGroup/IBEX/issues/2456) | Minor | Created Riken frontend OPI | 
|  [#1994](https://github.com/ISISComputingGroup/IBEX/issues/1994) | Minor| Build MSI kits |
| [#2475](https://github.com/ISISComputingGroup/IBEX/issues/2475)  | Minor | use cygwin64 versions of procServ, conserver and console |
|  [#1781](https://github.com/ISISComputingGroup/IBEX/issues/1781) | Patch | Fix error in PSCTRL ioc startup. |
| [#2114](https://github.com/ISISComputingGroup/IBEX/issues/2114)  | Minor | Add facility to produce a log file from an IOCs |
| [#1232](https://github.com/ISISComputingGroup/IBEX/issues/1232)  | Minor | Add an OPI and IOC for Zoom FINS PLC |
| [#2401](https://github.com/ISISComputingGroup/IBEX/issues/2401)  | Minor | Add an OPI and IOC for Sample positioning system on Engin-X |
| [#2439](https://github.com/ISISComputingGroup/IBEX/issues/2439)  | Minor | Stress rig put in databrowser graphs |
| [#2526](https://github.com/ISISComputingGroup/IBEX/issues/2526)  | Minor | Fixed slowest in BlockServer relating to run-control IOC | 
| [#2479](https://github.com/ISISComputingGroup/IBEX/issues/2479)  | Minor | Add IOC/Emulator/Tests for AG33220A |
| [#2502](https://github.com/ISISComputingGroup/IBEX/issues/2502)  | Minor | Blockserver: tests failing with new lxml library | 
| [#2410](https://github.com/ISISComputingGroup/IBEX/issues/2410)  | Minor | Update to EPICS base 3.15.5 |
| [#2400](https://github.com/ISISComputingGroup/IBEX/issues/2400)  | Minor | Add support for ENGIN-X Jaws |
| [#2488](https://github.com/ISISComputingGroup/IBEX/issues/2488)  | Minor | Added get_tcb command to genie, allowed optional arguments to set_tcb |
| [#2421](https://github.com/ISISComputingGroup/IBEX/issues/2421)  | Patch | Fixed bug where run control was not getting set through IBEX |
| [#2536](https://github.com/ISISComputingGroup/IBEX/issues/2536)  | Patch | Edit config dialog displays the correct config name |
| [#2455](https://github.com/ISISComputingGroup/IBEX/issues/2455)  | Minor | Add support for RIKEN PSUs |
| [#2515](https://github.com/ISISComputingGroup/IBEX/issues/2515)  | Minor | Add ASYN echo server (for testing) |
| [#2456](https://github.com/ISISComputingGroup/IBEX/issues/2456)  | Minor | Added RIKEN front end OPI |
| [#2113](https://github.com/ISISComputingGroup/IBEX/issues/2113)  | Minor | Add Instron stress rig waveform commands  |
| [#2545](https://github.com/ISISComputingGroup/IBEX/issues/2545)  | Minor | Improved the returned message in genie_python on changing the TCB |
| [#2510](https://github.com/ISISComputingGroup/IBEX/issues/2510)  | Minor | Print readable stack backtraces  |
| [#2557](https://github.com/ISISComputingGroup/IBEX/issues/2557)  | Minor | Get VisualDCT working again  |
| [#2487](https://github.com/ISISComputingGroup/IBEX/issues/2487)  | Minor | Write multiple log files  |
| [#2537](https://github.com/ISISComputingGroup/IBEX/issues/2537)  | Major| Make RUNSTATE_STR actually a string |
| [#2239](https://github.com/ISISComputingGroup/IBEX/issues/2239)  | Minor | Web dashboard: make run status obvious  |
| [#2440](https://github.com/ISISComputingGroup/IBEX/issues/2440)  | Patch | Make eurotherm graphs update continuously  |
| [#2443](https://github.com/ISISComputingGroup/IBEX/issues/2508)  | Patch | Make sure controls aren't cut off when the DAE system view is resized  |
| [#2489](https://github.com/ISISComputingGroup/IBEX/issues/2489)  | Minor | Add IOC for Cybaman |
| [#2561](https://github.com/ISISComputingGroup/IBEX/issues/2561)  | Patch | Print text that can't be split in DBUnitChecker  |
| [#2530](https://github.com/ISISComputingGroup/IBEX/issues/2530)  | Minor | Add HLG device |
| [#2469](https://github.com/ISISComputingGroup/IBEX/issues/2469)  | Minor | Add IOC for IEG |
| [#2338](https://github.com/ISISComputingGroup/IBEX/issues/2338)  | Minor | Make stress rig IOC work against real hardware  |
| [#2520](https://github.com/ISISComputingGroup/IBEX/issues/2520)  | Minor | Add LvDCOM IOC for engin-x collimators |
| [#2521](https://github.com/ISISComputingGroup/IBEX/issues/2521)  | Minor | Added engin-x collimator step scan script (add extra argument to genie_python waitfor) |
| [#2531](https://github.com/ISISComputingGroup/IBEX/issues/2531)  | Patch | Fix modbus excessive logging on disconnect (for SKF choppers) |
| [#2565](https://github.com/ISISComputingGroup/IBEX/issues/2565) | Patch | Fix duplicated entries in PV selector |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
