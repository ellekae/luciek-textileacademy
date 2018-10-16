---
description: values & protocols
---

# project management

  


**Learning outcomes**

* Understand the common values and principles for which the program stands
* Learn the process and tools used to document course work
* Acquire the necessary skills to publish projects, documentation and share the results of each assignment

**Assignment**

* Build a personal site describing you, your portfolio and motivation of attending the Fabricademy
* Create all the links for all the classes and connect them to the wiki
* Include a small tutorial on how you designed your website
* Plan and sketch a potential final project and add it to your website.
* Upload it to the class archive

**How will it be evaluated**

* Build a documentation website describing you and your motivation for the textile-academy, your portfolio and how you designed your website
* Upload it to the wiki.textile-academy.org
* Create all the links of all the Classes on your wiki and link them to your external website
* Draft your idea for a final project

### 

## git

git history

github / gitlab

## gitlab values

* collaboration
* results
* efficiency
* diversity
* iteration
* transparency

kindness - showing care for people - is mentioned first out of all the gitlab values. remembering kindness would help to counter jerk tendencies in a culture often dominated by brogrammers, which in turn would enable conditions for other values to emerge within a community. 

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

publishing a gitbook that continuously updates is dependent on the gibook toolchain, and requires gitlab-ci-yml. 

![gitlab-ci.yml authored by f.basile](.gitbook/assets/screen-shot-2018-10-16-at-12.49.32-pm.png)

i went through the process of setting up gitlab-ci myself. 

* installed and tested docker
* started a virtual server

![installing nginx webserver from docker](.gitbook/assets/new-webserver-docker.png)

![installing webserver](.gitbook/assets/nginx-bash.png)

![webserver installed and working](.gitbook/assets/nginx-server-successfully-installed.png)



