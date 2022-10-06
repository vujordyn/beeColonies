# beeColonies

## Data Description

* We got our data from [Kaggle](https://www.kaggle.com/datasets/jessicali9530/honey-production?resource=download). It has the following columns: state, numcol, yieldpercol, totalprod, stocks, priceperlb,prodvalue, year. For both visualizations, we wanted to show the trends in number of bee colonies across the United States over time. Therefore, we decided to use the variables state, numcol (number of honey producing colonies), and year.

* For visualization 1, we created a simplified version of the U.S. map with each state being represented as hexagons. To create this map, we used data from [Carto](https://team.carto.com/u/andrew/tables/andrew.us_states_hexgrid/public/map) and got the coordinates of each state hexagon. From our honey production dataset, we chose to show the maps for 2 distinct years 1998 and 2012, thus we filtered the data by year and created two subsets.

* For visualization 2, we created a line graph of the number of colonies in NY over time from 1998 to 2012. In order to create a subset that only contains data points for NY, we filtered the data by using const numColNY = data.filter(d => d.state=="NY")for. Also, to represent the years without the comma separating (e.g. 1,998), we used a time parser to format it nicely.

***

## Design Overview

### For the map visualization: 
- To show change over time, we made two different maps following the same procedures.
- Marks were the hexagons representing states, which we made all the same size because we wanted them to only vary by our saturation channel, not by size, as some of the smaller states would be harder to see in that case. A trade-off of the hexagon mark was that it displaced the states into odd positions, despite us using coordinates from a geoJSON file, making it potentially confusing for a viewer used to the traditional representation of the United States on a map. The way we addressed this was by labeling states by their acronyms.
- The channel we chose was saturation, with states with less colonies (taken from the numcol column in our honeyproduction.csv file) being less saturated in color (pale yellow) and states with more colonies being more saturated (brown). States with no data were colored a neutral gray. We chose six different colors for the scale. A benefit of choosing six colors for the scale is that it would not overwhelm the viewer, while a flaw is that it failed to differentiate between states with large gaps in colonies. More specifically, the range for the densest group was 359,000 while the range for the less dense groups was less than 50,000. This is largely due to some outlier states having a large number of colonies.

### For the line graph visualization:
- Marks were the circles representing years while channels included horizontal aligned position and vertical aligned position. We chose to make a line graph so the viewer could follow along the line to see how the number of bee colonies declined from 1998 to 2012, though there was an increase from 2001 to 2003. We curved the line to make the viewing experience more fluid.

***

## Story

***

## Contributions
### Collaboration
Coded the map visualization (2.5 hours):

- Jordyn Vu
- Julie Jeong
- Joanna Zhang
  
Coded the line graph visualization (1 hour):

- Jordyn Vu
- Julie Jeong

### Individual
- Jordyn Vu
  - Wrote the design rationale (20 minutes)
- Julie Jeong
  - Wrote the data description (20 minutes)
- Joanna Zhang
  - Planned and sketched the visualizations to be coded (20 minutes)
  - Wrote the story; researching and summarizing the project topic (45 minutes)
