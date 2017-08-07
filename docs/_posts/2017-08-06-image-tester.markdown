---
layout: post
title:  "Image test post!"
categories: [news]
date:   2017-08-06 08:19:12
images: /images/tester/left.png
front-image: /images/tester/right.png
---
This is to test a double image include. 

## One image

{% include single-image.html fileName="left.png" image_subfolder="tester" caption="Lalala I love images" %}

## Two images

{% include two-image-include.html left_image="left.png" right_image="right.png" image_subfolder="tester" caption="Here is a caption." %} 

## Three images

{% include three-image-include.html left_image="left.png" middle_image="left.png" right_image="right.png" image_subfolder="tester" caption="Here is another caption." %} 