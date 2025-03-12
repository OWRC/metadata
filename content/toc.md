---
title:  Metadata
author: Oak Ridges Moraine Groundwater Program
date:   2025-03-12
output: html_document
knit:   (
            function(input_file, encoding) {
                out_dir <- '';
                rmarkdown::render(
                    input_file,
                    encoding=encoding,
                    output_file=file.path(dirname(input_file), out_dir,
                    'toc.html')
                )
            }
        )
---



## Surfaces


- **[Hydrologically Conditioned DEM - Metadata](/metadata/surfaces/hdem.html)**

- **[Land Use _(full coverage)_ - Metadata](/metadata/surfaces/land_use.html)**

- **[Potential Discharge Areas - Metadata](/metadata/surfaces/potential_discharge.html)**

- **[Potentiometric Surface - Metadata](/metadata/surfaces/potentiometric_surface.html)**

- **[Surficial Geology _(full coverage)_ - Metadata](/metadata/surfaces/surficial_geology.html)**

- **[Topologically Conditioned Sub-watersheds - Metadata](/metadata/surfaces/topo_sws.html)**

- **[Topologically Conditioned Watercourses - Metadata](/metadata/surfaces/topo_watercourse.html)**

- **[Water Table - Metadata](/metadata/surfaces/water_table.html)**


<br>

<hr>

## External Sources

> The following layers were __*not*__ produced by the ORMGP, rather they are listed here for quick reference.

### OMNR 2006 DEM

[Metadata](/metadata/external/mnr2006dem/LIO%20MNR%20DEM%2010m%20Metadata.pdf)

### Ontario Provincial DEM

[Metadata](/metadata/external/pdem/)

### Ontario Geologic Survey

[Map legend](/metadata/external/ogs/surficial_geology_legend_p26.pdf)

### Provincial LiDAR--High-resolution DEM:

#### Sources

[South Central Ontario Orthophotography Project (SCOOP) 2013](https://geohub.lio.gov.on.ca/maps/ae8a9eb02559437b99e2ada0f276c54d/about) -- [Metadata](/metadata/external/LiDAR/SCOOP/)

[Digital Raster Acquisition Project Eastern Ontario (DRAPE) 2014](https://geohub.lio.gov.on.ca/datasets/lio::digital-raster-acquisition-project-eastern-ontario-drape-2014-1km-index/about) -- [Metadata](/metadata/external/LiDAR/DRAPE/)

#### Layers used

- OMAFRA Lidar DTM 2016-2018 (Peterborough 2016, A to I)
- Eastern Ontario DTM (2021-2022), West
- Belleville DTM (2022), A to V
- Kawartha Lakes DTM (2023), 01 to 09
- OMAFRA Lidar 2016-2018 (Lake Erie 2017), V to X
- Hamilton-Niagara DTM (2021), A to K
- DEDSFM Huron-Georgian Bay (2023), East
- GTA2014-2018 (Halton 2018), A to D
- GTA2014-2018 (Milton 2017), A
- GTA2014-2018 (Peel 2016), A and B
- GTA2014-2018 (Brampton 2015), A
- GTA2014-2018 (GTA 2015), A
- GTA2014-2018 (GTA 2015), B to F
- GTA2014-2018 (GTA 2014), A to D
- CLOCA (2018), A
- OMAFRA Lidar 2019 (York-LakeSimcoe), A to C
- OMAFRA Lidar 2022 (LakeSimcoe), A to C
- Muskoka 2018-2021 (2021-CGVD2013-DTM)
- Muskoka 2018-2021 (2023-CGVD2013-DTM-1)
- Muskoka 2018-2021 (2018-CGVD2013-DTM)
- Muskoka 2018-2021 (2023-CGVD2014-DTM-2)
- DRAPE (2014), B
- DRAPE (2014), A
- SCOOP (2013), H
- SCOOP (2013), G
- SCOOP (2013), F
- SCOOP (2013), E
- SCOOP (2013), D
- SCOOP (2013), C
- SCOOP (2013), B
- SCOOP (2013), A



<br>

*Last Modified: 2025-03-12*
