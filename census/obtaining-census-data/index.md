# How to Obtain Census Data for GIS Mapping

Sometimes new mappers are tripped up by census data, because in order to make a map, you  need to download two separate census files:
1. A table of statistics
2. A geography boundary file

## Sources

In this lesson, you will learn how to get these files from your choice of the following sources.

### Social Explorer

- User-friendly
- Requires a license
- [Access Social Explorer via Harvard Key](http://nrs.harvard.edu/urn-3:hul.eresource:socialex)

### NHGIS.org
- Somewhat less intuitive
- No license required
- [Access NHGIS.org for free](nhgis.org)

Either choice will provide you with census data well-tailored for GIS methods. We recommend using one of these sources for digital mapping, as opposed to downloading directly from The U.S. Census Bureau portal.


## Example data 
- We will be exploring `tenure` data, which looks at owner vs. renter-occupied units.
- We want census responses that have been aggregated to the **census tract** level.
- Our area of study is near the Harvard campus, in Somerville and Cambridge. 

> **Geography tip:** Census tracts are a popular aggregation unit, as they are more granular than county or state level data, but more available and statistically-reliable than block level data. 

The steps in this tutorial series will work for any U.S. census data, such as age, race, income, etc.

![Screenshot of final map, showing renter occupied units in Somerville and Cambridge](media/1.png)
_Example of the tenure data we will work with, uploaded to ArcGIS Online._

## Do I need data?
Sometimes, you don't need to download census data in order to make use of it for your research. Many tools, like [Social Explorer](http://nrs.harvard.edu/urn-3:hul.eresource:socialex), allow you to visualize the data directly in the browser, and even export rendered maps.

To help decide if you need to budget time for learning how to download and manipulate geospatial data, check out our [How to Decide If I Need Geospatial Data](https://harvardmapcollection.github.io/tutorials/census/do-i-need-data/) guide.

## Obtaining via Social Explorer

## Obtaining via NHGIS.org

1. Visit NHGIS.org.

2. Select `Get Data`.
![Screenshot of Get Data button on NHGIS.org](media/2.png)

3. Select `Topics`. 
![Screenshot of Topics facet on NHGIS.org](media/3.png)

4. Select `Housing`.
![Screenshot of Housing topic facet on NHGIS.org](media/4.png)

5. Check off `Tenure and Mortgage Status`.
![Screenshot of Tenure and Mortgage Status topic checked off on NHGIS.org](media/5.png)

6. Finalize your topics selection by choosing the `Submit` button.
![Screenshot of Submit button on NHGIS.org](media/6.png)

7. Under `Source Tables`, check off the **Tenure** data table. This add the table to our shopping cart.
![Screenshot of checked-off tenure table on NHGIS.org](media/7.png)

8. To find the census tract files, select `Geographic Levels`.
![Screenshot of Geographic Levels facet on NHGIS.org](media/8.png)




