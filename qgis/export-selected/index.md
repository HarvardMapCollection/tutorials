## How to export selected features in QGIS

Under development! Coming soon!

One helpful technique in GIS software is the ability to quickly create filtered subsets of an original data source. You may want a new dataset that only contains features of a certain type (e.g. only water bodies of a certain depth). Alternatively, you may want to select features based on their location.

In this tutorial, we will start with a dataset of all 351 towns in Massachusetts, and create a new dataset that only shows the boundary of Cambridge, MA. 


1. Download the example dataset by visiting [this page](https://github.com/HarvardMapCollection/tutorials/blob/main/sample-data/ma-towns.geojson) and clicking the `Download` button.
![Screenshot of download button on Github](media/1.png)

2. Add the downloaded vector polygon .geojson to a new QGIS project by following the steps in [this tutorial](https://harvardmapcollection.github.io/tutorials/qgis/open-vector/).

3. Open the dataset's underlying attribute table by right-clicking on the data layer in the layer list, and selecting 