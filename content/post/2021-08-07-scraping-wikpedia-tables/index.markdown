---
title: Scraping Wikpedia Tables
author: Adam J Campbell
date: '2020-06-23'
slug: scraping-wikpedia-tables
categories: []
tags: [rstats, wikipedia, scraping, rvest] 
subtitle: ''
summary: 'A quick how-to guide on scraping tables from Wikipedia, using R.'
authors: []
lastmod: '2021-08-07T20:42:55+12:00'
featured: no
aliases:
   - /post/wikipedia_table_scrape/wikitablescrape/
image:
  caption: ''
  focal_point: 'Center'
  preview_only: no
  alt_text: 'graphic with text: HOW TO: Scraping Wikipedia Tables'
projects: []
links:
 - name: "twitter"
   url: https://twitter.com/campbead/status/1277452002960609281
   icon_pack: fab
   icon: twitter
---

Want to know how get data from a [Wikipedia](https://en.wikipedia.org/wiki/Main_Page) table into your R script?  Look no further.  

I was recently attempting to scrape a table from Wikipedia.  I was responding to a group chat and wanted to make a quick histogram (something I love about R and ggplot).  In my search, I came across this very helpful tweet from [Julia Silge](https://twitter.com/juliasilge). 

*Update 12-July-2025: this account has now gone private and this tweet can no longer be displayed but the code displayed in the tweet was:*

```
    library(rvest)
    library(tidyverse)

    h <- read_html("https://t.co/gloY1eErBn")

    reps <- h %>%
    html_node("#mw-content-text > div > table:nth-child(18)") %>%
    html_table()

    reps <- reps[,c(1:2,4:9)] %>%
    as_tibble()
```

This is great piece of quick code to scrape the data from the table.  However this tweet is specific only to the example, and I want to generalize the code for any Wikipedia table.

I'm going to show you to scrape data from any Wikipedia table using Firefox browser and R (of course), although I'm sure this could be adapted to other browsers.  

I'll show how to change the above code into a code to scrape the table I was interested in, which was the [attendance size of Trump's rallies](https://en.wikipedia.org/wiki/List_of_rallies_for_the_2016_Donald_Trump_presidential_campaign).  Here, I'd like to scrape the `Primary rallies (June 2015–June 2016) ` table.

![Screen clip of table 'Primary rallies' from the List of rallies for the 2016 Donald Trump presidential campaign wiki ](Wiki_trump_rallies.png)

The first thing to change is the `read_html()` line:

```{}
read_html("https://en.wikipedia.org/wiki/Current_members_of_the_United_States_House_of_Representatives")
```


all we need to here is update the hyperlink by copying the web address of the wikipedia page:

```{}
read_html("https://en.wikipedia.org/wiki/List_of_rallies_for_the_2016_Donald_Trump_presidential_campaign")
```

The next thing to change is the `html_node()` line.  For this this you'll have to know the tag of the table in the html code.  To find this you'll have to [inspect the html code](https://www.lifewire.com/get-inspect-element-tool-for-browser-756549) of the wikipedia page you're looking at.

Inspect the table you're interested in and you'll see a line starting `<table class= ...`

![Screen capture of inspector, highlighting line <table class= ...](wikitable_example.png)

Right click on that line and select `Copy` -> `XPath`

![image displaying how to copy xpath](copy_xcode.png)


then update the with `html_node` line, using the `xpath` flag:

```{}
html_node(xpath = '/html/body/div[3]/div[3]/div[4]/div/table[2]')
```
