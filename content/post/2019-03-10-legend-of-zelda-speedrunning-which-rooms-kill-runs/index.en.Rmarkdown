---
title: Legend of Zelda speedrunning— Which rooms kill runs?
author: Adam J Campbell
date: '2019-03-10'
slug: legend-of-zelda-speedrunning-which-rooms-kill-runs
categories: []
tags: []
subtitle: ''
summary: ''
authors: []
draft: true
lastmod: '2022-06-13T12:37:14+12:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---
_Note: this article was originially published on [Medium](https://campbead.medium.com/legend-of-zelda-speedrunning-which-rooms-kill-runs-75c2b44d00d2)._

_This is the part 2 of my series on analyzing speedrunning of Legend of Zelda [(check out part 1: Legend of Zelda speedrunning — top 5 time wasting rooms)]({{< relref "/post/2018-02-23-legend-of-zelda-speedrunning-top-5-time-wasting-rooms" >}})_

If you’re like me you spent many hours as a kid playing the Legend of Zelda. I remember this game for its open world. It was the first video game I where I was free to choose how I wanted to explore the world.

<iframe src="https://giphy.com/embed/pvl3qUsgblNOo" width="480" height="173" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/secrets-pvl3qUsgblNOo">via GIPHY</a></p>

## The Project
A few months ago I got pretty into watching [Arcus](https://www.twitch.tv/arcus) on [Twitch](https://www.twitch.tv/), and at the time he was speedrunning the Legend of Zelda (speedrunning is where players try to complete the game in the fastest time possible). Arcus has this casual animated quality that really makes him a ton of fun to watch. I was on board with his mission of beating Legend of Zelda in under 30 minutes.

At the time I was also deciding that I wanted to leave the academic world and try to get into data science. To help accomplish that goal, I decided that I needed to learn Python since it’s a major language used in data science. I had already mastered Matlab with years of building models and data analysis during my PhD/postdoc, but I knew that wouldn’t cut it in the data science field. So I decided **I needed a project to force myself to learn Python.** I picked scraping Arcus’ stream and doing this data analysis you see here today. So enjoy!

## Speedrunning Legend of Zelda

A few things you should know about speedrunning before we get started. The Legend of Zelda has different rooms (also called screens), that the player has to travel through to eventually win the game. The Legend of Zelda is open in that the player is free to choose different paths to accomplish this goal. In speedrunning however, predefined routes are used to beat the game is the shortest time possible.

![The Double Hundo route has 9 overworld sections O1-O9 and 9 dungeons D1-D9 (note the dungeons are played out of order).](overworld-map.png "The Double Hundo route has 9 overworld sections O1-O9 and 9 dungeons D1-D9 (note the dungeons are played out of order).")

Arcus mostly ran what he called the “Double Hundo” route, named for the two 100 rubie secret rooms he visited on the route. He did a lot of runs (9472) in this push but I only was able to download videos for the most recent 4581 of Arcus’ runs. Let’s take a look at the rooms where those runs ended.

![die often and die fast — most of Arcus’ run ended before completing even one dungeon. each dot here represents deaths for an individual screen](reset_count_graphic.png "die often and die fast — most of Arcus’ run ended before completing even one dungeon. each dot here represents deaths for an individual screen")

On the figure we have dots representing rooms ordered in their position on the route on the horizontal (x-axis) and the number of times Arcus entered that room on the vertical (y-axis). We can see that the overwhelming majority of runs ended before Arcus completed his first dungeon (which in this route is Dungeon 3, remember players are mostly free to choose the order the complete the dungeons). We can also see that Arcus completed his run 102 times in this data set, or about 2.2% of the time.

The picture above gives us a good sense how quickly most runs ended, but it makes it difficult to interpret where runs were _most likely_ to end.

## Dangerous Rooms

We’re going to look at a simple question while examining my Arcus87 data set, which rooms in the speedrun kill the most runs? After exploring and becoming familiar with the data, I thought of two different ways to think about this question. First, I could count the run of times a run ended in particular room, I call this the **reset count** (seen in the figure above). Second I could calculate how likely the run is to end in that room, I call this the **reset fraction**.

The **reset count** gives a clear indication of which room are most troublesome in shear numbers. It is heavily weighted toward the beginning of the run, as you can easily see in the above figure. If the run gets off to a bad start, it’s likely to be reset. The **reset fraction** however, gives a better indication of the rooms overall difficulty of the room by showing us just how often that room killed a run. It’s for that reason that I’ll use the **reset fraction** as my metric for evaluating which rooms kill runs the most often.

### #10 — Dungeon 4 — Vire Room (before boss)
<iframe src="https://clips.twitch.tv/embed?clip=ConfidentTolerantJamPJSalt&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

Here Arcus must defeat 5 Vires before moving on to the next room. Coming into the room with a maximum of 4 hearts means the margin for error here is small. Vires, once they are hit split into two red Keese meaning there are actually 15 enemies to defeat on this screen. Arcus mitigates this using bombs, which are capable of killing Vires and the Keese they spawn. This room resulted in a death/reset about 12% of the time or 105 times in the runs I examined.

### #9 and #8 — Overworld 1 — Screen wraps
<iframe src="https://clips.twitch.tv/embed?clip=DullBlueDadBleedPurple&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

I’m going to count these rooms together since they are sequential rooms and they really have the same root cause of failure, the screen wrap. At a few points in the run, Arcus must perform a neat little trick called the screen wrap which allows him to warp Link from the right edge of the screen to the left edge of the screen. I’ll fully admit I spent about 30 minutes trying to do this technique at home and was not successful once! These room are the 2nd and 3rd rooms of the run. So Arcus doesn’t accept any failures here, if he misses a screen wrap here, he just resets the run. There are some screen wraps later in the run where a failure to execute this move is tolerated.

Individually, he’s able to pull off the move about 87% of the time. Which means that taken together these rooms kill about 1/4 runs, or 1054 runs total. WOW!

### #7 — Dungeon 5 — Digdogger (boss)
<iframe src="https://clips.twitch.tv/embed?clip=RacyAltruisticOtterTebowing&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

The Digdogger is a fast moving boss that needs to be killed a particular way. First the flute is used to transform the Digdogger into his second form. Then Arcus uses bomb to damage the boss and finishes him off with the sword. All the while he’s being shot at by Stone Statues. This room resulted in a death/reset about 14% of the time or 47 times in the runs I examined.

### #6 — Dungeon 9 — Gannon (final boss)
<iframe src="https://clips.twitch.tv/embed?clip=DeterminedAlluringAnacondaKeyboardCat&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

Gannon, the big boss. I was happy to see that Gannon made this list. He’s a tough boss and 15% of the time, Arcus would be defeated by him. I mean that’s actually pretty amazing that he’s able to defeat him 85% of the time. It’s probably a testament to all the work he has put into practicing these end-game rooms.

### #5 — Dungeon 3 — Red Darknut Room 2
<iframe src="https://clips.twitch.tv/embed?clip=WiseElegantEagleHumbleLife&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

In this room, Arcus faces off against 5 Darknuts. He must kill the Darknuts before the lower door opens allowing him to advance. This is a formidible task as this is his first Dungeon of the game and he only has a maximum of 3 hearts here. 18% the time he enters this room his run ends here.

_Note: He actually enters this room twice, the statistics quoted here only refer the the 2nd time he enters this room, and has to defeat the Darknuts_

### #4 — Dungeon 4 — Geelok (boss)
<iframe src="https://clips.twitch.tv/embed?clip=OutstandingSmokyPelicanNerfRedBlaster&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

The Geelok is a tough boss the kills Arcus runs 24% of the time. This multi-headed boss gets more powerful as you damage it, with heads detaching from the main body and flying around to attack Link.

### #3 — Dungeon 3 — Red Darknut Room 1
<iframe src="https://clips.twitch.tv/embed?clip=BlightedLitigiousDinosaurDxAbomb&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

This is the first big test for Arcus in his speedrun. In this room he has to quickly get a bomb move on to the next room. If picks up an early bomb, he can move along early, otherwise he is forced to defeat all three for an early bomb drop. 25% of the time his run ends here. As mentioned in my previous blog post, this room has big spread of times is takes to clear, 5.4 seconds difference between his median time and the top 10% of times.

### #2 — Dungeon 5 — Blue Darknut 2 (aka the Olive Garden)
<iframe src="https://clips.twitch.tv/embed?clip=CovertFrozenCobblerNinjaGrumpy&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

Of all the rooms that standout as troublesome while watching Arcus play, the Olive Garden stands out as being the most troublesome. This room is brutal. He has to defeat 6 Blue Darknuts here to move on to grab the flute (or Bread-stick, if you’re a fan of Arcus). An enormous 30% of runs end here and when he is able to complete this room, there is an 8.2 second spread between his median completion time and his 10% best times.


### #1 — Dungeon 3 — Manhandla (boss)
<iframe src="https://clips.twitch.tv/embed?clip=ExquisiteWrongKumquatAliens&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

This boss a tough one. Arcus comes into this room with only 3 hearts max, so the margin for error is small. A bad bomb placement here can kill the run. Even if he does defeat the boss, if the total run time is too high here, he’s likely to just reset the run himself. The Manhandla room gets the best of 34% the rooms.

<iframe src="https://giphy.com/embed/bNhwcJ5ukkMvu" width="480" height="360" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/the-legend-of-zelda-bNhwcJ5ukkMvu">via GIPHY</a></p>

## Which rooms never kill runs?

Most of them! In my data set, 134 of the 234 rooms I define never result in a death. The big story here is how different dungeons are from the overworld. 61 of 141 (43%) of dungeon rooms had zero deaths. In the overworld it’s 71 out of 93 (76%) never resulted in death. Of the 4479 runs that weren’t completed, 3162 (70%) ended in a dungeon. Only 1315 runs (30% of non-completed runs) ended in the overworld. If we filter the first overworld push where resets are frequent due to missed screen wraps, then that number drops to 68 (2% of non-completed runs).

_**The takeaway here: Dungeons are hard. This is by far where most deaths/resets occur.**_

## A Bit About the Data
I have developed a python script that scrapes Twitch VODs for Legend of Zelda, determining the time spent in each room, hearts, rubies, and bombs. I scraped data from over 4000 runs. My goal is explore this dataset using a variety of statistical tools. My Python script and documentation is still very much a work in progress, but feel free to have a look at it on my [Github](https://github.com/campbead/LoZscraper).
