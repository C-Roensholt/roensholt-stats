---
layout: post
published: true
title: Analysis of Premier League Goalkeepers 19/20 - Part 2 of 3
subtitle: >-
  Second part in a series of three posts, where I'll visualize and analyse the goalkeepers performance in the Premier League
date: '2020-03-6'
readtime: true
---
## Introduction

As touched upon in part one are the general metrics used to evaluate a goalkeepers performance (clean-sheets, save percentage, number of saves etc.) very influenced the performance of the rest of the team. Therefore we need to introduce metrics which can see past this and evaluate the goalkeepers performance more independent of the teams performance and  
In the second part of the series "Introduction to Goalkeeper Analysis and Visualization" we will therefore dive into some advanced metrics than in part 1. More specific expected Save percentage (xSv%) og adjusted Save percentage (aSv%).


**The code for the calculation of the metrics and creating of visualizations can be found [here](https://github.com/C-RNSHLT/football_analysis/blob/master/Goalkeepers%202019-2020/beginner_Visualizing_Goalkeeper_Performance_2_3.ipynb)**

Let's get stuck into this!


#### xSv% (Expected Save Percentage)

Expected goals, - assists, - threat, among others, has in recent years become a very popular metric in evaluating the "real" performance of a player or team, but it hasn't really adapted to goalkeepers. 
We calculate the xSv% following the calculation of the original Sv%, which uses Shots on Target Against (SoTA) and Goal Against (GA) **(SoTA-GA) / (SoTA)**. But to calculate the expected savepercentage we have to used the expected goals against instead of the actual against. StatsBombs Post Shot Expected Goals (PSxG) provides exactly this metric. PSxG is the cumulative expected goals of all the shots the goalkeepers faced which ended on target (i.e. discounting wayward freekick attempts and other shots way of target etc.). An explanation of PSxG from StatsBomb can be seen [here](https://statsbomb.com/2018/11/a-new-way-to-measure-keepers-shot-stopping-post-shot-expected-goals/)

**(SoTA - PSxG) / SoTA**

Calculating the expected save percentage is done exactly how you would calculate the normal Sv% for a goalkeeper. But instead of using the actual shots the goalkeeper has conceded we will use the PSxG, i.e. the number of goals the goalkeeper is expected to had conceded.

$\frac{SoTA-PSxG}{SoTA}$

![alt text](/img/EPL_xSv_barh.png "xSv%")

It is important to note that expected save percentage is **NOT** a measure the goalkeeper's actual performance, it merely serves as a benchmark for the Sv% that an average goalkeeper should have had, given the quality of chances he faced.

To use xSv% as a measure of performance it is necessary to put it into context, this is done by comparing it to actual save percentage of the goalkeeper.


![alt text](/img/EPL_actualSv_xSv_barh.png "actual vs xSv%")

Here we see the actual save percentage and xSv% of every goalkeeper in the league. If a goalkeeper has a higher actual Sv% than what is expected from him, he performs on a high level. If the actual save percentage is lower than what is expected (xSv%) then the goalkeeper is not performing good.

This statement is highlighted by the high performer Alisson and low performer Kepa.
Alisson has a xSv% of ~74% while his actual Sv% is ~85, which means that he saves 10%points more than what is expected of him. While Kepa, on the other hand, has a xSv% of ~62%, but an actual Sv% of ~55%. Meaning he saves ~7% less than what is expected.

This comparison of actual Sv% and xSv% is very useful, but from the visualization above it can be difficult to extract. Here enters adjusted Sv% (aSv%) the chat.

#### aSv% (Adjusted Save Percentage)

Adjusted Save Percentage (aSv%) is pretty straightforward when you understand xSv%, because aSv% is just the difference between xSv% and the actual Sv% of the goalkeeper. A **aSv% of 0** therefore means that the goalkeeper has performed exactly to the level of an average goalkeeper given the quality of chances he has faced. **A negative aSv%** means that the goalkeeper has conceded more goals than expected and **a positive aSv%** therefore means that the goalkeeper has saved more shots than expected.

This is a much more valuable stat than the standalone xSv%, because it highlights how a goalkeeper has performed regardless of the team in front of him. The fact that aSv% can see beyond the performance of the team in front of the goalkeeper makes it possible to compare goalkeepers from different teams across the Premier League and other leagues.

![alt text](/img/EPL_aSv_barh.png "aSv%")

The statements about Alisson's very good performance and the bad performance of Kepa, which we analysed through the xSv% and actual Sv% above, is now clearly showed through the aSv%.
Furthermore, we can see the great performances of Vicente Guaita from Crystal Palace and struggling Southampton's Alex McCarthy. Especially the great performance of Alex McCarthy isn't visible when we seperately look at his actual Sv% (68.5%) or his xSv% (61.85%). But when these are combined into aSv% we can see great "hidden" performances of goalkeepers who play behind a struggling team.

As we have seen can aSv% make it possible to compare goalkeepers performance across different teams. Therefore is aSv% the metric which, in my opinion is the best in analyzing the performance of a goalkeeper throughout the season. Another metric that can be used to compare goalkeeper performances is Goals Saved Above Average (GSAA). GSAA wil be covered in the last part of this little series about analysis and visualization of goalkeeper performances. Moreover, we will cover another metric which is Goals Saved Above Expectation (GSAE). What is so good about GSAE will be explored in the next episode.





