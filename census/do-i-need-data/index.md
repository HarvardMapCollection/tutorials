# How to Decide If I Need Geospatial Data

Deciding whether you need to download and process geospatial data is a good first step for your mapping project.

There are many online visualization tools and streaming data services that allow you to explore popular GIS datasets, and even export rendered maps without having to download data.

To download and process data requires additional time and skill-building. Knowing ahead of time whether you should budget this time and knowledge acquisition into your project is useful.

## Cheat sheet

### Times when explore tools will probably do the trick
- You want to get a better sense of the data, without the time spent creating your own visualization
- You want to create a simple map displaying the data with no customization, comparison with other datasets, or analysis
- A good tool exists for the data you are studying, like in the case of [Social Explorer tool](http://nrs.harvard.edu/urn-3:hul.eresource:socialex) for US census data

![An example of a .PNG map export from Social Explorer showing people age 18-34 by tract in Somerville and Cambridge](media/map.png)

![An example of the map legend which is exported from social explorer from the previous map](media/legend.png)
_Example of a rendered map exported from Social Explorer, showing percent of people aged 18-34 in Somerville and Cambridge_

### Times when you will probably need to download and process geospatial data

- You want your visualization to be more customized than what is available in the exploration tool. Some examples include:
    - editing the dataset's geography to lend focus to a specific place
    - styling the data in Adobe Illustrator to have more control over your map's look and feel 
- You need to perform some sort of math or analysis on the data "under the hood" prior to creating the visualization. Some examples include:
    - tallying or combining multiple fields 
    - overlaying and comparing with different datasets to understand the impact of a certain factor

### Example 

![Nice looking map of New York City showing sophisticated analysis and styling](media/1.png)
_Map created from the [PointsUnknown tutorial series](https://pointsunknown.nyc/qgis/2021/04/16/04A_Spatial_Analysis.html), a great way to get started learning how to make maps.

In the map above, the cartographer needed to download geospatial data for many reasons.

1. For the orange-colored census data, they want to show all people who require specific transit infrastructure, like elevators. This means they needed to _combine_ two census datasets, `population with abulatory difficulties` _and_ `population under age 5`

If they were using a tool like Social Explorer to make their maps, they would have to export maps of each dataset separately, which would look like this:

![Social Explorer map of ambulatory difficulty](media/2.png)
_Map showing ambulatory difficulty for census tracts in NYC._

![Social Explorer map of under age 5](media/3.png)
_Map showing population under age 5 for census tracts in NYC._

2. The second reason this cartographer needed to download the data, is because they needed to combine the population data with data about distances from train stations, in order to make the case for where more infrastructure services should be added.

3. Finally, this cartographer did some custom styling, to make the map appear more to their tastes, and to be able to communicate their argument, or story more effectively.

You can learn how to do each of these steps by following [the tutorial for creating this map](https://pointsunknown.nyc/qgis/2021/04/16/04A_Spatial_Analysis.html). 







