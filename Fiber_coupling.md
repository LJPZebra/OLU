# Let's couple the pulsed two-photon laser into the hollowo core fiber


Due to the very low fibers numerical aperture coupling a laser into the fiber is not trivial but can easily be accomplished with the following protocol.  

For the coupling we will need :
*	a coupling lens to focus the laser into the fiber
*	eventually a telescope to adjust the beam diameter for optimal coupling
*	a differential xyz-translation stage to position the fiber outlet precisely into the focal point of the coupling lens. 
*	Two coupling mirrors to align the laser with the fiber axis. One of the mirrors can be replaced by a dichroic that reflects the infrared laser but is transparent in the visible spectrum . This will allow coupling in addition a visible laser into the same fiber. 

*How to choose the coupling lens ?* 

For optimal coupling you should use an objective as coupling lens, e.g. the Olympus LMPLN5xIR/0.10. For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side has to match the mode field diameter of the fiber. In our case the mode field diameter was ??? um (measured at 1/e^2 and given by the spec sheet => add link). When a lens focuses a Gaussian beam the width of the beam, w_0, in the focus is given by $w_0 = \lambda / (\pi NA) = (\lambda 2 f)/(\pi n D)$ with D the diameter of the collimated beam on the lens and f the focal distance of the lens.  (make a drawing).

To match the mode field diameter, you have the laser diameter and the coupling lens focal distance to play with. A Gaussian beam is never perfectly collimated.

Our laser has at the output a width of …. and a divergence of …  (see spec sheet). 

D(x; w_L0)= lambda 2 f/ (\pi n ??? x).

In our case we placed the coupling unit at a distance of 1.5m and we used a coupling lens of ???mm. 



[<img width="100" alt="Test" src="https://user-images.githubusercontent.com/38736127/176673048-5717d417-f3cd-4252-8551-5a9e17c1132f.png">](https://www.youtube.com/watch?v=kQvhbJbDG0M)

GLO-photonics manual for fiber coupling:

[PIP_PMC-OEM.pdf](https://github.com/vbormuth/OLU/files/9039094/PIP_PMC-OEM.pdf)

Spec sheet of the fiber:

[PMC-C-K9005 B2_delivered_2019-01-16.pdf](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf)


Coupling the 488nm laser 
Fiber P1-460B-FC-2  (3mm jacket, NA1 = 0.1-0.14) => collimation lens C171TMD-A (f = 6.2 mm, NA = 0.6, Mounted Aspheric Lens, ARC: 350 - 700 nm) =>  coupling lens AC254-040-B-ML

We selected the collimation lens focal distance with the formula: f1 = f2*  NA1/NA2 = 40 * 0.02 / 0.13

========


We coupled the femtosecond pulsed Ti:Sapphire laser (MaiTai, Coherent, USA) with a mirror, a dichroic and a coupling lens (f=40mm, Thorlabs, AC254-040-B-ML) into the fiber that was hold by a differential xyz-translation stage. The coupling mirror was placed on a magnetic precision stand so that it could be temporally removed to use the laser on the standard microscope setup.


Due to the very low fibers numerical aperture coupling a laser into the fiber is not trivial but can easily be accomplished with the following pre-alignment protocol.  We first injected a fiber coupled visible laser through a fiber-to-fiber connector (Thorlabs, ADAF1) from the other side of the hollow core fiber. This was easily accomplished thanks to the FC/PC-connectorization of our hollow core fiber. In this configuration the visible laser traveled through the coupling optics in reverse order. We pre-align the optical components such that the laser was collimated by the coupling lens and projected onto both lasers output apertures. After the prealignment step the fiber of the visible laser was disconnected from the fiber end, a power meter was placed after the fiber outlet and the femtosecond laser was started at low power in order not to damage the fiber during further alignment. We measured directly sufficient laser transmission at the fiber output to further align the coupling elements until we reached laser transmission of $>$ 90\,$\%$. At 915\,nm wavelength, the central 2P absorption peak of GFP and of its calcium sensitive derivative GCaMP, we delivered through 1,5\,m fiber length 100\,fs laser pulses with 98\% power transmission efficiency  and minute pulse dispersion of 28\,nm (1\,dB/km·nm) that we fully precompensated with the Deepsee element of the MaiTai laser source. At 488\,nm,  the one-photon excitation maximum of GFP and GCaMP, we achieved a transmission efficiency of 75\,\%. 




 The continuous blue laser (488\,nm, Oxxius, France) was coupled into the same fiber through the aforementioned dichroic with two additional mirrors. For efficient optical coupling and suppression of higher laser modes the width of the laser focus projected onto the fiber input side had to match the mode field diameter of the fiber. For the femtosecond laser we placed the coupling unit at a distance to the laser source where the slightly diverging laser beam reaches the desired beam diameter necessary to match the mode field diameter in combination with the chosen coupling lens; for the blue laser we used a beam expander. 


Our system is : fiber - collimation lens - coupling lens - hollow core fiber. In Gaussian optics the beam waist after a lens is given by $w_o = \lambda / (\pi NA) = (\lambda 2 f)/(\pi n D)$ with D the diameter of the beam on the lens and f the focal distance of the lens. We find that the ratio of the laser waist in the two fiber appertures is $ w_{o1} / w_{o2} = f_1 / f_2  =>  f_1 = f_2 ( w_{o1} / w_{o2} ) = 25mm * (3\mu m / 23\mu m) $ . So we used a collimation lens after the blue single mode fiber with a focal distance $f_1 \approx 3$mm in order to match the mode field diameter of the hollow core fiber when we use a coupling lens with 25mm focal distance.



