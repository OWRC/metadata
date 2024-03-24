---
title:  "Metadata - 10km² sub-watersheds"
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

## ORMGP Topological Sub-Watersheds

### Description 

The [Provincial Digital Elevation Model (PDEM)](https://geohub.lio.gov.on.ca/maps/mnrf::provincial-digital-elevation-model-pdem/about) offered by the Ontario Ministry of Natural Resources and Forestry has been up-scaled and conditioned to acquire continuous flow paths. This product has been used to delineate 4,238 ~10km² sub-watersheds covering the extended ORMGP jurisdiction (~40,000km²). These sub-watershed are topologically correct, meaning that every sub-watershed is defined by its upstream and downstream neighbouring sub-watersheds. 


* **Type**
    + Vector - Polygon shapefile.
* **Geographic Extent**
    + The extended ORMGP Study Area covering the Niagara peninsula to the Bay of Quinty.
* **Maintenance Standard**
    + Periodically updated in coordination with [HDEM](/metadata/surfaces/hdem.html) updates.

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
    + Oak Ridges Moraine Ground Water Program (2023) Sub-Watersheds.
* **Agency Originator**
    + Oak Ridges Moraine Groundwater Program (ORMGP)
* **Agency Distributor**
    + Oak Ridges Moraine Groundwater Program (ORMGP)


### Methodology

* **Data Source - Hydrologically Conditioned Digital Elevation Model (HDEM)**
    + See source [**metadata**](/metadata/surfaces/hdem.html). 
* **Data Source - Ontario Hydro Network (OHN) - Waterbody**
    + See Source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/22bab3c9f37a4dd0845eb89e7b247a9f/info/metadata/metadata.xml?format=default&output=html) 
    
* **Vector Processing**
    + All waterbodies greater than 9km² are defined as sub-watersheds.

    + A hill-climbing algorithm is applied to the HDEM from all "outlet" points until an area close to 10km² is covered. the process repeats until the entire HDEM is covered.


* **Replaces or Updates**
    + Oak Ridges Moraine Groundwater Program (v2020) sub-watershed layer.


* **Contact**
    + email (support@owrc.ca)



<br>

*Last Modified: 2024-03-24*
