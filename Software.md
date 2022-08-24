
If you use your microscope already with a image aquisition software that allows to aquire z-stacks then 


* We used a [custom developped control software](https://github.com/LaboJeanPerrin/Lightsheet) written in Matlab to control the galvomirror and the objective piezo scanner via a national instrument card [PCIe-6363](https://www.ni.com/fr-fr/support/model.pcie-6363.html). The software is open source. 

* Alternatively, you can use:
    *  [ScanImage](https://www.scientifica.uk.com/products/vidrio-technologies-scanimage) the control software provided by Scientifica   
    *  [Micromanager](https://micro-manager.org/) that supports the control of all Scientifica stages as well as of most commen objective scanners from e.g. Physical Instrument or Piezo Jena.
    *  or the open source python software presented here: https://www.frontiersin.org/articles/10.3389/fcell.2022.875044/full
