---
title: Legend of Zelda speedrunning — top 5 time wasting rooms
author: Adam J Campbell
date: '2018-02-23'
slug: legend-of-zelda-speedrunning-top-5-time-wasting-rooms
categories: []
tags: [speedrunning, Legend of Zeland, analysis]
subtitle: ''
summary: ''
draft: false
authors: []
lastmod: '2022-06-12T13:19:27+12:00'
featured: no
image:
  caption: ''
  focal_point: 'Center'
  preview_only: true
  alt_text: 'Link holding Triforce'
projects: []
---

Note: this article was originially published on [Medium](https://campbead.medium.com/legend-of-zelda-speedrunning-top-5-time-wasting-rooms-3f3a311d16e8).

A few months ago I discovered the Retro channel on Twitch where folks play a lot of classic NES and SNES video games that I remember fondly from my childhood. My attention was quickly drawn toward one streamer in particular, [Arcus87](https://www.twitch.tv/arcus87) who was attempting to speedrun the Legend of Zelda in under 30 minutes ([a goal he recently achieved in January](https://www.twitch.tv/videos/220036001)). At the time I was vaguely familiar with speedrunning and video game competitions, having watched the King of Kong and few YouTube videos on the [history of speedrunning](https://www.youtube.com/channel/UCtUbO6rBht0daVIOGML3c8w). Heck, I even remember having informal Super Mario Brother speedrunning competitions in my college dorm. But until I watched Arcus I hadn’t realized just how active the speedrunning community is with competitors and fans alike.

![Link holding Triforce.](link.jpeg)

While watching Arcus, with his very approachable demeanor, I found myself wondering how the speedrun could be improved. I’ve always been a bit of a data geek so I thought I’d give it a go to try figure out which rooms of the LoZ speedrun have the most room for improvement.

What followed was really an attempt for me to learn a new programming language. So I chose the rather ambitious project of scraping Arcus’ Twitch videos for time spent in each room. After compiling and cleaning that data, I can now write up a few blogs based on what I found about this data. This series isn’t meant a definitive statement about how LoZ speedruns should be done. Rather, it’s an exploration of what I consider to be an interesting dataset.

For this first post, I’ll be exploring which rooms are the biggest time wasters of the run. Which I define as which rooms have the biggest difference between the best times and most common times (a more technical definition is give below for those interested). So without further ado, I present the Top 5, time wasting rooms…

## #5 Dungeon 2 — Red [Goriya](https://zelda.gamepedia.com/Goriya) room

<iframe src="https://clips.twitch.tv/embed?clip=CovertFrozenCobblerNinjaGrumpy&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

![](blank.png "Entering this room with bombs seems to be the key to a fast time")

In Dungeon 2, this room has 5 Red Goriyas that must be defeated to advance and pick up a bomb. Most times this takes 12.6 seconds, however during fastest runs, this room only takes 8.4 seconds, giving Arcus a **4.2 second** savings. I suspect this savings is because in his fastest runs, he is able to use bombs to quickly defeat the Goriyas. On further looking into the data, in his best times Arcus entered the room with an average of 6.3 bombs, and when we look at all times, he enters the room with 3.8 bombs _(technical note: these values are different for my chosen significance level of α = 0.01)._

![Histogram of times for Dungeon 2 — Red Goriya room](Red_Goriya_room_1.png "Histogram of times for Dungeon 2 — Red Goriya room")

We can break this data up a little bit by looking the bombs while entering the room:

![Histogram of times for Dungeon 2 — Red Goriya room](Red_Goriya_room_2.png "Histogram based on number of bombs when entering the room, lines represent median times")

It’s quite clear that entering this room with 6 or more bombs goes a long way toward an early finish. The difference between the median times is **almost 5 seconds.** Furthermore, entering this room with 6 or more bombs almost never takes longer than 15 seconds (the approximate median time for 5 or less bombs). Bottom line, it really pays to have bombs coming into this room.

## #4 Dungeon 8 — Triforce room

<iframe src="https://clips.twitch.tv/embed?clip=LongSmoothTigerRalpherZ&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

![](blank.png "Depending on how many hearts Arcus has, the triforce can take anywhere from 10 to 19 seconds to complete")

At the end of every dungeon in Legend of Zelda, Link grabs the Triforce and heals all of hearts up to full. This process of healing takes time, and depending on how much Link needs to heal, it can be quite a while. This room was a total shocker to me, I had no idea just how much of time sink it could be. The median time to clear this room is 16.2 seconds, while the best times are 11.2 seconds, representing a **5.0 second** difference between the best times and median time. I dug a little deeper into data I gathered to find the relationship between the amout of hearts while entering the room and completion time. Each empty heart takes about 0.7 seconds to fill.

![Time for completion of the Dungeon 8 Triforce room, each dot represent a single run and the line is a best fit](Triforce_room_1.png "Time for completion of the Dungeon 8 Triforce room, each dot represent a single run and the line is a best fit")

![Histogram of times for Dungeon 8 — Triforce room](Triforce_room_2.png "Histogram of times for Dungeon 8 — Triforce room")

## #2 (tied) Dungeon 3 — First Red Darknut Room

<iframe src="https://clips.twitch.tv/embed?clip=BlightedLitigiousDinosaurDxAbomb&parent=www.adam-campbell.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

![](blank.png "The First Red Darknut Room is first real test of the speedrun")

This is the first real test of the speedrun for Arcus. He needs to quickly get a bomb and clear the 3 Darknuts to proceed to the next room. This room holds a massive potential for time gains, with his best times being **5.4 seconds** better than his median time of 14.0 seconds. In this clip, Arcus finished the room with 56 seconds on the clock, a bit slow by his standards, however he went on to get sub-30 minutes in this same run.

![Histogram of times for Dungeon 3 — First Red Darknut Room](First_Red_Darknut_Room.png "Histogram of times for Dungeon 3 — First Red Darknut Room")

This is a very bimodal distribution of times. It doesn’t seem to correlate to having the beam sword (full health) or not. It also doesn’t depend on bombs prior to the room or not since this is the first room where Arcus gets bombs.

Killing the Darknuts in this room will result in a bomb drop, i.e. a bomb that can be picked up for later use. However sometimes a Darknut will drop a bomb early, before all three of them are defeated. I suspect that is why there is a bimodal spread in this data, however I didn’t collect any data that can specifically test this hypothesis.

## #2 (tied) Dungeon 8 — Second Blue Darknut Room

<iframe src="https://clips.twitch.tv/embed?clip=PlayfulWildCheetahBCouch&parent=www.example.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

![](blank.png "Arcus most clear 6 Blue Darknuts here")

This is the second room in Dungeon where Arcus most clear Blue Darknuts before advancing. In this room there are 6 Darknuts and 2 shooting dragon things (I couldn’t find their names). This room was tied (within my precision) with the Dungeon 3 Darknut room for time wasting. The best times were **5.4 seconds** faster than most completions. The first Blue Darknut room in Dungeon 8 would have made my top ten list at 3.7 seconds time difference. I think the reasons the room is a bit more consistent are that it has one fewer Darknut and Arcus is probably more likely to enter that room with the beam-sword.

![Histogram of times for Dungeon 8 — Second Blue Darknut Room](Second_Blue_Darknut_Room_1.png "Histogram of times for Dungeon 8 — Second Blue Darknut Room")

For this room I didn’t find any strong dependence on how many bombs Arcus had going into the room or any large improvement with or without the beam sword (full health). However, I did find that the times improved over Arcus’ time playing the game.

![Histogram based on era of the run, lines represent median times](Second_Blue_Darknut_Room_2.png "Histogram based on era of the run, lines represent median times")

The late era runs (which I define as the most recent half) are about 2 seconds faster than early era runs, when comparing median values. So it appears that Arcus’ experience has really benefited him for this room.

## #1 Dungeon 5 — The Olive Garden

<iframe src="https://clips.twitch.tv/embed?clip=CovertFrozenCobblerNinjaGrumpy&parent=www.example.com" frameborder="0" allowfullscreen="true" scrolling="no" height="378" width="620"></iframe>

For watchers of Argus’ stream there was never any question as to which room is the most troublesome of the room run. Yes it’s the infamous “Olive Garden.” This screen has a HUGE potential time saving with the best times clocking in **8.2 seconds** shorter than most completions.

![Histogram of times for Dungeon 5 — The Olive Garden](The_Olive_Garden.png "Histogram of times for Dungeon 5 — The Olive Garden")

I haven’t fully explored the distribution of times for the Olive Garden and why the range is so big. I’ll probably leave that to a future blog post.

## Conclusion

Some rooms in the Legend of Zelda speedrun have a pretty wide range in the time in it take to complete. Here we’ve taken a look at which rooms have the most room for improvement. In future posts, we’ll be analyzing this data a bit more by looking into some other factors. Stay tuned for more results and let me know if you have an ideas for analysis you’d like to see.

## A Bit About the Data

I have developed a python script that scrapes Twitch VODs for Legend of Zelda, determining the time spent in each room, hearts, rubies, and bombs. I scraped data from over 4000 runs. My goal is explore this dataset using a variety of statistical tools. For this present analysis, I compare the best times in each room to medians time in the room. I define the best times as the 0.05 quantile time, or put another way, 5% of the times this room is completed it’s with a time equal to or better than this time. A similar thing can be said about the median time, 50% of the times this room is completed it’s with a time equal to or better than the median time.
