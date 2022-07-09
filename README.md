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

#### Let's start to assemble

![BuildingInstructions](https://user-images.githubusercontent.com/38736127/176259875-00e95eff-b3b2-4a9b-b127-b309bcc323d5.png)



(1) Purchase the laser directly fiber coupled.

(2) 
* Prepare the main cube (green) of the light-sheet unit. It is  milled out of an aluminium block. If you do not have a mechanical workshop in house then you can download the 3D model, e.g. as a step file, and send it to an online milling service (e.g. https://xometry.eu/fr/usinage-cnc-fraisage-cnc/). 

* Fix the collimation objective to the cube. 

(3) Fix the piezocrystal to the cube (dark gray). 

(4) Fix the fiber holder to the piezo crystal (red).

(5-7) Fix the fiber to the FC/PC connector and screw the connector into the cyclinder (black) but not too far so that you can easily attach and detach the fiber. 

(8) Fix the fiber via the cylinder to the ligh-sheet unit.

(9) Before you switch on the laser prepare laser safety in the room (remove you juwlerie, make sure that nobody is in the laser path and that the laser will not hit any reflecting surfaces. Then switch on the laser at low laser power. Adjust the distance of the fiber relative to the collimation objective until the laser exits the cube well collimated. Switch off the laser again. 

(10) Insert the galvometer mirror and rotate it such that the laser will be reflected our of the opening that will hold the illumination objective (45 degree position). Switch on the laser. Carefully center the beam into the opening by fin adjusting the orentation of the galvometer mirror. Once done fix the mirror position with the fixation screw. 

(11) Detach the fiber to prevent to domage it and fix the ligh-sheet holder onto the motorized stage of the microscpe body.

(12) Fix the illumination objective to the light-sheet unit and attach again the fiber. Now you can attach the imaging objective to the microscope. 




![LightSheetUnit_different_Views](https://user-images.githubusercontent.com/38736127/175005382-7465c87b-a4d5-4bc8-8349-bc513ecaa548.png)


### Detection path

* fix the detection objectives and insert the filters (?,?,?) in to the filter holders. Attach the Hamamatsu camera to the camera port. 
* We used a Olympus 20x objective with a custom tube lens of 150mm focal lenth. 


### Sample holder

[Fiber coupling](Fiber_coupling.md)

[1P Multicolor Unit](1P_Multicolor_Unit.md)


[2P Unit](2P_Unit.md)





### CAD models

[CAD models](CAD_models)

[cube](CAD_models/cube.stl)

[1P&2P_Assembly](CAD_models/1P&2P_Assembly.stl)

[Light-Sheet_Holder](CAD_models/Light-Sheet_Holder_Assembly_v3.stl)

[Light-Sheet_Unit](CAD_models/Light-Sheet_Unit_Assembly_v6.stl)


