---
sidebar_position: 4
---

# Results

## Get started
Navigate to the Projects page and select the **View** button to view the pipeline results.

## Output
The output files are placed into separate folders named after the tool that produced them.

#### FASTQC
[**fastqc**](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) is a computer program used to examine the quality of raw sequence data.  Standard quality control metrics for each sample can be viewed by downloading the files ending with a *.html* extension to your computer and opening them in a web browser.

#### MULTIQC
[**multiqc**](https://seqera.io/multiqc/) is a computer program also used to examine the quality of raw sequence data.  This program aggregates all FASTQC files into a single report that can be easily viewed in a browser.

#### CELLRANGER 
[**cellranger**](https://www.10xgenomics.com/support/software/cell-ranger/latest) is a computer program developed by 10X Genomics that aligns single-cell reads to a reference genome and counts the number of genes within each cell.  Single-cell gene counts for each sample are stored in the `raw_feature_bc_matrix` and `filtered_feature_bc_matrix` folders.

:::tip
These two folders contains the output files needed to perform downstream clustering, cell typing and differential gene expression using [**Seurat**](https://satijalab.org/seurat/) in R or [**ScanPy**](https://scanpy.readthedocs.io/en/stable/) in Python.
:::

#### PIPELINE_INFO
pipeline_info is a folder containing auxillary information about the pipeline:
- pipeline software (`nf_core_rnaseq_software_mqc_versions.yml`)
- pipeline parameters (`params_2024-12-20_16-56-03.json`)
- execution report (`execution_report_2024-12-20_16-55-39.html`)

:::info
The information included in this folder can be helpful for writing the materials and methods section of your manuscript or grant; and learning more about what is happening under the hood of the pipeline.
:::