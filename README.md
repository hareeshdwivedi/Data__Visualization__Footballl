# Explanatory Data Visualization Using D3

## Summary

This dataset contains 1,157 baseball players including their handedness (right or left handed), height (in inches), weight (in pounds), batting average, and home runs.

In this project I analyze the data for performance of baseball players based on their `Height`, `Weight` and `Handedness`. I observe how these factors can affect the number of [Home Runs(HR)](https://en.wikipedia.org/wiki/Home_run) and [Batting Average(BA)](https://en.wikipedia.org/wiki/Batting_average) a player can have. 

I create two plots, one showing the relationship between `Height`, `Batting Average(BA)`, and `Home Runs(HR)`; another one showing the relationship between `Weight`, `Home Runs(HR)`, and `Handedness`. 

## Design 

To create a useful visualization that can help my audience understand the relationship, I tried to use simple elements and colors to avoid confusion. An informative visualization can be simple and at the same time transfer the message I intend to share with my audience quickly. 

Since for each player their height, weight, and handedness are provided in the dataset, I wanted to make use of all these variables in drawing my conclusions depending on whether I can find any patterns.

Before making the decision on the type of my visualization, I first did a bit of exploratory analysis using **R** on the data. I plotted simple histograms to see how the data is distributed among players. 

### Plot 1: How does the height of a player affect the Batting Average(BA) score? How does it relate to the Home Runs(HR)?

In this plot, I first drew a 2 dimension plot, displaying `height` against `batting average(BA)`. After the initial drawing, and with minimal modifications, it was visible that the batting average(BA) tends to drop as players' height increases. I grouped the data by height and I could immediately see a negative correlation between these two variables. As the height of players increased, their batting average (BA) intended to drop. The best way to show this correlation was to use a `line plot`, and adding _points_ for each height group. 

After a bit of searching on [how weight and height of baseball players can affect their performance](http://www.hardballtimes.com/does-size-matter-part-4/), I decided to add `home runs(HR)` to the same visualization to observe its relationship with `height`. Since I already was using lines to show height and batting average(BA), I decided to this time use bubbles to show height and home runs(HR) scores. I found that:
- The number of home runs (HR) seemed to have been more stable for those who were 70-75 inch tall
- There seems to be a sudden rise in the number of home runs (HR) for those who were 65-inch tall. Those players also have the highest number of batting average(BA) amongst the rest of the players.

To make the visualization more interactive, I used tooltips to show height, home runs and batting average as the mouse hovers over the bubbles or points on lines. 

One thing I would like to have in the dataset was a category showing how experienced a player is. It could be that the number of home runs(HR) or batting average(BA) score have correlations with the level of experience a player has.

### Plot 2: How does the weight of a player affect the number of Home Runs(HR)? Does handedness play a role in here as well?

In my second plot, I decided to observe how weight can/might affect the number of home runs(HR). I also wanted to use the `handedness` variable to see how weight and handedness are related. 

My initial plot was a simple 2D visualization hightlighting the relation of weight with home runs(HR). With this plot, I could see an overall positive correlation between the number of home runs(HR) and the weight of a player-- heavier players tend to have higher score of their home runs(HR). 

To make the plot a bit more interactive, I decided to bring in `handedness` variable. After adding this variable, it seemed to me that left-handed players tend to score higher on home runs(HR). I made the interaction more appealing by bringing in another variable, the `batting average`. I used a bubble chart to demonstrate these relationships:
- Grouped the players based on their weight (i.e. aggregated average weight) and handedness
- Used three colors to divide players based on their handedness: Left, right or both-handed
- Used size of bubbles to show the batting average(BA) score: Higher batting average(BA) is shown with bigger bubbles

Based on this plot, I saw a positive correlation between weight of players and the number of home runs(HR) they scored:
- As the weight of a player increases, the number of the home runs(HR) increases as well
- There also seems to be a trend for higher number of home runs(HR) among left-handed players

## Resources 

- https://bost.ocks.org/mike/selection/
- https://blog.decayingcode.com/post/Easy-Charting-in-JavaScript-with-d3js-and-Dimple-from-CSV-data/
- https://gist.github.com/rgilredondo/4580cf3269e5461efb866d47a6e94c4c
- https://gist.github.com/Amoozegar/b48cfdb57b52174a3c71fba0998f0258
- https://www.sitepoint.com/create-data-visualizations-javascript-dimple-d3/
- https://bost.ocks.org/mike/bar/
