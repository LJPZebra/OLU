# A Versatile and Open Source One- and Multi-Photon Light-Sheet Microscope Design

<!---  # An Open Source 1P and 2P miniDSPIM with broadband fiber based laser delivery    --->

### Abstract
Two-photon light sheet microscopy has a wide range of applications in biology. Here we report a novel open source design to transform a standard microscope into a 1P \& 2P light-sheet microscope. A specially designed broadband hollow core fiber shares the expansive pulsed laser source from other setups. The system provides uncompromised image resolution and speed and makes this technology widely accessible at reduced cost.

![CompilationFigure_v3](https://user-images.githubusercontent.com/38736127/174906572-d85802cc-6171-40a8-a8f5-7138b5235d8f.png)

(a) 3D model of the 1P- \& 2P-light-sheet forming unit. (b) 3D design model showing how the one- and two-photon light-sheet unit is mounted on the Scientifica scope. The unit is attached to the motorized stage of the system that moves the objective. (c) Attenuation and dispersion spectrum of the hollow-core negative curvature fiber with two transmission bands (loss $<$ 300dB/km) highlighted in yellow. Inset left: Schematic of the cross section of the hypocycloid fiber with 8 cladding tubes. Inset right: EM cross section image of the fiber (scale bar $10\mu m$). (d) Near and far field profile of the fiber output at 515nm and 1030nm laser wavelength. (e) Schematic of the fiber with its FC/PC connectorization and the lens to increase the numerical aperture (NA) to match the NA of the collimation objective (Obj1 in a). (f) Measured light-sheet profile. (g) Single layers of a volumetric brain scan recorded in one- and two-photon mode of a 6dpf old zebrafish larva expressing pan-neuronally GCaMP6f and localized to the cell nucleus (Elav3-H2B-GCaMP6f).


### Slow scan mode

https://user-images.githubusercontent.com/38736127/174906036-68fc1be2-bbdf-4325-b8a6-aef145c6db30.mp4

### Fast scan mode

https://user-images.githubusercontent.com/38736127/174905966-ccff40c7-d833-44e5-9909-21d087c44660.mp4

### High resolution zebrafish brain scans (elav3:H2B-GCaMP6)

* Left: one-photon mode excited @ 488nm
* Right:  two-photon mode excited @ 915nm

https://user-images.githubusercontent.com/38736127/178161973-748767bf-004d-487c-9377-4582a705d8d7.mp4


### Spontaneous brain activity recorded in two-photon mode



https://user-images.githubusercontent.com/38736127/174909302-b3901000-2807-471f-93b6-27f24e98cbe1.mp4


## Detailed Building instructions:


1. Build first a [multicolor one-photon version of the microscope](1P_Multicolor_System.md) with fiber delivery of lasers in the visible spectrum with a standard single mode optical fiber technology.

2. [Upgrade the one-photon unit into a two-photon system](2P-upgrade.md) by exploiting advanced hollow core fiber technology.

3. [Design idea for an alternative implementation](https://user-images.githubusercontent.com/38736127/177863005-d570b9a1-ee6d-4875-a736-51e224426fb9.png)



### CAD models

[CAD models](CAD_models)

* [cube](CAD_models/cube.stl)

* [1P&2P_Assembly](CAD_models/1P&2P_Assembly.stl)

* [Light-Sheet_Holder](CAD_models/Light-Sheet_Holder_Assembly_v3.stl)

* [Light-Sheet_Unit](CAD_models/Light-Sheet_Unit_Assembly_v6.stl)




