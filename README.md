# A Versatile and Open Source One- and Multi-Photon Light-Sheet Microscope Design

### Abstract
Two-photon light sheet microscopy has a wide range of applications in biology. Here we report a novel open source design to transform a standard microscopes into a 1P \& 2P light-sheet microscope. A specially designed broadband hollow core fiber shares the expansive pulsed laser source from other setups. The system provides uncompromised image resolution and speed and makes this technology widely accessible at reduced cost.

![CompilationFigure_v3](https://user-images.githubusercontent.com/38736127/174906572-d85802cc-6171-40a8-a8f5-7138b5235d8f.png)

*(a) 3D model of the 1P- \& 2P-light-sheet forming unit. (b) 3D design model showing how the one- and two-photon light-sheet unit is mounted on the Scientifica scope. The unit is attached to the motorized stage of the system that moves the objective. (c) Attenuation and dispersion spectrum of the hollow-core negative curvature fiber with two transmission bands (loss $<$ 300dB/km) highlighted in yellow. Inset left: Schematic of the cross section of the hypocycloid fiber with 8 cladding tubes. Inset right: EM cross section image of the fiber (scale bar 10\,$\mu$m). (d) Near and far field profile of the fiber output at 515\,nm and 1030\,nm laser wavelength. (e) Schematic of the fiber with its FC/PC connectorization and the lens to increase the numerical aperture (NA) to match the NA of the collimation objective (Obj1 in a). (f) Measured light-sheet profile. (g) Single layers of a volumetric brain scan recorded in one- and two-photon mode of a 6\,dpf old zebrafish larva expressing pan-neuronally GCaMP6f and localized to the cell nucleus (Elav3-H2B-GCaMP6f).*


### Slow scan mode

https://user-images.githubusercontent.com/38736127/174906036-68fc1be2-bbdf-4325-b8a6-aef145c6db30.mp4

### Fast scan mode

https://user-images.githubusercontent.com/38736127/174905966-ccff40c7-d833-44e5-9909-21d087c44660.mp4



### Spontaneous brain activity recorded in two-photon mode



https://user-images.githubusercontent.com/38736127/174909302-b3901000-2807-471f-93b6-27f24e98cbe1.mp4

## Building instructions


We start with the building instructions for a one-photon multicolor system. 



### Light-sheet cube



First order all part:

If you in
Objective: LMPLN5XIR
https://www.olympus-lifescience.com/modules/pdfgen/pdfmaker/en_pdf-export_objectives.7efd53eb1e8b4d509bc1bbe2184a7e28/LMPLN5XIR.pdf?rev=1615725199

* The main part of the light-sheet unit is  milled out of an aluminium block. If you do not have a mechanical workshop in house then you can download the 3D model, e.g. as a step file, and send it to an online milling service (e.g. https://xometry.eu/fr/usinage-cnc-fraisage-cnc/). 

* Attach the z- and x-translation stages to the cube. 

* Fix the adaptor plates to the system.

* Fix the collimation objective to the cube. 

* Fix the piezocrystal to the cube. 

* Fix the fiber holder to the piezo crystal.

* Screw in the FC/PC connector into the cyclinder and enter the cyclinder into the holder. 


* Connect the fiber. 

* Before you switch on the laser prepare laser safety in the room (remove you juwlerie, make sure that nobody is in the laser path and that the laser will not hit any reflecting surfaces. 

* Switch on the laser at low laser power. Adjust the distance of the fiber relative to the collimation objective until the laser is well collimated. 

* Switch off the laser. 

* Insert the galvometer mirror and rotate it such that the laser will be reflected our of the opening that will hold the illumination objective (45 degree position). 

* Switch on the laser.

* Carefully center the beam into the opening by fin adjusting the orentation of the galvometer mirror. Once done fix the mirror position with the fixation screw. 

* Fix the illumination objective.

* Detach the fiber to prevent to domage it and fix the ligh-sheet holder onto the motorized stage of the microscpe body.



### Detection path

* fix the detection objectives and insert the filters (?,?,?) in to the filter holders. Attach the Hamamatsu camera to the camera port. 


### Sample holder






















[Fiber coupling](Fiber_coupling)

[1P Multicolor Unit](1P_Multicolor_Unit)


[2P Unit](2P_Unit)


#### The light-sheet unit
![LightSheetUnit_different_Views](https://user-images.githubusercontent.com/38736127/175005382-7465c87b-a4d5-4bc8-8349-bc513ecaa548.png)


### CAD models

[CAD models](CAD_models)

[1P&2P_Assembly](CAD_models/1P&2P_Assembly.stl)

[Light-Sheet_Holder](CAD_models/Light-Sheet_Holder_Assembly_v3.stl)

[Light-Sheet_Unit](CAD_models/Light-Sheet_Unit_Assembly_v6.stl)


