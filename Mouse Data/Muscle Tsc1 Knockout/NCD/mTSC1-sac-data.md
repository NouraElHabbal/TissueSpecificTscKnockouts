---
title: "Tissue Weights for Muscle Tsc1 Knockout Mice on a Normal Chow Diet"
author: "Dave Bridges and Erin Stephenson"
date: "2019-02-08"
output:
  html_document:
    highlight: tango
    keep_md: yes
    number_sections: yes
    toc: yes
  pdf_document:
    highlight: tango
    keep_tex: yes
    number_sections: yes
    toc: yes
---



# Purpose

To determine tissue weights at sacrifice for fat pads and muscle tissues

# Experimental Details

At sacrifice, after a 16h fast data were entered and collected in the raw data sheet




These data can be found in **/Users/davebrid/Documents/GitHub/TissueSpecificTscKnockouts/Mouse Data/Muscle Tsc1 Knockout/NCD** in a file named **NCD Sacrifice Data.xlsx**.  This script was most recently updated on **Sat Mar  2 07:56:45 2019**.

# Analysis


 EWAT_mean.na   IWAT_mean.na   Quadriceps_mean.na   TricepsSurae_mean.na   Heart_mean.na
-------------  -------------  -------------------  ---------------------  --------------
          453          341.0                  213                    164             119
          110           72.8                  170                    131             135



 EWAT_length   IWAT_length   Quadriceps_length   TricepsSurae_length   Heart_length
------------  ------------  ------------------  --------------------  -------------
          20            20                  20                    20             20
           8             8                   8                     8              8

## Fat Pad Weights

![Weights of Fat Pads at Sacrifice](figures/wat-weights-1.png)

For the chow-fed mice, the fat pads were reduced in weight:


Table: Changes in Epididymal Fat Pad Weights

 Wild-Type   Knockout   Difference   Pct.Difference
----------  ---------  -----------  ---------------
       453        110          343             75.7



Table: Changes in Inguinal Fat Pad Weights

 Wild-Type   Knockout   Difference   Pct.Difference
----------  ---------  -----------  ---------------
       341       72.8          268             78.7


Table: Shapiro-Wilk Tests for each group

Knockout    IWAT_shapiro.p   EWAT_shapiro.p
---------  ---------------  ---------------
FALSE                0.001            0.038
TRUE                 0.102            0.602



Table: Pairwise tests for effects of knockout on Inguinal WAT weights.

 Levene   Mann.Whitney   Welch   Student
-------  -------------  ------  --------
  0.053              0       0     0.012



Table: Pairwise tests for effects of knockout on Gonadal WAT weights.

 Levene   Mann.Whitney   Welch   Student
-------  -------------  ------  --------
  0.014              0       0     0.002

For the chow-fed mice, normality can not be assumed, but not equal variance, so a Mann-Whitney t-test wsa used, which had a p-value of 0.000043 for inguinal WAT and 0.000019 for epididymal WAT.

## Muscle Weights

![Weights of Muscle Depots at Sacrifice](figures/muscle-weights-1.png)

# Session Information


```r
sessionInfo()
```

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
##  [1] gridExtra_2.3      ggplot2_3.1.0      RColorBrewer_1.1-2
##  [4] car_3.0-2          carData_3.0-2      forcats_0.3.0     
##  [7] bindrcpp_0.2.2     readxl_1.2.0       dplyr_0.7.8       
## [10] tidyr_0.8.2        knitr_1.21        
## 
## loaded via a namespace (and not attached):
##  [1] zip_1.0.0         Rcpp_1.0.0        plyr_1.8.4       
##  [4] pillar_1.3.1      compiler_3.5.0    cellranger_1.1.0 
##  [7] highr_0.7         bindr_0.1.1       tools_3.5.0      
## [10] digest_0.6.18     gtable_0.2.0      evaluate_0.12    
## [13] tibble_2.0.0      pkgconfig_2.0.2   rlang_0.3.1      
## [16] openxlsx_4.1.0    cli_1.0.1         curl_3.2         
## [19] yaml_2.2.0        haven_2.0.0       xfun_0.4         
## [22] rio_0.5.16        withr_2.1.2       stringr_1.3.1    
## [25] hms_0.4.2         grid_3.5.0        tidyselect_0.2.5 
## [28] glue_1.3.0        data.table_1.11.8 R6_2.3.0         
## [31] foreign_0.8-71    rmarkdown_1.11    purrr_0.2.5      
## [34] magrittr_1.5      scales_1.0.0      htmltools_0.3.6  
## [37] abind_1.4-5       assertthat_0.2.0  colorspace_1.3-2 
## [40] labeling_0.3      stringi_1.2.4     lazyeval_0.2.1   
## [43] munsell_0.5.0     crayon_1.3.4
```