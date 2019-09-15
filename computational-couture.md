---
description: >-
  exploring computational design methods as a means of reinterpreting a
  traditional fashion accessory
---

# computational couture

![](.gitbook/assets/img_0655.jpg)

## post-cartesian world

rapid and sweeping changes to how we see ourselves in our world are destabilising the traditional role of the designer. in the face of extreme pollution, designers are responding to the complete commingling of agency in complex networks of human and non-human actors, consequently the organic and synthetic have merged in the making practices of many designers. similarly, big data and AI have disrupted and rearranged our ideas around systems design, community and what it means to construct and claim an identity. contending with new technological advances has positioned designers to redefine what is meant when we speak about design. rather than seeking  stable ground in empiricism, designers are continually redefining an unstable epistêmê through a new technê that finds itself only in relationship to the systems within which we are enmeshed. how we can design from this place of uncertainty?

### computation driven design

allowing algorithms to inform design processes is a means many have adopted as a way to bring the organic in direct relationship to technologies of simulation. this methodology allows for an emergent aesthetic derived from abstracted, measurable behaviours thus making space for a certain ambivalence around design decisions. by embracing the techniques of simulacra designers have been able to create and apply visual and material languages previously only found in medical slides, traffic data or leaf veination to speak about highly-technologically mediated experiences deeply embedded in biological systems.

## making a model

![draping on the stand - tussah silk](.gitbook/assets/img_9337.JPG)

![adding beeswax to prepare the model for 3d scanning ](.gitbook/assets/img_9138%20%281%29.jpg)

![shaping the panel](.gitbook/assets/img_9132.jpg)

![scanning the panel](.gitbook/assets/compcout-3dscan.gif)

