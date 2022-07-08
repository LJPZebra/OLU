# Coupling of a pulsed two-photon laser and a of visible laser into the hollowo core fiber


## The optical path

The following schematic shows a possible optical path for the laser coupling. You can adapt the arrangement to the space availability on your setup (mirro, M, lens, L, dichroic, D, wave plate, W, polarizor, P):

<img width="400" alt="OpticalPath" src="https://user-images.githubusercontent.com/38736127/178027710-59000f23-4e21-449d-b615-3f9d77ad908b.png">

We will give a step-by-step explanation of how to built up this optical path and to do the alignment of the optical components. But before we start some preparatory notes and general background:

### Alignment procedure
For the alignment we will follow a protocol well explained in an excellent youtube tutorial that you find here and that we advice you to watch carefull before starting. The video explains a first prealignment step based on backpropagation of a laser in the reverse direction. To use this trick first connect a standard single mode fiber to the coupling unit. Use a fiber tester to inject a visible laser through the fiber. Then follow the steps as in the tutorial to co-align the alignement laser and the IR laser. Then disconnect the fiber and connect the hollow core fiber. If the first step was well done you should have direcly transmission through the fiber enough to optimize the further fiber coupling as described in the tutorial. To watch the video just click on the snap shoot: 

[<img width="400" alt="AlignmentTutorial" src="https://user-images.githubusercontent.com/38736127/176673048-5717d417-f3cd-4252-8551-5a9e17c1132f.png">](https://www.youtube.com/watch?v=kQvhbJbDG0M)

### Handling of the hollow core fiber
*  The hollow core fiber front face is not protected and cannot be easily polished, which is standart for conventional single mode fibers. Also never try to clean the fiber outlet with ethanol or acethon because these solutions will enter the fiber core by capillary forces making the fiber unusalbe. You can use an [fiber inspection scope](https://www.thorlabs.com/thorproduct.cfm?partnumber=FS201) to inspect the fiber core.

* The fiber has a very high domage threshold but only if the laser is well coupled. So it is adviced to do the alignemnt procedure at low laser power. This improves also laser safety. We will regulate the laser intensity with a rotatable [lambda wave plate](https://www.newport.com/p/10RP52-2) installed in series with a [polarizor]([https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS25-1064-HP](https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS252/M)). 


### Selection of the coupling lens
For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side has to match the mode field diameter of the fiber. Or in other words the opening angle of the focused laser beam has to match the numerical apperture of the fiber. Our fiber has a numerical apperture of 0.02 (see [fiber spec sheet](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf))

The numercial apperture of the coupling system is given by $NA = \frac{D}{2 f}$, with *D* the diameter of the laser beam at the position of the coupling lens, and *f* the coupling lens' focal length. The laser company normally gives the beam width and the beam divergent angle. At the position were one can place the coulping unit after the laser output the beam divergence angle determines the beam width. You can measure the diameter of the laser either with a beam profiler (Thorlabs BC207VIS/M) or with the [moving knif technique](https://www.researchgate.net/profile/Emerson-Lima-2/publication/23771279_Measurement_of_Gaussian_laser_beam_radius_using_the_knife-edge_technique_Improvement_on_data_analysis/links/00b7d533ec8470fe22000000/Measurement-of-Gaussian-laser-beam-radius-using-the-knife-edge-technique-Improvement-on-data-analysis.pdf?origin=publication_detail). In our case, with a Ti:Sapphire laser (MaiTai, Coherent, USA), we measured a beam diameter of 1.6mm at the position where we decided to install the coupling unit and we thus chose a coupling lens with focal length $f = \frac{D}{2 NA} = \frac{1.6mm}{2 * 0.02} = 40mm$. 

We got reasonalbe coupling with the achromatic coupling lens. If you want to further optimize the coupling you can use an objective as coupling lens, e.g. the Olympus LMPLN5xIR/0.10. You can install a telescope to adjust the beam diameter to match the fiber numerical apperture with the choosen coupling lens focal distance.  

Further tips for the fiber coupling can be found in the [manual from GLO-photonics](https://github.com/vbormuth/OLU/files/9039094/PIP_PMC-OEM.pdf).

## Now Let's do it 

### Coupling the IR laser
*	Position the [motorized flip mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=MFF101/M) (**M1**) holding a [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) directly after the infrared laser output to highcheck the laser for coupling into the optical fiber. Flipping the mirror allows to select the setup into which you want to direct the laser. Alternatively, you can use a [beam splitter](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=6208&pn=BS033) to use the laser source on both setups simultaneously. The pertinance of the latter solution depends on the  laser power that you need in both setups for your experimets. For a standard scanning two-photon system you need in average < 100mW. The MaiTai laser has an average output power of 1.8mw at 915nm wavelength. With a 90:10% beam splitter and assuming 50% loss of laser power until the sample you can perform light-sheet microscopy with an average laser power of 400mW and two-photon scanning on the standard system with a mean power of 90mW. 
*	Next install the optics to control the laser intensity. Position the [lambda wave plate](https://www.newport.com/p/10RP52-2) and the [polarizor]([https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS25-1064-HP](https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS252/M)) in series. 
*   Before switching on the laser prepare for laser safety in the room and wear [laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*   Install the power meter to measure laser intensity after the polarizer (**P**)
*   Switch on the laser and rotate the wave plate until the transmitted laser power is minimal. 
*   Increase again slowly the laser power until you start to see the laser spot onto the IR detection card
*   Close the laser shutter
*   Position the two [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) (**M2 & M3**) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0). A good distance between these two mirrors is about 20cm. With these two mirrors you will later align the laser with the fiber axis. Select the hight of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) that hold the mirrors compatible with the hight of your laser beam.
*  Install the [longpass dichroic mirror](https://www.thorlabs.com/thorproduct.cfm?partnumber=DMLP650R) that is transparent for the infrared laser but reflects the visible spectrum . This will allow later the coupling of an addition visible laser into the same fiber. 
*	Mount the the differential **xyz-translation stage** ([MAX313D/M](https://www.thorlabs.com/thorproduct.cfm?partnumber=MAX313D/M#ad-image-0)) at about 20cm distance of mirror M3. This stage will allow to position the fiber outlet precisely into the focal point of the coupling lens. 
*  Install the half-wave plate mounted in a [high-precision rotation mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=PRM1/M) to adjust laser the polarization of the laser. 
*  Fix the  [mounting bracket](https://www.thorlabs.com/thorproduct.cfm?partnumber=AMA009) onto the non-moving front of the xyz-stage and mount onto it a [SM1-Compatible Flexure Stage Mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) to hold the coupling lens.
*  Screw the coupling lens into the holder ([AC254-040-B-ML](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-040-B-ML)) 
*  Mount the [SM1-compatible flexure stage mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) onto the moving platform of the xyz-stage and screw into this mount the [FC/PC fiber adapter plate with its external SM1 threading](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1FC2). To this FC/PC adapter you will later connect the optical fiber.
*	Attache the [single mode fiber](https://www.thorlabs.com/thorproduct.cfm?partnumber=P1-460B-FC-2) for prealignment to the FC/PC adaptor plate. 
*	Attache the other side of the fiber to the [cable continuity tester](https://www.flukenetworks.com/datacom-cabling/fiber-testing/VisiFault-Visual-Fault-Locator) for prealigment.
*	Switch on the red laser of the continuity tester. You should see the laser exiting out of the other side of the fiber
*	Adjust the distance of the coupling lens (**L1**) relative to the fiber outlet unitl the red laser light from the continouity tester is well collimated by the coupling lens. 
*	Now follow the alignement steps explained in the youtube tutorial. Eventually, watch the video again.
*	Now where you know how to do it insure laser safety in the room and wear [laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*	Prepare a [VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2) to visualize the invisible infrared laser
*   Open the laser shutter.
*   Now move the two mirrors **M2** and **M3** to co-align the red laser and the IR laser as was explained in the video.
*   Switch off the laser shutter
*   Detach the single mode fiber from the coupling unit
*   Attach the negative curvature broad band hollow core [fiber](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf) to the coupling unit.
*   Position the powermeter before the coupling lens and adjust the power to about ???mW.
* Install an FC/PC adaptor plate and fix to it the other end of the fiber. Install the powermeter just after the fiber to measure the transmitted laser power.
* Open again the laser shutter. You should measure laser transmission through the fiber.
* Now adjust the mirrors M2 and M3 as was discribed in the video until you get > 90% laser transmission. 
* Close the laser shutter
* Detach the NCF-fiber from the coupling unit.

### Coupling the visible laser
* Fix the [fiber coupled laser](https://github.com/vbormuth/OLU/files/9057780/WEBSITE-Datasheet-LBX-488.pdf) onto the table.
* Position mirror **M3** and **M4** with a distance of about 20cm between each other and such that mirror M4 is placed about 20cm from the coupling lens. As mirrors choose again [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0) to align the laser with the fiber axis. Select the length of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) compatible with the hight of your laser beam.
* Attach the fiber splitter to the laser that you purchases with prealigned fiber coupler.
* Install a [prealigned fiber collimators](https://www.thorlabs.com/thorproduct.cfm?partnumber=F110FC-532) that you mount into a [kinematic mirror mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=KM05/M#ad-image-0) using an [adaptor](https://www.thorlabs.com/thorproduct.cfm?partnumber=AD11BA) and positioned onto the adequat [posts](https://www.thorlabs.com/thorproduct.cfm?partnumber=TR1) and its [universal post holder](https://www.thorlabs.com/thorproduct.cfm?partnumber=UPH1).
     * We selected the collimation lens focal distance with the formula: $f_{collimation} = f_{coupling} *  \frac{NA_{fiber}}{NA_{laser fiber}} = 40mm * \frac{0.02}{0.13}$
Which boils down to the fact to choose the coupling lens focal distance such that the collimated laser beam diameter is matches the diameter of the infrared beam that we previously coupled into the fiber using the choosen coupling lens. 
* Attach one of the outputs of the fiber coupler to this collimator lens. 
* Attach the other side to the FC/PC connector plate on the xyz-translation stage of the coupling unit. If the fiber is to short you can extend it with a [fiber-to-fiber connector](https://www.thorlabs.com/thorproduct.cfm?partnumber=ADAF1) and the single mode fiber that you have used in the previous prealignment step.
* prepare laser satety and switch on the laser at lowerst power possible were you can see with the [VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2) the laser.
* Now use the mirror **M3** and **M4** to co-align the two laser beams that traval in revers direction through the system as explained in the alignment youtube tutorial. 
* Switch off the laser and replace the single mode fiber that is connected to the coupling unit with the negative curvature fiber.
* Switch the laser again on.
* You should detect with the powermeter a transmission through the fiber.
* Adjust mirror **M3** and **M4** until you have more than 75% percent of transmission

At 915nm wavelength, the central two-photon absorption peak of GFP and of its calcium sensitive derivative GCaMP, we delivered through 1.5m fiber length 100fs laser pulses with 98% power transmission efficiency and minute pulse dispersion of 28nm (1dB/km·nm) that we fully precompensated with the Deepsee element of the MaiTai laser source. At 488nm,  the one-photon excitation maximum of GFP and GCaMP, we achieved a transmission efficiency of ~75%. 

### Measure the laser beam diameter with the moving kif technique

To measure the beam width you can use the [moving knif technique](https://www.researchgate.net/profile/Emerson-Lima-2/publication/23771279_Measurement_of_Gaussian_laser_beam_radius_using_the_knife-edge_technique_Improvement_on_data_analysis/links/00b7d533ec8470fe22000000/Measurement-of-Gaussian-laser-beam-radius-using-the-knife-edge-technique-Improvement-on-data-analysis.pdf?origin=publication_detail).

the normalized transmitted power is given by 0.5(1+erf((x-x0)/w))  with w the beam width at 1/e

https://www.researchgate.net/figure/Measurement-of-the-focal-spot-size-by-the-knife-edge-method-The-measured-signal-gray_fig12_8185920

which is the width between the point where the intesisty is between 1-0.92 times the maximum and 0.92 times the maximum. 
we2 = we1 * \sqrt(2)

Translation stage: XRN25C/M
PC2/M holder for thin plate 
for horizontal mounting RA90



To match the mode field diameter, you have the laser diameter and the coupling lens focal distance to play with. A Gaussian beam is never perfectly collimated.

Our laser has at the output a width of …. and a divergence of …  (see spec sheet). 

D(x; w_L0)= lambda 2 f/ (\pi n ??? x).

In our case we placed the coupling unit at a distance of 1.5m and we used a coupling lens of ???mm. 



========

=====






* a [collimation lens](https://www.thorlabs.com/thorproduct.cfm?partnumber=C171TMD-A). 




We coupled the femtosecond pulsed Ti:Sapphire laser (MaiTai, Coherent, USA) with a mirror, a dichroic and a coupling lens (f=40mm, Thorlabs, AC254-040-B-ML) into the fiber that was hold by a differential xyz-translation stage. The coupling mirror was placed on a magnetic precision stand so that it could be temporally removed to use the laser on the standard microscope setup.


## For the coupling we will need :
*	the negative curvature broad band hollow core [fiber](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf) with FC/PC connectors.
*	a coupling lens to focus the laser into the fiber ([AC254-040-B-ML](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-040-B-ML))
*	eventually a telescope to adjust the beam diameter for optimal coupling
*	a differential xyz-translation stage ([MAX313D/M](https://www.thorlabs.com/thorproduct.cfm?partnumber=MAX313D/M#ad-image-0)) to position the fiber outlet precisely into the focal point of the coupling lens. You might have to mount this stage on a platform to match the beam hight (**CAD drawing here for compatibility with a MaiTai laser**). Alternativeley you can lower the beam path with a [periscope](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=883).  
    - Use the [SM1-Compatible Flexure Stage Mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) to mount a [FC/PC Fiber Adapter Plate with External SM1 threading](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1FC2) onto this stage. To this FC/PC adapter you will later connect the optical fiber.
    - Use the  [Mounting Bracket](https://www.thorlabs.com/thorproduct.cfm?partnumber=AMA009) and a [SM1-Compatible Flexure Stage Mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) to position and hold the coupling lens in front of the fiber. 
*	Two [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0) to align the laser with the fiber axis. Select the length of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) compatible with the hight of your laser beam.
*	a [longpass dichroic mirror](https://www.thorlabs.com/thorproduct.cfm?partnumber=DMLP650R) that is transparent for the infrared laser but reflects the visible spectrum . This will allow coupling in addition a visible laser into the same fiber. Alternatively, you can also use a short pass dichroic (transparent for the visible laser and reflecting the infrared light). Both configurations will work.
*	a [Single mode fiber](https://www.thorlabs.com/thorproduct.cfm?partnumber=P1-460B-FC-2) for prealignment 
*	a [VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2) to visualize the invisible infrared laser
*	a [cable continuity tester](https://www.flukenetworks.com/datacom-cabling/fiber-testing/VisiFault-Visual-Fault-Locator) for prealigment
*	[laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*	a [fiber inspection scope](https://www.thorlabs.com/thorproduct.cfm?partnumber=FS201) to inspect the fiber core
*	eventually a [fiber-to-fiber connector](https://www.thorlabs.com/thorproduct.cfm?partnumber=ADAF1) for prealignement 
*	a half-wave plate mounted in a [high-precision rotation mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=PRM1/M) to adjust the polarization
*	a [motorized flip mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=MFF101/M) holding a [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) to remove the mirror out of the laser path when you want to use the laser in the standart system. Alternatively, you can use a [beam splitter](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=6208&pn=BS033) to use the laser source on both setups simultaneously. 

 For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side had to match the mode field diameter of the fiber. For the femtosecond laser we placed the coupling unit at a distance to the laser source where the slightly diverging laser beam reaches the desired beam diameter necessary to match the mode field diameter in combination with the chosen coupling lens; for the blue laser we used a beam expander. 


Our system is : fiber - collimation lens - coupling lens - hollow core fiber. In Gaussian optics the beam waist after a lens is given by $w_o = \lambda / (\pi NA) = (\lambda 2 f)/(\pi n D)$ with D the diameter of the beam on the lens and f the focal distance of the lens. We find that the ratio of the laser waist in the two fiber appertures is $ w_{o1} / w_{o2} = f_1 / f_2  =>  f_1 = f_2 ( w_{o1} / w_{o2} ) = 25mm * (3\mu m / 23\mu m) $ . So we used a collimation lens after the blue single mode fiber with a focal distance $f_1 \approx 3$mm in order to match the mode field diameter of the hollow core fiber when we use a coupling lens with 25mm focal distance.



