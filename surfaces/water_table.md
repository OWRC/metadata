---
title:  "Metadata - Water Table (WT0 and WT1)"
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
                    'water_table.html')
                )
            }
        )
---

## Water Table Surface and Depth to Water Table, WT0 and WT1 - June/July 2021

### Description 

The Water Table surface reflects the elevation (in metres-above-sea-level, masl) of the saturated water table.  Two Surfaces are created: the Data Driven Water Table (WT0) and the Enhanced Water Table (WT1).  These surfaces can be used to estimate the direction and gradient of ground water flow in the shallow sediments/rock beneath any area.

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
    + Oak Ridges Moraine Ground Water Program (2021) Water Table
* **Agency Originator**
    + Oak Ridges Moraine Groundwater Program (ORMGP)
* **Agency Distributor**
    + Oak Ridges Moraine Groundwater Program (ORMGP)

### Methodology

* **Data Source - Wells**
    + The Water Table was created by contouring the static water levels from all wells (ORMGP database, as of 20210615) where the bottom of the well is less than 20 m deep. Wells up to 50 m deep were incorporated within the Oak Ridges Moraine boundary. It should be noted that the measured static water levels reflect measurements from wells that were drilled in all seasons as well as in wetter and dryer years. So the water table presented here is the average water table. For wells with more than one measurement all water levels are averaged.  Given the dynamic nature of the groundwater system, it should be noted that the actual water table at any given time of year may be on the order of up to 2 or 3 metres higher or lower than reflected in the map.  Note that the creation of the WT0 relies entirely upon this dataset (unless otherwise specified).  The WT1 incorporates all modifications described below.
* **Data Source - Water Bodies (Lakes)**
    + Each of Lake Ontario, Lake Simcoe and Georgian Bay were extracted from the 'Ontario Hydrographic Network - Water Bodies' dataset (20110623).  These were converted from polygons to points and assigned a standard elevation (Georgian Bay - 176 masl; Lake Simcoe - 219 masl; Lake Ontario - 74 masl).
* **Data Source - Rivers**
    + The river network was found in the 'Water Virtual Flow - Seamless Provincial Data Set, 2008'.  This dataset was divided into two sets based upon the river segment Strahler Code: one set comprised of Strahler Codes greater than 3; and the second set comprised of Strahler Codes of either 3 or 2.  Both sets were converted from polylines to points and tagged with elevations based upon the 'MNR DEM 10m v2' surface for the ORMGP study area.  Strahler Class The sampling distance for this dataset was approximately 500m (along-stream).  Points found within Georgian Bay, Lake Simcoe or Lake Ontario were removed (these would have been part of the original virtual flow network).  In addition, a borehole density layer was created to determine those areas under-serviced by borehole locations.  Where the density was below 3 boreholes with a 1km radius, no river network nodes were used.
* **Rasterization**
    + Each of the input datasets (i.e. shallow groundwater levels, water body shoreline points and river network points (Strahler Code > 3) were rasterized at a 50m resolution, then combined and averaged (for points falling within any particular raster cell).
* **Point Density (for areas above the Niagara Escarpment and north of the Canadian Shield**
    + Because the water table appeared to be quite deep in some areas to the north and above the escarpment a routine was run to see if additional stream points could assist to reasonably raise the water table. A point density surface was created using bins/grids of 1000, 2000 and 5000m. The 2000m grid density surface provided a balance between the loose (1000m) and tight (5000m) surfaces (i.e. large unsampled areas versus small unsampled areas). Areas west of the escarpment and north of the Canadian Shield were found to have a low density of points to reasonably reflect the water table surface.
* **River Network (Strahler codes 2 and 3; for areas above the Niagara Escarpment and north of the Canadian Shield)**
    + Based upon the vectorized 2000m density surface, additional river network points (Strahler Codes 3 and 2) were added and rasterized to 50m resolution.
* **Interpolation**
    + Interpolated in Surfer using Kriging (with the 'auto' model setting, i.e. 64 point search).
* **Depth Correction (to curb Water Table from being above the ground surface)**
    + To select a reasonable depth for Water Table 'correction', an examination of the distribution/count of values across the depth range of 0 to 0.5m was undertaken.  Given the fairly constant set of counts across the range, a 0.5m 'correction depth' was selected.  At a 50m resolution, the Water Table was 'corrected' to a depth of 0.5 m below the DEM (DEM-0.5) in all areas with a negative depth values (i.e. the uncorrected surface exceeds the DEM).  Both WT0 and WT1 use this step for creating the final surfaces.
* **Source/Citations**
    + The database of wells in the ORMGP includes all of the MOECC water well records as well as additional geotechnical/hydrogeological wells that have been entered into the database from other sources (consultant reports, Ontario Geological Survey, consultant databases, partner agency staff, etc.). Water levels are measured at nearly all wells at the time of drilling.  The recorded static water level may or may not effectively reflect the water table position, depending upon when it was measured. Usually upon completion of drilling the well is pumped to estimate well capacity - sometimes insufficient time has passed to record a 'true' static water level (i.e. the well has fully recovered after pumping).
* **Replaces or Updates**
    + Oak Ridges Moraine Groundwater Program (2019) Water Table.
* **Significant Changes**
    + Wells incorporated in the ORMGP database since the previous version of this dataset have been included within the interpolation process.
* **Contact**
    + Mike Doughty (mdoughty@owrc.ca)



*Last Modified: 2022-03-31*
