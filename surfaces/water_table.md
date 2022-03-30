---
title:  "Metadata - Water Table (WT0 and WT1)"
author: "ORMGP"
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


