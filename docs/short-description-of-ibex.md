The following text is a short description of IBEX.  It is suggested for inclusion in papers where a short description of IBEX is required.


***

IBEX is a client-server application which coordinates the activities of a number of software components, each of which controls a separate aspect of an ISIS experiment :

(i) The Instrument Control Program (ICP) controls the Data Acquisition Electronics (DAE), informing it when to start and stop data collection, including automatically suspending data collection temporarily if certain conditions (e.g. sample temperature or pressure, or synchronisation of the chopper) are not within user-defined limits. The ICP is also responsible for transferring the final data from the DAE to a file.

(ii) the IBEX server is a collection of cooperating software components, based on the EPICS control-system framework (https://epics-controls.org/).  The primary components of the IBEX server are Input-Output Controllers (IOCs) and the Blockserver.  The IOCs control sample environment equipment and beamline hardware devices.  The Blockserver coordinates the activities of IOCs and other components, including the ICP and a data archiver.

(iii) The IBEX client is a graphical user interface program, which communicates with IBEX server and provides the primary means by which the experimenter can interact with the components of the IBEX server and the ICP to monitor and control an experiment.  The IBEX client also provides a simple scripting environment for running genie_python scripts.

(iv) LabVIEW (National Instruments - http://www.ni.com/en-gb/shop/labview.html) is a visual programming language designed to produce programs, called Virtual Instruments (VIs), for controlling hardware such as sample environment equipment and beamline components.  VIs are used to control equipment for which no EPICS driver is available.  IBEX uses an in-house designed interface layer to communicate with VIs.

(v) genie_python is an in-house library of Python (https://www.python.org/) commands which permit the automation of an experiment, for example enabling unattended overnight data collection from a sample at a number of temperatures in a furnace or cryostat, or from a number of samples in a sample changer.

***
