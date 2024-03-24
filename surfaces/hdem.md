---
title:  "Metadata - Hydrologically Conditioned DEM"
author: "ormgpmm"
date:   "20240324"
output: html_document
knit:   (
            function(input_file, encoding) {
                out_dir <- '';
                rmarkdown::render(
                    input_file,
                    encoding=encoding,
                    output_file=file.path(dirname(input_file), out_dir,
                    'water_table.html')
                )
            }
        )
---

## Hydrologically Conditioned Digital Elevation Model (HDEM)

### Description 

The [Provincial Digital Elevation Model (PDEM)](https://geohub.lio.gov.on.ca/maps/mnrf::provincial-digital-elevation-model-pdem/about) offered by the Ontario Ministry of Natural Resources and Forestry has been up-scaled and conditioned to acquire continuous flow paths. This product is necessary for catchment delineation to any point within the extended ORMGP boundary.

* **Type**
    + Raster - Gridded on 60m cells.
* **Geographic Extent**
    + The extended ORMGP Study Area covering the Niagara peninsula to the Bay of Quinty.
* **Maintenance Standard**
    + Periodically updated in coordination with PDEM updates and by noted flowpath discrepancies discovered by our user base (see *Manual Adjustments* below).

### Georeferencing and Accuracy

* **Horizontal Datum**
    + North American Datum 1983
* **Vertical Datum**
    + CGVD2013 (EPSG 6647)
* **Ellipsoid**
    + GRS 1980
* **Prime meridian**
    + Greenwich
* **Projection**
    + Ontario MNR Lambert (EPSG 3161)
* **Horizontal Accuracy**
    + 1.5m
* **Unit**
    + metre
* **Information source**
    + Ontario Ministry of Natural Resources via Conservation Ontario.


### Data Sources and Restrictions

* **Use Constraint**
    + None - in accordance with ORMGP disclaimer
* **Citation**
    + Oak Ridges Moraine Ground Water Program (2023) Hydro-DEM.
* **Agency Originator**
    + Oak Ridges Moraine Groundwater Program (ORMGP)
* **Agency Distributor**
    + Oak Ridges Moraine Groundwater Program (ORMGP)


### Methodology

* **Data Source - Provincial Digital Elevation Model (PDEM)**
    + See source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/882a9059ec7c4881abbdb6afa0ae73e6/info/metadata/metadata.xml?format=default&output=html). 

* **Raster Upscaling**
    + PDEM is upscaled from a 30m horizontal resolution to 60m by taking the mean of the 4 intersecting cells. 

* **Raster Processing**
    + Automated depression filling (Wang and Liu, 2006) was applied to the DEM.

    + Flat regions were adjusted according to the depression filling fix of Garbrecht and Martz (1997).

    + Flow paths are computed based on the "D8" algorithm (O'Callaghan and Mark, 1984).

* **Manual Adjustments**

    + Flow directions are imposed using hand-drawn flow paths where the algorithm fails to discover the true flow direction. Flow paths are save as polyline shapefiles, where its vertices are ordered according to flow direction.


* **Derivative Products**

    + Cell slopes and slope-aspects are computed using a 9-point planar regression from every cell's elevation plus its 8 neighbouring grid elevations.


* **Replaces or Updates**
    + Oak Ridges Moraine Groundwater Program (v2020) HDEM.

* **References**
    + Garbrecht, J, and L. Martz, 1997. The assignment of drainage direction over flat surfaces in raster digital elevation models. Journal of Hydrology, 193, 204-213.

    + O'Callaghan, J.F., and D.M. Mark, 1984. The extraction of drainage net-works from digital elevation data, Comput. Vision Graphics Image Process., 28, pp. 328-344

    + Wang, L., H. Liu, 2006. An efficient method for identifying and filling surface depressions in digital elevation models for hydrologic analysis and modelling. International Journal of Geographical Information Science 20(2): 193-213.

* **Contact**
    + email (support@owrc.ca)



<br>

*Last Modified: 2024-03-24*
