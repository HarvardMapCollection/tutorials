# How to Decide If I Need Geospatial Data

Deciding whether you need to download and process geospatial data is a good first step for your mapping project.

There are many online visualization tools and streaming data services that allow you to explore popular GIS datasets, and even export rendered maps without having to download data.

To download and process data requires additional time and skill-building. Knowing ahead of time whether you should budget this time and knowledge acquisition into your project is useful.

![An example of a .PNG map export from Social Explorer showing people age 18-34 by tract in Somerville and Cambridge](media/map.png)

_Example of a map you can export from [Social Explorer](http://nrs.harvard.edu/urn-3:hul.eresource:socialex), a tool that lets you interactively explore census data. This map shows percent of people aged 18-34 in Somerville and Cambridge_


## Cheat sheet

| **Use explore tools**     | **Probably need data** |
| ----------- | ----------- |
| Good explore tools exist for my dataset  | No explore tools exist      |
| Get a sense of the data quickly     | Want to dive deeper into the data      |
| No analysis needed   | Need to do analysis, combine, or edit the data       |
| No comparison with other datasets needed  | Want to compare with other datasets       |
| No custom map design needed | Want to control look of final map output   |


### Case study

Now, we will look at an example of a map depicting census data, and go through some of the reasons why the cartographer needed to download and manipulate GIS census data, rather than using a tool like Social Explorer. The example map tells a story about people in New York City who have impaired mobility, and why there needs to be more robust transit infrastructure to serve them.

![Nice looking map of New York City showing sophisticated analysis and styling](media/1.png)
_Map created from the [PointsUnknown tutorial series](https://pointsunknown.nyc/qgis/2021/04/16/04A_Spatial_Analysis.html), a great way to get started learning how to make maps._




#### Data download reason #1: Editing the data tables

For the demographic data, which, in this map appears as the orange-red gradient, the cartographer wanted to show all people who might require specific transit infrastructure, such as elevators. This means they needed to _combine_ population statistics from two census tables and put them on one map: `population with abulatory difficulties` _and_ `population under age 5`.

If this cartographer had been using a tool like Social Explorer to generate their maps, rather than downloading and editing the datasets on their desktop, they would have had to export prerendered maps of each demographic separately, which would have looked like this:

![Social Explorer map of ambulatory difficulty](media/3.png)
_Map showing ambulatory difficulty for census tracts in NYC._

![Social Explorer map of under age 5](media/2.png)
_Map showing population under age 5 for census tracts in NYC._

By downloading the data tables, they were able to do some math in Excel to tally up the demographic statistics into one mappable column. 

#### Data download reason #2: Performing analysis


The second reason this cartographer needed to download the data, is because they wanted to make a point about places where there were large pockets of mobility-impaired citizens over a ten-minute walking distance from a train station. This required using both datasets together with analysis tools to create the distance buffers. 


#### Data download reason #3: Custom styling the map

Finally, this cartographer did some custom styling, which allowed them to communicate their argument, or story more effectively than the boilerplate exports from Social Explorer would have.

You can follow along [the tutorial for creating this map](https://pointsunknown.nyc/qgis/2021/04/16/04A_Spatial_Analysis.html) from PointsUnknown. 







