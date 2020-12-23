## Update instructions

### IMAT

- Ticket 1685: MySQL is not running correctly in the correct place. Move to new location:
    1. Open services.msc
    1. Ensure that the process is running under `NETWORK SERVICE` and copy the command line (screen shot)
    1. Open command line in admin mode
    1. Remove the old service: `"C:\Program Files\MySQL\MySQL Server 5.6\bin\mysqld" --remove MySQL56`
    1. Move the data file from `C:\ProgramData\MySQL\data` to `C:\Instrument\Var\mysql\data`
    1. Copy the my.ini file into `C:\Instrument\Var\mysql\` from upgrade resources in `EPICS\misc\upgrade\master\Upgrade_v2.2.0_TO_v3.0.0`
    1. Replace `<INST NAME>` with `NDXIMAT`.
    1. Create a new service: `"C:\Program Files\MySQL\MySQL Server 5.6\bin\mysqld" --install MySQL56 --defaults-file=\"C:\Instrument\Var\mysql\my.ini\"
    1. Set the user running the service: LogOn tab -> This account to `NETWORK SERVICE` no password (this removes the notes and when you click start adds them back in)
    1. Start the service

### All instruments

- Ticket 1644: 
    - Review the configurations, components and synoptics for all instruments and adjust references to `EUROTHERM_nn` IOCs to `EUROTHRM_nn`, and PVs from `EUROTHERMn` to `EUROTHERM_0n`.
    - Update EUROTHERM to EUROTHRM for autosave files to preserve persisted behaviour.
    - Check user and instrument scripts for instances of EUROTHERM that need converting to EUROTHRM
    - Remember to update any references to EUROTHERM macros in `globals.txt`
- Ticket 1895:
    - As above for MK3CHOPPER renamed to MK3CHOPR
    - Pay particular note to the `globals.txt` file as this generally holds the MK3 chopper configuration macro
- Ticket 1685: 
    Add the lines after `[mysqld]` to `C:\Instrument\Var\mysql\my.ini`

    ```
    # turn off the performance schema
    performance_schema=OFF
    ``` 

    Stop the instrument and then restart the mysql service. (run services.msc, right click on mysql56 -> properties restart)
- Ticket 1765:
    1. Update the experimental data schema with `"c:\Program Files\MySQL\MySQL Server 5.6\bin\mysql.exe" -u root -p < C:\Instrument\Apps\EPICS\SystemSetup\exp_data_mysql_schema.txt`
    1. You will need to enter the root password
- Update System:
    1. Update the sql server password using: `c:\Program Files\MySQL\MySQL Server 5.6\bin\mysqladmin.exe" -u root -p  password`
    1. It will then prompt for the old password followed by the new password which is found in the passwords doc

## Summary of all changes

| Ticket | Type  | Change |
| ------ | ----  | ------------- |
|  [#1644](https://github.com/ISISComputingGroup/IBEX/issues/1644) | Major | `EUROTHERM` IOCs have been renamed to `EUROTHRM` for consistency with EPICS 8-character naming to help prevent PV overflow. Eurotherm PVs have been adjusted to the standard format such that `EUROTHERMn` would now be `EUROTHRM_0n`. |
|  [#1985](https://github.com/ISISComputingGroup/IBEX/issues/1895) | Major | `MK3CHOPPER` IOCs have been renamed to `MK3CHOPR` for consistency with EPICS 8-character naming to help prevent PV overflow |
| [#1685](https://github.com/ISISComputingGroup/IBEX/issues/1685) | Server | Normalise mysql database settings and ensure performance schema is turned off. |
| [#1765](https://github.com/ISISComputingGroup/IBEX/issues/1765) | Major | Update sql access to allow repeated RB numbers more correctly. |
| [#1903](https://github.com/ISISComputingGroup/IBEX/issues/1903) | Minor | Throttle communication with Eurotherm to avoid record scan error. |

Change Types: 

* Major - Backward compatible breaking change
* Minor - Change in API/functionality
* Patch - Bug fix no change in functionality
