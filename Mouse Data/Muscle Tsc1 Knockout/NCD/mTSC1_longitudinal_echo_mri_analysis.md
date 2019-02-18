---
title: "Analysis of Body Weights for Muscle Tsc1 Knockouts"
author: "Erin Stephenson, Matt Peloquin and Dave Bridges"
date: "February 23, 2015"
output:
  html_document:
    keep_md: yes
  pdf_document:
    keep_tex: yes
---




# Normal Chow Fed Animals



This retrieved 1934 measurements.

![](figures/scatterplot-Body-weight-1.png)<!-- -->

![](figures/scatterplot-lean-mass-1.png)<!-- -->

![](figures/scatterplot-fat-mass-1.png)<!-- -->

![](figures/scatterplot-fat-mass-weekly-1.png)<!-- -->

![](figures/scatterplot-lean-mass-weekly-1.png)<!-- -->

# Summary

![](figures/summary-1.png)<!-- -->

This analysis uses measurements between 125, 175, with only one measurement per animal.

## Statistics

First, we tested whether there was a difference between the control animals.  The p-values for these tests are below:

% latex table generated in R 3.5.0 by xtable 1.8-3 package
% Mon Feb 18 14:44:13 2019
\begin{table}[ht]
\centering
\begin{tabular}{rrr}
  \hline
 & Shapiro & ANOVA \\ 
  \hline
Total.Fat.Mass & 0.083 & 0.378 \\ 
  Percent.Fat.Mass & 0.619 & 0.604 \\ 
  Body.Weight & 0.414 & 0.232 \\ 
  Lean.Mass & 0.220 & 0.355 \\ 
   \hline
\end{tabular}
\caption{Statistical tests for control strains} 
\end{table}

These tests suggest that it is appropriate to combine the controls and compare to the knockouts.  These tests are shown below:

![](figures/ko-statistics-1.png)<!-- -->

Table: Pairwise tests for body composition, after combining the controls

                      Shapiro      Levene  Test              pval
-----------------  ----------  ----------  ----------  ----------
Total.Fat.Mass      0.0197057   0.0001100  Wilcoxon     0.0000013
Percent.Fat.Mass    0.5344418   0.0006355  Welch's      0.0000000
Body.Weight         0.4466816   0.0061261  Welch's      0.6995812
Lean.Mass           0.1831920   0.1821235  Student's    0.7438294

The total fat mass was reduced by 41.8939496% wheras the percent fat mass was reduced by 36.0694359%.

# Session Information

```
## R version 3.5.0 (2018-04-23)
## Platform: x86_64-apple-darwin15.6.0 (64-bit)
## Running under: macOS  10.14.2
## 
## Matrix products: default
## BLAS: /Library/Frameworks/R.framework/Versions/3.5/Resources/lib/libRblas.0.dylib
## LAPACK: /Library/Frameworks/R.framework/Versions/3.5/Resources/lib/libRlapack.dylib
## 
## locale:
## [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
## [1] car_3.0-2          carData_3.0-2      xtable_1.8-3      
## [4] tidyr_0.8.2        bindrcpp_0.2.2     dplyr_0.7.8       
## [7] RColorBrewer_1.1-2 knitr_1.21        
## 
## loaded via a namespace (and not attached):
##  [1] zip_1.0.0         Rcpp_1.0.0        highr_0.7        
##  [4] cellranger_1.1.0  pillar_1.3.1      compiler_3.5.0   
##  [7] bindr_0.1.1       forcats_0.3.0     tools_3.5.0      
## [10] digest_0.6.18     evaluate_0.12     tibble_2.0.0     
## [13] pkgconfig_2.0.2   rlang_0.3.1       openxlsx_4.1.0   
## [16] curl_3.2          yaml_2.2.0        haven_2.0.0      
## [19] xfun_0.4          rio_0.5.16        stringr_1.3.1    
## [22] hms_0.4.2         tidyselect_0.2.5  glue_1.3.0       
## [25] data.table_1.11.8 R6_2.3.0          readxl_1.2.0     
## [28] foreign_0.8-71    rmarkdown_1.11    purrr_0.2.5      
## [31] magrittr_1.5      htmltools_0.3.6   abind_1.4-5      
## [34] assertthat_0.2.0  stringi_1.2.4     crayon_1.3.4
```
