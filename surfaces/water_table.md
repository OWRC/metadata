---
title:  "Metadata - Water Table (WT0 and WT1)"
author: "ormgpmd"
date:   "20220330"
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

## Water Table Surface and Depth to Water Table, WT0 and WT1 - June/July 2021

#### Description

Characteristic       | Description
-------------------- | -----------
Summary | The Water Table surface reflects the elevation (in metres-above-sea-level, masl) of the saturated water table.  Two Surfaces are created: the Data Driven Water Table (WT0) and the Enhanced Water Table (WT1).  These surfaces can be used to estimate the direction and gradient of ground water flow in the shallow sediments/rock beneath any area.
Type | Raster - Gridded on 100m cells.  A 50m cell working resolution was chosen with the final result resampled to a 100m cell final grid
Geographic Extent | Entire ORMGP Study Area (with a 25km buffer).
Maintenance Standard | Periodically updated as new wells are added into the ORMGP database.
                    
#### Georeferencing and Accuracy

------------------ | -------------------
Horizontal Datum | North America Datum 1983
Vertical Reference | Well elevations set to MNR DEM (2006 Version 2, 10m cell resolution) based on *Accuracy*, below



