# Tissue Weight Analysis of HPD Fed Animals
Innocence Harvey and Dave Bridges  
August 10, 2015  





This data uses the input file HPD fat pad weights.csv.  This script was most recently run on Mon Aug 10 11:03:29 2015.

# Adipose Tissue

The iWAT and eWAT values are the sum of the left and right fat pads for each mouse.



We tested whether normality can be assumed for eWAT and iWAT by a Shapiro-Wilk test.  The p-values for this were all greater than 0.158.  For summary statistics see below.


Table: Inguinal Fat Pads (mg)

Diet                  n   Average    SD    SE   Shapiro
------------------  ---  --------  ----  ----  --------
Control Diet          6       848   452   185     0.308
High Protein Diet     6       502   275   112     0.428



Table: Epididymal Fat Pads (mg)

Diet                  n   Average    SD    SE   Shapiro
------------------  ---  --------  ----  ----  --------
Control Diet          6      1458   829   338     0.206
High Protein Diet     6       814   442   180     0.158

![](figures/hpd-adipose-weights-1.png) 


We next tested whether equal variance can be assumed via Levene's test.  For iWAT the p-value was 0.033 and for eWAT the p-value was 0.046.  Therefore in both cases, equal variance can not be assumed and Welch's *t* tests were performed.  These p-values were **0.249** for iWAT and **0.233** for eWAT.

# Muscle Tissues

The TS and Quadriceps values are the sum of the left and right fat pads for each mouse.



We tested whether normality can be assumed for TS, Quadriceps and Heart by Shapiro-Wilk tests.  The p-values for this were all greater than 0.11.  For summary statistics see below.


Table: Triceps Surae Weights (mg)

Diet                  n   Average     SD      SE   Shapiro
------------------  ---  --------  -----  ------  --------
Control Diet          6       342   30.7   12.55      0.16
High Protein Diet     6       378   21.3    8.71      0.11



Table: Quadriceps Weights (mg)

Diet                  n   Average      SD      SE   Shapiro
------------------  ---  --------  ------  ------  --------
Control Diet          6       480   33.41   13.64     0.210
High Protein Diet     6       516    5.16    2.11     0.168



Table: Heart Weights (mg)

Diet                  n   Average     SD     SE   Shapiro
------------------  ---  --------  -----  -----  --------
Control Diet          6       126   2.89   1.18     0.558
High Protein Diet     6       135   8.13   3.32     0.385

![](figures/hpd-muscle-weights-1.png) 


We next tested whether equal variance can be assumed via Levene's test.  For quadriceps the p-value was 0.239,  for TS the p-value was 0.862 and for heart the p-value was 0.122.  Therefore in all cases, equal variance can be assumed and Student's *t* tests were performed.  These p-values were **0.075** for quadriceps, **0.1** for TS, and **0.083** for heart.


# Session Information


```
## R version 3.2.0 (2015-04-16)
## Platform: x86_64-apple-darwin13.4.0 (64-bit)
## Running under: OS X 10.10.4 (Yosemite)
## 
## locale:
## [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
## [1] car_2.0-25   dplyr_0.4.2  knitr_1.10.5
## 
## loaded via a namespace (and not attached):
##  [1] Rcpp_0.12.0     magrittr_1.5    splines_3.2.0   MASS_7.3-43    
##  [5] lattice_0.20-33 R6_2.1.0        minqa_1.2.4     highr_0.5      
##  [9] stringr_1.0.0   tools_3.2.0     nnet_7.3-10     parallel_3.2.0 
## [13] pbkrtest_0.4-2  grid_3.2.0      nlme_3.1-121    mgcv_1.8-7     
## [17] quantreg_5.11   DBI_0.3.1       htmltools_0.2.6 yaml_2.1.13    
## [21] lme4_1.1-8      lazyeval_0.1.10 assertthat_0.1  digest_0.6.8   
## [25] Matrix_1.2-2    nloptr_1.0.4    formatR_1.2     evaluate_0.7   
## [29] rmarkdown_0.7   stringi_0.5-5   SparseM_1.6
```
