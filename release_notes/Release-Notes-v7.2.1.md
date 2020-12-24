This was a patch release which was only deployed to SANS2D. It was based on [Release 7.2.0](Release-Notes-v7.2.0.md)

# Instrument Specific Changes

| Instrument| Ticket | Type  | Change |
| --------- | ------ | ------| ------------- |
| SANS2D | [#5602](https://github.com/ISISComputingGroup/IBEX/issues/5602) | Minor | Migrate galil homing routines from SECI |
| SANS2D | [#4587](https://github.com/ISISComputingGroup/IBEX/issues/4587) | Minor | Collision avoidance for components in the vacuum tank has been added. Motors will be stopped if any component is too close and getting closer. There is an override. |
| SANS2D | [#5625](https://github.com/ISISComputingGroup/IBEX/issues/5625) | Minor | Motor disconnected Scraper Aperture fixed, Pillar OPI in Vacuum Tank unit changed from mm to degree, Vacuum status on Scraper Aperture removed, All the apertures and guides fits into the OPI without scrolling, minor typos fixed SANS2D Opi