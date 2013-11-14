---
layout: page-sass
title: "sass-guidelines"
date: 2013-10-24 21:39
comments: true
sharing: true
footer: true
---

##Project Setup

<a id="gitignore">&nbsp;</a>
###.gitignore

	.sass-cache
  
<a id="config">&nbsp;</a>
###config.rb


	environment = :production


	# You can select your preferred output style here (can be overridden via the command line):
	# output_style = :expanded or :nested or :compact or :compressed

	output_style = (environment == :development) ? :expanded : :compressed

<a id="type">&nbsp;</a>
##Typography

###REM

Set all type using REM with a fall back of px for old IE.

http://compass-style.org/reference/compass/typography/

https://github.com/bitmanic/rem

http://mrdanadams.com/2012/pixel-ems-css-conversion-sass-mixin/#.Umkt4pRgYv8


###Vertical Rhythm

http://atendesigngroup.com/blog/vertical-rhythm-compass

http://compass-style.org/reference/compass/typography/vertical_rhythm/#mixin-adjust-font-size-to

<a id="colours">&nbsp;</a>
##Colours

###RGBA

compass-rgba

https://github.com/aaronrussell/compass-rgbapng

http://aaronrussell.co.uk/legacy/cross-browser-rgba-support/

	@include rgba-background-inline(rgba(0,0,0,0.75));

<a id="compass-extensions">&nbsp;</a>
##Compass Extensions

http://snugug.com/musings/drupalcon-munich-presentation

http://munich2012.drupal.org/program/sessions/responsive-design-sass-compass-and-drupal-7.html

https://github.com/Team-Sass

<a id="grid-system">&nbsp;</a>
###Grid system

Singularity - https://github.com/Team-Sass/Singularity

Breakpoint - https://github.com/Team-Sass/breakpoint


Toolkit - https://github.com/Team-Sass/toolkit



