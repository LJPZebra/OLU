# Add to the 1P-Multicolor system the Two-Photon Mode

The two-photon unit is basically identical in its design to the 1P-Multiphoton light-sheet unit. So please follow the detailed instructions given there by taking into account the following modifications: 

* Use in step (3) as collimination and illumination objectives  the [Olympus LMPLN5xIR/0.1](https://www.olympus-lifescience.com/modules/pdfgen/pdfmaker/en_pdf-export_objectives.7efd53eb1e8b4d509bc1bbe2184a7e28/LMPLN5XIR.pdf?rev=1615725199) objective optimized for near infrared transmission. Eventhough not optimized for visible wavelength we can use the same objective also for one-photon imaging later. To screw it into the light-sheet cube use the this [adaptor](https://punchout.webdev02.thorlabs.com/thorproduct.cfm?partnumber=RMSA3).

* In addition to step (2) couple the two-photon laser and the one-photon laser sources into a single hollowcore crystal fiber for combined fiber delivery to the light-sheet unit. Find here a [detailed instruction of the coupling procedure](Fiber_coupling.md) and here some background about [hollocore negative curvature fibers](FiberOpticsReview.md). 

## Detection path
* Install in addition the [multiphoton short-pass emission filter](https://www.semrock.com/filterdetails.aspx?id=ff01-750/sp-25) to block also the pulsed infrared laser source.

## Alignement
* Perform the alignment in one-photon mode as explained for the [1P-Multiphoton system](1P_Multicolor_Unit.md)

## Example high resolution zebrafish brain recordings (elav3:H2B-GCaMP6)

* Left: one-photon mode excited @ 488nm
* Right:  two-photon mode excited @ 915nm

https://user-images.githubusercontent.com/38736127/178161973-748767bf-004d-487c-9377-4582a705d8d7.mp4
