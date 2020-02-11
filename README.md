FPIFoam-3.0.1
==================

## Description

This code coupled a premixed flame tabulated chemistry model with flow solver.
The solver is based on ''rhoReactingFoam'', i.e. it is pressure-based (PISO), compressible and runs with both LES and RAS turbulence.
 
The calculation of these flamelets is a one-dimensional problem and can be done in a pre-processing step.
Integration using a presumed beta-Probability Density Function (PDF) accounts for the interaction between turbulent fluctuations and chemistry.
The results of the pre-processing procedure are stored in tables which are accessed during the simulation.
Values of interest, such as species mass fraction or enthalpy, are looked-up and connected to the flow using three parameters - the mixture fraction, its variance and the progress parameter.
In doing so, the expensive solution of chemical mechanisms during run-time can be avoided and the run-time thus reduces significantly.

## Installation

This version works with OpenFOAM-3.0.1

* Prepare a directory on your system, e.g.:  

  `mkdir ~/OpenFOAM/FPIFoam-v3.0.1/`

* Download FPIFoam using git:

  `git clone https://github.com/weixian001/FPIFoam-v3.0.1.git ~/OpenFOAM/FPIFoam-v3.0.1/`

* Set an environment variable to the FPIFoam src folder:

  `export LIB_FPIFoamV301_SRC=~/OpenFOAM/FPIFoam-v3.0.1/src/`

* Execute `./Allwmake`

## Notes

This solver was based on the work done by Prof Pfitzner, FlameletFoam created at the Universität der Bundeswehr München, Thermodynamics Institute (Prof. Pfitzner). http://sourceforge.net/projects/openfoam-extend/files/OpenFOAM_Workshops/OFW8_2013_Jeju/Fri/Track3/HagenMuller-OFW8.tar/download

The FPIFoam was developed by a NanyangCFD team at Nanyang Technological University, Singapore lead by Prof Wai Lee CHAN. 
Main contributor is Wei Xian LIM (weixian001@e.ntu.edu.sg).
Coresponding Author: chan.wl@ntu.edu.sg

# FPIFoam-v3.0.1
