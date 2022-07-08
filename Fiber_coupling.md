# Let's couple the pulsed two-photon laser into the hollowo core fiber

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


Note: Do the coupling procedure at very low laser power for laser safety and to protect the fiber. The fiber has a very high domage threshold but only if the laser is well coupled. 

You can regulate the laser intensity with a [lambda wave plate](https://www.newport.com/p/10RP52-2) and a [polarizor]([https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS25-1064-HP](https://www.thorlabs.com/thorproduct.cfm?partnumber=CCM1-PBS252/M)). 

## Some planning to do:

For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side has to match the mode field diameter of the fiber. Or in other words the opening angle of the focused laser beam has to match the numerical apperture of the fiber. Our fiber has a numerical apperture of 0.02 (see [fiber spec sheet](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf))

The numercial apperture of the coupling system is given by $NA = \frac{D}{2 f}$, with *D* the diameter of the laser beam at the position of the coupling lens, and *f* the coupling lens' focal length. The laser company normally gives the beam width and the beam divergent angle. At the position were one can place the coulping unit after the laser output the beam divergence angle determines the beam width. You can measure the diameter of the laser either with a beam profiler (Thorlabs BC207VIS/M) or with the [moving knif technique](https://www.researchgate.net/profile/Emerson-Lima-2/publication/23771279_Measurement_of_Gaussian_laser_beam_radius_using_the_knife-edge_technique_Improvement_on_data_analysis/links/00b7d533ec8470fe22000000/Measurement-of-Gaussian-laser-beam-radius-using-the-knife-edge-technique-Improvement-on-data-analysis.pdf?origin=publication_detail). In our case we measured a beam diameter of 1.6mm and thus chose a coupling lens with focal length $f = \frac{D}{2 NA} = \frac{1.6mm}{2 * 0.02} = 40mm$. 

We got reasonalbe coupling with the achromatic coupling lens. If you want to further optimize the coupling you can use an objective as coupling lens, e.g. the Olympus LMPLN5xIR/0.10. 

## Let's build the optical path:

The following schematic shows a possible optical path for the laser coupling. You can adapt the arrangement to the space availability on your setup. 


*	Position a [motorized flip mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=MFF101/M) (**M1**) holding a [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) directly after the infrared laser output to highcheck laser for coupling into the optical fiber. Alternatively, you can use a [beam splitter](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=6208&pn=BS033) to use the laser source on both setups simultaneously. If this is possible depends on the laser power that you require on the different systems. 
*	Position the half wave plate and the polarizor
*   Insure laser safety in the room and wear [laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*   Prepare the power meter
*   Switch on the laser and rotate the wave plate to lower the laser power until you interrupt totally the laser. 
*   increase again slowly the laser power until you start to see the laser spot onto the IR detection card
*   Close the laser shutter
*   Position the two [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) (**M2 & M3**) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0). A good distance between these two mirrors is about 20cm. With these two mirrors you will later align the laser with the fiber axis. Select the length of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) that hold the mirrors compatible with the hight of your laser beam.
*  Install the [longpass dichroic mirror](https://www.thorlabs.com/thorproduct.cfm?partnumber=DMLP650R) that is transparent for the infrared laser but reflects the visible spectrum . This will allow coupling in addition a visible laser into the same fiber. 
*	Mount the the differential **xyz-translation stage** ([MAX313D/M](https://www.thorlabs.com/thorproduct.cfm?partnumber=MAX313D/M#ad-image-0)) at about 20cm distance of mirror M3. This stage will allow to position the fiber outlet precisely into the focal point of the coupling lens. 
*	Install the half-wave plate mounted in a [high-precision rotation mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=PRM1/M) to adjust the polarization
*  Fix the  [Mounting Bracket](https://www.thorlabs.com/thorproduct.cfm?partnumber=AMA009) onto the front of the xyz-stage and mount onto it a [SM1-Compatible Flexure Stage Mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031)
*  Screw the coupling lens into the holder ([AC254-040-B-ML](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-040-B-ML)) 
*  Mount the [SM1-Compatible Flexure Stage Mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=HCS031) onto the moving platform of the xyz-stage and screw into this mount the a [FC/PC Fiber Adapter Plate with External SM1 threading](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM1FC2). To this FC/PC adapter you will later connect the optical fiber.
*	attache the [Single mode fiber](https://www.thorlabs.com/thorproduct.cfm?partnumber=P1-460B-FC-2) for prealignment to the FC/PC adaptor plate. 
*	attache the other side of the fiber to the [cable continuity tester](https://www.flukenetworks.com/datacom-cabling/fiber-testing/VisiFault-Visual-Fault-Locator) for prealigment
*	Adjust the distance position of the coupling lens (**L1**) relative to the fiber outlet unitl the red laser light from the continouity tester is well collimated by the coupling lens. 
*	Watch this following youtube tutorial on fiber coupling. You will follow the same procedure to adjust the installed optics.
*	Now where you know how to do it insure laser safety in the room and wear [laser safety glasses](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3) to protect your eyes!
*	Prepare a [VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2) to visualize the invisible infrared laser
*	And prepare the power meter.
*   Open again the laser shutter.
*   Now move the two mirrors **M2** and **M3** to co-align the red laser and the IR laser as was explained in the video.
*   Switch off the laser shutter
*   Detach the single mode fiber from the coupling unit
*   Attach the negative curvature broad band hollow core [fiber](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf) to the FC/PC connector on the e xyz-stage.
*   position the powermeter before the coupling lens and adjust the power to about ???mW
* Position a FC/PC adaptor plate to hold the fiber outlet to measure the transmitted laser power
* Open again the laser shutter. You should measure laser transmission through the fiber
* Now adjust the mirror M2 and M3 as was discribed in the video until you get > 90% laser transmission. 
* Close the laser shutter
* detach the NCF-fiber from the coupling unit
* position mirror M3 and M4 again at a distance of about 20cm between each other and such that mirror M4 is placed about 20cm from the coupling lens
* attach the fiber splitter to the laser 
* attach on one output the collimator and hold it with ...
* attach the other side to the FC/PC connector plate on the xyz-translation stage of the coupling unit. If the fiber is to short you can prolong it with the fiber-to-fiber connector and the single mode fiber that you have used in the previous prealignment step
* prepare laser satety and switch on the laser at lowerst power possible were you can see with the laser detection card the laser
* Now use the mirror M3 and M4 to co-align the two laser beams that traval in revers direction through the system. 
* Switch off the laser and replace the fiber with the negative curvature fiber
* Switch the laser again on
* You should detect with the powermeter a transmission through the fiber
* Adjust mirror M3 and M4 until you have more than 75% percent of transmission



*	eventually a telescope to adjust the beam diameter for optimal coupling
*	a [fiber inspection scope](https://www.thorlabs.com/thorproduct.cfm?partnumber=FS201) to inspect the fiber core
*	eventually a [fiber-to-fiber connector](https://www.thorlabs.com/thorproduct.cfm?partnumber=ADAF1) for prealignement 













=======
* Place the beam splitter or the flip mirror (M1) into the optical path directly after the laser  this will allow you to highcheck parts of the laser power or the full laser power for coupling into the optical fiber. 
* position the two coupling mirrors M2 and M3 with a spacing between the mirrors of approximataly 20cm
* install the xyz differential stage at a distance of approimately 20cm from the mirror M3
* Mount the FC/PC connecor
* Fix the mounting bracket to the stage

<img width="800" alt="Test" src="https://user-images.githubusercontent.com/38736127/177995312-f05bb464-852f-4180-af0d-67d408d3eada.png">


Once you have positioned the optics you have to align them. Here you find an excellent youtube tutorial that explains the procedure. Just click on the snap shoot: 


[<img width="400" alt="Test" src="https://user-images.githubusercontent.com/38736127/176673048-5717d417-f3cd-4252-8551-5a9e17c1132f.png">](https://www.youtube.com/watch?v=kQvhbJbDG0M)

The video explains a first prealignment step based on backpropagation of a laser in the reverse direction. To use this trick first connect a standard single mode fiber to the coupling unit. Use a fiber tester to inject a visible laser through the fiber. Then follow the steps as in the tutorial. Once the alignment laser and the IR laser are align disconnect the fiber and connect the hollow core fiber. If the first step was well done you should have direcly transmission through the fiber enough to optimize the futher fiber coupling as described in the tutorial. 

You could also use the broadband hollow core fiber in the prealignment step. In this case you can connect via a fiber-to-fiber connector the fiber coupled 488nm laser to the fiber outlet. We did this and it works very well. But we do not recommend this. The hollow core fibers are not protected and cannot be easily polished as you can do for single mode fibers. If you get some dusk on the fiber outlet you can damage the fiber. Also never try to clean the fiber outlet with ethanol or acethon because these solutions will enter the fiber by capillary forces and you cannot use them anymore. 

After the prealignment step we measured directly sufficient laser transmission at the fiber output to further align the coupling elements until we reached laser transmission of >90%. At 915nm wavelength, the central 2P absorption peak of GFP and of its calcium sensitive derivative GCaMP, we delivered through 1.5m fiber length 100fs laser pulses with 98% power transmission efficiency  and minute pulse dispersion of 28nm (1dB/km·nm) that we fully precompensated with the Deepsee element of the MaiTai laser source. At 488nm,  the one-photon excitation maximum of GFP and GCaMP, we achieved a transmission efficiency of 75%. 


Further tips for the fiber coupling can be found in the [manual from GLO-photonics](https://github.com/vbormuth/OLU/files/9039094/PIP_PMC-OEM.pdf).





# Let's add the visible laser


## For the coupling you will need 

* a [fiber coupled laser](https://github.com/vbormuth/OLU/files/9057780/WEBSITE-Datasheet-LBX-488.pdf)
* Two [protected silver mirrors](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01) mounted in [kinematic mirror mounts](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K05#ad-image-0) to align the laser with the fiber axis. Select the length of the [posts](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_ID=9079) compatible with the hight of your laser beam.
* a [collimation lens](https://www.thorlabs.com/thorproduct.cfm?partnumber=C171TMD-A). You can also use [prealigned fiber collimators](https://www.thorlabs.com/thorproduct.cfm?partnumber=F110FC-532) that you mount with an [adaptor](https://www.thorlabs.com/thorproduct.cfm?partnumber=AD11BA) that you can mount with a [kinematic mirror mount](https://www.thorlabs.com/thorproduct.cfm?partnumber=KM05/M#ad-image-0) 

* TR1  Ø1/2" Optical Post, SS, 8-32 Setscrew, 1/4"-20 Tap, L = 1"
* UPH1  Ø1/2" Universal Post Holder, Spring-Loaded Locking Thumbscrew, L = 1" 




We selected the collimation lens focal distance with the formula: $f_{collimation} = f_{coupling} *  \frac{NA_{fiber}}{NA_{laser fiber}} = 40mm * \frac{0.02}{0.13}$

Which boils down to the fact to choose the coupling lens focal distance such that the collimated laser beam diameter is matches the diameter of the infrared beam that we previously coupled into the fiber using the choosen coupling lens. 

## Let's do it:

The continuous blue laser (488\,nm, Oxxius, France) was coupled into the same fiber through the aforementioned dichroic with two additional mirrors. 
At 488\,nm,  the one-photon excitation maximum of GFP and GCaMP, we achieved a transmission efficiency of 75\,\%. 

====

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


We coupled the femtosecond pulsed Ti:Sapphire laser (MaiTai, Coherent, USA) with a mirror, a dichroic and a coupling lens (f=40mm, Thorlabs, AC254-040-B-ML) into the fiber that was hold by a differential xyz-translation stage. The coupling mirror was placed on a magnetic precision stand so that it could be temporally removed to use the laser on the standard microscope setup.


Due to the very low fibers numerical aperture coupling a laser into the fiber is not trivial but can easily be accomplished with the following pre-alignment protocol.  We first injected a fiber coupled visible laser through a fiber-to-fiber connector (Thorlabs, ADAF1) from the other side of the hollow core fiber. This was easily accomplished thanks to the FC/PC-connectorization of our hollow core fiber. In this configuration the visible laser traveled through the coupling optics in reverse order. We pre-align the optical components such that the laser was collimated by the coupling lens and projected onto both lasers output apertures. After the prealignment step the fiber of the visible laser was disconnected from the fiber end, a power meter was placed after the fiber outlet and the femtosecond laser was started at low power in order not to damage the fiber during further alignment. We measured directly sufficient laser transmission at the fiber output to further align the coupling elements until we reached laser transmission of $>$ 90\,$\%$. At 915\,nm wavelength, the central 2P absorption peak of GFP and of its calcium sensitive derivative GCaMP, we delivered through 1,5\,m fiber length 100\,fs laser pulses with 98\% power transmission efficiency  and minute pulse dispersion of 28\,nm (1\,dB/km·nm) that we fully precompensated with the Deepsee element of the MaiTai laser source. 



 For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side had to match the mode field diameter of the fiber. For the femtosecond laser we placed the coupling unit at a distance to the laser source where the slightly diverging laser beam reaches the desired beam diameter necessary to match the mode field diameter in combination with the chosen coupling lens; for the blue laser we used a beam expander. 


Our system is : fiber - collimation lens - coupling lens - hollow core fiber. In Gaussian optics the beam waist after a lens is given by $w_o = \lambda / (\pi NA) = (\lambda 2 f)/(\pi n D)$ with D the diameter of the beam on the lens and f the focal distance of the lens. We find that the ratio of the laser waist in the two fiber appertures is $ w_{o1} / w_{o2} = f_1 / f_2  =>  f_1 = f_2 ( w_{o1} / w_{o2} ) = 25mm * (3\mu m / 23\mu m) $ . So we used a collimation lens after the blue single mode fiber with a focal distance $f_1 \approx 3$mm in order to match the mode field diameter of the hollow core fiber when we use a coupling lens with 25mm focal distance.



