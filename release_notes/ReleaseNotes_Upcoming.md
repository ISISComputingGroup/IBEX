Changes merged into master but not in an official release yet.

See [here](https://github.com/ISISComputingGroup/IBEX/wiki#instrument-information--hotfixes) for which version of IBEX your instrument is on, including any hotfixes.

# Highlights and Breaking Changes

| Ticket | Type | Description |
| ------ | ---- | ----------- |

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| INTER | [#7979](https://github.com/ISISComputingGroup/IBEX/issues/7979) | Patch | Add arbritary fields from/to INTER tank beckhoff |
| RIKEN | [#8002](https://github.com/ISISComputingGroup/IBEX/issues/8002) | Patch | Update trace on Muon Separator Tuning OPI even if the value doesn't change |
| RIKEN | [#7975](https://github.com/ISISComputingGroup/IBEX/issues/7975) | Minor | Add RKNMNTR IOC to provide calibrated temperature PVs for certain magnets. |

# Devices

### Newly supported devices

| Ticket | Device | Notes|
| ------ | ------ | -----|
| [#6048](https://github.com/ISISComputingGroup/IBEX/issues/6048) | PEARL Sample Alignment Motor OPI | Used on PEARL |
| [#7820](https://github.com/ISISComputingGroup/IBEX/issues/7820) | Fermi Chopper Condition monitoring box | Add IOC for PRE4500/Fermi chopper condition monitoring box | 

### Modified devices

| Ticket | Type | Device | Change |
| ------ | --- |------| ------------- |
| [#7890](https://github.com/ISISComputingGroup/IBEX/issues/7890) | Patch | DG645 | Fix delay width readback to correctly represent the time difference between leading and trailing edge |
| [#7889](https://github.com/ISISComputingGroup/IBEX/issues/7889) | Patch | DG645 | Plots x axes update if needed. |
| [#7887](https://github.com/ISISComputingGroup/IBEX/issues/7887) | Minor | DG645 | Units now displayed in delay readback blocks | 
| [#7863](https://github.com/ISISComputingGroup/IBEX/issues/7863) | Minor | Fermichopper | Changed fault colour of the LEDs to a brighter hue of red | 
| [#7966](https://github.com/ISISComputingGroup/IBEX/issues/7966) | Patch | Sorensen | Added minor fixes found during testing with device | 
| [#7958](https://github.com/ISISComputingGroup/IBEX/issues/7958) | Patch | MK3 Chopper | Updated communications DLL to v8.7 |
| [#7892](https://github.com/ISISComputingGroup/IBEX/issues/7892) | Minor | DG645 | Labels added to readback delays on OPI | 
| [#8000](https://github.com/ISISComputingGroup/IBEX/issues/8000) | Minor | FINS PLC | Added support for the remote control of the SANDALS V2 Valve | 
| [#7878](https://github.com/ISISComputingGroup/IBEX/issues/7878) | Minor | Aeroflex | Add Local and Remote control buttons for Aeroflex Signal Generator | 
| [#6341](https://github.com/ISISComputingGroup/IBEX/issues/6341) | Minor | Cryogenic SMS PSU | Add fully tested funtionality for magnet control |
| [#8010](https://github.com/ISISComputingGroup/IBEX/issues/8010) | Minor | Beckhoff/TwinCAT | Forward max velocity from beckhoff to table of motors | 
| [#8039](https://github.com/ISISComputingGroup/IBEX/issues/8039) | Patch | Beckhoff/TwinCAT | Fix typo in velocity forwarding record name | 
| [#8031](https://github.com/ISISComputingGroup/IBEX/issues/8031) | Minor | PEARL Pressure Controller | Lock certain PVs when DAE is not in Setup state or Manager mode is off |
| [#8078](https://github.com/ISISComputingGroup/IBEX/issues/8078) | Patch | Jaws manager | Allow adding engineering units to sample/mod gaps and centers | 
| [#8070](https://github.com/ISISComputingGroup/IBEX/issues/8070) | Patch | PACE 5000 | Add option to vent and see vent status, enforce bar as unit | 

### Reflectometry IOC

| Ticket | Type | Change |
| ------ | --- | ------------- |
| [#7649](https://github.com/ISISComputingGroup/IBEX/issues/7649) | Minor | Added a new type of read-only parameter which is used to propagate the beam intersect of a component to given motor axes | 

#  IBEX Client

### Configurations

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#6047](https://github.com/ISISComputingGroup/IBEX/issues/6047) | Minor | Added the configuration files needed to support the alignment motor | 
| [#8037](https://github.com/ISISComputingGroup/IBEX/issues/8037) | Minor | Add ability to home even if limit is engaged for Beckhoff/TwinCAT motor controllers | 

### Script Generator
| Ticket | Type  | Change |
| ------ | ----- | ------ |
| [#7843](https://github.com/ISISComputingGroup/IBEX/issues/7843) | Major | Moved several of the script generator buttons into the right-click menu. |
| [#6922](https://github.com/ISISComputingGroup/IBEX/issues/6922) | Minor | Steps in the script generator are now read-only once they are being executed, this is to avoid confusion, as updating them once running would not update the running script. |
| [#7932](https://github.com/ISISComputingGroup/IBEX/issues/7932) | Minor | Prevent users from accidentally modifying the existing script definitions, users can no longer update git repo from script generator. Dialoges improved to notify of dirty repo as well as if are updates available. |
| [#6658](https://github.com/ISISComputingGroup/IBEX/issues/6658) | Minor | Imporved the readability of generated scripts via action parameter order consistency, action id comments, action section comment |
| [#5124](https://github.com/ISISComputingGroup/IBEX/issues/5124) | Minor | Added ENUM dropdown support to scripts |


### Other

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
| [#7985](https://github.com/ISISComputingGroup/IBEX/issues/7985) | patch | Adding a block from the beam status perspective context menu now correctly unchecks "is local" by default. |
| [#7699](https://github.com/ISISComputingGroup/IBEX/issues/7699) | Minor | Added a combined spectra plot to the DAE |
| [#7921](https://github.com/ISISComputingGroup/IBEX/issues/7921) | Minor | Added "Show Title and Users in Dataweb Dashboard Page" to dashboard |
| [#7896](https://github.com/ISISComputingGroup/IBEX/issues/7896) | Minor | Show IOC - COM port mapping on Moxa Ports perspective. |
| [#7632](https://github.com/ISISComputingGroup/IBEX/issues/7632) | Minor | Help icons added in Script Server perspective and Scripting perspective console menu bar. |
| [#8021](https://github.com/ISISComputingGroup/IBEX/issues/8021) | Minor | Add ability to show COM port mapping dialog when adding/editing a configuration. |
| [#8020](https://github.com/ISISComputingGroup/IBEX/issues/8020) | Patch | Fix error when trying to open a device screen with undefined macro |
| [#8032](https://github.com/ISISComputingGroup/IBEX/issues/8032) | Patch | Disable Advanced tab in PEARL Pressure Controller OPI (PEARLPC) if not in manager mode. |
| [#8050](https://github.com/ISISComputingGroup/IBEX/issues/8050) | Minor | Show extra diagnostic data for galil/beckhoff in manager mode on table of motors "simple" view |
| [#8052](https://github.com/ISISComputingGroup/IBEX/issues/8052) | Patch | Show 8 axes in beckhoff engineering view and add lookup for error codes. |
| [#8071](https://github.com/ISISComputingGroup/IBEX/issues/8071) | Minor | Show full filepath of motion setpoints file in motion setpoints screen |
| [#8061](https://github.com/ISISComputingGroup/IBEX/issues/8061) | Minor | Remove outdated Slit 4 from INTER reflectometry panel and added controls for beam block + monitor | 
| [#7823](https://github.com/ISISComputingGroup/IBEX/issues/7823) | Patch | Allow/fix scientific notation in run control settings of blocks | 
| [#8013](https://github.com/ISISComputingGroup/IBEX/issues/8013) | Minor | Units hidden by zeros on dashboard blocks if high precision specified |
| [#8091](https://github.com/ISISComputingGroup/IBEX/issues/8091) | Minor | Make INTER tank screen more user friendly |

# genie_python

| Ticket | Type  | Change |
| [#8033](https://github.com/ISISComputingGroup/IBEX/issues/8033) | Minor | load_script handles inst dir script linting errors | 


extend pre/post dae commands #7022
# InstrumentScripts

| Ticket | Type  | Change |
| ------ | ------| ------------- |


# Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |

# Internal changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#7961](https://github.com/ISISComputingGroup/IBEX/issues/7961) | Minor | New script for standardising colours and fonts used in OPIs |
| [#7982](https://github.com/ISISComputingGroup/IBEX/issues/7982) | Minor | Modified Galil install step to be automated based upon the previous deploy's Galil decision |
| [#7987](https://github.com/ISISComputingGroup/IBEX/issues/7987) | Minor | Improve upgrade script to check MySQL, Java, Git versions automatically, add git status step, check backup directory space, and some other minor changes |
| [#8081](https://github.com/ISISComputingGroup/IBEX/issues/8081) | Minor | Changed RoboCopy func from just copy to move the backup dir, to stage-deleted |
| [#8001](https://github.com/ISISComputingGroup/IBEX/issues/8001) | Minor | Improves implementation/functionality of the deploy script steps: LabView recording (knows whether to ask this step or not based on the instrument), motor/block/blockserver backups (occur in parallel as one step), backup (zips files as well as transfering to stage-deleted)  |

# Support Issues Solved

| Ticket | Type  | Change |
| ------ | ------| ------------- |


Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality

# Dependencies

### Server dependencies

what | version | where | last updated/checked
|---- | ------- | ----- | --------------------|

### GUI Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|

### genie_python Dependencies

Dependency | Version | last updated/checked
|---- | ------- | --------------------|

