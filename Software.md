# Control software

If you use your microscope already with an image aquisition software that allows to aquire z-stacks then 


* To control the light-sheet volumetric scanning you can use our [custom developped control software](https://github.com/LaboJeanPerrin/Lightsheet) written in Matlab. Via a national instrument card [PCIe-6363](https://www.ni.com/fr-fr/support/model.pcie-6363.html) this software controls the galvomirror and the objective piezo scanner. The software is open source. 

![Screen1](https://user-images.githubusercontent.com/38736127/188240052-591e071c-c2ae-4251-a0e8-cf1be3b949b5.PNG)
![Screen2](https://user-images.githubusercontent.com/38736127/188240063-00330c47-2eac-4d3f-bd4d-2ac0d1c1b25f.PNG)

* Alternatively, you can use:
    *  [ScanImage](https://www.scientifica.uk.com/products/vidrio-technologies-scanimage) the control software provided by Scientifica   
    *  [Micromanager](https://micro-manager.org/) that supports the control of all Scientifica stages as well as of most commen objective scanners from e.g. Physical Instrument or Piezo Jena.
    *  or the open source python software presented here: https://www.frontiersin.org/articles/10.3389/fcell.2022.875044/full
