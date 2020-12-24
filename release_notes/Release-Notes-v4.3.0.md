# Dependencies

- MySQL 5.7.21
- JRE 1.8.0 update 161

## Changes to make on specific instruments when releasing

- Ticket 2548: Inform instrument scientists that `genie_python` has been updated. In the latest version, type checking on blocks is more strict. Specifically, floats cannot be passed to enumerated record types. If they do, they'll get an error message `Expected int, got float`

### All instruments

- Ticket 1197: At next instrument scientist meeting, ask whether they'd like to migrate to the new sample stack

# Changes in software for Zoom Commissioning



### ZOOM COMMISSIONING (Do not transfer until ZOOM commissioning)
- Set up the `axes.cmd` file to point the sample changer at the correct PVs. An example is:
```
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:X,mAXIS=MTR0101")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:Y,mAXIS=MTR0102")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:ZHI,mAXIS=MTR0103")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:THETA,mAXIS=MTR0104")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:PSI,mAXIS=MTR0105")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:CHI,mAXIS=MTR0106")
$(IFDMC01) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:ZLO,mAXIS=MTR0107")
$(IFDMC02) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:XRAIL,mAXIS=MTR0201")
$(IFDMC02) dbLoadRecords("$(AXIS)/db/axis.db","P=$(MYPVPREFIX)MOT:,AXIS=STACK:YRAIL,mAXIS=MTR0202")
```
This will point the first 7 PVs (JJ X-Ray movements) at galil controller 1 and the last 2 (rail movement) at galil controller 2.

- When commissioning Julabo the read termination character may need to be set to be `\n` not `\r\n`.

- For the FINS PLC Vacuum controller you should add a configuration file to `configuration\fins\`. The important points to change are the IP address and the `Q` macro, which is just the prefix to address the PLC by:
```
#Init and connect
finsUDPInit("PLC", "$(PLCIP=<ip-address>)", "TCP")

## Load our record instances

dbLoadRecords("${TOP}/db/zoom-vacuum.db","P=$(MYPVPREFIX),Q=VACUUM:,RECSIM=$(RECSIM=0),DISABLE=$(DISABLE=0)")
```

## IBEX changes

### Features

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2900](https://github.com/ISISComputingGroup/IBEX/issues/2900) | Minor | Journal Viewer: empty perspective |
| [#2901](https://github.com/ISISComputingGroup/IBEX/issues/2901) | Minor | Journal Viewer: connection status indicator |
| [#2902](https://github.com/ISISComputingGroup/IBEX/issues/2902) | Minor | Journal viewer: add manual refresh |
| [#2903](https://github.com/ISISComputingGroup/IBEX/issues/2903) | Minor | Journal viewer: extract and see data |

### Devices

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#646](https://github.com/ISISComputingGroup/IBEX/issues/646) | Minor | Lakeshore 460 IOC/emulator/OPI/tests |
| [#2567](https://github.com/ISISComputingGroup/IBEX/issues/2567) | Minor | SKF G5 Chopper: removed rounding error on angle when parking |
| [#2840](https://github.com/ISISComputingGroup/IBEX/issues/2840) | Minor | Add extra controls to Mercury iTC |
| [#2831](https://github.com/ISISComputingGroup/IBEX/issues/2831) | Minor | Galil no longer autosaves if given the wrong macros |
| [#2943](https://github.com/ISISComputingGroup/IBEX/issues/2943) | Patch | Make MK3 chopper reconnect in more cases |
| [#2759](https://github.com/ISISComputingGroup/IBEX/issues/2759) | Minor | IOC for MAPS fermi chopper |
| [#2859](https://github.com/ISISComputingGroup/IBEX/issues/2859) | Minor | Add GEM jaws manager screen |
| [#2893](https://github.com/ISISComputingGroup/IBEX/issues/2893) | Minor | Add Oxford Instruments ILM 200 series |
| [#2951](https://github.com/ISISComputingGroup/IBEX/issues/2951) | Patch | MERLIN Fermi chopper comms patch |
| [#2138](https://github.com/ISISComputingGroup/IBEX/issues/2138) | Minor | Added GEM beamscraper jaws |
| [#2828](https://github.com/ISISComputingGroup/IBEX/issues/2828) | Minor | Add IOC for Triton dilution fridge |
| [#2808](https://github.com/ISISComputingGroup/IBEX/issues/2828) | Minor | Adjustments to GEM Oscillating Radial Collimator following commissioning |

### UI

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2948](https://github.com/ISISComputingGroup/IBEX/issues/2948) | Patch | Fixed DAE Tables displayed in IBEX client going out of sync |
| [#1575](https://github.com/ISISComputingGroup/IBEX/issues/1575) | Patch | Add extra logging output on failure to load synoptic |

### Interfaces

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2932](https://github.com/ISISComputingGroup/IBEX/issues/2932) | Patch | Fix SciPY import and test all modules import |
| [#2957](https://github.com/ISISComputingGroup/IBEX/issues/2957) | Patch | Fix genie_python load_script for scripts containing python 2 style print statements |

### Performance

| Ticket | Type  | Change |
| ------ | ------| ------------- |

### Back end

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2836](https://github.com/ISISComputingGroup/IBEX/issues/2836) | Minor | add additional serial port diagnostics |
| [#2813](https://github.com/ISISComputingGroup/IBEX/issues/2813) | Minor | Add riken changeover logic (COORD IOC) |
| [#2980](https://github.com/ISISComputingGroup/IBEX/issues/2980) | Patch | Remove excess git logging from blockserver |

### Development process

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2692](https://github.com/ISISComputingGroup/IBEX/issues/2692) | Minor | Merge the master branch of the configurations repository into the local branch on instrument update. |

### Other

| Ticket | Type  | Change |
| ------ | ------| ------------- |
| [#2694](https://github.com/ISISComputingGroup/IBEX/issues/2694) | Minor | Modify web dashboard style |
| [#2929](https://github.com/ISISComputingGroup/IBEX/issues/2929) | Patch | Fixed EMMA-A webdashboard |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
