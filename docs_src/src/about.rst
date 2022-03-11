.. _about:

Summary
---------------

The notebooks contain a DE analysis, using the normal vs tumour for the **PE.2 KIRP** dataset from TCGA.

Data processing and download can be found in **KIRP_DNAMethyaltion.ipynb**, this also contains individual statistical
tests between genes of interest for both DNA methylation and RNAseq data.

Code for the R analysis can be reproduced by following the script in **KIRP_type2.rmd** and **KIRP_type2_FHdeficient.Rmd**.
These include a DESeq2 analysis and visualisations of the most variable genes.

Raw code can be found at: https://github.com/ArianeMora/KIRP_HIRA

Data
----

The data are as follows and stored on `github LFS <https://github.com/ArianeMora/KIRP_HIRA/tree/main/KIRP_type2/data>`_:

**DEseq2_NormalVsTumour_KIRP-PE2.csv**
Output from running the DEseq2 for the KIRP PE2 tumour vs normal. LogFC is positive if it is higher in the normal vs the tumour.

**TCGA_kidney_counts_13082020.csv**
These are the counts for all the samples in the TCGA database (KIRP, KIRC, KICH)

**TCGA_kidney_HumanMethylation450_13082020.csv**
These are the DNA methylation beta values for all the samples in the TCGA database (KIRP, KIRC, KICH)

**TCGA_kidney_counts_KIRP-only_13082020.csv**
These are the counts for KIRP only from TCGA database

**TCGA_kidney_counts_KIRP-PE2-only_13082020.csv**
These are the counts for KIRP only from TCGA database filtering on the samples labelled in the paper: https://www.sciencedirect.com/science/article/pii/S2211124716301279

**KIRP_type2_FHdeficient.Rmd**
This file is a DE analysis taking FH low vs high into account as a factor. This would need to be improved (i.e. take a random sample from the high group) to use as an actual analysis but gives a general idea about how it works.

**annotated-rna_kirp-Cimp_20200814.csv**
The CIMP count data with annotation using FH lowest 25% or FH > lowest 25%.

**annotated-rna_kirp-Pe2_20200814.csv**
The Pe2 count data with annotation using FH lowest 25% or FH > lowest 25%.

**annotated-rna_kirp_20200814.csv**
KIRP count data with annotation using FH lowest 25% or FH > lowest 25%.

The columns are labelled to include as much sample information as possible:
The column names are of the format:

.. code-block:: python

    [subtype_project_sampleType_gender_race_tumourStage_dataType_timeTillDeath_fileIDstuff] e.g. here is an example:
    PE2_TCGA-KIRP_SolidTissueNormal_male_white_3_htseq.counts_--_TCGA-KIRP_TCGA-BQ-5890_a7c5e2d2-efcd-461f-b795-9bd0e522149e


Figures
-------

Generated images can be found in the HTML or in the `img_DNAmethylation <https://github.com/ArianeMora/KIRP_HIRA/tree/main/KIRP_type2/img_DNAMethylation>`_
or `img_RNA <https://github.com/ArianeMora/KIRP_HIRA/tree/main/KIRP_type2/img_RNA/>`_ folders.