Running R Scripts
===================

Once the counts tables are generated for both gene counts and exon counts, all the other analyses are run using the scripts used here.  All analysis file are R scripts as Rmarkdown (Rmd) files.  These files can be run inside RStudio https://www.rstudio.com/ and will generate the md and html files which include the processed data.  For more information on using R and using these files see http://cran.us.r-project.org/.

## Running the Differential Expression Analyses

We use DESeq2 to do the differential expression analysis.  This takes the htseq-counts file (**../data/raw/htseq-counts**) along with the sample mapping file (**../data/raw/sample_mapping.csv**) and generates the results file (**../data/processed/Binary DESeq Results.csv**).  It also generates the normalized counts file used in other scripts.  This file is found at **../data/processed/Binary Normalized Counts.csv**.  This script also generates the diagnostic dispersion, MA and PCA plots as well as the heatmap.