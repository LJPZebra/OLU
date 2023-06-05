# Two-photon upgrade


- [Part Liste](#part-liste)
- [Building Instructions](#building-instructions)
  * [Multiphoton Light-sheet unit](#multiphoton-light-sheet-unit)
  * [Fiber coupling of the pulsed femtosecond laser](#fiber-coupling-of-the-pulsed-femtosecond-laser)
    + [Historical background](#historical-background)
    + [The used fiber](#the-used-fiber)
    + [Optical path with step-by-step instructions to adchieve efficient fiber coupling](#optical-path-with-step-by-step-instructions-to-adchieve-efficient-fiber-coupling)
    + [Adapt the fiber output](#adapt-the-fiber-output)
  * [The Detection path](#the-detection-path)
- [Alignement](#alignement)
- [Example high resolution zebrafish brain recordings (elav3:H2B-GCaMP6)](#example-high-resolution-zebrafish-brain-recordings--elav3-h2b-gcamp6-)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>





## Part Liste

## Building Instructions

### Multiphoton Light-sheet unit

The multiphoton light-sheet unit is basically identical in its design to the one photon multicolor desing. To build the two-photon system follow [the building instruction of the 1P-Multicolor system](1P_Multicolor_System.md) but take into account the following modification: 

Use in step (3) as collimation and illumination objectives  the [Olympus LMPLN5xIR/0.1](https://www.olympus-lifescience.com/modules/pdfgen/pdfmaker/en_pdf-export_objectives.7efd53eb1e8b4d509bc1bbe2184a7e28/LMPLN5XIR.pdf?rev=1615725199) objective optimized for near infrared transmission. Even though not optimized for visible wavelength one can use this objective also for one-photon imaging later. To screw it into the light-sheet cube use a [thread adaptor](https://punchout.webdev02.thorlabs.com/thorproduct.cfm?partnumber=RMSA3).

### Fiber coupling of the pulsed femtosecond laser

#### Historical background
Efficient, dispersion-free, and broadband fiber coupling of a two-photon laser source is a long-standing challenge in the field of two-photon microscopy ([Helmchen et al., 2011](http://cshprotocols.cshlp.org/content/2013/10/pdb.top078147.long)) and of fiber optics design ([Wang et al., 2013](https://www.cambridge.org/core/journals/high-power-laser-science-and-engineering/article/hollowcore-photonic-crystal-fibre-for-high-power-laser-beam-delivery/8D2851845D043DA937A93F431D9F9D9C)). The difficulty arises from the fact that standard single-mode optical glass fibers are associated with strong linear and non-linear pulse dispersion, which reduces the two-photon efficiency. Pre-compensation methods are only efficient at low laser powers and are therefore impractical in the context of fast volumetric two-photon imaging, which requires high photonic fluxes. 

The development of single-mode photonic bandgap fibers, in which the light travels through an air filled hollow core, dramatically reduce dispersion and nonlinear effects and achieve transmission ratios greater than 50% ([Wang et al., 2013](https://www.cambridge.org/core/journals/high-power-laser-science-and-engineering/article/hollowcore-photonic-crystal-fibre-for-high-power-laser-beam-delivery/8D2851845D043DA937A93F431D9F9D9C), [Cregan et al., 1999](https://www.science.org/doi/10.1126/science.285.5433.1537)). These fibers have been successfully used for pulsed laser delivery in the context of multiphoton imaging ([Tai et al., 2004](https://opg.optica.org/abstract.cfm?URI=oe-12-25-6122), [Flusberg et al., 2005](https://opg.optica.org/abstract.cfm?URI=ol-30-17-2272), [Engelbrecht et al., 2008](https://opg.optica.org/abstract.cfm?URI=oe-16-8-5556), [Piyawattanametha et al,. 2009](https://opg.optica.org/abstract.cfm?&uri=ol-34-15-2309), [Choi et al., 2014](https://www.nature.com/articles/srep06626)). However, as the light guiding mechanism is based on the creation of an optical bandgap, these fibers only allow single wavelength transmission and are currently only commercially available for laser wavelengths of 800 nm or 1064 nm (NTK photonics). However, with the rapidly growing collections of genetically encoded actuators and sensors, broadband fiber delivery of the near infrared spectrum and optimally extended to visible wavelengths, is a prerequisite to take full advantage of 2P-LSFM in all possible applications while enabling laser source sharing between different setups.

Broadband fiber delivery spanning the visible and the near-infrared spectrum is possible with negative curvature hollow-core photonic crystal fibers (NCF), which do not rely on an optical bandgap for light-confinement ([Yu et al., 2016](https://opg.optica.org/abstract.cfm?URI=oe-24-12-12969), [Pryamikov et al., 2011](https://opg.optica.org/abstract.cfm?URI=oe-19-2-1441), [Yu et al., 2012](https://doi.org/10.1364/OE.20.011153)). The simplest cross-sectional geometry of an NCF is based on a ring of touching or non-touching tubes surrounding the core ([Pryamikov et al., 2011](https://opg.optica.org/abstract.cfm?URI=oe-19-2-1441)). Core diameter, tube diameter, inter-tube distance, and tube wall thickness together control the spectral transmission bands, the attenuation level, the quality of higher-order mode suppression, and the sensitivity of the optical properties to bending. Attenuation levels < 0.07 dB/km and bending loss < 0.03 dB/m are reported ([Debord et al., 2017](https://doi.org/10.1364/OPTICA.4.000209)). Due to the minimal lattice structure and the reduced light interaction with the cladding structure, these fibers have very high damage thresholds and can even be used for very high laser energy delivery of up to 100 $\mu\textrm{J}$ peak power when the core is vacuum pumped to reduce nonlinear effects at these high powers ([Li et al., 2019](https://doi.org/10.1016/j.ijleo.2019.163093)). Negative curvature fibers are on the verge of being used in several applications such as laser micromachining and laser surgery. A recent study demonstrated the successful use of a custom HC-NCF with a transmission band of 600 – 830 nm at < 0.3 dB/m attenuation in the design of a handheld two-photon microscopy scanner for human skin autofluorescence ([Sherlock et al., 2016](https://doi.org/10.1002/jbio.201500290)).

#### The used fiber

Together with [GLO Photonics](https://www.glophotonics.fr/), we selected a HC-NCF fiber whose optical characteristics appear to be ideally suited for laser delivery in the context of combined one- and two-photon light-sheet microscopy (![Figure 1](link_to_figure)). 

The outer fiber diameter is 200 ± 2 μm and the fiber coating diameter is 600 ± 30 μm. The fiber has an air-filled 30 μm-in-diameter core surrounded by a ring of eight non-contacting ~10 μm-in-diameter cladding tubes. In this so-called hypocycloid fiber structure, the negative curvature of the core contour is created by the tubes surrounding the core. Tube diameters, inter-tube distance, tube wall thickness, and core size together control the fiber transmission spectrum. They yield two broad transmission bands that are compatible with 1, 2, and 3P imaging, respectively (see ![Figure 1c](link_to_figure_c)): One in the near infrared from 700 - 1500 nm (I), and another in the visible spectrum from 400 - 535 nm (II). Within these spectral bands, the loss is less than 300 dB/km (corresponding to a transmission efficiency of more than 93% for a one-meter-long fiber), and the pulse dispersion is less than 1 dB/(km·nm) of spectral pulse width. 

The fiber is commercially available as a patch chord cable with standard FC/PC connectors. This proves extremely convenient as it allows one to disconnect and reconnect the fiber to the optical setup without the need for subsequent realignment on either end. The small core diameter compared to the large infrared wavelength further ensures near single-mode guidance.

The Gaussian beam properties of the laser are also well preserved at the fiber output with M^2 values of 1.23 and 1.18 that we measured at 1030 nm and 515 nm laser wavelength. The near field and far field profiles are symmetric with minimal ellipticity of 97.25% and 85.57%. The mode field diameters at 1/e^2 are 23 ± 1 μm and 26 ± 1 μm, respectively, which correspond to a fiber's numerical aperture (NA) of approximately 0.02. Due to negligible interactions between the light and the fiber material, the fiber exhibits a very high damage threshold: We could not observe any fiber damage up to the maximal tested peak powers of 40 μJ at 1030 nm and 10 μJ at 515 nm for 400 fs pulses, corresponding to an average laser power of 20W and 4W, respectively. These characteristics demonstrate that high-quality Gaussian beams can be delivered with this fiber across a broad spectral range with high transmission and low dispersion, which is a prerequisite for its application in high-resolution microscopy.



#### Optical path with step-by-step instructions to adchieve efficient fiber coupling
* In addition to step (2) , couple the **two-photon laser** and the **one-photon laser** sources into a single hollow core crystal fiber for combined fiber delivery to the light-sheet unit. Find here a [detailed instruction of the coupling procedure](Fiber_coupling.md) and here some background about [hollow core negative curvature fibers](FiberOpticsReview.md).

#### Make the fiber output compatible with the light-sheet unit

* The collimation and illumination objective form a one-to-one telescope. If we would simply connect the hollow core fiber to the light-sheet unit as we did in the 1P-Multicolor system then the light-sheet thickness would correspond to the mean field diameter of the hollow core fiber which is $23\mu m$ ([fiber spec sheet](https://github.com/vbormuth/OLU/files/9039097/PMC-C-K9005.B2_delivered_2019-01-16.pdf)). To get the same resolution as in the one-photon implementation we have to install an extra lens after the fiber to demagnify the laser waist from the fiber output to about $5\mu m$ and at the same time to increase the divergence angle of the laser to match the numerical aperture of the collimation objective. The numerical aperture of the fiber is 0.02 and thus a factor 5 times smaller compared to the numerical aperture of the detection objective.
* With a [lens](https://www.thorlabs.com/thorproduct.cfm?partnumber=C151TMD-B) with a focal distance of f = 2mm and a numerical aperture of 0.5 you can demagnify the laser output from the fiber by a magnification of m = 0.2. Mount this lens via an [adaptor](https://www.thorlabs.com/thorproduct.cfm?partnumber=S05TM06) into the the [lens tube](https://www.thorlabs.com/thorproduct.cfm?partnumber=SM05M10) which you prepared in step (5-7) of the [manual of the 1P-Multicolor unit](1P_Multicolor_System.md).  
* Place the lens at a distance $s = f \left( \frac{1}{m} - 1\right) = f \left( 5 - 1\right) = 4 \cdot f = 8\textrm{mm}$ after the fiber output. The lens refocuses the laser at a new position $s' = f \cdot \left[ 1 + \frac{1}{s/f - 1} \right] = 1.2 \cdot f = 2.4\textrm{mm}$ after the lens down to a waist of $w_0^{'} = m \cdot w_0 = 0.2 \cdot 23 \mu m = 4.6\mu m$ with an angle of divergence of the laser corresponding to a numerical aperture of $m \cdot 0.02 = 0.1$ thus matching the numerical aperture of the collimation objective.


![NA_Expander](Figures/Coupling2P_update.png)

[Focusing of spherical Gaussian beams by Sidney A. Self](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.1091.571&rep=rep1&type=pdf)




### The Detection path
* Install in addition the [multiphoton short-pass emission filter](https://www.semrock.com/filterdetails.aspx?id=ff01-750/sp-25) to block also the pulsed infrared laser source.

## Alignement

* Align the system in one-photon mode following the instructions provided for the [1P-Multiphoton system](1P_Multicolor_System.md). This alignment procedure will also align the two-photon pathway.

* Align the polarization of the two-photon laser within the light-sheet plane. Visualize the two-photon laser using a fluorescein solution. Rotate wave plate W2, which is installed in front of the xyz-translation stage in the fiber coupling optical pathway. Continue rotating the wave plate until the fluorescence signal is maximized, indicating the optimal position.

* Note that the alignment and transmission efficiency of the hollow-core fiber in the infrared are not affected by fiber bendings. However, bending the fiber will indeed affect the polarization by changing its direction and ellipticity. Once you have set the rotation angle of wave plate W2, it is crucial not to move the fiber any further. If the fiber is inadvertently moved, the rotation angle of the wave plate will need to be readjusted accordingly to ensure optimal performance. For further information regarding the dependency of light-sheet fluorescence microscopy on polarization, please refer to [Vito et al. Optic Express 2020](https://opg.optica.org/boe/fulltext.cfm?uri=boe-11-8-4651&id=433823).

## Example high resolution zebrafish brain recordings (elav3:H2B-GCaMP6)

* Left: one-photon mode excited @ 488nm
* Right:  two-photon mode excited @ 915nm

https://user-images.githubusercontent.com/38736127/178161973-748767bf-004d-487c-9377-4582a705d8d7.mp4
