---
title:  "Metadata - (contiguous) OGS Surficial Geology"
author: "ormgpmm"
date:   "20230324"
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

## Surficial Geology, complete ORMGP coverage 2023

### Description 

The [Ontario Geological Survey](https://www.ontario.ca/page/ontario-geological-survey) (OGS) [Surficial geology of southern Ontario](https://data.ontario.ca/dataset/surficial-geology-of-southern-ontario) surface has been expanded and infilled in the few regions where the original layer remains incomplete. The process was necessary to obtain a contiguous surface covering the greater ORMGP jurisdiction.

* **Type**
    + Raster - Gridded on 15m cells.
* **Geographic Extent**
    + The extended ORMGP Study Area covering the Niagara peninsula to the Bay of Quinty.
* **Maintenance Standard**
    + Periodically updated in coordination with OGS updates.

### Georeferencing and Accuracy

* **Horizontal Datum**
    + North American Datum 1983
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
    + Oak Ridges Moraine Ground Water Program (2023) Surficial Geology
* **Agency Originator**
    + Oak Ridges Moraine Groundwater Program (ORMGP)
* **Agency Distributor**
    + Oak Ridges Moraine Groundwater Program (ORMGP)

### Methodology

* **Data Source - Surficial geology of southern Ontario**
    + See source [**metadata**](https://www.geologyontario.mndm.gov.on.ca/mndmfiles/pub/data/imaging/MRD128-REV//MRD128-REV_metadata.pdf?).
* **Data Source - Agricultural Resource Inventory - Final**
    + See source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/cf961d62ee1345c7b191808c9d60a4d7/info/metadata/metadata.xml?format=default&output=html).

* **Vector Overlay**
    + Vector overlay methodology of CAMC (2009) is applied as follows.

    + Agricultural soils map with OGS surficial geology map for the areas under investigation using `AND` operations (this keeps the attributes from both datasets).  (Note that for the OGS surficial map, bedrock areas (both Paleozoic and Precambrian) have been removed.) The field of interest in the OGS surficial geology is the 'group_number'; this has assembled the surficial types into standard numerical categories (e.g. 'bedrock drift complex', 'till', 'ice contact stratified deposits' and etc.).
     
    + For all the 'group numbers' (i.e. the geologic types) present in the resulting layer, add a presence/absence field (e.g. 'till', 'glacfluv', etc.).  These are then populated appropriately (a '1' value for the particular geologic type, a '0' for the remainder).

    + A logistic regression analysis is then performed using all the input presence/absence fields (the attributes) as well as the slope, stoniness, thinness ratio and fractal dimension index against the presence/absence geologic group fields. This results in a set of coefficients (one set foreach geologic type) relating the input variables to the particular geologic type. These coefficients can then be used to calculate the probability of a particular record (a spatial object) belonging to a particular geologic type.  Once the probabilities are calculated, the geologic type with the highest probability is assigned to the record.

    + The removed types (e.g. 'organic' and 'modern alluvial') are reincorporated.

    + The OGS surficial geology layer for the region is used to fill in the remainder of the empty areas.

    + Additional processing notes:

        + Removal of all 'rockland' (and related) polygons.

        + Removal of all 'water' polygons.

        + Removal of all 'bottom land' polygons (these become 'modern alluvial').

        + Removal of all 'marsh', 'bog' and etc ... (these become 'organic').

        + Removal of all polygons without attributes in: CLI_1; DRAINAGE1; HYDRO1; or TEXTURE1.

        + Addition of fields to convert categorical fields (i.e. CLI_1, DRAINAGE1, ...) to presence/absence fields.  For example:

        + HYDRO1 becomes - HY_A, HY_B, HY_C and HY_D

        + DRAINAGE1 becomes - DR_VR, DR_R, DR_W, DR_MW, DR_I, DR_P and DR_VP

        + Conversion of value in each of the categorical fields to the comparable presence/absence field.

        + In addition to these fields, STONINESS1 and SLOPE1 is also used as part of the analysis.

        + Calculation of 'thinness ratio' and 'fractal dimension index' (both based upon the polygon area and perimeter) as additional parameters.

* **Rasterization**
    + Each of the input datasets (i.e. OGS zone 17, OGS zone 18, and the vector overlay product) were re-projected and rasterized at a 15m resolution.

* **References**
    + Conservation Authorities Moraine Coalition (CAMC), 2009. Trent Source Water Protection Study, Recharge Study-Draft Report. 33pp.

    + Ontario Geological Survey 2010. Surficial geology of southern Ontario; Ontario Geological Survey, Miscellaneous Release— Data 128 – Revised.

    + Ontario Ministry of Agriculture, Food and Rural Affairs. 2022. Agricultural Resource Inventory - Final.

* **Contact**
    + email (support@owrc.ca)



<br>

*Last Modified: 2024-03-24*
