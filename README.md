ORM Cheatsheet
=============

ORM Cheatsheet is an ORM definition guide and reference manual. Purpose of the site is to aggregate ORM Definitions, basic commands for ORM frameworks and useful links to blogs, documentation or examples.

All other frameworks are welcome, but because I, the Mighty Maintainer work with Doctrine, Doctrine2 and Propel, other frameworks will need contributors. Fork and edit, or let me know what you would like to add.

contact:
developers@ormcheatsheet.com


#### include section

`{% include section.html %}` parameters:

- imgsource - path to images directory
- imgfile - actual image name, if '' image will not be loaded, else it tries to load even if the path is invalid

- rootdir - must not be empty and must be valid, specifies path to the tab structure
- element - not required, must be eiter valid or empty, used to better organize files
- format - assigned automatically
- file - must be valid file name in *.md
- usedtabs - specifies which tabs will be displayed, string, recognized contents: 'xml'; 'yml'; 'php'; 'more'; 'links'

#### tab file structure:

allways loaded (file must exist for page to build)

~~~
rootdir\element\file
~~~

loaded based on used tabs (file must exist if the format is specified by used tabs, or the page won't build)

~~~
rootdir\element\xml\file
rootdir\element\yml\file
rootdir\element\php\file
rootdir\element\more\file
rootdir\element\xml\file
~~~

- only the apropriate *.md file has to be modified
- to add new tab simply create the directory structure and edit the 'usedtabs' for appropriate section
- to add new image, specify the 'imgsource/imgfile' for appropriate section

#### header/variable structure:

~~~html
<h1>Top level</h1>

{% assign rootdir='toplevel/' %}
{% assign imgsource='/images/' %}

<h2 id="navbaritem">Mid level</h2>
{% assign element='midlevel/' %}

<h3>LowLevel</h3>

{% assign file='lowlevel.md' %}
{% assign imgfile='lowlevel.jpg'%}
{% assign usedtabs='xml, yml, php, more, link' %}
{% include section.html %}
~~~
