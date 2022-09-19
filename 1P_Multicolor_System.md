# Building instructions

<img width="200" alt="BraintegrationSetup" src="https://user-images.githubusercontent.com/38736127/191005334-d6b4648a-3c93-444d-b89d-bb6020adbc93.png">

<img width="200" alt="ZoomOnLightsheetUnit" src="https://user-images.githubusercontent.com/38736127/191005465-878de37b-74be-4a11-a2f8-290c814e2811.png">


## Purchase list

[List of parts](Partlist.md)



## Pieces to send for milling
    
    
These pieces are  milled out of an aluminum block. If you do not have a mechanical workshop in house then you can send the *.step files that we provide below to an [online milling service](https://xometry.eu/fr/usinage-cnc-fraisage-cnc/).
* The light-sheet unit central cube: [View the 3D model](CAD_models/Cube.stl) or [download the CAD model as a step file ????](CAD_models/Cube.stp).
* The fiber holder  ?????: [View the 3D model????](CAD_models/FiberHolder.stl) or [download the CAD model as a step file ?????](CAD_models/FiberHolder.stp).
* Adaptor plate 1 ??????: [View the 3D model????](CAD_models/AdaptorPlate1.stl) or  [download the CAD model as a step file ?????](CAD_models/AdaptorPlate1.stl).
* Adaptor plate 2 ???????: [View the 3D model????](CAD_models/AdaptorPlate2.stl) or  [download the CAD model as a step file????](CAD_models/AdaptorPlate2.stl).
* Sample holder: [View the 3D model](CAD_models/SampleHolder.stl) or [download the CAD model as step file](CAD_models/SampleHolder.stp).
* Piezoactuator placeholder ????: [View the 3D model????](PiezoactuatorPlaceHolder.stl) or [download the CAD model as step file?????](CAD_models/PiezoactuatorPlaceHolder.stp). This piece is only necessary if you do not want to install the piezo actuator required for the fast scan mode.
    


## Pieces for 3D printing
* [Sample chamber](CAD_models/SampleChamber.stl). You can download the [CAD model as step file](CAD_models/SampleHolder.stp) here to send it to your 3D printing service.


## Let's start to assemble

### The light-sheet unit

![BuildingInstructions](https://user-images.githubusercontent.com/38736127/178075149-4b1e094c-851a-4eff-bd80-95e90b93983e.png)


(1) Purchase a blue 488nm and a green 5??????nm [laser with prealigned fiber coupler](https://github.com/vbormuth/OLU/files/9057780/WEBSITE-Datasheet-LBX-488.pdf)

(2) To combine the two lasers into a single mode fiber attach the two inputs of the [fiber optic coupler](https://www.thorlabs.com/thorproduct.cfm?partnumber=TW470R5F2) to the FC/PC connector of each laser. The blue and the green lasers will be combined and are available at both output fiber ports.

(3) Start assembling the light-sheet unit
* Fix the [collimation objective](https://www.micro-shop.zeiss.com/en/us/shop/objectives/420330-9901-000/Objective-EC-Plan-Neofluar-5x-0.16-M27) to the light-sheet unit central cube (green).
* Fix the [piezocrystal (PZ 400 SG OEM)](https://www.piezosystem.com/product/pz-400-oem/) to the cube (dark gray). If you want to start with a simple low cost version that uses only the slow scanning mode then install instead the piezo placeholder element. This part is milled out of aluminum. You can download the [CAD step file of the piezo place holder ????](CAD_models/PiezoPlaceHolder.stp) here to send it to your milling service.

(4) Fix the fiber holder (red) to the piezo crystal. The fiber holder is milled out of aluminum. You can download the [fiber holder](CAD_models/FiberHolder.stp) here to send it to your milling service.


(5-7) Take the [FC/PC connector](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM05FC#ad-image-0) which will later hold the optical fiber that delivers the laser. Screw the connector into the [lens tube](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM05M10) (black) but not too far so that you can easily attach and detach the optical fiber. Fix the connector with the two retaining rings.

(8) Fix the lens tube cylinder that you prepared in step (5-7) to the light-sheet unit via the optical fiber holder (red) and attach one of the output fibers of the fiber optic coupler to the connector.

(9) Before you switch on the laser, prepare laser safety in the room (remove your jewelry, make sure that nobody is in the laser path and that the laser will not hit any reflecting surfaces. Then switch on the laser at low laser power. Adjust the distance of the fiber relative to the collimation objective until the laser exits the cube well collimated. Switch off the laser again.

(10) Insert the [galvanometer mirror](https://www.thorlabs.com/thorproduct.cfm?partnumber=GVS011) and switch it on. Rotate the galvo system such that the laser will be reflected out of the opening that will hold the illumination objective (45 degree position). Switch on the laser. Carefully center the beam into the opening by carefully adjusting the orientation of the galvanometer mirror. Once done, fix the mirror position with the fixation screw.

(11-14) Screw the x-translation stage onto the z-translation stage and fix the assembly to the two adaptor plates (blue).

(15) Screw the light-sheet cube onto the x-translation stage.

(16) Fix the light-sheet cube via the adapter plate onto the motorized stage of the microscope body. (?????? Do we have to drill holes into the microscope parte first ????? )

(17) Fix the [illumination objective](https://www.micro-shop.zeiss.com/en/us/shop/objectives/420330-9901-000/Objective-EC-Plan-Neofluar-5x-0.16-M27) to the light-sheet unit and attach again the optical fiber and fix the illumination objective onto the light-sheet cube.


![LightSheetUnit_different_Views](https://user-images.githubusercontent.com/38736127/175005382-7465c87b-a4d5-4bc8-8349-bc513ecaa548.png)


### The detection path

To configure the detection path you use the standard ports and configuration of the Scientifica scope.

* Use a detection objective that is best adapted to your application. If you want to install the fast z-scan mode then install the objective with an [objective scanning piezo system](https://www.pifrance.fr/fr/produits/platines-de-nanopositionnement-a-structure-deformable/support-objectif-pifoc-et-scanners-pinano-pour-la-microscopie/p-725-pifoc-objective-scanner-with-long-travel-range-200375/).
<!--- We used an [Olympus 20x objective](https://www.thorlabs.com/catalogpages/Obsolete/2019/N60XW-PF.pdf) in combination with a lens of 150mm focal length as [tube lens](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-150-A) to reduce the magnification to 16x for the imaging system. --->
* Install the filters into the filter wheel
     * a [notch filter to block the 488nm laser line](https://www.thorlabs.com/thorproduct.cfm?partnumber=NF488-15)
     * a [GFP Emission Filter](https://www.thorlabs.com/thorproduct.cfm?partnumber=MF525-39).
* Attach the camera to the camera port. We used the [Hamamatsu ORCA-Flash4.0 V3 camera](https://www.hamamatsu.com/content/dam/hamamatsu-photonics/sites/documents/99_SALES_LIBRARY/sys/SCAS0134E_C13440-20CU_tec.pdf)




### The sample chamber holder and sample chamber

* Install the [sample holder](CAD_models/SampleHolder.stl). This part is milled out of aluminum. You can download the [CAD step file of holder](CAD_models/SampleHolder.stp) here to send it to your milling service.
* 3D print the [sample chamber](CAD_models/SampleChamber.stl). You can download the [CAD step file of the sample chamber](CAD_models/SampleHolder.stp) here to send it to your 3D printing service. Glue with superglue two glass windows on both side (??????) as well as an [O-ring](https://www.oring.fr/joint-torique/22-1.html?search_query=&results=45) into the hole on the short side which will allow you later to hold and position the sample via a [capillary](https://www.alphalabs.co.uk/5-000-2050) (inner diameter 0.85mm, outer diameter 1.47mm, length 115mm) for the imaging sessions. As glue we use a UV glue (????) but you can also use standard superglue. Place the sample chamber into the predefined opening of the sample holder.

![SampleHolder](https://user-images.githubusercontent.com/38736127/178137631-2c89b6cf-9c1a-4c7f-b7f9-2d27c1fac82d.png)



<!--- https://www.fishersci.fi/shop/products/plunger-acura-capillary-micropipettes/p-8481034 --->



### Now let's align the system
* Fill the sample chamber with water and add a drop of ????mM fluorescein to visualize the laser. Switch-on the laser at low power until you can see the fluorescence laser profile. Be careful not to look directly into the laser!

<img width="200" alt="Picture of laser" src="https://user-images.githubusercontent.com/38736127/186088660-4590242d-2d1e-4357-8bcd-4d5d63d3d97d.jpg">

* Align the laser waist under the detection objective by moving the entire light-sheet forming unit with the x-translation stage
* Switch on the camera and align the laser into the focal plane of the detection objective by moving the light-sheet forming unit with the z-translation stage until you see a sharp image of the laser with the camera. If you do not see the laser move the galvanometer mirror to bring the laser into the field of view.
* Fine align the laser waist into the center of the field of view using the x-translation stage
* Now drive the galvanometer with a saw tooth pattern. You can do this without computer interfacing by using a [function generator]() via a function generator by using an [I/O-card]() and controlled via a dedicated [computer software](Software.md) to generate the light-sheet. Adjust the amplitude of the movement such that the light-sheet covers exactly the field of view.
* Now you can place your prefered sample into the light-sheet and image it! Move the manual objective focus of the microscope and you can scan in 3D through your sample or record 3D time lapse movies using your microscope control software that synchronizes the objective movement with image acquisition.
* Troubleshooting:
    * Your image is not sharp homogeneously across the field of view: The light-sheet might be tilted with respect to the focal plane of the detection objective.  In this case you can correct this by tilting slightly the entire unit. For this, unscrew slightly screws that fix the unit via the adapter plate to the microscope translation stage. Insert a thin paper partly between the adapter plate and the stage such that the unit gets tiltited in the correct direction once you refix the screws. Repeat this procedure until your image is in focus across the entire field of view.

### Advanced version for fast volumetric imaging

* Mount the detection objective via an objective [focus scanner for microscope ojektives](https://www.physikinstrumente.de/de/produkte/piezo-nanopositioniertische/pifoc-objektivscanner-pinano-probentische-fuer-die-mikroskopie/p-725xcde2-pifoc-objektivscanner-mit-langem-stellweg-412418521/)
* Install the [piezo crystal to rapidly move the fiber outlet](https://www.piezosystem.com/product/pz-400-oem/)
* Use the monitor signal of the focus scanner as the control signal of the piezo crystal that drives the height of the fiber. Calibrate the voltage with a [potentiometer](add link here ??????)


## Example recordings:

Using the green laser. Shown is a high resolution recording of a zebrafish brain (6dpf) with a pan-neuronally expressed red calcium indicator (elav3-jRGECO):

https://user-images.githubusercontent.com/38736127/186108000-6d6c7374-28b0-485f-a63a-da5b19ce9631.mp4



## Upgrade the one-photon unit into a two-photon system


[Click here for detailed instructions](2P-upgrade.md)










