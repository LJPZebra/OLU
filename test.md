# Coupling of a pulsed two-photon laser and a of visible laser into the hollow core fiber


## The optical path

The following schematic shows a possible optical path for the laser coupling. You can adapt the arrangement to the space availability on your setup (mirror, **M**, lens, **L**, dichroic, **D**, wave plate, **W**, polarizer, **P**):

<img width="400" alt="OpticalPath" src="https://user-images.githubusercontent.com/38736127/178073728-e55b142f-e37f-4267-9c27-1f29199aaddd.png">


If you do not have space on your table you can mount easily a platform on top of your IR pulsed laser source and bring the laser beam with a [periscope](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=883) up to the platform. 

We will give a step-by-step explanation that describes how to build this optical path and how to align the optical components to achieve optimal fiber coupling. But before we begin, we will give some preparatory notes and general background:

### Alignment procedure
For the alignment we will follow a protocol well explained in an excellent YouTube tutorial that you find here and that we advise you to watch carefully before starting. The video explains a first prealignment step based on backpropagation of a laser in the reverse direction. To use this trick first connect a standard single mode fiber to the coupling unit. Use a fiber tester to inject a visible laser through the fiber. Then follow the steps as in the tutorial to co-align the alignment laser and the IR laser. Then disconnect the fiber and connect the hollow core fiber. If the first step was well done you should have directly transmission through the fiber enough to optimize the further fiber coupling as described in the tutorial. To watch the video just click on the snap shoot: 

