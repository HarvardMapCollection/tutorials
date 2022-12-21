# How to add a spreadsheet

This tutorial will cover how to add tabular data to a QGIS project.

> **Tip:** GIS software prefer tabular data to be in `.csv` format, rather than `.xlsx`. Before attempting to bring any spreadsheets into either QGIS or ArcGIS Pro, please be sure to [Save as .csv](https://support.microsoft.com/en-us/office/save-a-workbook-to-text-format-txt-or-csv-3e9a9d6c-70da-4255-aa28-fcacf1f081e6).

1. Open [QGIS](https://harvardmapcollection.github.io/tutorials/qgis/download/).

2. In the main QGIS menu (banner across the top of the computer screen), select `Layer → Add Layer → Add delimited text layer`.
![Screenshot of the add delimited text wizard in QGIS](media/1.png)

3. Under `File name` select the ellipses dots icon to navigate to the `.csv` you wish to import.

4. Pay attention to `Record and Field options`. You can start by accepting the defaults, but depending on the way your data is structured, you may want to make use of some of these settings.

5. 
- If your data does not have point coordinates (latitude and longitude) and you plan on making this data spatial by [performing a join](https://harvardmapcollection.github.io/tutorials/qgis/join/), under `Geometry definition` select `No Geometry (attribute only table)`. 
- If your data *does* have point coordinates, select `Point coordinates` and define which field in the spreadsheet is `X` (longitude), and which is `Y` (latitude).

6. Select `Add`.

7. Select `Close`.