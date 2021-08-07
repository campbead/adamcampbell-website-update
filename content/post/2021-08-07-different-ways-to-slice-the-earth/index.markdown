---
title: Different ways to slice the Earth
author: Adam J Campbell
date: '2020-08-03'
slug: different-ways-to-slice-the-earth
categories: []
tags: [rstats, sf, geospatial, ggplot2, geography] 
subtitle: ''
summary: "About 2/3's the Earth's land in is the northern hemisphere.  How would that change if the equator were in a different location"
authors: []
#lastmod: '2021-08-07T19:43:25+12:00'
featured: no
image:
  caption: 'One hundred ways to slice the Earth in half'
  focal_point: 'Center'
  preview_only: true
projects: []
---
One interesting feature of the Earth is the asymmetry in land distribution.  The northern hemisphere contains about 67% of the Earth's land, while the southern hemisphere contains 33%. 

I was wondering if the distribution of land across the northern and southern hemispheres was unique.  To explore this, I randomly generated 100 great circles that each cut the Earth into 2 equal hemispheres. 


![](one_hundred_slices.png)

I then calculated the land area percent fraction for each hemisphere for each of my 100 randomly generated Earth slices.  We can look at how common the Earth's land distribution is compared to other's that could be achieved.


![](hemisphere_dist.png)


It's clear by looking at the graph that the current distribution is actually quite common.  Some configurations result in 50-50 northern-southern hemisphere land distribution, but they are less common than the ~70-30 we have on Earth.  