[<img width="400" alt="AlignmentTutorial" src="https://user-images.githubusercontent.com/38736127/176673048-5717d417-f3cd-4252-8551-5a9e17c1132f.png">](https://www.youtube.com/watch?v=kQvhbJbDG0M)

### Handling of the hollow core fiber
*  The hollow core fiber front face is not protected and cannot be easily polished, which is a standard procedure used for conventional single mode fibers. Also never try to clean the fiber outlet with ethanol or acetone because these solutions will enter the fiber core by capillary forces making the fiber unusable. You can use an [fiber inspection scope](https://www.thorlabs.com/thorproduct.cfm?partnumber=FS201) to inspect the fiber core.

* The fiber has a very high damage threshold but only if the laser is well coupled. So it is advice to do the alignment procedure at low laser power. This improves also laser safety. We will regulate the laser intensity with a rotatable [lambda wave plate](https://www.newport.com/p/10RP52-2) installed in series with a [polarizor]([https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS25-1064-HP](https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS252/M)). 

### Selection of the coupling lens

For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side has to match the [mode field diameter of the fiber](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=14203). Or in other words the opening angle of the focused laser beam has to match the numerical aperture of the fiber. Our fiber has a numerical aperture of 0.02 (see [fiber spec sheet](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf)).






## Now Let's build it 

### Coupling the IR laser
*	Position the [motorized flip mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=MFF101/M) (**M1**) holding a [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) directly after the infrared laser output to hijack the laser for coupling into the optical fiber. Flipping the mirror allows to select the setup into which you want to direct the laser. Alternatively, you can use a [beam splitter](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=6208&pn=BS033) to use the laser source on both setups simultaneously. The pertinence of the latter solution depends on the  laser power that you need in both setups for your experiments. For a standard scanning two-photon system you need in average < 100mW. The MaiTai laser has an average output power of 1.8mw at 915nm wavelength. With a 90:10% beam splitter and assuming 50% loss of laser power until the sample you can perform light-sheet microscopy with an average laser power of 400mW and two-photon scanning on the standard system with a mean power of 90mW. 
*	Next install the optics to control the laser intensity. Position the [lambda wave plate](https://www.newport.com/p/10RP52-2) and the [polarizor]([https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS25-1064-HP](https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS252/M)) in series. 
*   Before switching on the laser prepare for laser safety in the room and wear [laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*   Install the power meter to measure laser intensity after the polarizer (**P**)
*   Switch on the laser and rotate the wave plate until the transmitted laser power is minimal. 
*   Increase again slowly the laser power until you start to see the laser spot onto the IR detection card
*   Close the laser shutter
*   Position the two [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) (**M2 & M3**) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0). A good distance between these two mirrors is about 20cm. With these two mirrors you will later align the laser with the fiber axis. Select the height of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) that hold the mirrors compatible with the height of your laser beam.
*  Install the [long pass dichroic mirror](https://www.thorlabs.com/thorproduct.cfm?partnumber=DMLP650R) that is transparent for the infrared laser but reflects the visible spectrum . This will allow later the coupling of an addition visible laser into the same fiber. 
*	Mount the differential **xyz-translation stage** ([MAX313D/M](https://www.thorlabs.com/thorproduct.cfm?partnumber=MAX313D/M#ad-image-0)) at about 20cm distance of mirror **M3**. This stage will allow to position the fiber outlet precisely into the focal point of the coupling lens. You might have to mount this stage on a platform to match the beam height  (**CAD drawing [here ?????](fads) for compatibility with a MaiTai laser**). Alternatively you can lower the beam path with a [periscope](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=883).  
*  Install the half-wave plate mounted in a [high-precision rotation mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=PRM1/M) to adjust laser the polarization of the laser. 
*  Fix the  [mounting bracket](https://www.thorlabs.com/thorproduct.cfm?partnumber=AMA009) onto the non-moving front of the **xyz-stage** and mount onto it a [SM1-Compatible Flexure Stage Mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) to hold the coupling lens **L1**.
*  Screw the coupling lens into the holder ([AC254-040-B-ML](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-040-B-ML)) 
*  Mount the [SM1-compatible flexure stage mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) onto the moving platform of the xyz-stage and screw into this mount the [FC/PC fiber adapter plate with its external SM1 threading](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1FC2). To this FC/PC adapter you will later connect the optical fiber.
*	Attach the [single mode fiber](https://www.thorlabs.com/thorproduct.cfm?partnumber=P1-460B-FC-2) for prealignment to the FC/PC adaptor plate. 
*	Attach the other side of the fiber to the [cable continuity tester](https://www.flukenetworks.com/datacom-cabling/fiber-testing/VisiFault-Visual-Fault-Locator) for prealignment.
*	Switch on the red laser of the continuity tester. You should see the laser exiting out of the other side of the fiber
*	Adjust the distance of the coupling lens (**L1**) relative to the fiber outlet until the red laser light from the continuity tester is well collimated by the coupling lens. 
*	Now follow the alignment steps explained in the YouTube tutorial. Eventually, watch the video again.
*	Now where you know how to do it insure laser safety in the room and wear [laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*	Prepare a [VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2) to visualize the invisible infrared laser
*   Open the laser shutter.
*   Now move the two mirrors **M2** and **M3** to co-align the red laser and the IR laser as was explained in the video.
*   Switch off the laser shutter
*   Detach the single mode fiber from the coupling unit
*   Attach the [negative curvature broad band hollow core fiber](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf) to the coupling unit.
*   Position the power meter before the coupling lens and adjust the power to about ???mW.
* Install an FC/PC adaptor plate and fix to it the other end of the fiber. Install the power meter just after the fiber to measure the transmitted laser power.
* Open again the laser shutter. You should measure laser transmission through the fiber.
* Now adjust the mirrors **M2** and **M3** as was described in the video until you get > 90% laser transmission. 
* Close the laser shutter

### Install and adjust the NA expander
The collimation and illumination objective form a one-to-one telescope. If we would simply connect the hollow core fiber to the light-sheet unit as we did in the 1P-Multicolor system than the light-sheet thickness would correspond to the mean field diameter of the fiber which is ????um. To get the same resolution as in the one-photon implementation we have to install an extra lens after the fiber to demagnify the laser waist at the fiber output to about 5um and at the same time to increase the divergence angle of the laser to match the numerical aperture of the collimation objective. The numerical aperture of the fiber is 0.02 and thus a factor 5 times smaller compared to the numerical aperture of the detection objective. 

We chose a [lens](https://www.thorlabs.com/thorproduct.cfm?partnumber=C151TMD-B) with a focal distance of f = 2mm and a numerical aperture of 0.5. We place the lens at a distance $s = f \left( \frac{1}{m} - 1\right) = f \left( 5 - 1\right) = 4 \cdot f = 8 \textrm{mm}$ after the fiber output. The lens refocuses the laser at a new position $s' = f \cdot \left[ 1 + \frac{1}{s/f - 1} \right] = 1.2 \cdot f = 2.4\textrm{mm}$ after the lens with an angle of divergence of the laser corresponding to a numerical aperture of 0.1 and a waist of $m \cdot w_0 = 0.2 \cdot 23 \mu m = 4.6\mu m$. 


[Focusing of spherical Gaussian beams by Sidney A. Self](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.1091.571&rep=rep1&type=pdf)

### Coupling the visible laser
* Fix the [fiber coupled laser](https://github.com/vbormuth/OLU/files/9057780/WEBSITE-Datasheet-LBX-488.pdf) onto the table.
* Position mirror **M3** and **M4** with a distance of about 20cm between each other and such that mirror **M4** is placed about 20cm from the coupling lens. As mirrors choose again [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0) to align the laser with the fiber axis. Select the length of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) compatible with the hight of your laser beam.
* Attach the fiber splitter to the laser that you purchases with prealigned fiber coupler.
* Install a [prealigned fiber collimators](https://www.thorlabs.com/thorproduct.cfm?partnumber=F110FC-532) **L2** that you mount into a [kinematic mirror mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=KM05/M#ad-image-0) using an [adaptor](https://www.thorlabs.com/thorproduct.cfm?partnumber=AD11BA) and positioned onto the adequate [posts](https://www.thorlabs.com/thorproduct.cfm?partnumber=TR1) and its [universal post holder](https://www.thorlabs.com/thorproduct.cfm?partnumber=UPH1).
     * We selected the collimation lens focal distance with the formula: $f_{collimation} = f_{coupling} *  \frac{NA_{fiber}}{NA_{laser fiber}} = 40\textrm{mm} * \frac{0.02}{0.13}$
Which boils down to the fact to choose the coupling lens focal distance such that the collimated laser beam diameter is matches the diameter of the infrared beam that we previously coupled into the fiber using the chosen coupling lens. 
* Attach one of the outputs of the fiber coupler to this collimator lens. 
* Attach the other side to the FC/PC connector plate on the **xyz-stage** of the coupling unit. If the fiber is to short you can extend it with a [fiber-to-fiber connector](https://www.thorlabs.com/thorproduct.cfm?partnumber=ADAF1) and the single mode fiber that you have used in the previous prealignment step.
* prepare laser safety and switch on the laser at lowest power possible were you can see with the [VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2) the laser.
* Now use the mirror **M3** and **M4** to co-align the two laser beams that travel in reverse direction through the system as explained in the alignment YouTube tutorial. 
* Switch off the laser and replace the single mode fiber that is connected to the coupling unit with the negative curvature fiber.
* Switch the laser again on.
* You should detect with the power meter a transmission through the fiber.
* Adjust mirror **M3** and **M4** until you have more than 75% percent of transmission

At 915nm wavelength, the central two-photon absorption peak of GFP and of its calcium sensitive derivative GCaMP, we delivered through 1.5m fiber length 100fs laser pulses with 98% power transmission efficiency and minute pulse dispersion of 28nm (1dB/km·nm) that we fully precompensated with the Deepsee element of the MaiTai laser source. At 488nm,  the one-photon excitation maximum of GFP and GCaMP, we achieved a transmission efficiency of ~75%. 









 








