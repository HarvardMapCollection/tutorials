# How to add vector data to QGIS

A predominant spatial data format is the **shapefile**. This is a format created for storing vector data.

Vector data consists of:
- points (e.g. landmarks)
- lines (e.g. roads, rivers)
- polygons (e.g. towns, bodies of water)

![Image showing an example of points, lines and polygons](media/1.jpeg)

Since the advent of geospatial technology, **shapefiles** have been the most common format for storing vector information. Today, other file formats exist for storing vector information, such as the **geopackage (.gpkg)**, or **geoJSON (.geoJSON)**, but shapefiles are still widely used, and many of the datasets you will encounter will come in this format.

## Adding vector data to QGIS

1. Open QGIS. You can [download the free program here](https://harvardmapcollection.github.io/tutorials/qgis/download/).

2. In QGIS, open a `New empty project`.


3. From your computer file directory,  drag the vector data file (shapefile, geojson, geopackage) into the map browser. If your data is in shapefile format, drag the file that ends in the `.shp` extension. 
> You can click through any warning messages about the data projection at this point.
![Screen recording of dragging the file into the QGIS program](media/1.gif)
 

### Menu add
If the quick add approach is not cooperating, you can add data through the menu add.

1. In the menu, select `Layer → Add Layer → Add Vector Layer`.

2. Under `Source → Vector Dataset(s)` click the browse ellipses.

3. Navigate to the file you want to add. If it is a shapefile, select the file with the `.shp` extension.

4. Select `Open`.

5. Select `Close`.