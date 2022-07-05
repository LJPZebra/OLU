# Let's couple the pulsed two-photon laser into the hollowo core fiber
Test
## For the coupling we will need :
*	a coupling lens to focus the laser into the fiber ([AC254-040-B-ML](https://www.thorlabs.com/thorproduct.cfm?partnumber=AC254-040-B-ML))
*	eventually a telescope to adjust the beam diameter for optimal coupling
*	a differential xyz-translation stage ([MAX355D/M](https://www.thorlabs.com/thorproduct.cfm?partnumber=MAX355D/M)) to position the fiber outlet precisely into the focal point of the coupling lens. 
*	Two coupling mirrors to align the laser with the fiber axis. 
*	a dichroic that is transparent for the infrared laser but reflexs the visible spectrum . This will allow coupling in addition a visible laser into the same fiber. Alternatively, you can also use a dichroic transparent for the visible laser and reflecting the infrared light. Both configurations will work.
*	Two coupling mirrors to align the visible laser into the fiber.
*	[VIS/IR Detector Card](https://www.thorlabs.com/thorproduct.cfm?partnumber=VRC2)
*	[Laser Safety Glasses: 48% Visible Light Transmission](https://www.thorlabs.com/thorproduct.cfm?partnumber=LG3)

Note: Do the coupling procedure at very low laser power for laser safety and to protect the fiber and to protect the fiber. The fiber has a very high domage threshold but only if the laser is well coupled. 

## Let's do it:
A possible configuration of the fiber coupling optical setup that we used is shown in the following figure:

<img width="400" alt="Test" src="https://user-images.githubusercontent.com/38736127/177211832-9b103593-d3d3-4efb-b24c-df840a2f0456.png">

For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side has to match the mode field diameter of the fiber. Or in other words the opening angle of the focused laser beam has to match the numerical apperture of the fiber. Our fiber has a numerical apperture of 0.02 (see [fiber spec sheet](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf))

The numercial apperture of the coupling system is given by $NA = \frac{D}{2 f}$, with *D* the diameter of the laser beam at the position of the coupling lens, and *f* the coupling lens' focal length. The laser company normally gives the beam width and the beam divergent angle. At the position were one can place the coulping unit after the laser output the beam divergence angle determines the beam width. You can measure the diameter of the laser either with a beam profiler (Thorlabs BC207VIS/M) or with the moving knif technique. In our case we measured a beam diameter of 1.6mm and thus chose a coupling lens with focal length $f = \frac{D}{2 NA} = \frac{1.6mm}{2 * 0.02} = 40mm$. 

We got reasonalbe coupling with the achromatic coupling lens. If you want to further optimize the coupling you can use an objective as coupling lens, e.g. the Olympus LMPLN5xIR/0.10. 

Once you have positioned the optics you have to align them. Here you find an excellent youtube tutorial that explains the procedure. Just click on the snap shoot: 


[<img width="400" alt="Test" src="https://user-images.githubusercontent.com/38736127/176673048-5717d417-f3cd-4252-8551-5a9e17c1132f.png">](https://www.youtube.com/watch?v=kQvhbJbDG0M)

The video explains a first prealignment step based on backpropagation of a laser in the reverse direction. To use this trick first connect a standard single mode fiber to the coupling unit. Use a fiber tester to inject a visible laser through the fiber. Then follow the steps as in the tutorial. Once the alignment laser and the IR laser are align disconnect the fiber and connect the hollow core fiber. If the first step was well done you should have direcly transmission through the fiber enough to optimize the futher fiber coupling as described in the tutorial. 

You could also use the broadband hollow core fiber in the prealignment step. In this case you can connect via a fiber-to-fiber connector the fiber coupled 488nm laser to the fiber outlet. We did this and it works very well. But we do not recommend this. The hollow core fibers are not protected and cannot be easily polished as you can do for single mode fibers. If you get some dusk on the fiber outlet you can damage the fiber. Also never try to clean the fiber outlet with ethanol or acethon because these solutions will enter the fiber by kapillary forces and you cannot use them anymore. 

Further tips for the fiber coupling can be found in the [manual from GLO-photonics](https://github.com/vbormuth/OLU/files/9039094/PIP_PMC-OEM.pdf).





# Let's add the visible laser


## For the coupling we will need 

Once the pulsed infrared laser is coupled
Fiber P1-460B-FC-2  (3mm jacket, NA1 = 0.1-0.14) => collimation lens C171TMD-A (f = 6.2 mm, NA = 0.6, Mounted Aspheric Lens, ARC: 350 - 700 nm) =>  coupling lens AC254-040-B-ML

We selected the collimation lens focal distance with the formula: f1 = f2*  NA1/NA2 = 40 * 0.02 / 0.13

you can also use prealigned fiber collimators: F110FC-532  (f=6.09mm and aligned for 532nm)
* mount with adaptor AD11BA
* KM05/M	Kinematic Mirror Mount for Ø1/2" Optics, M4 Taps
* TR1  Ø1/2" Optical Post, SS, 8-32 Setscrew, 1/4"-20 Tap, L = 1"
* UPH1  Ø1/2" Universal Post Holder, Spring-Loaded Locking Thumbscrew, L = 1" 

## Let's do it:

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


Due to the very low fibers numerical aperture coupling a laser into the fiber is not trivial but can easily be accomplished with the following pre-alignment protocol.  We first injected a fiber coupled visible laser through a fiber-to-fiber connector (Thorlabs, ADAF1) from the other side of the hollow core fiber. This was easily accomplished thanks to the FC/PC-connectorization of our hollow core fiber. In this configuration the visible laser traveled through the coupling optics in reverse order. We pre-align the optical components such that the laser was collimated by the coupling lens and projected onto both lasers output apertures. After the prealignment step the fiber of the visible laser was disconnected from the fiber end, a power meter was placed after the fiber outlet and the femtosecond laser was started at low power in order not to damage the fiber during further alignment. We measured directly sufficient laser transmission at the fiber output to further align the coupling elements until we reached laser transmission of $>$ 90\,$\%$. At 915\,nm wavelength, the central 2P absorption peak of GFP and of its calcium sensitive derivative GCaMP, we delivered through 1,5\,m fiber length 100\,fs laser pulses with 98\% power transmission efficiency  and minute pulse dispersion of 28\,nm (1\,dB/km·nm) that we fully precompensated with the Deepsee element of the MaiTai laser source. At 488\,nm,  the one-photon excitation maximum of GFP and GCaMP, we achieved a transmission efficiency of 75\,\%. 




 The continuous blue laser (488\,nm, Oxxius, France) was coupled into the same fiber through the aforementioned dichroic with two additional mirrors. For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side had to match the mode field diameter of the fiber. For the femtosecond laser we placed the coupling unit at a distance to the laser source where the slightly diverging laser beam reaches the desired beam diameter necessary to match the mode field diameter in combination with the chosen coupling lens; for the blue laser we used a beam expander. 


Our system is : fiber - collimation lens - coupling lens - hollow core fiber. In Gaussian optics the beam waist after a lens is given by $w_o = \lambda / (\pi NA) = (\lambda 2 f)/(\pi n D)$ with D the diameter of the beam on the lens and f the focal distance of the lens. We find that the ratio of the laser waist in the two fiber appertures is $ w_{o1} / w_{o2} = f_1 / f_2  =>  f_1 = f_2 ( w_{o1} / w_{o2} ) = 25mm * (3\mu m / 23\mu m) $ . So we used a collimation lens after the blue single mode fiber with a focal distance $f_1 \approx 3$mm in order to match the mode field diameter of the hollow core fiber when we use a coupling lens with 25mm focal distance.



