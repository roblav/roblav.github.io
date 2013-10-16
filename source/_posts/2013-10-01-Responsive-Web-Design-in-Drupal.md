---
layout: post
title: "Responsive Web Design in Drupal"
date: 2013-10-01 13:00
comments: true
categories: 
---

This blog post is coming off the back of a presentation that I recently gave at my local Drupal meet up. This is an opportunity for me to review that presentation and consolidate some of my thoughts.

As I was preparing I quickly realised that a 1 hour presentation about RWD in Drupal was only really ever going to scratch the surface. My primary objective was to give the audience a brief primer about RWD and then open up the discussion about our collective knowledge and experience.

##Ethan Marcotte - Responsive Web Design

Responsive web design really started from an [article on A List Apart](http://alistapart.com/article/responsive-web-design) by Ethan Marcotte in 2010. He basically outlined 3 main components for RWD, which are:

*   Fluid grids
*   Flexible images	
*   Media queries

I’d also recommend Ethan’s book on RWD - http://www.abookapart.com/products/responsive-web-design

<!-- more -->

Something to bare in mind there are myriad of overlapping techniques that will often be discussed using umbrella term responsive web design; mobile first, progressive enhancement, graceful degredation. There are differences between each of these strategies so it's worth finding out about them and experimenting to find out the best mix for you.

##Adaptive vs responsive

*   **Fixed** websites have a set width and resizing the browser or viewing it on different devices won’t affect on the way the website looks.

*   **Fluid** websites are built using percentages for widths. As a result, columns are relative to one another and the browser allowing it to scale up and down fluidly.

*   **Adaptive** websites introduce media queries to target specific device sizes, like smaller monitors, tablets, and mobile.

*   **Responsive** websites are built on a fluid grid and use media queries to control the design and its content as it scales down or up with the browser or device.

[Source](http://teamtreehouse.com/library/websites/build-a-responsive-website/introduction-to-responsive-web-design/fixed-fluid-adaptive-and-responsive)

Read this article for an in depth overview - http://uxdesign.smashingmagazine.com/2012/11/08/ux-design-qa-with-christian-holst

##Grids

[960gs](http://sonspring.com/journal/960-grid-system) - The 960 Grid System has been around since 2008. It’s the grid system I’m most familiar with because that’s what the Omega grid system is based on. It doesn’t really matter which grid system you use, as long as you understand the principles behind using a grid system and it’s limitations. 

Before tackling grids on a website it’s well worth understanding a little bit of history about how grids have been used in graphic design. Two fantastic sources of information are [Mark Boulton](http://www.markboulton.co.uk/journal/five-simple-steps-to-designing-grid-systems-part-1) and [Khoi Vihn](http://grids.subtraction.com/).

[960 Grid Generator](960 grid generator http://bit.ly/14yuE6G) - A fantastic online resource for quickly understanding different grids.

###Grids in Omega

Omega comes with a whole host of [panel layouts](http://drupalcode.org/project/omega.git/tree/refs/heads/7.x-3.x:/omega/panels/layouts) out of the box for 12, 16 and 24 column layouts, and if any of them don’t quite suit your needs then creating your own versions as part of your sub-theme is pretty straight forward. [Omega Panel tutorial](http://zugec.com/blog/83-custom-grid-panels-layout-omega-theme).

Here’s some sample code of what a grid layout looks like:

```
<div class="container-12 clearfix">
  <div class="grid-4">
    <!-- Content here -->
  </div>
  <div class="grid-4">
    <!-- Content here -->
  </div>
  <div class="grid-4">
    <!-- Content here -->
  </div>
  <div class="grid-4">
    <!-- Content here -->
  </div>
  <div class="grid-12">
    <div class="grid-12 alpha omega">
      <!-- Content here -->
    </div>
    <div class="grid-6 alpha">
      <!-- Content here -->
    </div>
    <div class="grid-6 omega">
      <!-- Content here -->
    </div>
  </div>
</div>
```

##Flexible Images

http://unstoppablerobotninja.com/entry/fluid-images/

```
img {
  max-width: 100%;
}

img,
object {
     max-width: 100%;
}
```

> "This solved the problem beautifully. Instead of just rendering at its native width and overflowing its containing box, the image would render at its native dimensions as long as its width didn’t exceed the width of its container."

---

> "Modern browsers are intelligent enough to keep the image’s proportions intact, even as the page scales up or down accordingly. And as it turns out, this works just fine for most embedded videos, too:"

**IE**

> “Older versions of Internet Explorer don’t support max-width. So for especially large images, I’ve been relying on a simple width: 100% rule in an IE-specific stylesheet.”

##Media Queries

Media queries can be used within a link statement or directly within the CSS file.

```
<link rel="stylesheet" type="text/css"
  media="screen and (max-width: 480px)"
  href="shetland.css" />
```

```
@media screen and (max-width: 480px) {
  .column {
    float: none;
  }
}
```

##Doing it with Drupal

**Themes**

* Omega
* Zen
* Adaptive

**Mobile Menu**

* Responsive navigation
* Responsive menu
* Tiny Nav

**Flexible images**

* Responsive images and styles 
* Adaptive images
* Picture
* Breakpoints
* FitVids

**Responsive slideshow**

* FlexSlider
* Adaptive images

**Misc.**

* Layout

##Other things to consider

**Flexible typography**

**Adaptive JS** - Only load the css that is required. With breakpoints the css files are loaded anyway.

**Touch target** - 44px by 44px

**No hover state** - Don’t hide content

**Retina display**

**Font sizes: px em rem** - http://aralbalkan.com/notes/responsive-pixels/

**Flow Type** - http://simplefocus.com/flowtype/

**Nested grids**

**Testing**

**Ish** - http://bradfrostweb.com/demo/ish/

``` 
<meta name="viewport" content="initial-scale=1">
```

**Stop using Drupal!**

The best way to learn about RWD is to stop using Drupal. Create some basic html pages and start testing the JavaScript libraries, typically a lot of Drupal modules like responsive-navigation, adaptive-images are ports of these scripts. It’s helpful to find out about them first hand.

##Additional Reading

* http://bradfrost.github.io/this-is-responsive/patterns.html
* http://bradfrost.github.io/this-is-responsive/resources.html
* http://blog.cloudfour.com/css-media-query-for-mobile-is-fools-gold


