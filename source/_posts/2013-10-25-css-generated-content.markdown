---
layout: post
title: "CSS Generated Content"
date: 2013-10-25 16:44
comments: true
categories: css
---

{% img /images/css-gen-content-1.jpg  Examples of CSS Generated Content %}

Generated content is content that can be added via css. The content doesn't appear in the DOM but is 
visable on the page to the user. For this reason generated content is perfect for design embelishments, 
but not good for user required content, as anyone using IE7 or older won't be able to see it.

The other advantages are there is one less request to the server if it replaces an image on the page, 
and CSS shapes and Unicode entities can be scaled, unlike bitmap images.

###How does it work

Use the :before or :after pseudo class to make use of the content property.

	div:after {
		content: "";
	}

If you use a clearfix class to clear floats, you've probably already used generated content.[^1]

	.clearfix:after {
	  content: "";
	  display: table;
	  clear: both;
	}

<!-- more -->

[^1]: [http://nicolasgallagher.com/micro-clearfix-hack/](http://nicolasgallagher.com/micro-clearfix-hack/)

###Shapes Demo

Here's a [demo](/demo/css-generated-content.html) of the shapes you can create.

Find out about all the crazy cool CSS content you can create - [http://css-tricks.com/pseudo-element-roundup/](http://css-tricks.com/pseudo-element-roundup/)


###Unicode entities


Look at all these fun unicode entities you can use.

<div style="font-size: 6em;">♞ ☂ ★ ❤</div>

Find lots of nice Unicode to use here [copypastecharacter.com](http://copypastecharacter.com) and here [unicode-table.com](http://unicode-table.com)

You can copy and paste the entity directly as it is ♞ or you can convert it to a CSS Hex value using [Entity Conversion Calculator](http://www.evotech.net/articles/testjsentities.html)

> CSS 'content' does not accept named entities or regular numeric entities such as &#64;, but does render ASCII text and unicode.
> [~ evotech.net - Using Unicode](http://www.evotech.net/blog/2007/04/named-html-entities-in-numeric-order/)

###Examples

* Tooltip
* Contact detail icons
* CSS Shapes
* CSS Ribbon

###Support:

IE8+ (IE6 & 7 don't support the :before :after pseudo class)


###Further reading: 

[standardista.com - Generated content](http://www.standardista.com/css3/creating-counters-with-generated-content/)
