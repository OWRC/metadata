---
title:  "Metadata - Potentiometric Surface (Deep)"
author: "ormgpmd"
date:   "20220331"
output: html_document
knit:   (
            function(input_file, encoding) {
                out_dir <- '';
                rmarkdown::render(
                    input_file,
                    encoding=encoding,
                    output_file=file.path(dirname(input_file), out_dir,
                    'potentiometric_surface.html')
                )
            }
        )
---

## Potentiometric Surface (Deep; PS0) - August 2021

### Description 

The Potentiometric Surface reflects the elevation (in metres-above-sea-level,
masl) of the water level found in the *deep* aquifer system.  This has been
represented by a likely minimu depth value applied across the entire ORMGP
study area (rather than based on an individual formation/aquifer system).  This is
referenced as PS0.

* **Type**
    + Raster - Gridded on 100m cells.  A 50m cell working resolution was chosen with the final result resampled to a 100m cell final grid.
* **Geographic Extent**
    + Entire ORMGP Study Area (with a 25km buffer).
* **Maintenance Standard**
    + Periodically updated as new wells are added into the ORMGP database.

### Georeferencing and Accuracy

* **Horizontal Datum**
    + North American Datum 1983
* **Vertical Reference**
    + Well elevations set to MNR DEM (2006 Version 2, 10m cell resolution) based on *Accuracy*, below
* **Horizontal Accuracy**
    + Based on accuracy of well locations - refer to ORMGP Database Manual

### Data Sources and Restrictions

* **Use Constraint**
    + None - in accordance with ORMGP disclaimer
* **Citation**
    + Oak Ridges Moraine Ground Water Program (2021) Potentiometric Surface (Deep)
* **Agency Originator**
    + Oak Ridges Moraine Groundwater Program (ORMGP)
* **Agency Distributor**
    + Oak Ridges Moraine Groundwater Program (ORMGP)

### Methodology

* **Data Source - Wells**
    + The Potentiometric Surface (PS0) was created by
    interpolating the static water levels from all wells (ORMGP database, as of
    20210615) where the top-of-screen (in the well) is greater-than or
    equal-to 40 m deep. It should be noted that the measured static water
    levels reflect measurements from wells that were drilled in all seasons as
    well as in wetter and dryer years. So the surface presented here can only
    be considered an average. For wells with more than one measurement all water levels are averaged.  Given the dynamic nature of the groundwater system, it should be noted that the actual water table at any given time of year may be on the order of up to 2 or 3 metres higher or lower than reflected in the map.
* **Rasterization**
    + The input dataset (i.e. shallow groundwater levels) were rasterized at a 50m resolution and averaged.
* **Interpolation - Water Table**
    + Interpolated in Surfer using Kriging (with the 'auto' model setting, i.e. 64 point search).
* **Depth Correction**
    + The initial Potentiometric Surface was 'corrected' to a depth of 0.5m
    below the DEM (i.e. DEM-0.5) in all areas with negative depth values (i.e.
    the uncorrected surface exceeds the DEM).
* **Source/Citations**
    + The database of wells in the ORMGP includes all of the MOECC water well records as well as additional geotechnical/hydrogeological wells that have been entered into the database from other sources (consultant reports, Ontario Geological Survey, consultant databases, partner agency staff, etc.). Water levels are measured at nearly all wells at the time of drilling.  The recorded static water level may or may not effectively reflect the water table position, depending upon when it was measured. Usually upon completion of drilling the well is pumped to estimate well capacity - sometimes insufficient time has passed to record a 'true' static water level (i.e. the well has fully recovered after pumping).
    + Refer also to 'Oak Ridges Moraine Groundwater Program (2021)' for other
    details.
* **Replaces or Updates**
    + Oak Ridges Moraine Groundwater Program (2018) Potentiometric Surface (Deep).
* **Significant Changes**
    + Wells incorporated in the ORMGP database since the previous version of this dataset have been included within the interpolation process.
* **Contact**
    + Mike Doughty (mdoughty@owrc.ca)



*Last Modified: 2022-03-31*
