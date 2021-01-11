---
layout: post
published: true
title: Analysis of Premier League Goalkeepers 19/20 - Part 3 of 3
subtitle: >-
  Third part in a series of three posts, where I'll be visualize and analyse the goalkeepers performance in the Premier League
date: '2020-03-18'
readtime: true
---
## Introduction

In the last part of our analysis of goalkeeper performance we will look at a new metric in football, but a very used metric in the analysis of goalkeeper performance in Ice Hockey. This metric is Goals Saved Above Average (GSAA). We will then build on top of this metric by looking at Goals Saved Above Expectation, that with the use of Expected Goals against can distinquish between as they face different difficulty of shots.

#### GSAA (Goals Saved Above Average)

The first metric discussed is the GSAA. The best way to give an intuition to what GSAA is, is to see how it is calculated. To calculate a goalkeepers GSAA you take the league average save percentage and apply that to the number of shots the goalkeepers has faced. This gives you the numbers goals a "league average" goalkeepers would had let in if he faced the same number of goals the goalkeeper had throughout the season. This number can now be compared to the goalkeeper we are analyzing. A plus/minus number is created, where a plus means how many goals the goalkeeper have saved compared to the "league average" goalkeeper. On the other hand, a minus mean that the goalkeeper is performing below the "league average" goalkeeper in the same situation.

Thus GSAA looks beyond the performance of the team the goalkeeper plays. It equalizes the goalkeepers across the league, which makes it possible to compare performance directly between the goalkeepers. Moreover, gives the GSAA an indication of how much a team relies on the performance of their goalkeeper. If a team gives up a lot of shots, but the goalkeepers saves a lot of them, he will have a high GSAA. So if the team had a "league average" goalkeeper or worse, they would have conceded a lot more goals.

Let's see how the Premier League goalkeepers compares in GSAA.

![alt text](/img/EPL_GSAA_barh.png "GSAA")

In the Premier League there is a huge disparity in the GSAA of the goalkeepers. Dean Henderson (6.01) and Alisson  (5.72) have approximately a positive GSAA of 6, which means that they have saved 6 goals more than a "league average" would had, if he had faced the same amount of shots. Or in others words would Sheffield and Liverpool had conceded 6 more goals if they had a "league average" goalkeeper in goal.

On the other we have Kepa with a negative GSAA of 8.23. Which means that if Chelsea had a "league average" goalkeeper they would had conceded EIGHT!! less goals. Indicating that Kepa has massively underperformed when we compare him to the rest of the Premier League goalkeepers.

But GSAA have some floors. The main one lies in the fact that the difficulty of all the shots the goalkeepers has faced had a similarly difficulty 

#### GSAE (Goals Saved Above Expectation)

Goals Saved Above Expectation accounts for everything that GSAA does, but this metric takes into account the fact that the goalkeepers haven't faced equally difficulty of shots. This is because this metric is based upon Post Shot Expected Goals, i.e. the amount of the goalkeeper is expected to concede. Thus this metric sees beyond the performance of other goalkeepers and only looks at how the goalkeeper have performed relative to the shot quality he has faced. 
This chart can therefore be used to describe present performance, not to predict future performance.

![alt text](/img/EPL_GSAE_barh.png "GSAE")

As we again can see is the performance from Hugo Lloris very impressive. He has saved almost 10 more goals for Spurs than he was expected to and on the other hand we again see the dreadful performance from Kepa. With almost 10 goals conceded which was expected to be saved Kepa is again leading the race of the worst performing goalkeeper in the Premier League in the 2019/2020 season.

This concludes the analysis/visualization of the Premier League goalkeepers performances in the 2019/2020 season. A season where the goalkeepers from the two most dominant clubs doesn't stand out as both Alisson and Ederson played behind two very strong teams.
We've seen a very good performance by Hugo Lloris. A performance which isn't much appreciate in the common press, but he stands out in all the important metric especially aSv%, GSAA and GSAE. Another mention must go to Emiliano Martínez. He replaced a very well performing Bernd Leno, but just performed even better and ended the season with the highest Sv% and aSv% and in just 8 games saved 4 goals more than expected (GSAE of 4).

