---
title: "Analysis of mTSC1 Knockout CLAMS Experiments"
author: "Erin Stephenson and Dave Bridges"
date: "January 31, 2019"
output:
  html_document:
    highlight: tango
    keep_md: yes
    number_sections: no
    toc: yes
  pdf_document:
    highlight: tango
    keep_tex: yes
    number_sections: yes
    toc: yes
---



# Purpose

To evaluate energy expenditure and other parameters in muscle _Tsc1_ knockout mice.  This script was most recently updated on **Tue Feb  5 15:19:53 2019**.

# Experimental Details

Mice were run in the CLAMS in several batches, and combined.

# Raw Data

## Sample Key



## Oxymax Input

There are two batches of data, baseline and after 3 months of diet.

### Baseline Data


Table: Total animals tested by genotype

Genotype      Sex        n
------------  -------  ---
+/+; +/+      Female    16
+/+; +/+      Male      17
+/+; Tg/+     Female    11
+/+; Tg/+     Male       8
fl/fl; +/+    Female    17
fl/fl; +/+    Male       8
fl/fl; Tg/+   Female    18
fl/fl; Tg/+   Male      11
NA            NA        24



Table: Total animals tested by knockout

Knockout   Sex        n
---------  -------  ---
Control    Female    44
Control    Male      33
Knockout   Female    18
Knockout   Male      11
NA         NA        24

The baseline raw data files can be found in Oxymax/Oxymax files by time period/Baseline.  The MRI data can be found in EchoMRI.

## VO2 Analysis

![VO2 Summary Light/Dark Boxplot](figures/vo2-analysis-light-dark-1.png)![VO2 Summary Light/Dark Boxplot](figures/vo2-analysis-light-dark-2.png)

![](figures/vo2-analysis-linegraph, fig-1.png)<!-- -->

### VO2 Summary Data

![Linegraph of VO2 Data](figures/vo2-summarized-data-1.png)![Linegraph of VO2 Data](figures/vo2-summarized-data-2.png)

# Heat Production

Another way to present these data is to evaluate this by heat instead of VO2. We calculated this manually from VO2 data.  The equation for Heat production from the CLAMS is the Lusk Equation:

$$(3.815 + 1.232 * RER)*VO2$$

![Linegraph of Heat Data](figures/heat-production-1.png)![Linegraph of Heat Data](figures/heat-production-2.png)

## Heat Production Statistics


Table: Average changes in heat production form wt to knockout

Sex      Light/Dark    Control   Knockout   Change   Pct.Change
-------  -----------  --------  ---------  -------  -----------
Female   Dark             23.7       25.5    1.767        7.451
Female   Light            21.9       22.0    0.066        0.302
Male     Dark             18.5       21.6    3.139       17.008
Male     Light            17.0       18.8    1.755       10.319

To test whether these groups are different we constructed a linear model with the following formula:

Fat Mass ~ as.factor(Time) + Lean + Sex + `Light/Dark` + Knockout + Knockout:`Light/Dark` + (1 | Subject).  

We used this model because the base model was that Heat production changes over the day.  We asked if lean mass modified the time dependent effect, and it did (p=4.403&times; 10^-10^).  After adjusting for lean mass, we asked if there was any additional benefit to including the light/dark cycle in addition to the time of day, and found that there was no significant effect, so that was not included in the model (p=1).  we added sex as a covariate which had no significant effect 0.076. We chose to keep sex in the model though as it was borderline significant.  We next added knockout to the model and found no significant effect 0.147.  Finally we asked if Sex modified the effect of the knockout and found no significant effect 0.413.

Since it appears from the figures that the elevation in energy expenditure is restricted to the awake cycle, we next asked if there was an *interaction* between genotype and the Light/Dark cycle.  Adding this interaction was highly significant 1.033&times; 10^-117^.  This represents a 

The full results are shown below:


Table: Estimates and p-values from mixed linear models, excluding time of day.

                                      Estimate   Std..Error   t.value     p.z
-----------------------------------  ---------  -----------  --------  ------
Lean                                    -0.507        0.178     -2.85   0.004
SexMale                                 -1.972        1.091     -1.81   0.071
KnockoutKnockout                         2.148        0.737      2.92   0.004
`Light/Dark`Light:KnockoutKnockout      -2.200        0.095    -23.24   0.000

## RER Analysis

![RER Summary Light/Dark Boxplot](figures/rer-analysis-light-dark-1.png)

![](figures/rer-analysis-linegraph, fig-1.png)<!-- -->

### RER Summary Data

![Linegraph of RER Data](figures/rer-summarized-data-1.png)

## Activity Analysis

![Activity Summary Light/Dark Boxplot](figures/activity-analysis-light-dark-1.png)

![](figures/activity-analysis-linegraph, fig-1.png)<!-- -->

### Activity Summary Data

![Linegraph of Activity Data](figures/activity-summarized-data-1.png)


# Interpretation

A brief summary of what the interpretation of these results were

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
##  [1] multcomp_1.4-8  TH.data_1.0-9   MASS_7.3-51.1   survival_2.43-3
##  [5] mvtnorm_1.0-8   lme4_1.1-19     Matrix_1.2-15   ggplot2_3.1.0  
##  [9] lubridate_1.7.4 readr_1.3.1     bindrcpp_0.2.2  readxl_1.2.0   
## [13] dplyr_0.7.8     tidyr_0.8.2     knitr_1.21     
## 
## loaded via a namespace (and not attached):
##  [1] zoo_1.8-4        tidyselect_0.2.5 xfun_0.4         purrr_0.2.5     
##  [5] reshape2_1.4.3   splines_3.5.0    lattice_0.20-38  colorspace_1.3-2
##  [9] htmltools_0.3.6  yaml_2.2.0       rlang_0.3.1      pillar_1.3.1    
## [13] nloptr_1.2.1     glue_1.3.0       withr_2.1.2      bindr_0.1.1     
## [17] plyr_1.8.4       stringr_1.3.1    munsell_0.5.0    gtable_0.2.0    
## [21] cellranger_1.1.0 codetools_0.2-16 evaluate_0.12    labeling_0.3    
## [25] highr_0.7        Rcpp_1.0.0       scales_1.0.0     hms_0.4.2       
## [29] digest_0.6.18    stringi_1.2.4    grid_3.5.0       tools_3.5.0     
## [33] sandwich_2.5-0   magrittr_1.5     lazyeval_0.2.1   tibble_2.0.0    
## [37] crayon_1.3.4     pkgconfig_2.0.2  assertthat_0.2.0 minqa_1.2.4     
## [41] rmarkdown_1.11   R6_2.3.0         nlme_3.1-137     compiler_3.5.0
```
