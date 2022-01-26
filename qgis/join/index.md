Under development! Coming soon!

# How to Join Data in QGIS

It is common for mappers to find information with a spatial component available in formats that are not yet optimized to work with mapping software. One such occurrence is working with spreadsheet data. 


In this tutorial you will learn how to **join** tables to **GIS shapefiles** to create a new, mappable dataset with both geographic boundaries *and* statistical information.

## Background on joins

Why do we join?
![Screenshot of ](media/1.png)
![Screenshot of ](media/2.png)
![Screenshot of ](media/3.png)
![Screenshot of ](media/4.png)



- Without statistical data, GIS shapefiles are "empty" -- GIS software knows how to display them visually on a map, but there is no statistical substance to them.
![Screenshot of the table behind a census tracts shapefile](media/1.png)
_Pictured above is the data table of a census tracts shapefile. There are fields for the name of the tract, size in area, but for this data to become **meaningful** and **mappable** we must connect it to some demographic data from the census._


- Without GIS shapefiles, statistical data are just rows and columns in a spreadsheet. GIS programs don't know how to interpret .xlsx or .csv files, unless they have fields for x,y coordinates. 

The reality is, most phenomena happen _somewhere_, and more often than not, tabular spreadsheets, even ones that lack addresses or coordinates, have _some_ value that can be used for mapping. Enter joins.

### Joins 101
- All that's needed to perform a join is a statistical file and a spatial file that share _one_ column between them
    - Often, this is the name of a place (town name), or a unique identification code.
    - e.g. Each row of data in the statistical file represents some occurrence, and has a column for the town where it happened. You would also download a [towns shapefile](https://www.arcgis.com/home/item.html?id=bf251288bf9b4c83b8dce00340e533b8), and join them both together to make spatial data. 
    > **Learning tip:** Explore the [Massachusetts towns shapefile](https://github.com/NewtonMAGIS/GISData/blob/master/Massachusetts%20Town%20Boundaries/MassTowns.geojson) and observe how the data table has no real meaningful information in it. It is just the boundaries of towns, a
- Joins are literal: the software matches values from the table's join column to the same values in the GIS dataset.