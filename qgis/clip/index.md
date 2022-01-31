# How to clip GIS data

Clipping is a way of cropping GIS data to a certain extent. 

![Image of input, clip, and output data, illustrating a clip](media/1.png)
> From [ESRI documentation on clipping](https://desktop.arcgis.com/en/arcmap/10.3/tools/coverage-toolbox/clip.htm). 

There are two main reasons you might want to clip:
1. Larger datasets are more unwieldy and difficult to work with.
2. You can create more effective visualizations if your data is focused.

## Tutorial data

We are going to clip a shapefile of all census tracts in the United States to create a new shapefile of *only* census tracts in Cambridge, Massachusetts.

### Download the example data

Data to clip: **United States census tracts**
- Learn how to obtain with [this tutorial](https://harvardmapcollection.github.io/tutorials/census/obtaining-census-data/).
- Skip ahead by downloading at [this link](https://geodata.socialexplorer.com/collection/90937129-3414-434e-a880-e358308654b4). (Choose 2019).

Data to clip *by*: **Boundary of Cambridge, MA**
- Learn how to obtain with [this tutorial](https://harvardmapcollection.github.io/tutorials/qgis/export-selected/).
- Skip ahead by downloading at [this link](https://raw.githubusercontent.com/HarvardMapCollection/tutorials/main/sample-data/cambridge.geojson). (Right-click anywhere on the screen and select `Save As`.)