model was scanned using the thor 3d scanner with reconstruction sensitivity set to 5, texture brightness set to 6.   
[http://thor3dscanner.com/thor3d](http://thor3dscanner.com/thor3d)

![opening the model in rhino](.gitbook/assets/screen-shot-2018-11-09-at-17.32.25.png)

![top view of scanned textile model](.gitbook/assets/screen-shot-2018-11-11-at-17.22.42.png)

##  parametric weave

i began by following the parametric weave [tutorial](https://vimeo.com/24138876) of b.james

![create a grid](.gitbook/assets/screen-shot-2018-11-09-at-22.40.11.png)

![insert param viewer and cull function to view and control how the weave behaves](.gitbook/assets/screen-shot-2018-11-09-at-22.48.47.png)

![use boolean toggles \(T F function\) connected to cull component to control outer columns](.gitbook/assets/screen-shot-2018-11-09-at-22.52.44.png)

![connecting an amp component to control the height of the z-axis](.gitbook/assets/screen-shot-2018-11-10-at-00.25.29.png)

![](.gitbook/assets/screen-shot-2018-11-10-at-00.29.18%20%281%29.png)

connect centre point to a plane \(plane normal\) component, then connect this plane to an amp component so the weave height can be set and adjusted. 

![](.gitbook/assets/screen-shot-2018-11-10-at-06.11.05%20%281%29.png)

![](.gitbook/assets/screen-shot-2018-11-10-at-06.20.32.png)

raise the outer branches, set an origin point for raised plane, set a center point for the array by multiplying the x & y by 0.5, set the output as x & y coordinates to create a point object

![](.gitbook/assets/screen-shot-2018-11-10-at-06.24.01.png)

reorient the branches by adding a flip matrix component so that point indices which were arranged by column will instead be arranged by rows. connect the flip component to the branch output. for the outer branches, connect flip to move.

![](.gitbook/assets/screen-shot-2018-11-10-at-15.43.24.png)

connect branch output to a rotate 3D component to rotate outer branches. take centre point from the grid \(following from the multiply &gt; construct pt &gt; plane components\) as the point of rotation

![checking the boolean pattern in the definition](.gitbook/assets/screen-shot-2018-11-10-at-15.44.35.png)

![connect to pipe component, set pipe dimensions](.gitbook/assets/screen-shot-2018-11-10-at-22.34.36.png)

![the final parametric weave definition ](.gitbook/assets/screen-shot-2018-11-11-at-06.41.48.png)

![parametric weave](.gitbook/assets/screen-shot-2018-11-11-at-06.29.33.png)

{% embed url="https://vimeo.com/300655327" %}

{% hint style="info" %}
this definition did not work when applied to a 3d form. i created a 3d surface based on 2 curves and linked these curves into this parametric weave definition by substituting out the grid. unsure how to rectify this error, i began a new definition. 
{% endhint %}

###  applying weave definitions over an approximation of the model surface

![](.gitbook/assets/screen-shot-2018-11-11-at-12.29.02.png)

![tracing the 3d scan in rhino](.gitbook/assets/screen-shot-2018-11-12-at-12.50.09.png)

![redraw the 3d shape. create a surface. ](.gitbook/assets/screen-shot-2018-11-12-at-12.53.12.png)

![offset the surface to establish an origin point for the raised weave](.gitbook/assets/screen-shot-2018-11-12-at-13.17.31.png)

![establish T F conditions across the surface](.gitbook/assets/screen-shot-2018-11-12-at-13.21.22.png)

divide the surface with a rectangular grid of control points. for a 3d surface, rather than having x, y, z coordinates, points can be expressed in u & v coordinates. u & v sliders control the number of points expressed across the surface. dispatch turns these points into boolean controlled points - T or F. these points are brought into a weave, then a curve can be interpolated from these points.

![an additional dispatch command clips the definition](.gitbook/assets/screen-shot-2018-11-12-at-13.25.11.png)

dispatch works in a similar way to how cull works in the previous definition

![flip matrix to establish points/curves in the other direction](.gitbook/assets/screen-shot-2018-11-12-at-13.26.02.png)

![mirror commands for the flipped section to add rows to existing columns \(add warp to weft\)](.gitbook/assets/screen-shot-2018-11-12-at-13.29.09.png)

  
the second definition was not a real weave at this point, but it flowed over the 3d surface in a way that the previous definition did not. i am still learning from b.james' definition, though it seems there is a simpler way to create a parametric weave. 

###  recreating the model as a surface

![redrawing from a 3d scan](.gitbook/assets/screen-shot-2018-11-13-at-08.41.00.png)

![applying the second weave definition to the new surface](.gitbook/assets/screen-shot-2018-11-13-at-08.43.24.png)

![duplicate the warp to establish weft curves](.gitbook/assets/screen-shot-2018-11-13-at-10.28.57.png)

![adjust density](.gitbook/assets/screen-shot-2018-11-13-at-10.33.04.png)

{% embed url="https://vimeo.com/300655327" %}



bake. export selection to .stl. 

![preparing the file to 3d print](.gitbook/assets/img_9346.jpg)

the file is ready in 31 hours... 

{% embed url="https://vimeo.com/300500589" %}

![salvaged tussah silk threads to weave through 3d printed PLA](.gitbook/assets/img_9364.jpg)

![](.gitbook/assets/img_0657%20%281%29.jpg)

{% hint style="info" %}
there are other ways to create weave definitions in grasshopper, i have briefly explored 2 means. i am discovering more and hope to apply these in future projects.  
{% endhint %}

#### LINKS

{% embed url="http://smart-jewellery.com/archives/category/lab-filament-compendium/filament-compendium" %}

{% embed url="https://vimeo.com/282106863" %}

{% embed url="http://mathartblog.com/?p=464" %}

{% embed url="https://www.youtube.com/watch?v=9HI8FerKr6Q" %}

{% embed url="https://n-e-r-v-o-u-s.com/projects/albums/floraform-sculptures/" %}

{% embed url="https://vimeo.com/3111916" %}

{% embed url="https://vimeo.com/24138876" %}

{% embed url="https://parametric3d.com/en/parametric-pattern-weave/" %}

{% embed url="https://youtu.be/SW-zjySs5ko" %}

