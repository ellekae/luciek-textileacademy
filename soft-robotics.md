# soft robotics

{% embed url="https://vimeo.com/305716621" %}



[sher minn chong](http://pages.cs.wisc.edu/~sher/) has developed and shared an[ l-systems renderer](http://piratefsh.github.io/p5js-art/public/lsystems/) which generates recursive patterns through a simple string rewriting system. 

![a binary tree](.gitbook/assets/screenshot-2018-12-11-at-17.47.25.png)

an example is a binary tree, which consists of the following:

```text
X=F[-X][+X]

X axiom
F draw a line
+ turn left
- turn right
[ save current state
]restore saved state
angle 30º
```

in a similar way to the example above, the equation -

```text
X=F[-X][+X]
```

can be placed into grasshopper to give form to an l-system model for 2d and 3d design applications

 using [rabbit](https://morphocode.com/rabbit/) for grasshopper, it is possible to model l-systems through simple definitions

  
rabbit uses axiom and production rules to generate and visualise l-systems models, as such:

```text
F = Move forward a step of length d
f = Move forward a step of length d without drawing a line
+ = Turn left by angle b
– = Turn left by angle b
\ = roll left
/ = roll right
^ = pitch up
& = pitch down
| = turn around
```

i created a simple binary tree using a few components in rabbit 

![a simple grasshopper definition used to create a basic recursive pattern](.gitbook/assets/capture02%20%281%29.PNG)

the l-system component contains

```text
A = axiom – first Word in the l-system. the ‘seed’ or ‘initiator’
PR = production rules – created in L-system language.
N = number of generations.
W = last word derived by the L-system.
L = list of words generated by the L-system
LS = l-system object, based on the specified axiom and production rules.
```

the turtle component contains

```text
S = Source String
L = Length of the turtle’s step
dL = Step scale length
A = Default angle of the turtle used for rotation
dA = Default angle scale
O = Initial position and orientation of the turtle
TS = Tube settings
```

using the l-system component, i specified an axiom \(x\), a rule \( X=F\[-X\]\[+X\] \)and a number of derivations \(7\). this component was connected to the turtle component in order to visualise the l-system. i specified a step length and an angle increment, then connected the turtle component to a curve, and baked. 

summary source: [https://parametricmonkey.com/2016/03/09/fractals-2/](https://parametricmonkey.com/2016/03/09/fractals-2/)

{% embed url="https://vimeo.com/305749313" %}

![](.gitbook/assets/capture02.PNG)

this form was then used to create a 3d mould to cast a bio silicone inflatable model

![trim the shape to a plane to create a half pipe](.gitbook/assets/img_0107.jpg)

![divide and trim excess elements from the 3d model](.gitbook/assets/img_0109.jpg)

![check for excess](.gitbook/assets/img_0114.jpg)

![side view](.gitbook/assets/img_0115.jpg)

![duplicate edge &amp; offset](.gitbook/assets/img_0120.jpg)

![align the object to a vertical spline](.gitbook/assets/img_0118.jpg)

![rotate](.gitbook/assets/img_0127.jpg)

![extrude a rectangle to create a mould](.gitbook/assets/img_0122.jpg)

![extrude a curve within this solid shape](.gitbook/assets/img_0126.jpg)

![adjust dimensions](.gitbook/assets/img_0128.jpg)

![crop the mould](.gitbook/assets/img_0130.jpg)

inspired by [clara davis](https://clara-davis.com/) virtuosic command of bio plastics in the creation of an inflatable piece, i wanted to create my own bioplastic inflatable using local ingredients

![vietnamese gracilis &amp; seaweed agar, used for making &apos;rau cau&apos; - jellies](.gitbook/assets/img_0134.jpg)

![stretch bio foil](.gitbook/assets/img_0143.jpg)

* 3g agar
* 20g gelatine
* 15ml glycerine
* 400ml water

![agar bio foil ](.gitbook/assets/img_0144%20%281%29.jpg)

* 50g agar
* 15g glycerine
* 250ml water

![agar bio plastic](.gitbook/assets/img_0150.jpg)

* 4g agar
* 3g glycerine
* 400ml later

![casting agar based bio plastic](.gitbook/assets/img_0166.jpg)

![removing the bio plastic from its mould](.gitbook/assets/img_0168.jpg)

![cast agar bioplastic](.gitbook/assets/img_0170.jpg)

![after 1 day](.gitbook/assets/img_0199.jpg)

![after 3 days, bearing an uncanny resemblance to my youngest son&apos;s preserved umbilical cord](.gitbook/assets/img_0293.jpg)

  
bio siilcone

* 48g gelatine
* 24g glycerine
* 240ml water

![bio silicone](.gitbook/assets/img_0232.jpg)

![casting bio silicone](.gitbook/assets/img_0200.jpg)

![removing bio silicone from its mould](.gitbook/assets/img_0204.jpg)

![second attempt](.gitbook/assets/img_0210.jpg)

![painting an additional batch of bio silicone along the perimeter](.gitbook/assets/img_0233.jpg)

  
bio silicone with a higher glycerin content

* 30g gelatine
* 30g glycerine
* 150ml water

![aligning top and base](.gitbook/assets/img_0255.jpg)

![bio silicone inflatable](.gitbook/assets/img_0356%20%281%29.jpg)



###  inflatable with upcycled textile

i dismantled a secondhand windbreaker. i would like to create an oversized jacket that becomes insulated and assumes its 'true' form when inflated. i created some experiments towards this objective by inserting layers of hot melt film and its waxed backing in between layers of synthetic windbreaker panels and applying heat. 

{% embed url="https://vimeo.com/305750549" caption="creating an inflatable from upcycled textile" %}

![](.gitbook/assets/img_0289.jpeg)

![](.gitbook/assets/img_0290.jpeg)

![a digitised embroidery](.gitbook/assets/screenshot-2018-12-09-at-00.11.39.png)

####  attempting laser bonding 

![hairline ](.gitbook/assets/img_0314.jpg)

![](.gitbook/assets/screenshot-2018-12-10-at-15.21.07.png)

![hairline](.gitbook/assets/img_0319%20%281%29.jpg)

![raster](.gitbook/assets/img_0313.jpg)

![laser cut polyolefin adhesive](.gitbook/assets/img_0334.jpg)

![creating a custom connection to work with an air blower in the lab](.gitbook/assets/img_0323.jpg)

![a model of the air blower](.gitbook/assets/img_0324.jpg)

![printing the connection](.gitbook/assets/img_0329.jpg)

  
to be continued..

  




### LINKS

{% embed url="https://cvdmark.home.xs4all.nl/tutor.html" %}

{% embed url="https://generativelandscapes.wordpress.com/2014/10/07/fractal-trees-basic-l-system-example-9-4/" %}

