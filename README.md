# Project Overview

This Shiny app was designed for the 2024 Women in Sports Data Hackathon. This hackathon asked participants to create projects & analysis based on bat tracking data.

## Description & Purpose

This Shiny app was designed to allow users to determine the most likely pitch speed range (or pitch type) during a chosen game scenario and then analyze the ideal bat swing speed range that will optimize the batter's chances of hitting the ball into play. 

Because the sample data had a very limited number of plays where the pitch type was identified, the application defaults to analyze the pitcher's speed range. 

## App Contents

This application has two tabs that allow the user to determine the best batting strategy based on the **pitch speed range** or the **pitch type**. The user can toggle between the two tabs at the top of the page.

### Part I:

The first part of the application allows the users to see the most likely pitch speeds (or pitch types) thrown by the opposing team in a variety of scenarios.

**Game Scenario Filters**: Within the first card, users can use three filters to evaluate how a pitcher's strategy generally changes based on different game scenarios. These three filters are:

* Innings: filters by the inning(s) in which the plays were pitched (1 to 9)
  
* Outs: the number of outs in the inning when the pitch was thrown (0, 1, 2)

* Strikes: the number of strikes for the batter when the pitch was thrown (0, 1, 2)
  
**Pitch Speed (Type) Probability Graph**: Based on the applied filters, the user can see the pitch speed ranges (or pitch types) that will most likely happen in the chosen scenario. When considering the pitch speed, the user has the ability to change the number of bins used in the graph. 


### Part II:

The second part of the application allows the users to apply the likely pitch speed range (or pitch type) to determine the bat swing speed that will yield the most success. 

**Pitch Speed (Type) Filter**: This filter allows users to apply the desired pitch speed range (or select a specific pitch type).

**Bat Swing Visuals**: The user has the ability to toggle between two different visuals. The default view is of a layered histogram that displays the total number of swings within a specified bat swing speed range and further breaks down this total into swings that resulted in a hit into play (success = blue) or a strike (failure = red). The other visual is a data table that shows very similar data as the graph but has the ability to calculate the overall success rate in each range. *In this app, bat swing speed is calculated from bat tracking at the bat's head position*. Both visuals are affected by the "# of bins" visual.

**Statistics of Non Swing Plays**: This final visual provides additional context into the probability that a 'Ball' will be called instead of a 'Strike' if the batter does not swing for the filtered pitch speed range (or pitch type). This additional information can assist users in determining if batters would be better off not attempting to swing the bat for certain pitch types or speeds.

## Directions for App Usage

To use the app from the wisd_hackathon file:

1. Open a new session in R
2. Set the working directory to the wisd_hackathon file
3. From the wisd_hackathon file, open 'app.R'
4. Click 'Run App'

### Required Files:

In order to run the Shiny app in your desktop, the following files/folders must be downloaded and contained within the submission folder 'wisd_hackathon'

* wisd_hackathon.Rproj

* app.R
  
* app_data

### Required Packages:

The following packages were used in this Shiny app and will need to be installed if they are have not already been:

* tidyverse

* readr
  
* dplyr
  
* shiny

* bslib

* plotly

* htmlwidgets

* reactablefmtr

* rsconnect

* DT

* data.table

### Potential Additions to App

In an ideal situation, a team could use this Shiny app to prepare their batting strategy against the opposing team’s pitchers. For instance, a player would have an idea of how aggressive they need to swing their bat against a specific pitcher. However, the provided bat tracking data limits are ability to differentiate between pitchers at this time. 

Additionally, the app could further be improved by identifying the optimal bat positioning in relation to the ball in order to increase the likelihood of a hit into play for various pitch speeds and types. 

## Link to Live Application

A live version of the application can be found [here](https://megan-hunt.shinyapps.io/wisd_hackathon/).
