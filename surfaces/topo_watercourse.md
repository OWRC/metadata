---
title:  "Metadata - topological watercourse"
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

## ORMGP Topological Watercourses

### Description 

The [Ontario Hydro Network (OHN) - Watercourse](https://geohub.lio.gov.on.ca/datasets/mnrf::ontario-hydro-network-ohn-watercourse/about) layer offered by the Ontario Ministry of Natural Resources and Forestry has been analyzed based on a spatial analysis to define a connectivity network and a directional graph. Watercourse channel segments are topologically correct, meaning that every segments is defined by its upstream and downstream segments. 


* **Type**
    + Vector - Polyline shapefile.
* **Geographic Extent**
    + The extended ORMGP Study Area covering the Niagara peninsula to the Bay of Quinty.
* **Maintenance Standard**
    + Periodically updated in coordination with OHN updates.

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

* **Data Source - Ontario Hydro Network (OHN) - Watercourse**
    + See Source [**metadata**](https://www.arcgis.com/sharing/rest/content/items/a222f2996e7c454f9e8d028aa05995d3/info/metadata/metadata.xml?format=default&output=html) 
    
* **Vector Processing**
    + OHN watercourse layer is reprojected to EPGS 3161

    + Watercourses are *"segmentized"*: polylines are defined as single linear features from junction to junction.

    + Certain stream segments were manually removed in order to prevent "unnatural" flow connectivity. (This commonly occurs along man-made canal routes such as the Trent-Severn waterway.)

    + An adjacency matrix is built to collect segment endpoints that are close to one another. Adjacency is assumed to imply segment connectivity.

    + topological ordering is then performed, attributing segments with their appropriate Strahler (1952) code.


* **Replaces or Updates**
    + Oak Ridges Moraine Groundwater Program (v2020) sub-watershed layer.

* **References**
    + Strahler, A.N., 1952. Hypsometric (area-altitude) analysis of erosional topology, Geological Society of America Bulletin 63(11): 1117–1142.

* **Contact**
    + email (support@owrc.ca)



<br>

*Last Modified: 2024-03-24*
