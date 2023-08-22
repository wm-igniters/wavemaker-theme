INSTRUCTIONS
============

Install Prerequisites
--------

* Node.js v10.17.x+

You can check if you have Node and npm installed by typing:
<pre>
$ node --version && npm --version
</pre>

If you need to upgrade or install Node, the easiest way is to use an installer for your platform. Download the .msi for Windows or .pkg for Mac from the [NodeJS website](https://nodejs.org/download/).

* Git
You can check if you have Git installed by typing:
<pre>
$ git --version
</pre>
If you don't have Git, grab the installers from the [git website](http://git-scm.com/).


Install Grunt & Bower
--------

Once you’ve got Node installed, install the Grunt and Bower:
<pre>
$ npm install --g bower grunt-cli
</pre>

(Make sure above commands execute with sudo/administrator permissions depending on OS eg, UNIX)


Setup WaveMaker Theme Repository
--------
To clone the wavemaker-theme repository, use git clone:

<pre>
 git clone https://github.com/wavemaker/wavemaker-theme.git
 cd wavemaker-theme
 npm install
</pre>


Understanding the Repository
--------
<pre>
+--src
|  +--web
|     +--fonts/
|     +--.wmproject.properties
|     +--css-variables.less
|     +--style.less
|     +--theme.png
|     +--variables.less
+--dist
|  +--web.zip
+--Gruntfile.js
|
+--package.json
|
+--bower.json
</pre>


Fonts
-----
The default font for css-variables.less (src/web) is **Lexend** font, which can be changed by importing the Google font API URL in the style directory (src/web/css-variables.less) and updating the font name to the **--font-family** variable.


Project Properties
-----
You can easily personalize your theme by changing its name. The default theme name is **Material Default**, but you can make it unique with a specified name. 


CSS Variables
-----
The CSS variables are located in the css-variables.less file within the src/web directory and can be modified for customizing themes. 


Build
--------
To build the WaveMaker Theme run the below command from wavemaker-theme directory

<pre>
cd wavemaker-theme
grunt themes
</pre>

Run Time Theme change
--------
To change the theme during runtime, update the values for the specified CSS variables and append them to the root element.

