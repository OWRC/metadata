---
title:  Metadata - MOECP Access Environment Records
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

## Access Environment Records - ORMGP Database

### Description

The Access Environment Records dataset contains environmental approval and registration records downloaded from Ontario's Access Environment search portal and hosted by the Oak Ridges Moraine Groundwater Program (ORMGP). Access Environment is a map-based search tool for registrations on the Environmental Activity and Sector Registry, Renewable Energy Approvals, and Environmental Compliance Approvals issued by the Ontario environment ministry from December 1999 onward.

These records provide a spatial and attribute-based index of regulated environmental activities that may be relevant to groundwater, surface water, land use, infrastructure, waste management, stormwater, drinking water, and other environmental planning or hydrogeologic review tasks within the ORMGP study area.

  * Type
    * Vector - Point, polygon, or tabular records, depending on the form downloaded and processed from Access Environment.
  * Geographic Extent
    * Ontario records downloaded from Access Environment, with ORMGP-hosted coverage focused on the ORMGP study area and surrounding partner-agency jurisdictions.
  * Maintenance Standard
    * Periodically updated as new Access Environment downloads are incorporated into ORMGP-hosted datasets.

### Georeferencing and Accuracy

  * Horizontal Datum
    * North American Datum 1983, where spatial coordinates are provided or assigned within ORMGP GIS/database processing.
  * Vertical Reference
    * Not generally applicable unless individual records include elevation or site-specific engineering information.
  * Horizontal Accuracy
    * Positional accuracy varies by record and by the information available through Access Environment. Some records may be mapped to a precise facility or site location, while others may reflect approximate coordinates, property-level locations, address-derived locations, or locations inherited from the source approval or registration record.
  * Attribute Accuracy
    * Attribute completeness and consistency depend on the Access Environment source record, the type of approval or registration, and the fields included in the downloaded dataset. Users should verify critical details against the original Access Environment record and associated approval or registration documents before site-specific interpretation.

### Data Sources and Restrictions

  * Use Constraint
    * None - in accordance with the ORMGP disclaimer. Users are responsible for confirming suitability for their intended application.
  * Citation
    * Ontario Access Environment records, hosted by Oak Ridges Moraine Groundwater Program.
  * Agency Originator
    * Ontario Ministry of the Environment, Conservation and Parks / legacy Ontario environment ministry records available through Access Environment.
  * Agency Distributor
    * Oak Ridges Moraine Groundwater Program (ORMGP).
  * Primary Source Categories
    * Environmental Compliance Approvals.
    * Environmental Activity and Sector Registry registrations.
    * Renewable Energy Approvals.
    * Records categorized under Access Environment themes such as WATER, LAND, Waste & Recycling, Drinking Water, Stormwater Management, Wells, Source Water Protection, Agriculture & Farming, Air, and related environmental subject areas.
  * ORMGP Context
    * ORMGP is a partnership of Ontario government agencies, regional municipalities, and conservation authorities that manages and provides access to geological, hydrogeological, hydrological, and related environmental data through an interactive web-based mapping system.

### Methodology

  * Data Compilation
    * Records are downloaded from Ontario's Access Environment portal and incorporated into ORMGP-hosted data products for viewing, searching, and spatial reference within the ORMGP database environment.
  * Location Representation
    * Spatial records represent the mapped location associated with an environmental approval, registration, facility, activity, site, or related regulatory record. The mapped location may not always represent the exact point of environmental impact, discharge, intake, monitoring, infrastructure, or activity.
  * Database Linkage
    * ORMGP-hosted records may include identifiers, names, approval or registration numbers, addresses, categories, activity descriptions, and other fields that support lookup against the original Access Environment record.
  * Source Harmonization
    * Access Environment fields may be standardized, renamed, filtered, joined, or spatially processed during ORMGP import. Processing may include coordinate validation, assignment to ORMGP map layers, clipping or filtering to the ORMGP study area, and preservation of source identifiers where available.
  * Temporal Data Association
    * The dataset reflects regulatory records available from Access Environment at the time of download. Access Environment includes records issued from December 1999 onward, but the ORMGP-hosted copy should be treated as a snapshot unless an update date is specified.
  * Updates
    * The dataset should be refreshed periodically from Access Environment to capture new, amended, revoked, or otherwise changed records.

### Typical Attributes

The available attributes may vary depending on the Access Environment download, ORMGP processing, and exported GIS/database view. Typical fields may include:

  * Approval, registration, or instrument number.
  * Record type or approval category.
  * Facility, company, applicant, or owner name.
  * Site name or activity name.
  * Address, municipality, or geographic description.
  * Access Environment category or subject matter.
  * Issue date, effective date, or status date, where available.
  * Record status, where available.
  * Activity description or approval description.
  * Environmental medium or program area, where available.
  * Source URL or lookup reference to the Access Environment record, where available.
  * Coordinates or mapped geometry.
  * ORMGP database linkage fields or import identifiers.

### Limitations

  * Records are derived from a public regulatory search portal and may not contain all supporting technical information associated with an approval or registration.
  * Spatial accuracy varies and should not be assumed to represent exact discharge points, wells, intakes, infrastructure, property boundaries, or operational footprints.
  * Some records may be duplicated, superseded, amended, expired, revoked, or otherwise changed in the source system after the ORMGP-hosted copy was downloaded.
  * Attribute fields may vary across approval types and across download dates.
  * The presence of a record does not confirm ongoing activity, current compliance status, current site operation, or environmental impact.
  * Users should consult the original Access Environment record and any associated approval documents before using the data for regulatory review, hydrogeologic interpretation, groundwater modelling, site screening, or decision-making.

### Replaces or Updates

  * This dataset may replace or update previous ORMGP-hosted Access Environment downloads when a newer extract from the provincial source system is incorporated.

### Significant Changes

  * New records may be added as they appear in Access Environment.
  * Existing records may change if approval status, registration status, applicant information, activity descriptions, or mapped locations are updated in the source system.
  * ORMGP processing changes may include improved georeferencing, field standardization, duplicate handling, or filtering to the ORMGP study area.

### Contact

  * Oak Ridges Moraine Groundwater Program (ORMGP)

Last Modified: 2026-05-15

© 2026 Oak Ridges Moraine Groundwater Program
