# How to Join Data in QGIS

It is common for mappers to find information with a spatial component available in formats that are not yet optimized to work with mapping software. One such occurrence is working with spreadsheet data. 


In this tutorial you will learn how to join **tables** to **GIS shapefiles** to create a new, mappable dataset with both geographic boundaries *and* statistical information.

## Why do we join?

Often, spreadsheets contain useful information we want to map. GIS software, however, does not know how to translate a spreadsheet without any *inherent spatial information* (such as point coordinates) into a visual map.

Take, for instance, [this spreadsheet](https://www.mass.gov/info-details/archive-of-covid-19-cases-in-massachusetts) of weekly COVID rates for each town in Massachusetts for the week of January 26, 2022. 

![Screenshot of Massachusetts COVID data in an Excel spreadsheet](media/2.png)

Despite the obvious role of geography in this data (the data is arranged by town), if we were to bring this spreadsheet into a GIS program, the program would not know (without being told by us) which column to interpret as the "geography" to display visually. The formats `.csv` or `.xlsx` are not inherently spatial data formats. 

On the other hand, take this Massachusetts municipalities dataset which we downloaded from the state government's open data portal and opened up in a desktop mapping software. The data comes available as a `shapefile`, which is an inherently geospatial format.

![Screenshot of a QGIS mapping project open with a map of Massachusetts towns](media/1.png)

Because this data is spatial, GIS software can recognize it, and automatically make a map out of it. 

The image above shows how mapping software *displays* GIS data, but what does the "data" actually look like? Let's look at the data's underlying `attribute table`.

![Screenshot of the town GIS data's underlying data table](media/5.png)

Here, we can see that for each row, which represents a single GIS `feature` (in this case, a town), there are some basic facts (each column) about that town. Included here are town name, town ID, population count, etc.

Besides this basic information and the geospatial polygon shapes of the towns, this dataset is not entirely useful for mapping, when it comes to showing any meaningful statistics.

 

Most of the time, the information we *want* to map, such as our example COVID rates, are not made available as shapefiles. They are created and distributed as spreadsheets, and in order to map them, we must join the spreadsheet together with GIS shapefile data using a GIS software like [QGIS](https://harvardmapcollection.github.io/tutorials/qgis/download/).


![Map of covid rates per town. Red for towns with higher rates than last week, yellow for lower, gray for no change.](media/4.png)
_Map of weekly Massachusetts COVID data spreadsheet from January 26, 2022, after being joined to a [Massachusetts municipalities shapefile](https://www.mass.gov/info-details/massgis-data-municipalities) from MassGIS._

## How do joins work?

In this tutorial, we will walk step-by-step through performing a join in QGIS. This tutorial is part of a series called the [census data to ArcGIS Online starter pack](https://harvardmapcollection.github.io/tutorials/census/census2agol/), but you can also use this guide separately to learn about joins.

Before we dive in to step-by-step instructions, however, let's go over the basic concept of **how joins work**.

To perform a join, you must have a column in each dataset which contains the same values.

For instance, when we joined the COVID spreadsheet to the Massachusetts municipalities shapefile, we used a column common to both datasets: `town name`.

## Tutorial data

>If you don't already have the tutorial data, you can either:
1. Follow the [census data to ArcGIS Online starter pack series](https://harvardmapcollection.github.io/tutorials/census/census2agol/) to obtain them.
2. Download them here
> **Tip:** Right-click anywhere on the screen and select `Save As`:
- [Census tracts in Cambridge, MA](https://raw.githubusercontent.com/HarvardMapCollection/tutorials/main/sample-data/cambridge-tracts.geojson).
- [Tenure statistics .CSV](https://raw.githubusercontent.com/HarvardMapCollection/tutorials/main/sample-data/tenure-2019.csv)
Refer to the tenure[codebook](https://github.com/HarvardMapCollection/tutorials/blob/main/sample-data/tenure-2019-codebook.txt) to make sense of the statistical files' structure.

## Tutorial steps

1. Add the census tract shapes data to the QGIS document by following [these steps](https://harvardmapcollection.github.io/tutorials/qgis/open-vector/)

2. Add the statistical tenure data to the map by following [these steps](https://harvardmapcollection.github.io/tutorials/qgis/add-csv/)

3. Right-click the tracts layer in the layer list and select `Properties`.

4. In the menu, select `Joins`.

5. In the bottom of the wizard interface, select the green plus sign `Add new join` icon.
![Screenshot of add a new join button in QGIS](media/6.png)

6. 


