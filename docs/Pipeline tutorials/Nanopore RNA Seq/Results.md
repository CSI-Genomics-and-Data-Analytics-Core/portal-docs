---
sidebar_position: 4
---

# Results
## Get started

Navigate to the Projects page and select the **Result** button to view the pipeline results.

## Output
The output files are placed into separate folders named after the tool that produced them.

#### FASTQC
[**fastqc**](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) is a computer program used to examine the quality of raw sequence data.  Standard quality control metrics for each sample can be viewed by downloading the files ending with a *.html* extension to your computer and opening them in a web browser.

#### MULTIQC
[**multiqc**](https://seqera.io/multiqc/) is a computer program also used to examine the quality of raw sequence data.  This program aggregates all FASTQC files into a single report that can be easily viewed in a browser.

#### MINIMAP2 
[**minimap2**](https://github.com/lh3/minimap2) is a computer program used to align long-read sequence data to a reference genome.  The output of this program is a collection of `BAM` files that are used for gene and transcript quantification.

#### BAMBU
[**bambu**](https://www.bioconductor.org/packages//release/bioc/vignettes/bambu/inst/doc/bambu.html) is computer program used to quantify gene expression from long-read sequencing data.  Transcript and gene-level counts for each sample are stored in the `counts_gene.txt` and `counts_transcript.txt` files.

:::tip
This directory contains the output files needed to perform downstream data visualization and statistical analysis.  These files can be directly loaded into R or RStudio and analyzed using your favorite software packages.
:::

#### PIPELINE_INFO
pipeline_info is a folder containing auxillary information about the pipeline:
- pipeline software (`nf_core_rnaseq_software_mqc_versions.yml`)
- pipeline parameters (`params_2024-12-20_16-56-03.json`)
- execution report (`execution_report_2024-12-20_16-55-39.html`)

:::info
The information included in this folder can be helpful for writing the materials and methods section of your manuscript or grant; and learning more about what is happening under the hood of the pipeline.
:::
