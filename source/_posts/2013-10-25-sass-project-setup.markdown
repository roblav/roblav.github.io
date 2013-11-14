---
layout: post
title: "SASS Project setup"
date: 2013-10-25 08:57
comments: true
categories: sass
---

##.gitignore

	.sass-cache
  
##config.rb


	environment = :production


	# You can select your preferred output style here (can be overridden via the command line):
	# output_style = :expanded or :nested or :compact or :compressed

	output_style = (environment == :development) ? :expanded : :compressed
