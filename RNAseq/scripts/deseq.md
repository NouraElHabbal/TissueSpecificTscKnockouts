# DESeq Analysis of Mck-TSC Quadriceps
Dave Bridges  
June 13, 2014  





This file uses the counts table in ../data/raw/htseq-counts from ../data/raw/sample_mapping.csv.  This script was most recently run on Wed May 20 16:02:08 2015





The calculated data was exported to ../data/processed/Binary DESeq Results.csv.  There was a total of **4451** significantly different genes out of 14423 that met our testing criteria.  These are broken down into up and downregulated genes below:

<!-- html table generated in R 3.1.2 by xtable 1.7-4 package -->
<!-- Wed May 20 16:03:05 2015 -->
<table border=1>
<caption align="bottom"> Number of Genes Up/Downregulated and Significant or Not </caption>
<tr> <th>  </th> <th> Upregulated FALSE </th> <th> Upregulated TRUE </th>  </tr>
  <tr> <td align="right"> Significant FALSE </td> <td align="right"> 5223 </td> <td align="right"> 4749 </td> </tr>
  <tr> <td align="right"> Significant TRUE </td> <td align="right"> 1970 </td> <td align="right"> 2481 </td> </tr>
   </table>

Diagnostic Plots
----------------

![](figure/ma-plots-1.png) 

![](figure/heatmap-1.png) 

Plotting Estimated Dispersions
-------------------------------
![](figure/dispersion-plot-1.png) 


Principal Component Analysis
------------------------------

![](figure/pca-plot-1.png) 


Session Information
-------------------


```
## R version 3.1.2 (2014-10-31)
## Platform: x86_64-apple-darwin13.4.0 (64-bit)
## 
## locale:
## [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
## 
## attached base packages:
## [1] parallel  stats     graphics  grDevices utils     datasets  methods  
## [8] base     
## 
## other attached packages:
##  [1] gplots_2.17.0             RColorBrewer_1.1-2       
##  [3] xtable_1.7-4              biomaRt_2.20.0           
##  [5] DESeq2_1.4.5              RcppArmadillo_0.5.100.1.0
##  [7] Rcpp_0.11.6               GenomicRanges_1.16.4     
##  [9] GenomeInfoDb_1.0.2        IRanges_1.22.10          
## [11] BiocGenerics_0.10.0       knitr_1.10               
## 
## loaded via a namespace (and not attached):
##  [1] annotate_1.42.1      AnnotationDbi_1.26.1 Biobase_2.24.0      
##  [4] bitops_1.0-6         caTools_1.17.1       DBI_0.3.1           
##  [7] digest_0.6.8         evaluate_0.7         formatR_1.2         
## [10] gdata_2.16.1         genefilter_1.46.1    geneplotter_1.42.0  
## [13] grid_3.1.2           gtools_3.4.2         htmltools_0.2.6     
## [16] KernSmooth_2.23-14   lattice_0.20-31      locfit_1.5-9.1      
## [19] magrittr_1.5         RCurl_1.95-4.6       rmarkdown_0.5.1     
## [22] RSQLite_1.0.0        splines_3.1.2        stats4_3.1.2        
## [25] stringi_0.4-1        stringr_1.0.0        survival_2.38-1     
## [28] tools_3.1.2          XML_3.98-1.1         XVector_0.4.0       
## [31] yaml_2.1.13
```
