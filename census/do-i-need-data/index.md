# How to Decide If I Need Geospatial Data

Deciding whether you need to download and process geospatial data is a good first step for your mapping project.

There are many online visualization tools and streaming data services that allow you to explore popular GIS datasets, and even export rendered maps without having to download data.

To download and process data requires additional time and skill-building. Planning in advance whether you should budget this time and knowledge acquisition into your project will help you get more mileage out of what you can accomplish.

![An example of a .PNG map export from Social Explorer showing people age 18-34 by tract in Somerville and Cambridge](media/map.png).

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
_Map created from the [PointsUnknown tutorial series](https://pointsunknown.nyc/tutorial_list/), a great way to get started learning how to make maps._




#### Data download reason #1: Editing the data tables

In this map, the census variable represented, is actually a combination of _two_ census variables. This combination was accomplished by adding two fields together in a program like Excel, Google Sheets, or LibreOffice Calc.

The cartographer is trying to make a point about people who have difficulty getting to train stops more than ten minutes away, as well as those who require features such as elevators. Therefore, they combined two demographic factors: `population with abulatory difficulties` _and_ `population under age 5`.

They probably could have used a tool like Social Explorer to get an inital sense of where the most people with ambulatory difficulties, or people under age 5 live, before they dove into their mapping project, but if they wanted to export maps from this tool, they would have had to do each variable separately.

![Social Explorer map of ambulatory difficulty](media/3.png)
_Social Explorer map showing ambulatory difficulty for census tracts in NYC._

![Social Explorer map of under age 5](media/2.png)
_Social Explorer map showing population under age 5 for census tracts in NYC._

#### Data download reason #2: Performing analysis

One of the goals for this map is to show places where large pockets of mobility-impaired citizens live further than a ten-minute walking distance from any train station. Accomplishing this required using both census datasets together with desktop mapping software analysis tools, in order to create the distance buffers. 


#### Data download reason #3: Custom styling the map

Finally, this cartographer did some custom styling, which allowed them to communicate their points, or story more effectively than they could have with boilerplate exports from a tool like Social Explorer.

If you'd like to learn how to make the map in this example, you can follow [this map making tutorial](https://pointsunknown.nyc/qgis/2021/04/16/04A_Spatial_Analysis.html) from PointsUnknown. 







