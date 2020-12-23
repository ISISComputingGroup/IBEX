## Instructions for Release

### All instruments

- Ticket 1662: Any scripts using `genie_python` function `cget` may need to be updated owing to the addition of a new key, and modified return value when disconnected.

### IMAT 

- Ticket 1544: Change reference in `FINS_01.cmd` in `var/settings/config/NDXXXX/fins`. From `imat-attn.db` to `imat-plc-attn.db`. 

### IRIS

- Ticket 1589: Replace Lakeshore 336 IPADDR macro with HOST macro, value ls336-1
- Ticket 1646: Ensure that the Scan field of OUT_SP is NOT commented out (`C:\Instrument\Apps\EPICS\ioc\master\EUROTHERM\db\devEurotherm.db` line 181). 


## Summary of all changes

| Ticket | Type  | Change |
| ------ | ------| ------------- |
|  [#1571](https://github.com/ISISComputingGroup/IBEX/issues/1571) | Patch | Fixed a bug where block values would be overwritten by "error" in GUI when receiving erroneous block alarm state (now triggers minor alarm instead) |
|  [#1589](https://github.com/ISISComputingGroup/IBEX/issues/1589) | Patch | Lakeshore336 IP address macro has been replaced with `HOST` which takes the host name of the device |
|  [#1515](https://github.com/ISISComputingGroup/IBEX/issues/1515) | Minor | The database server SQL connection code has been refactored to reduce the number of new connections and improve performance. The `INTERESTING_PVS` PV has been removed as it is no longer used |
|  [#1589](https://github.com/ISISComputingGroup/IBEX/issues/1589) | Patch | Changed Lakeshore 336 IPADDR macro to be the host name of the device instead |
|  [#1470](https://github.com/ISISComputingGroup/IBEX/issues/1470) | Minor | The current config can no longer be selected in the delete configuration dialog |
|  [#1546](https://github.com/ISISComputingGroup/IBEX/issues/1546) | Patch | The McLennan IOC can now be launched in simulation mode with multiple motors. Launching in non-simulation mode already works |
|  [#1555](https://github.com/ISISComputingGroup/IBEX/issues/1555) | Patch | genie_python cshow for a single block is faster |
|  [#1556](https://github.com/ISISComputingGroup/IBEX/issues/1556) | Patch | genie_python cget is faster |
|  [#1587](https://github.com/ISISComputingGroup/IBEX/issues/1587) | Patch | Fixed a bug in the installation of Lakeshore 218 whereby the protocol file wasn't in the expected location and the internal macros didn't work |
|  [#1587](https://github.com/ISISComputingGroup/IBEX/issues/1587) | Patch | Fixed a bug in the genie_python installation where iPython wasn't set up correctly if Python wasn't already installed |
|  [#1632](https://github.com/ISISComputingGroup/IBEX/issues/1632) | Patch | Fixed formatting of current in dashboard so it can now display up to 9999.99 |
|  [#1648](https://github.com/ISISComputingGroup/IBEX/issues/1648) | Patch | Dashboard set to auto-size better, so to handle up to 8 digits in the good and raw frames values |
|  [#1545](https://github.com/ISISComputingGroup/IBEX/issues/1545) | Patch | Re-sized linking containers pointing at motor.opi in a number of other OPIs |
|  [#1359](https://github.com/ISISComputingGroup/IBEX/issues/1359) | Minor | Script checker is enabled with better algorithm |
|  [#1507](https://github.com/ISISComputingGroup/IBEX/issues/1507) | Minor | Table columns are now resizable in various places in the GUI. |
|  [#1631](https://github.com/ISISComputingGroup/IBEX/issues/1631) | Minor | lvDCOM driver for HIFI Magnet |
|  [#1662](https://github.com/ISISComputingGroup/IBEX/issues/1662) | Major | cget now has a 'connected' field and the value returned as None if it is disconnected. People (James, Rob, Ian?) using this need to be informed of the change. |
|  [#1679](https://github.com/ISISComputingGroup/IBEX/issues/1679) | Minor | Database server locks SQL queries to prevent multiple threads making simultaneous queries on the same connection |
|  [#1614](https://github.com/ISISComputingGroup/IBEX/issues/1614) | Patch | Database server commits SELECT queries to avoid data from repeat queries becoming out of sync with database. Fixes issues with IOC data not updating in the client such as interesting PVs and running state. |
|  [#1709](https://github.com/ISISComputingGroup/IBEX/issues/1709) | Patch | Temporary fix so Eurotherm does not send setpoint at startup. Will be superceded by [#1646](https://github.com/ISISComputingGroup/IBEX/issues/1646). |
|  [#1703](https://github.com/ISISComputingGroup/IBEX/issues/1703) | Patch | If the raw Eurotherm setpoint and readback differ by more than a tolerance then a request is made to reissue the setpoint up to N times at 1 second intervals. |
|  [#1708](https://github.com/ISISComputingGroup/IBEX/issues/1708) | Minor | McLennan motors now support negative encoder ratios and can be set up to work with the sample changer OPIs |
|  [#1550](https://github.com/ISISComputingGroup/IBEX/issues/1550) | Minor | Log messages can now be filtered by severity from a dropdown menu (hiding all messages of lower severity than the one selected) |
|  [#1458](https://github.com/ISISComputingGroup/IBEX/issues/1458) | Patch | IOC status in IOC dialog editor panel no longer gets out of sync if IOC is started/stopped outside of the GUI |
|  [#1663](https://github.com/ISISComputingGroup/IBEX/issues/1663) | Minor | The PV names for the Iris cryo valve have been updated so that they will now work with `cset` in `genie_python`. The old PV names have been preserved for backwards compatibility |
|  [#1711](https://github.com/ISISComputingGroup/IBEX/issues/1711) | Minor | RunControl auto-restart setting is no longer-reapplied when the IOC restarts. This helps prevent an observed error whereby the RunCotrol IOC was not restarted when a configuration was updated. |
|  [#1635](https://github.com/ISISComputingGroup/IBEX/issues/1635) | Minor | Block logging is now enabled by default |
|  [#1347](https://github.com/ISISComputingGroup/IBEX/issues/1347) | Minor | Implemented edit config window V2 design (summary moved from tab into main window) |
|  [#1632](https://github.com/ISISComputingGroup/IBEX/issues/1632) | Minor | Danfysik 8800: Record to start change in current ramping |
|  [#1110](https://github.com/ISISComputingGroup/IBEX/issues/1110) | Minor | Custom instruments are now remembered on IBEX restart |
|  [#1679](https://github.com/ISISComputingGroup/IBEX/issues/1679) | Minor | Improve the stability of the Database Server |
|  [#1764](https://github.com/ISISComputingGroup/IBEX/issues/1764) | Minor | Improve the stability of the Database |  [#1646](https://github.com/ISISComputingGroup/IBEX/issues/1646) | Patch | Eurotherm no longer set set point to 0 when it starts. Also update read value from it to reduce errors. |
|  [#1592](https://github.com/ISISComputingGroup/IBEX/issues/1592) | Minor | Big and small double values are now displayed in scientific notation |
|  [#1713](https://github.com/ISISComputingGroup/IBEX/issues/1713) | Minor | The tabs in the Eurotherm OPI now say "Sensor" rather than "Eurotherm". |
|  [#1109](https://github.com/ISISComputingGroup/IBEX/issues/1109) | Patch | Update log and alarm settings so that they don't rely on custom instrument names having the "ND" prefix |
|  [#1222](https://github.com/ISISComputingGroup/IBEX/issues/1222) | Patch | The instruments list code has undergone some refactoring to improve the overall structure, reliability and readability |
|  [#1686](https://github.com/ISISComputingGroup/IBEX/issues/1686) | Minor | Improve performance of the database server and experimental database server |
|  [#1125](https://github.com/ISISComputingGroup/IBEX/issues/1125) | Minor | Added a dialogue for editing the device screens |
|  [#1689](https://github.com/ISISComputingGroup/IBEX/issues/1689) | Patch | Dashboard size has been increased to accommodate additional digits in displayed data. |
|  [#1665](https://github.com/ISISComputingGroup/IBEX/issues/1665) | Minor | Removed the `optional` flag from some method arguments in the genie_python documentation that were placed incorrectly. |
|  [#1596](https://github.com/ISISComputingGroup/IBEX/issues/1596) | Minor | Change the title of the bottom right panel in the Beam Status perspective from `Beam stats` to `Beam statistics`. |
|  [#1518](https://github.com/ISISComputingGroup/IBEX/issues/1518) | Minor | Blockserver no longer emits spurious messages from the `FILEWTCHR` when synoptics are deleted. |
|  [#1549](https://github.com/ISISComputingGroup/IBEX/issues/1549) | Patch | Set development version to 0.0.0. |
|  [#1510](https://github.com/ISISComputingGroup/IBEX/issues/1510) | Minor | Genie python set instrument knows about he instrument list and does better at guessing the PV Prefix. |
|  [#1706](https://github.com/ISISComputingGroup/IBEX/issues/1706) | Minor | GUI assumes test machines use TE:<machine name>: prefix. All machine names truncated to 8 characters with CRC8 if needed.|
|  [#1705](https://github.com/ISISComputingGroup/IBEX/issues/1705) | Minor | If on instrument name does not appear in the list and instrument at top has instrument name not host name.|
|  [#1479](https://github.com/ISISComputingGroup/IBEX/issues/1479) | Minor | MUONFE now works as an instrument name when setting instrument. |
|  [#1454](https://github.com/ISISComputingGroup/IBEX/issues/1454) | Minor | PV prefixes for developer machines are now TE:[MACHINE_NAME]:. PV prefixes for all machines longer than 8 characters are truncated to 6 characters plus an auto-generated 2-character identifier. |
|  [#1734](https://github.com/ISISComputingGroup/IBEX/issues/1734) | Patch | Modules required by the script server have been added to genie_python. |
|  [#1673](https://github.com/ISISComputingGroup/IBEX/issues/1673) | Minor | Improved block server behaviour when git repository is locked. |
|  [#1688](https://github.com/ISISComputingGroup/IBEX/issues/1688) | Patch | Experiments which have changed duration or date are deleted before being added in experimental database update. |
|  [#1377](https://github.com/ISISComputingGroup/IBEX/issues/1377) | Minor | Improved validation of block log settings and fixed a bug where state was apparently not saved when exiting edit block dialog |
|  [#1351](https://github.com/ISISComputingGroup/IBEX/issues/1351) | Minor | Removed currently selected text window in selection dialogs |
|  [#1500](https://github.com/ISISComputingGroup/IBEX/issues/1500) | Patch | All PV writes to the blockserver are queued.|
|  [#1735](https://github.com/ISISComputingGroup/IBEX/issues/1735) | Patch | Run control settings flushed on begin run.|
|  [#1521](https://github.com/ISISComputingGroup/IBEX/issues/1521) | Patch | GUI no longer processes log updates on every message but groups them, this allows it to be responsive under high log message load. |
|  [#1733](https://github.com/ISISComputingGroup/IBEX/issues/1733) | Patch | Eurotherm is not in alarm on start up; unless there is an actual alarm. |
|  [#1743](https://github.com/ISISComputingGroup/IBEX/issues/1743) | Patch | RBNumber in iocs now always updated. |
|  [#1767](https://github.com/ISISComputingGroup/IBEX/issues/1767) | Patch | When homing is requested on a McLennan motor, it will execute a constant velocity move until it encounters a limit switch. The McLennan behaviour is described in more detail [here](https://github.com/ISISComputingGroup/IBEX/wiki/McLennan-motors). |
|  [#1774](https://github.com/ISISComputingGroup/IBEX/issues/1774) | Patch | IOC list points to correct PV. |
|  [#1544](https://github.com/ISISComputingGroup/IBEX/issues/1544) | Enhancement | Add IMAT PLC vacuum readback |
|  [#1379](https://github.com/ISISComputingGroup/IBEX/issues/1379) | Patch | Configurations are now pushed to version control |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
