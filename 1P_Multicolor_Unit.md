## Purchase list

## Pieces to send for milling

#### Let's start to assemble


![BuildingInstructions](https://user-images.githubusercontent.com/38736127/178075149-4b1e094c-851a-4eff-bd80-95e90b93983e.png)


(1) Purchase a blue 488nm and a green 5??nm [laser with prealigned fiber coupler](https://github.com/vbormuth/OLU/files/9057780/WEBSITE-Datasheet-LBX-488.pdf)

(2) To combine the two lasers into a single mode fiber attach the two inputs of the [fiber optic coupler](https://www.thorlabs.com/thorproduct.cfm?partnumber=TW470R5F2) to the FC/PC connector of each laser. The blue and the green lasers will be combined and are available at both output fiber ports. 

(3) 
* Prepare the main cube (green) of the light-sheet unit. It is  milled out of an aluminium block. If you do not have a mechanical workshop in house then you can download the [3D model](CAD_models/Cube.stl), e.g. as a step file, and send it to an online milling service (e.g. https://xometry.eu/fr/usinage-cnc-fraisage-cnc/). 

* Fix the [collimation objective](https://www.micro-shop.zeiss.com/en/us/shop/objectives/420330-9901-000/Objective-EC-Plan-Neofluar-5x-0.16-M27) to the cube. 

* Fix the [piezocrystal (PZ 400 SG OEM)](https://www.piezosystem.com/product/pz-400-oem/) to the cube (dark gray). 

(4) Fix the fiber holder to the piezo crystal (red).

(5-7) Fix one of the output fibers of the fiber optic coupler to the [FC/PC connector](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM05FC#ad-image-0) and screw the connector into the cyclinder (black) but not too far so that you can easily attach and detach the fiber. 

(8) Fix the fiber via the cylinder to the ligh-sheet unit.

(9) Before you switch on the laser prepare laser safety in the room (remove you juwlerie, make sure that nobody is in the laser path and that the laser will not hit any reflecting surfaces. Then switch on the laser at low laser power. Adjust the distance of the fiber relative to the collimation objective until the laser exits the cube well collimated. Switch off the laser again. 

(10) Insert the [galvometer mirror](https://www.thorlabs.com/thorproduct.cfm?partnumber=GVS011) and rotate it such that the laser will be reflected our of the opening that will hold the illumination objective (45 degree position). Switch on the laser. Carefully center the beam into the opening by fin adjusting the orentation of the galvometer mirror. Once done fix the mirror position with the fixation screw. 

(11) Detach the fiber to prevent to domage it and fix the ligh-sheet holder onto the motorized stage of the microscpe body.

(12) Fix the [illumination objective](https://www.micro-shop.zeiss.com/en/us/shop/objectives/420330-9901-000/Objective-EC-Plan-Neofluar-5x-0.16-M27) to the light-sheet unit and attach again the fiber. Now you can attach the imaging objective to the microscope. 
 

![LightSheetUnit_different_Views](https://user-images.githubusercontent.com/38736127/175005382-7465c87b-a4d5-4bc8-8349-bc513ecaa548.png)



### Detection path

* fix the detection objectives 
* Install the filters
     * a [notch filter to block the 488nm laser line](https://www.thorlabs.com/thorproduct.cfm?partnumber=NF488-15)
     * a GFP bandpass fiber (?,?,?) in to the filter holders. Attach the Hamamatsu camera to the camera port. 
* We used a Olympus 20x objective with a custom tube lens of 150mm focal lenth. 


### Sample holder
