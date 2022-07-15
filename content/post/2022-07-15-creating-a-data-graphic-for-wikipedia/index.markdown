---
title: 'HOW-TO: Create a data graphic for Wikipedia'
author: Adam J Campbell
date: '2022-07-15'
slug: how-to-create-a-data-graphic-for-wikipedia
categories: []
tags:
  - wikipedia
  - data graphic
  - how-to
subtitle: ''
summary: ''
authors: []
#lastmod: '2022-07-15T12:04:15+12:00'
featured: no
draft: true
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
links:
 - name: "code"
   url: https://github.com/campbead/JapaneseSmokingGraphic
   icon_pack: fab
   icon: github
---

I recently was browsing [Wikipedia](https://en.wikipedia.org/wiki/Smoking_in_Japan) and noticed this outdated data graphic:

![Smokers as a Percentage of Adult Population](https://upload.wikimedia.org/wikipedia/commons/a/ab/Smokers-as-a-percentage-of-adult-pop.jpg)

The data only covered a limited range and the style left something to be desired. I decided update this graphic with newer data and give it my own style. I was able to easily [locate the data](https://data.oecd.org/healthrisk/daily-smokers.htm) using the source provided in the image so I knew that this project would be possible.

## Step 1 - Creating the graphic
To create the graphic I use R with the ggplot2 package, I won't go into too much detail here about generating the image but [the code is availble on github](https://github.com/campbead/JapaneseSmokingGraphic). I used RColorBrewer for the point colors and [camptheme](https://github.com/campbead/camptheme) for the theme.  I think the final version turned out quite nicely.

But you can use any method you please to create the code to generate the image. Overall I'm happy with how it turned out.

![Smokers as a percentage of the Adult (15+) population for selected countries 1980-2019](Smokers-as-a-percentage-of-adult-pop-1980-2019.png)

## Step 2 - Upload to Github
Once your code is ready, you can upload to Github.  I won't go into the details here but [this is a good introduction to using Github if you need it](https://lab.github.com/githubtraining/introduction-to-github).

The important part is to use the correct license with your Github Repository.  Wikimedia requires using a[ Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) license for the image, so I chose to use the same license for the code to generate the image. 

Unfortunately, this license isn't a default license on Github so you'll have to generate the license yourself.  However, I found a great resource to use the [CC Attribution-ShareAlike 4.0 International license](https://github.com/santisoler/cc-licenses#cc-attribution-sharealike-40-international).  That guide shows how to update your README.md and LICENSE files in your Github repository with the appropriate details.

## Step 3 - Upload to Wikimedia
Now with your graphic created, and your code published, you can publish your graphic to [Wikimedia Commons](https://commons.wikimedia.org).  First create an account if you don't have one (this can also be used to edit Wikipedia). Secondly, navigate to **Upload file** under the **Participate** heading. 

The page you guide you through the process. You'll upload the image, certify it's your own work, and then describe the image.  Once you reach the **Add data** tab you'll want to add two references.  First add the link to your Github repository to the **source code repository** field, and add the link to the source data to the **external data available** field.

![Picture of reference fields to update on Wikimedia](wikimedia_demo.png)

## Step 4 - Edit the Wikipedia page
The last step is to go to the original Wikipedia page and update the reference from the outdated graphic to the new graphic.  

Click on the **Edit** tab scroll to find the reference to the outdated graphic.  Update the reference with your new filename and update the description.  

![Exampled of editing Wikipedia page to update link to data graphic](Wikipedia_edit.png)

That's it! Great job. You've improved Wikipedia and made the world slightly more knowledgable.
