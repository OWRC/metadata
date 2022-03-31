---
title:  "Metadata - Table of Contents"
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
                    'toc.html')
                )
            }
        )
---

## Table of Contents

**[Potential Discharge Areas - Metadata](/metadata/surfaces/potential_discharge.html)**

**[Potentiometric Surface - Metadata](/metadata/surfaces/potentiometric_surface.html)**

**[Water Table - Metadata](/metadata/surfaces/water_table.html)**


*Last Modified: 2022-03-31*
