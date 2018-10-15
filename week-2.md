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

> ..gentlemen in imperial metropolises believed that they could “‘divide’ and ‘hold’ land by means of representations of the place rather than by participation or engagement with it, by reliance on mimetic artifacts rather than local and dynamic methexis”. This is exactly what Latour meant when he explained how a random place, through repeated cycles of accumulation, grew to be the center by “acting at a distance” \(L: 222\). And this action at a distance is both corporeal and semiotic

 is science to reproduce and imitate nature or to dissect and analyze it?

by drawing a map on paper, you bring the remote land back to the center while you are not really taking the actual land with you, creating "immutable mobiles" 

### an im/mutable mobile

i began with an idea of a mobile - digitally embroidered lungs, diaphanous, permeable and floating. i wanted to capture the precision and detail of the digital though question the certainty of technically advanced mapping to represent an unknown territory. 

![](.gitbook/assets/img_8386.jpg)



![](.gitbook/assets/img_8387.jpg)

  


## acquiring a model 

in order to see inside the body, we need medical instruments. generally, to look at the lungs, either an x-ray or a computed tomography \(CT\) scan will be used, though magnetic resonance imaging \(MRI\) is [increasingly being adopted](https://bmccancer.biomedcentral.com/articles/10.1186/1471-2407-11-242) for various diagnostic purposes. to look all the way through the lungs, we need to look at a CT scan. CT scans of the lungs will usually only be taken in the axial plane. the medical imaging industry standard is digital imaging and communications in medicine \(DICOM\) ****image . dicom images have metadata attached, which includes patient information and often include multiple frames. a similar image type without the metadata is an .nrrd file. 

![lung map - mapping lung development](.gitbook/assets/lung-from-lungmap-3d-02.png)

lungmap is a multi-stakeholder project looking into the early development of the lungs. it is possible to view direct volume rendering through their 3d [mmvr site.](https://www.lungmap.net/3d-mmvr) 

![cancer imaging archive image search](.gitbook/assets/cancer-imaging-archive.png)

living in hcmc with its chronic air pollution makes the idea of cancer a constant source of anxiety for many, and a traumatic reality for some. trawling through images of people who had been given a number as their lungs were being attacked felt black and heavy. i found this difficult. there is an ocean of lung scans on this repository. 

to download a dicom image, you need a [TCIA downloader ](https://wiki.cancerimagingarchive.net/display/NBIA/Download+Manager+6.5)

various software can be used to open and work with dicom images, with varying success.

photoshop has recently enabled dicom viewing and updated 3d capacities. once you have loaded multiple files you can access the dicom images to create a 3d rendering, animate frames or edit and export as commercial image file types.  

![loading dicom files](.gitbook/assets/screen-shot-2018-10-05-at-1.40.22-pm.png)

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

the output files are precise though extremely low resolution. this method would not be suitable for my immutable mobile.   


another application which can be used to open and work with dicom and nrrd files is [3d slicer](http://www.slicer.org/). 3d slicer is a platform for the analysis and visualisation of medical data, and also open source software. 

 

![load dicom volume](.gitbook/assets/load-dicom-volume.png)

![lungs in axial, sagittal and coronal views](.gitbook/assets/lung-tissue.png)

![volume rendering presets ](.gitbook/assets/3d-view-options.png)

![generating segmentations in coronal and sagittal planes](.gitbook/assets/segmentation.png)

![labelmap - labelling types to render](.gitbook/assets/filtering-3d-rendering.png)

![label map - displaying segments](.gitbook/assets/bone-rendering.png)

i considered several means of obtaining segments and exporting as a set of files which i could open to generate embroidery from.

* running matlab scripts in 3d slicer \(thus enabling the software to run script to output coronal slices to a local directory\)
* using the emsegmenter function
* using the volume resampling function according to a spatial transform
* exporting screenshots generated within the app using segment editor
* change threshold values
* exporting dicom to mrml \(scene\)
* spline transform
* export to vtk file, load to automate segmentation at predefined intervals

i also looked into whether pixel interpolation might be possible with resampling, since the resolution of coronal slices is low. based on information on the 3dslicer forums, it appears high resolution image output is not something the medical community requires. 

i have not yet been able to resolve this issue. based on the limited understanding gained from exploration of 3dslicer software and its network, it would seem that exporting a coronal slices, or resampling coronal slices according to a spatial transform, then automating pixel interpolation may be possible though may still not yield the kind of images i would require to work from to create an embroidered model. i would need more time and support to look into this further. 

![bone view](.gitbook/assets/screenshot_1.png)

### output to 3d

3d slicer can also be used to generate stereolithography interface format \(.stl\) files. 

![.stl file generated from a CT coronary arteries preset  ](.gitbook/assets/stil-in-3dslicer-02.png)

  
once an .stl file has been created in 3dslicer, it can be exported and clean up in blender.

![transform to origin](.gitbook/assets/transform-geometry-to-origin.png)





![edit mode - deleting vertices](.gitbook/assets/blender-edit-02.png)



![not there yet](.gitbook/assets/not-there-yet.png)



3d models will not help me create the lung mobile representation as i envisaged since 3d renderings are infact hollow mesh, however they would be useful in generating outlines. 



### back to tactility

![proposing a textile structure](.gitbook/assets/img_8459.jpg)

since i had come to understand that it may not be possible to export coronal slices of the lung data i had, i began to reconsider the model so that it would represent axial slices. 

i decided to separate areas as in the labelmap function in 3d slicer so that, for example, bone would embroidered in cotton, lung tissue in silk. since cotton and silk are different fibre types with different properties, this can be exploited when dyeing the model certain dye types will be taken up by certain fibres, while others will remain unchanged. i chose to work on poly organza remnants since this textile will not take natural dyes, is robust enough to withstand machine embroidery yet it has a diaphanous quality. 

silk is not available for machine embroidery. polyester is the standard and there are few exceptions. to get silk to machine embroid for the project i had to ask a weaver to specially wind some tussah silk onto industrial spools for me. the weight of the thread is about the same as cotton \(40-50tex\), so testing will need to be done. i have tested machine embroidery of organic cotton previously thus am confident it is possible. 







#### LINKS

[https://public.cancerimagingarchive.net/ncia/login.jsf](https://public.cancerimagingarchive.net/ncia/login.jsf)

[http://www.slicer.org/](http://www.slicer.org/)

{% embed url="https://www.slicer.org/w/images/e/e0/Slicer4.5minute\_SoniaPujol.pdf" %}

#### CITATIONS



[https://dspace.mit.edu/bitstream/handle/1721.1/103818/sts-310-fall-2005/contents/assignments/paper2.pdf](https://dspace.mit.edu/bitstream/handle/1721.1/103818/sts-310-fall-2005/contents/assignments/paper2.pdf)



