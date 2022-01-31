# How to clip GIS data

Clipping is a way of cropping GIS data to a certain extent. 

![Image of input, clip, and output data, illustrating a clip](media/1.png)
> From [ESRI documentation on clipping](https://desktop.arcgis.com/en/arcmap/10.3/tools/coverage-toolbox/clip.htm). 


## Why do we clip?
- Larger datasets are more unwieldy and difficult to work with.
- You can create more effective visualizations if your data is focused.

## Tutorial data

In this tutorial you will clip a shapefile of all census tracts in the United States to create a new shapefile of *only* census tracts in Cambridge, Massachusetts. 

#### United States Census tracts
This is the large dataset that needs to be *clipped*. 
- [Learn how to get](https://harvardmapcollection.github.io/tutorials/census/obtaining-census-data/)
- [Download](https://geodata.socialexplorer.com/collection/90937129-3414-434e-a880-e358308654b4) 
    - **Tip:** Select the 2019 option.

#### Boundary of Cambridge, MA
This is the the desired extent dataset used to *clip with*.
- [Learn how to get](https://harvardmapcollection.github.io/tutorials/qgis/export-selected/)
- [Download](https://raw.githubusercontent.com/HarvardMapCollection/tutorials/main/sample-data/cambridge.geojson)
    - **Tip:** Right-click anywhere on the screen and select `Save As`.


## Clip by attribute

Before we clip by geography, let's first extract only census tracts in the state of Massachsuetts. This will make our data much easier to work with, and will make the clipping processes run faster.

1. Open [QGIS](https://harvardmapcollection.github.io/tutorials/qgis/download/). 

2. Add the tracts file to QGIS. To learn how to add vector files to a desktop GIS program, follow [these steps](https://harvardmapcollection.github.io/tutorials/qgis/open-vector/). 

3. Open the dataset's attribute table by right-clicking the tracts layer in the layer list, and selecting `Open Attribute Table`.

> Filter the table to only show records that have a [state FIPS code](https://www.nrcs.usda.gov/wps/portal/nrcs/detail/?cid=nrcs143_013696) of 25, the Massachusetts state FIPS code. 

4. In the bottom-right hand corner click `Show All Features`. 

5. Select `Field Filter → STATEFP`.

6. In the search box to the right of `STATEFP` type in `25`. 

7. Press the `enter key`. It will take a long time to return results because there are so many records to search through. 

8. Highlight all of the records in the table by clicking to the left of a row to highlight it, then holding the shift key, and selecting the rest. 
> Any feature you have selected will appear yellow on the map to indicate it is highlighted. All of Massachusetts should be highlighted. 
![Select all function in QGIS attribute table](media/1.gif)