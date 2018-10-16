---
description: values & protocols
---

# project management

## git

git came out of linux, and is centred around open access code

> In 2005, the relationship between the community that developed the Linux kernel and the commercial company that developed BitKeeper broke down, and the tool’s free-of-charge status was revoked. This prompted the Linux development community \(and in particular Linus Torvalds, the creator of Linux\) to develop their own tool based on some of the lessons they learned while using BitKeeper. Some of the goals of the new system were as follows:

github and gitlab are similar, they are both git repositories. the former was bought by microsoft recently, causing many to cross over. gitlab is fully free and open source.

## gitlab values

* collaboration
* results
* efficiency
* diversity
* iteration
* transparency

kindness - showing care for people - is mentioned first out of all the gitlab values. remembering kindness would help to counter [jerk](http://bobsutton.typepad.com/my_weblog/2006/10/the_no_asshole_.html) tendencies in a culture often dominated by [brogrammers](https://en.wikipedia.org/wiki/Brogrammer), which in turn would enable conditions for other values to emerge within a community. 

## setting up a website

### html & css - text wrangler

i began by teaching myself html & css by building a basic portfolio site in [text wrangler](https://www.barebones.com/products/textwrangler/). i began by creating the index.html and style.css files and saving to designated, labelled folders. i prepared web content in separate folders within these folders, saving images and video in appropriate formats and sizes. i used photoshop to save for web \(legacy\), ensuring that images didn't exceed 1000x1000px. 

![creating an html document](.gitbook/assets/screen-shot-2018-10-03-at-12.14.43-pm.png)

![opening the html file in a browser](.gitbook/assets/screen-shot-2018-10-03-at-12.19.22-pm.png)

![adding tables](.gitbook/assets/screen-shot-2018-10-03-at-1.15.18-pm.png)

  


most html is quite intuitive 

*  [&lt;div&gt; ](https://www.w3schools.com/Tags/tag_div.asp)is used to create a division within the document
* [&lt;iframe&gt;](https://www.w3schools.com/Tags/tag_iframe.asp) embeds another document \(generally another web page\) within the document
* &lt;p&gt; denotes a paragraph
* &lt;body&gt; defines the document body
* &lt;br&gt; is a line break
* [&lt;header&gt;](https://www.w3schools.com/Tags/tag_header.asp) indicates a heading,  &lt;h1&gt; &lt;h2&gt; &lt;h3&gt; are elements of this tag
* &lt;a&gt; is a link

tags must be opened &lt; &gt; and closed &lt;/ &gt; 

![adding a div](.gitbook/assets/screen-shot-2018-10-04-at-12.01.38-pm.png)

  
to borrow a tired cliché we can think of a website like we do a house - html creates the structure, css is the interior design. html only describes the content of the page - it is good practice to keep css separate from html. css is where you specify colours, fonts, padding, margins and the position of html elements in relation to the page and each other. 

we specify the tag we wish to style, then enclose the styling commands in { curly brackets }. it is important to check that propery: & value; have colons and semi colons added to avoid broken links.  

![styling an \#id](.gitbook/assets/screen-shot-2018-10-04-at-12.01.43-pm.png)

  
an \#id is a way of styling a specific element, by tagging the element in the html document, then styling the \#id in css.

![styling a .class](.gitbook/assets/screen-shot-2018-10-04-at-12.02.54-pm.png)

  
a .class is a means of specifying a set of elements to be styled as a group. css attached to a .class applies to all elements. 

![styling html elements with css](.gitbook/assets/screen-shot-2018-10-04-at-1.16.13-pm.png)

![css styled site, viewed in a browser](.gitbook/assets/screen-shot-2018-10-04-at-1.20.04-pm.png)

  
through inspector, we can view and check individual elements within a site to understand which part of html/css code is controlling any element we wish to understand. 

![](.gitbook/assets/screen-shot-2018-10-04-at-11.35.14-am.png)

### html & css - dreamweaver

the same process of writing an html file and styling the html with a separate, linked css file is the same in dreamweaver. dreamweaver uses colour coding to communicate syntax errors, which is useful for people such as myself who are new to coding. dreamweaver has a live window, changes to code are immediately visible. viewing the site from a browser can be lauched with a single click. dreamweaver is linked to creative cloud resources, such as visually balanced fonts. the same content was brought across from text wrangler as i continued to learn more coding.  

![editing css in dreamweaver](.gitbook/assets/screen-shot-2018-10-16-at-12.20.15-pm.png)

  
i will need more than a week to create a site i am happy with publishing. even just choosing a font took me a few days, and i am not satisfied with the font yet. i really enjoy html and css. unfortunately i have fallen into a trap of creating &lt;div&gt; salad, i am seeking the help of experienced web developer to tidy up my site. 

### gitbook

as work on my projects has progressed concurrent with my attempts to create a platform within which to document and share my work, i searched urgently for a solution that would allow me to document intuitively - working simultaneously with images, captions, text and quotes. i though i had found a solution in gitbook. 

> `gitbook` is a command line tool \(and Node.js library\) for building beautiful books using GitHub/Git and Markdown \(or AsciiDoc\). This documentation has been generated using \`gitbook.
>
> `gitbook` can output your content as a website \([customizable](https://toolchain.gitbook.com/themes/) and [extensibles](https://toolchain.gitbook.com/plugins/)\) or as an ebook \(PDF, ePub or Mobi\).

![i am cw this site in gitbook](.gitbook/assets/screen-shot-2018-10-16-at-12.28.57-pm.png)

gitbook is mentioned on pages 37, 33, 24, 35 and 36 of the fab academy handbook. as stated in the handbook:

> gitbook allows \[insert pronoun\] to generate:
>
> * a web ready version of your book
> * a pdf version
> * a mobi/epub version for e-book readers
>
> all from the same source files

gitbook publishes directly to a github repository. the github repository then needs to be cloned, mirrored and imported into gitlab.  

![clone the repository in github](.gitbook/assets/clone-repo-github.png)

![import the repository from github](.gitbook/assets/import-gitlab.png)

![select repository and destination to import](.gitbook/assets/mirror-gitlab.png)

![my gitbook on gitlab](.gitbook/assets/screen-shot-2018-10-16-at-1.37.01-pm.png)

publishing a gitbook that continuously updates is dependent on the gitbook toolchain, and requires gitlab-ci-yml, which is a more complicated process than the above-mentioned. 

![gitlab-ci.yml authored by f.basile](.gitbook/assets/screen-shot-2018-10-16-at-12.49.32-pm.png)

i went through the process of setting up gitlab-ci myself. 

* installed and tested docker
* started a virtual server

![installing nginx webserver from docker](.gitbook/assets/new-webserver-docker.png)

![installing webserver](.gitbook/assets/nginx-bash.png)

![webserver installed and working](.gitbook/assets/nginx-server-successfully-installed.png)

###  building a gitbook

* build the book from terminal
* add a .gitignore file into the local directory
* push the folder to gitlab using github desktop
* add gitlab-ci.yml to root on gitlab

![building a gitbook from terminal os x](.gitbook/assets/screen-shot-2018-10-14-at-9.50.57-pm.png)

![pull a runner \(australian joke :p\)](.gitbook/assets/screen-shot-2018-10-14-at-10.45.49-pm.png)

![ran into issues...](.gitbook/assets/screen-shot-2018-10-14-at-10.54.03-pm.png)

  
publishing/sharing my gitbook will need some additional work..

## proposed thematic link: assignments and final project

 throughout the duration of the course I will focus on various aspects of breathing and the breath.

an early idea for a final project proposes a wearable device which supports asthma management in children - a "Breathing Blanket"

![](.gitbook/assets/breathing-blanket-sketch.jpg)

### context

according to the World Health Organisation \(2008\), Asthma affects over 235 million people worldwide, with the director general warning that Asthma is on the rise everywhere. Asthma is the most chronic disease amongst children.

there are many treatments for asthma the disease based on solid medical research, however the felt experience of a child in hospital has perhaps received less attention. Often children being treated for asthma will be asked to patiently endure protracted periods of time in hospital in a tangle of tubes, cords and wires. The issue of how to monitor vital signs unobtrusively is currently being addressed by many in the field of wearable technology. In addition to the benefits of employing wearable technologies in the treatment of asthma in medical contexts is through an increased capacity for self-management. As Daines \(2016\) states, supported self-management is a key component of asthma care. Asthma management in practice can be a hybrid of various approaches and strategies, pieced together around a core care for a patient and their ability to breathe freely.

the project seeks to understand in what ways the design of wearable tech can support in making asthma management and self-care more straight-forward for caregivers and more enjoyable for children.

### design

the blanket is comprised of quilted upcycled silk remnants. armholes are cut and frey-checked on the textile surface using steil-stitch digital embroidery. this makes the blanket a piece which can be handled or worn in various ways, though is primarily envisaged as a vest that drapes like a cape. the back panel of the garment is embroidered with an RFID tag which monitors and transmits data related to the breathing of the wearer unobtrusively. the blanket will harvest energy from the excursion of the lungs. In addition the blanket incorporates interactive components featuring simple circuits which encourage tactile, sensory play. these simple circuits are located to the left and right hand sides of the blanket such that when the blanket is worn as a vest, the circuits sit where the hands naturally fall/lie.

at this stage it is preferable to leave detailed specifics to emerge from further experimentation and prototyping activities. the design envisages an artefact that connects with the body such as to ascertain specific data related to breathing, however simultaneously will allow for a subjective experience of breathing to be explored and authored.

![](.gitbook/assets/fa_fp-av_sketch01.jpg)



#### TEXTS CITED

Bianchi, M. ‘A Fabric-Based Approach for Wearable Haptics’ in Scilingo EP & Valenza G\(Eds\) 2017. Wearable Electronics and Embedded Computing Systems for Biomedical Applications. MDPI Journal: Switzerland.

Dieffenderfer J, Goodell H, Mills S, McKnight M, Yao S, Lin F, Beppler E, Bent B, Lee B, Misra V, Zhu Y, Oralkan O, Strohmaier J, Muth J, Peden D, & Bozkurt A. 2016. ‘Low-Power Wearable Systems for Continuous Monitoring of Environment and Health for Chronic Respiratory Disease’ in IEEE Journal of Biomedical and Health Informatics, Vol 20. No. 5.

Kettley, S. 2006. Designing with Smart Textiles. Bloomsbury: London

Koski, E, Bjorninen, T, Koski K, Ali Babar A. 2012. “Fabrication of embroidered UHF RFID tags” Conference Paper presentated at International Symposium \(Digest\) \(IEEE Antennas and Propagation Society\) · July 2012

Haruki, Yutaka., Homma, Ikuo., Umezawa, Akio., & Masaoka, Yuri. \(2001\). Respiration and Emotion. Tokyo: Springer Japan : Imprint: Springer.

Hui X & Kan EC. ‘Monitoring vital signs over multiplexed radio by near-field coherent sensing’, Nature Electronics Vol. 1 JANUARY 2018, p74–78 [http://www.nature.com/natureelectronics](http://www.nature.com/natureelectronics)

Kwon S, Kim H, Choi S, Jeong EG, Kim D, Lee S, Lee HS, Seo YC, and Choi KC. 2017. Weavable and Highly Efficient Organic Light-Emitting Fibers for Wearable Electronics: A Scalable, Low-Temperature Process. Nano Lett 2018, 18, 347−356. Available at \[pubs.acs.org/NanoLett\]

Moradi E, Koski K, Ukkonen L, Rahmat-Samii Y, Björninen T & Sydänheimo L. 2013. Embroidered RFID Tags in Body-Centric Communication. International Workshop on Antenna Technology.

Suh, M. 2015. ‘Wearable sensors for athletes’ in Electronic Textiles. Elsevier: Amsterdam.

Wang Z, Volakis JL, Kiourti A. 2015. ‘Embroidered antennas for communication systems’ in Dias, T. 2015. Electronic Textiles. Elsevier: Amsterdam

Waqar S, Wang L, John S. 2015. ’Piezoelectric energy harvesting from intelligent textiles’ in Dias, T. 2015. Electronic Textiles. Elsevier: Amsterdam

Yu F, Lyon KG, Kan EC. 2010. Harmonic Generation from Integrated Nonlinear Transmission Lines for RFID Applications. School of Electrical and Computer Engineering. Cornell University: NY

