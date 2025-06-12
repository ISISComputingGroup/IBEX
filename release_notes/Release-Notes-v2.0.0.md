# TODO as part of this release

1. Update Java to java Version 8 Update 91 (https://github.com/ISISComputingGroup/ibex_developers_manual/wiki/Upgrade-java)

## LARMOR
* For ticket #1002 (add GALIL IOCs 09 and 10):
In the LARMOR `globals.txt` file, there was a line setting the `MTRCTRL` macro of CONEXAGP to 09 (this would conflict with GALIL 09), but this line was commented out. The macro value has changed to something higher, with a note in a comment.
There are two other Settings files in LARMOR that refer to `MTR09`, which presumably would need updating:
      NDXLARMOR\configurations\configurations\larmor_SEMSANS\blocks.xml (lines 53 and 65)
      NDXLARMOR\Python\LSS\Setup_CONEXAGP.py (multiple lines)
* For ticket #1248 (configure the Danfysik):
The Baud rate will need to be updated to match the device (this is not currently a macro, but it will be in a future release), so in the st.cmd set the Baud Rate to 115200
* For ticket #1053 Make sure that synoptic names are less than 30 characters. If any are changed make any references are updated e.g. as the default synoptic for a configuration
* For ticker #1199 Ensure that the IOC can contact and interact with the labview VI for the ISISstat.

## IMAT
* For ticket #1002 (add GALIL IOCs 09 and 10):
In the `globals.txt` file, there is a line setting the `MTRCTRL` macro of PIMOT_01 to 09 (this would conflict with GALIL 09), and needs to be changed to something higher than 10. There doesn't seem to be any other files in the IMAT Settings folder which refer to MTR09 or MTR10.
* For ticket #1053 Make sure that synoptic names are less than 30 characters. If any are changed make any references are updated e.g. as the default synoptic for a configuration

# Changes since previous version

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|  [#1053](https://github.com/ISISComputingGroup/IBEX/issues/1053) | Major | Changed synoptic PVs namespace (From ..CS:BLOCKSEVER:SYNOPTICS to ..CS:SYNOPTICS); max synoptic name length is 30 characters |
|  [#1002](https://github.com/ISISComputingGroup/IBEX/issues/1002) | Minor | Added IOCs for GALIL 09 and 10 |
|  [#1007](https://github.com/ISISComputingGroup/IBEX/issues/1007) | Minor | genie_python command `waitfor_move` flags soft limit violations; also new genie_python command `check_limit_violations` |
|  [#1061](https://github.com/ISISComputingGroup/IBEX/issues/1061) | Minor | A graph of the recent beam current has been added to the Beam Status view |
|  [#1093](https://github.com/ISISComputingGroup/IBEX/issues/1093) | Minor | User can type instrument name |
|  [#1161](https://github.com/ISISComputingGroup/IBEX/issues/1161) | Minor | Default synoptic automatically selected in edit config |
|  [#1199](https://github.com/ISISComputingGroup/IBEX/issues/1199) | Minor | Add Mercury IOC |
|  [#1162](https://github.com/ISISComputingGroup/IBEX/issues/1162) | Patch | More informative error if MCR news is unavailable |
|  [#1163](https://github.com/ISISComputingGroup/IBEX/issues/1163) | Patch | Fixed an initialisation error for the web links view |
|  [#1278](https://github.com/ISISComputingGroup/IBEX/issues/1278) | Patch | Added extra homing routines to the Galils |
|  [#1193](https://github.com/ISISComputingGroup/IBEX/issues/1193) | Patch | DAE tabs can be viewed while instrument is running |
|  [#1223](https://github.com/ISISComputingGroup/IBEX/issues/1223) | Patch | Fix memory leak in IOC Log Server |
|  [#1281](https://github.com/ISISComputingGroup/IBEX/issues/1281) | Patch | MACROs set in the GUI are actioned on IOC startup |
|  [#1170](https://github.com/ISISComputingGroup/IBEX/issues/1170) | Patch | Post testing fixes for Lambda Genesys and Danfysik |
|  [#1220](https://github.com/ISISComputingGroup/IBEX/issues/1220) | Patch | The COM port is available as a macro and can be set via the GUI for appropriate hardware |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality