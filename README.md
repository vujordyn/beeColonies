# beeColonies

## Data Description

* We got our data from [Kaggle](https://www.kaggle.com/datasets/jessicali9530/honey-production?resource=download). It has the following columns: state, numcol, yieldpercol, totalprod, stocks, priceperlb,prodvalue, year. For both visualizations, we wanted to show the trends in number of bee colonies across the United States over time. Therefore, we decided to use the variables state, numcol (number of honey producing colonies), and year.

* For visualization 1, we created a simplified version of the U.S. map with each state being represented as hexagons. To create this map, we used data from [Carto](https://team.carto.com/u/andrew/tables/andrew.us_states_hexgrid/public/map) and got the coordinates of each state hexagon. From our honey production dataset, we chose to show the maps for 2 distinct years 1998 and 2012, thus we filtered the data by year and created two subsets.

* For visualization 2, we created a line graph of the number of colonies in NY over time from 1998 to 2012. In order to create a subset that only contains data points for NY, we filtered the data by using const numColNY = data.filter(d => d.state=="NY")for. Also, to represent the years without the comma separating (e.g. 1,998), we used a time parser to format it nicely.

***

## Design Overview

* For the map visualization: Marks were the hexagons representing states, which we made all the same size because we wanted them to only vary by our saturation channel, not by size, as some of the smaller states would be harder to see. The channel we chose was saturation, with states with more colonies being more saturated in color.

* For the line graph visualization: Marks were the circles representing years while channels included 

***

## Story

***

## Contributions
* Jordyn Vu
  * Coded the map visualization
  * Wrote the design rationale
  * Estimated time contribution: 1.5 hours
* Julie Jeong
  * Coded the line graph visualization
  * Wrote the data description
  * Estimated time contribution: 1.5 hours
* Joanna Zhang
  * Planned and sketched the visualizations to be coded
  * Wrote the story, summarizing the project
  * Estimated time contribution: 1.5 hours