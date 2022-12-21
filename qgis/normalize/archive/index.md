# How to normalize data

"To normalize, in a statistical sense, is to transform a set of measurements so that they may be compared in a meaningful way. Technically, normalization involves factoring out the size of the domain when you wish to compare counts collected over unequal areas or populations. Normalization transforms measures of magnitude (counts or weights) into measures of intensity."
- [pcbgis.com](https://www.pbcgis.com/normalize/)

This tutorial will cover how to turn counts into percents in QGIS.

## Normalization sample data
Download the sample data, [tenure by census tract in Cambridge, MA](https://downgit.github.io/#/home?url=https://github.com/HarvardMapCollection/tutorials/blob/main/sample-data/cambridge-tenure-counts.geojson). 


## Normalization steps

1. Right click the tenure data layer in the layer list and select `Open Attribute Table`.

2. Scroll all the way to the right to find the three census variables we will be working with. Note their names, something along the lines of `tenure-2019_SE_A10060_001`, `tenure-2019_SE_A10060_002`, and `tenure-2019_SE_A10060_003`. From the [codebook which came along with the download](https://github.com/HarvardMapCollection/tutorials/blob/main/sample-data/tenure-2019-codebook.txt) we know that these fields are the total number of housing units, the *number* (or count) of owner-occupied units, and the number of renter-occupied units. We need to use these fields to create new *percent* fields.

3. Select the menu icon that looks like an abacus called `Open field calculator`.

4. Ensure `Create a new field` is checked **on**. 

5. Under `Output field name`, name the field `OwnerPct`.

6. Under `Output field type`, select `Decimal number (real)`.

7. In the expression box type `("tenure-2019_SE_A10060_002" / "tenure-2019_SE_A10060_001") * 100`.
> You will know your expression is valid if under the expression box there is an `Output preview` with a value that looks like a valid percentage.

8. Select `OK` and scroll to the right of the attribute table to ensure your new field has populated.

9. Repeat steps 3-8 for the renter occupied variable. 

10. **IMPORTANT!** Make sure to save your newly created columns by toggling the editing mode pencil icon in the attribute table menu.