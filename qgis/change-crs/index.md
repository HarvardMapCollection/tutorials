# How to change a datasets CRS in QGIS

In order to use multiple datasets together for visualization and analysis, it is often important that each dataset is saved in the same coordinate reference system (CRS).

![Image of four human heads stretched in funny ways to mimic what commonly used projections do to flatten a round globe onto a flat surface](media/2.jpeg)

## Concepts

"Map projections try to portray the surface of the earth, or a portion of the earth, on a flat piece of paper or computer screen. In layman’s term, map projections try to transform the earth from its spherical shape (3D) to a planar shape (2D).

A coordinate reference system (CRS) then defines how the two-dimensional, projected map in your GIS relates to real places on the earth. The decision of which map projection and CRS to use depends on the regional extent of the area you want to work in, on the analysis you want to do, and often on the availability of data." - *[QGIS documentation](https://docs.qgis.org/3.16/en/docs/gentle_gis_introduction/coordinate_reference_systems.html)*


## Importance

Every mapmaker at one point or another has been frustrated by their data layers not lining up on the map, or map data appearing in the middle of the ocean instead of where it is supposed to be. This can almost always be chalked up to data being in the wrong CRS.

There are many resources available on [how to choose a map projection](http://www.geo.hunter.cuny.edu/~jochen/gtech201/lectures/lec6concepts/map%20coordinate%20systems/how%20to%20choose%20a%20projection.htm#:~:text=When%20you%20choose%20a%20projection,area%E2%80%94to%20achieve%20that%20purpose.).

In this tutorial, you will learn a straightforward, practical way to make sure all datasets are in the same CRS so you can get started mapping.

## How to change a dataset's CRS

1. Note the project's current CRS by checking the bottom right of the map document interface.
![Screenshot highlighting the project CRS in the bottom right of the map document in QGIS](media/1.png)

In the example data, the data layer was obtained from MassGIS, the open data portal for Massachusetts. The creators used CRS `NAD83 | Massachusetts Mainland`. The code for this CRS is `EPSG: 26986`. QGIS defaults the project CRS to that of the first dataset added to the map document.

2. In the bottom-right of the QGIS window, click the button that says `EPSG: some code`.

3. An interface will pop up prompting us to select the CRS for the whole project. Let's change the project CRS to `WGS 84`. Select `WGS 84 EPSG: 4326`. If you can't find it in the menu, you can search for it next to the `Filter` box.

4. Select `OK`.
> You'll notice your data may shape when you change the project CRS. If cartography is your primary concern, you should pick a projection that matches the location you are mapping. If you aren't sure, or want to ensure your data will work with all web mapping applications, you can default to `WGS 84 EPSG: 4326`.


