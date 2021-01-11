---
layout: post
published: true
title: Analysis of Premier League Goalkeepers 19/20 - Part 1 of 3
subtitle: >-
  First part in a series of three posts, where I'll visualize and analyse the goalkeepers performance in the Premier League
date: '2020-02-16'
readtime: true
---
## Introduction

This is the post in a series of three where I will introduce, visualize and analyze Goalkeeper performance in football. The visualization and analysis will be performed through Python and Matplotlib, with data provided by StatsBomb through fbref.com.

A little disclaimer is that I don't have any qualification in football analysis, but I'm just a data science student interested and passionate about learning and explore the field of sports analytics and data science.
This post, along with the coming my coming posts, is therefore not a comprehensive analysis of player, teams and tactics. Though, stats and trends which I find interesting and/or fun will be commented.

## Basics of Goalkeeper analysis

But let's get stuck into it. 
A goalkeepers performance is usually measured and analyzed in three different metrics:
* Shot stopping
* Claims (crosses and sweeping outside penalty area)
* Distribution


In the post I'll cover some of the more common metrics used in evaluation a goalkeepers performance, e.g. clean-sheets, clean-sheets percentage, number of saves, save percentage. The second post will go a bit deeper in goalkeeper metrics, where we will look at expected save percentage (xSv%) and adjusted savepercentage (aSv%). These metrics are definitely better in evaluation performance, but more on that later. The installment in this little miniseries will collect data from the rest of the top European leagues and compare the performance of all goalkeepers.


## Data visualization

#### Clean-sheets

First I'll present some of the metrics which are useful to visualize and analyze a goalkeepers performance.
The most common metrics are clean-sheets and clean-sheet percentage (clean-sheets/games played)


![alt text](/img/EPL_(CS_CS90)_barh.png "Clean-sheets stats")

Clean-sheets are obviously not a true representation of a goalkeepers performance, mostly because clean-sheets are highly influenced by the team in-front of the goalkeeper. This favor goalkeepers who play in defensive strong and/or better overall team, like Kasper Schmeichel (with 8 clean-sheets) and Alisson (with a clean-sheet in almost half of his games)

This is why it's also interesting to see goalkeepers like Dean Henderson, Nick Pope and Lukasz Fabianski at top in regards to clean-sheets. Not only it is a reflection of their very performances so far this year, but also that they play for teams who would rather win play 1-0 than 3-2.

#### Saves

A metric which is more directly connected to the individual performance of the goalkeeper is the number of saves.

![alt text](/img/EPL_(Sv_Svper)_barh.png "Saves stats")

Goalkeepers who stands behind a defensive weak team have a higher possibility of making saves, thus they tend to top this metric. Which is why keepers like Dubravka, Matthew Ryan and Tom Heaton (and even Leno) tops this chart, with the most saves in the league. In contrast we have Alisson and Adrian with the least amount of saves, who both are in goal behind a strong Liverpool team.

Alisson even has a very high save percentage, which shows that when the opposition finds a way through the Liverpool defense Alisson can be counted on. Although it could also indicate that the Liverpool defense are good a pressing the oppositions attackers in tough positions when they shoot, thus Alisson are given better conditions. This concept will be discovered later.

Visualized in a scatter plot we see the extraordinary performance of Alisson even better, the bad performance of Angus Gunn also stands out, (Gunn's performance is though highly influenced by the 0-9 defeat to Leicester) and an underperforming Kepa in goal for Chealsea. 

![alt text](/img/EPL_(Sv_Svper)_scatter.png "Saves stats scatterplot")

If we look at saves per game and saves per goal against, some interesting tendencies are highlighted.


![alt text](/img/EPL_(Sv90_SvGA)_bubble.png "Saves stats bubbleplot")

Alisson is again an outlier with a total of 5 saves for every goal he concedes, furthermore is the performance of the highly criticized Roberto from West Ham highlighted. A total of 4,72 saves per match means he leads this metric by a mile. This could indicate that Roberto actually has been performing on a high level, but the West Ham defense has left him for dead to often. This assertion can be answered if we look at Post Shot Expected Goals per Shot on Target (PSxG / SoT). Post Shot xG shows from a goalkeepers point the difficulty of the independent, this is then normalized by the number of Shots on Target. Therefore this metric illustrates the difficulty of each shot the keeper has to deal with.


![alt text](/img/EPL_(PSxG_SoT)_barh.png "PsxG bar plot")

Here we see Roberto and West Ham has a high oTxG/SoT, which means that West Ham has given Roberto very bad conditions for performing high in the general metrics. Roberto's high number of saves per games shows that he actually has done a quite good job.

It is also interesting to Ederson in the top of his metric with 0.37 PsxG/SoT. Which shows Manchester City is team who let the opponent have big chances when they get through on goal leaving Ederson with a hard job. City's offensive playing style could be the reason, which allows their opponents with a lot of counterattacks. On the other hand we see Alisson with a league low of only 0.27 PsxG/SoT. Thus the strong defence of Liverpool undoubtedly has helped Alisson leading a lot of these metrics.


If you got this far, so a big thank for reading along. There is a lot to improve from my side and the next post in this series will, hopefully, be an improvement. In the post I will cover more in depth metrics, like Goals Saved Above Average (GSAA), expected Save percentage (xSv%) and more.
