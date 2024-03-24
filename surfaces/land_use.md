---
title:  "Metadata - (contiguous) Land Use"
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

## Land Use, complete ORMGP coverage 2023

### Description 

The [Southern Ontario Land Resource Information System (SOLRIS) version 3.0](https://geohub.lio.gov.on.ca/documents/0279f65b82314121b5b5ec93d76bc6ba/about) surface has been expanded and infilled in the northern regions where the original layer remains incomplete. The process was necessary to obtain a contiguous surface covering the greater ORMGP jurisdiction.

* **Type**
    + Raster - Gridded on 15m cells.
* **Geographic Extent**
    + The extended ORMGP Study Area covering the Niagara peninsula to the Bay of Quinty.
* **Maintenance Standard**
    + Periodically updated in coordination with SOLRIS updates.

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
    + Oak Ridges Moraine Ground Water Program (2023) Land Use
* **Agency Originator**
    + Oak Ridges Moraine Groundwater Program (ORMGP)
* **Agency Distributor**
    + Oak Ridges Moraine Groundwater Program (ORMGP)

### Methodology

* **Data Source - Southern Ontario Land Resource Information System (SOLRIS) 3.0**
    + See source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/0279f65b82314121b5b5ec93d76bc6ba/info/metadata/metadata.xml?format=default&output=html).
* **Data Source - Ontario Road Network (ORN) Road Net Element**
    + See Source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/2fd52bccdb77479da0133c86545503f8/info/metadata/metadata.xml?format=default&output=html)
* **Data Source - Wetlands (Ontario GeoHub)**
    + See Source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/5216a770ef684d2fae8bcc13ee9c4357/info/metadata/metadata.xml?format=default&output=html)
* **Data Source - Ontario Hydro Network (OHN) - Waterbody**
    + See Source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/22bab3c9f37a4dd0845eb89e7b247a9f/info/metadata/metadata.xml?format=default&output=html)    

* **Vector Overlay**
    + Vector overlay of roads, wetlands and water bodies, areas outside of the SOLRIS data bounds (typically up on the Canadian Shield) are filled in with the appropriate SOLRIS land use class index (201, 150, 170, respectively–MNRF, 2019).

    + All remaining area not covered by SOLRIS is assumed Forest (SOLRIS land use class index 90), as visually observed from satellite imagery and air photos.

* **Rasterization**
    + Each of the input datasets (i.e. SOLRIS, ORN, OHN waterbody and wetlands) were re-projected and rasterized at a 15m resolution.

* **References**
    + Ministry of Natural Resources and Forestry, 2019. Southern Ontario Land Resource Information System (SOLRIS) Version 3.0: Data Specifications. Science and Research Branch, April 2019.

* **Contact**
    + email (support@owrc.ca)



<br>

*Last Modified: 2024-03-24*
