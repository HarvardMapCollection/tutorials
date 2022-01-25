# How to Join Data in QGIS

It is common for mappers to find information with a spatial component available in formats that are not yet optimized to work with mapping software. One such occurrence is spreadsheet data. In this tutorial you will learn how to join tables to GIS shapefiles to create a new, mappable dataset with both geographic boundaries and statistical information.

In this tutorial you will learn how to **join** tables to **GIS shapefiles** to create a new, mappable dataset with both geographic boundaries *and* statistical information.

## Background on joins

Why do we join?
- Without statistical data, GIS shapefiles are "empty" -- they include boundaries, but no statistical substance or phenomena to map
- Without GIS shapefiles, statistical data are just rows. GIS programs do not know how to display them geographically. 

Spreadsheet data:
- Is common
- Often represents occurrences that happened _somewhere_
- Cannot be automatically displayed on a map with no field for coordinates

So how do we make table data work with GIS software?
- GIS practitioners use a method called "joins" to make table data "spatial"
- All that's needed is a column for _where_ the row occurred, and an accompanying spatial data file at a corresponding geographic unit
    e.g. Each row of data has a column for the town where it happened, and you also download the [towns shapefile](https://www.arcgis.com/home/item.html?id=bf251288bf9b4c83b8dce00340e533b8)
- Joins are literal: the software matches values from the table's join column to the same values in the GIS dataset.