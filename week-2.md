---
description: >-
  representing the body in 3 dimensions using digital imaging and fabrication
  technologies
---

# digital bodies

**Learning outcomes**

* Get an overview digital tools that complement analog tools in order to design, represent, make and modify the human figure
* Get basic training for using the infrastructure of the laboratory.
* Learn the safety procedures to be followed to protect yourself and the equipment
* Learn how to use software for designing and/or acquiring via scanning a human figure
* Learn how to use digital fabrication processes to produce a part or an entire human figure

**How will it be evaluated?**

* Documented the use of 3D scanner and softwares to acquire a model
* Documented the process of repairing a 3D mesh
* Created your ready to cut file for laser cutting
* Learned how to use the laser cutter and the parameters for your materials
* Built and/or assembled your own mannequin
* Created a stop motion of assemblying your mannequin
* Included all the source files in the documentation

## Cycles of Accumulation

> .. the cycle starts with sending out an explorer, in his ship fully loaded with equipments, bearing a mission of drawing a complete map of the remote land. The explorer arrives in a remote land, meets with native people, draws a map on notebooks and sketchbooks, leaves the remote land, and finally returns to the metropolitan center with a map in his hand. The next explorer is sent out, this time not only with ships and equipments but also with maps drawn from the previous expedition. He comes back with another, arguably better, map. A new map is added to the existing piles of maps. Science, of which cartography is one branch, is none other than these repeated cycles of accumulation"

this project proposed to translate what Latour terms inscriptions into representations. layers of inscriptions. good instruments and accurate measurements. the explorer, probing, stepping into unknown lands. 

 

> ..gentlemen in imperial metropolises believed that they could “‘divide’ and ‘hold’ land by means of representations of the place rather than by participation or engagement with it, by reliance on mimetic artifacts rather than local and dynamic methexis” This is exactly what Latour meant when he explained how a random place, through repeated cycles of accumulation, grew to be the center by “acting at a distance” \(L: 222\). And this action at a distance is both corporeal and semiotic

 Is science to reproduce and imitate nature or to dissect and analyze it?

> The computer simulation attracts not merely future information but also money, institutions, monkeys, and people, and in doing so, it becomes the “center of calculation” which produces high order abstractions and creates extended networks of technoscience. The higher degree of abstractions you produce, the closer to the center you approach. Unlike Galison’s experimenter, Latour’s actors never get lost in confusion about who they are and what they do. They simply get more powerful.

"immutable mobiles" -  by drawing a map on paper, you bring the remote land back to the center while you are not really taking the actual land with you. \(produced by inscription and transported back to the center, and then combined with other such objects\)

### immutable mobile

i began with an idea of a mobile - digitally embroidered lungs, diaphanous, permeable and floating. i wanted to capture the precision and detail of the digital though question the certainty of technically advanced mapping to represent an unknown territory. 

![](.gitbook/assets/img_8386.jpg)



![](.gitbook/assets/img_8387.jpg)

  


## acquiring a model 

in order to see inside the body, we need medical instruments. generally, to look at the lungs, either an x-ray or a computed tomography \(CT\) scan will be used, though magnetic resonance imaging \(MRI\) is [increasingly being adopted](https://bmccancer.biomedcentral.com/articles/10.1186/1471-2407-11-242) for various diagnostic purposes. to look all the way through the lungs, we need to look at a CT scan. CT scans of the lungs will usually only be taken in the axial plane. the medical imaging industry standard is digital imaging and communications in medicine \(DICOM\) ****image . dicom images have metadata attached, which includes patient information and often include multiple frames. a similar image type without the metadata is an .nrrd file. 

![lung map - mapping lung development](.gitbook/assets/lung-from-lungmap-3d-02.png)

lungmap is a multi-stakeholder project looking into the early development of the lungs. it is possible to view direct volume rendering through their 3d [mmvr site.](https://www.lungmap.net/3d-mmvr) 

![cancer imaging archive image search](.gitbook/assets/cancer-imaging-archive.png)

to download a dicom image, you need a [TCIA downloader ](https://wiki.cancerimagingarchive.net/display/NBIA/Download+Manager+6.5)

various software can be used to open and work with dicom images, with varying success.

photoshop has recently enabled dicom viewing and updated 3d capacities. once you have loaded multiple files you can access the dicom images to create a 3d rendering, animate frames or edit and export as commercial image file types.  

![](.gitbook/assets/screen-shot-2018-10-05-at-1.40.22-pm.png)

![creating a 3d volume from dicom images](.gitbook/assets/screen-shot-2018-10-05-at-1.45.21-pm.png)

photoshop did not retain the dicom image order, and when recomposing the images as a 3d form did so as a disorganised stack. upon trawling photoshop forums tagged \#dicom, it appears as if the dicom editing capacity could use further development and support. 

![](.gitbook/assets/screen-shot-2018-10-05-at-1.50.18-pm.png)

![3d rendering of a dicom volume could use some further practice](.gitbook/assets/screen-shot-2018-10-05-at-2.01.41-pm.png)

![a gif was not a problem](.gitbook/assets/ct-scan-lung.gif)

matlab is another application which can be used to open and process dicom images, and can also be used to generate alternative segments - for example to output sagittal slices from an axial source. 

matlab provides an[ example ](https://www.mathworks.com/help/images/exploring-slices-from-a-3-dimensional-mri-data-set.html#d120e14702)with sample data set for exploring slices of dicom images taken from a brain MRI.   


![accessing a sample data set](.gitbook/assets/screen-shot-2018-10-04-at-3.34.34-pm%20%281%29.png)

![extract data for mid sagittal slice](.gitbook/assets/screen-shot-2018-10-04-at-3.34.57-pm.png)

![affine, resample, imtransform](.gitbook/assets/screen-shot-2018-10-04-at-3.35.03-pm.png)

![output sagittal slice ](.gitbook/assets/mri-brain-sagittal-slice.jpg)

the output files are precise though extremely low resolution.   


another application which can be used to open and work with dicom and nrrd files is 3d slicer. 





#### LINKS

[https://public.cancerimagingarchive.net/ncia/login.jsf](https://public.cancerimagingarchive.net/ncia/login.jsf)





#### CITATIONS



[https://dspace.mit.edu/bitstream/handle/1721.1/103818/sts-310-fall-2005/contents/assignments/paper2.pdf](https://dspace.mit.edu/bitstream/handle/1721.1/103818/sts-310-fall-2005/contents/assignments/paper2.pdf)



