---
title:  Metadata - Groundwater Monitoring Locations
author: Oak Ridges Moraine Groundwater Program
date:   "20230324"
output: html_document
knit:   (
            function(input_file, encoding) {
                out_dir <- '';
                rmarkdown::render(
                    input_file,
                    encoding=encoding,
                    output_file=file.path(dirname(input_file), out_dir,
                    'monitoring_gw.html')
                )
            }
        )
---

## Groundwater Monitoring Locations - ORMGP Database

### Description

The Groundwater Monitoring Locations dataset is a GIS point layer representing groundwater monitoring locations hosted by the Oak Ridges Moraine Groundwater Program (ORMGP). The dataset includes monitoring wells, observation wells, boreholes, municipal monitoring wells, Provincial Groundwater Monitoring Network (PGMN) wells, and other hydrogeologic monitoring locations compiled from ORMGP partner agencies and supporting data providers.

These locations provide the spatial framework for groundwater-level, groundwater-temperature, barometric-pressure, conductivity, pumping, and related hydrogeologic records stored in the ORMGP database. The point features identify where groundwater observations have been collected and allow users to locate monitoring sites, assess spatial monitoring coverage, and link GIS locations to associated database records.

  * Type
    * Vector - Point features.

  * Geographic Extent
    * ORMGP study area and contributing partner-agency jurisdictions, including the Oak Ridges Moraine and surrounding municipal and conservation authority areas represented in the ORMGP database.

  * Maintenance Standard
    * Periodically updated as new monitoring locations, well records, municipal datasets, conservation authority datasets, PGMN records, logger files, and related groundwater datasets are added to the ORMGP database.

### Georeferencing and Accuracy

  * Horizontal Datum
    * North American Datum 1983.

  * Vertical Reference
    * Elevation references vary by source dataset. Where available, ground surface elevations, measuring-point elevations, or reference elevations are carried forward from the source record or assigned/standardized during ORMGP database processing.

  * Horizontal Accuracy
    * Positional accuracy varies by source. Monitoring locations may originate from field-surveyed coordinates, municipal databases, conservation authority datasets, consultant reports, PGMN records, Ontario water well records, or other compiled hydrogeologic datasets.
    * Users should refer to the [ORMGP database documentation](https://owrc.github.io/database-manual/Contents/TOC.html) and source-specific records for information on coordinate precision, elevation source, and location reliability.

  * Attribute Accuracy
    * Attribute completeness varies by monitoring location and source dataset. Some locations may include detailed construction information, screened interval, ground elevation, reference elevation, water-level records, logger records, or water-quality-related measurements, while other records may contain only basic well or borehole information.

### Data Sources and Restrictions

  * Use Constraint
    * None - in accordance with the ORMGP disclaimer. Users are responsible for confirming suitability for their intended application.

  * Citation
    * Oak Ridges Moraine Groundwater Program (ORMGP). Groundwater Monitoring Locations.

  * Agency Originator
    * Oak Ridges Moraine Groundwater Program (ORMGP), compiled from ORMGP partner agencies and external data providers.

  * Agency Distributor
    * Oak Ridges Moraine Groundwater Program (ORMGP).

  * Primary Source Categories
    * Ontario Ministry / MECP water well records and water well database updates.
    * Provincial Groundwater Monitoring Network (PGMN) records.
    * Conservation authority groundwater monitoring datasets.
    * Regional and municipal groundwater monitoring datasets.
    * Municipal production-well, pumping, logger, and SCADA datasets.
    * Consultant, field-program, and user-imported hydrogeologic monitoring datasets.
    * Logger water-level, barometric-pressure, groundwater-temperature, conductivity, and related monitoring files.

  * Example Source Agencies and Programs
    * Regional Municipality of Peel.
    * Regional Municipality of York.
    * Regional Municipality of Durham.
    * Halton Region / Halton-area monitoring datasets.
    * Toronto and Region Conservation Authority (TRCA).
    * Credit Valley Conservation (CVC).
    * Central Lake Ontario Conservation Authority (CLOCA).
    * Lake Simcoe Region Conservation Authority (LSRCA).
    * Lower Trent Region Conservation Authority (LTRCA).
    * Ganaraska Region Conservation Authority (GRCA / GaRCA).
    * Nottawasaga Valley Conservation Authority (NVCA).
    * Other ORMGP partner-agency and project-specific groundwater datasets.

### Methodology

  * Data Compilation
    * Groundwater monitoring locations are compiled from source datasets imported into the ORMGP database. Sources include well and borehole inventories, monitoring-well networks, PGMN datasets, municipal monitoring programs, logger records, manual water-level records, pumping datasets, barometric-pressure records, groundwater-temperature records, conductivity records, and project-specific imports.

  * Location Representation
    * Each GIS point represents a groundwater monitoring location, well, borehole, or related monitoring site. Where multiple monitoring intervals or nested wells occur at a single site, records may be represented through associated database identifiers and linked interval-level information.

  * Database Linkage
    * Monitoring locations are linked to ORMGP database records through internal identifiers. These identifiers support joins to related tables containing water-level measurements, logger measurements, well construction information, screened interval details, elevation information, source agency information, and other hydrogeologic attributes where available.

  * Source Harmonization
    * Source datasets are standardized during import into the ORMGP database. Standardization may include assigning database identifiers, mapping source fields to ORMGP database fields, associating measurements with monitoring intervals, and preserving source-file or import-history information.

  * Temporal Data Association
    * The GIS point layer identifies monitoring locations. Time-series records such as manual water levels, logger water levels, temperature, conductivity, barometric pressure, pumping, or SCADA records are maintained as related database records and are not necessarily stored directly as attributes in the GIS point layer.

  * Updates
    * The dataset is updated as new source records are added to the ORMGP database. Source history includes multiple historical and recent imports from provincial, municipal, conservation authority, and project-specific datasets.

### Typical Attributes

The available attributes may vary depending on the exported GIS layer and source database view. Typical fields may include:

  * Monitoring location identifier.
  * Well, borehole, or station name.
  * Source agency or data provider.
  * Source dataset or import reference.
  * Location coordinates.
  * Ground surface elevation, measuring-point elevation, or reference elevation, where available.
  * Well or borehole type.
  * Monitoring interval or screened interval information, where available.
  * Construction or depth information, where available.
  * Data availability indicators for water level, logger, temperature, conductivity, pumping, or related records.
  * Database linkage fields for joining to detailed ORMGP tables.

### Limitations

  * Monitoring locations are compiled from multiple sources with different measurement standards, coordinate accuracies, naming conventions, and update histories.
  * Some locations may have high-quality surveyed coordinates and detailed construction records, while others may have approximate or incomplete information.
  * Temporal coverage varies by location. Some monitoring locations include long-term logger or manual water-level records, while others may contain only short-duration or historical records.
  * The presence of a monitoring location does not imply that all related water-level, temperature, conductivity, or pumping records are complete or current.
  * Users should review source-specific metadata, ORMGP database documentation, and associated measurement records before using the data for detailed hydrogeologic interpretation, groundwater modelling, regulatory analysis, or site-specific decision-making.

### Replaces or Updates

  * This dataset is periodically updated as new groundwater monitoring locations and related records are incorporated into the ORMGP database.

### Significant Changes

  * New monitoring locations and related records are added as partner-agency, municipal, conservation authority, PGMN, provincial, and project-specific datasets are imported.
  * Recent source updates include well/borehole database updates and ORMGP-hosted logger, water-level, barometric, and municipal monitoring datasets.

### Contact

  * Oak Ridges Moraine Groundwater Program (ORMGP)


<br>

*Last Modified: 2026-05-14*