---
title: "Identifying Undervalued Advertising Keywords"
author: fastzhong
highlighter: highlight.js
output:
  html_document:
    keep_md: yes
job: null
knit: slidify::knit2slides
mode: standalone
hitheme: tomorrow
subtitle:
framework: io2012
widgets: []
---



## Summary

Search engines allow advertisers to bid on keywords. Some are more expensive and some 
are submitted more often. What are the most cost-effective keywords to bid?

![Common Keywords](assets/fig/unnamed-chunk-2-1.png) 

--- .class #id

## Advertising Bidding Data
Notice the skewed distribution of continuous variables.

```r
summary(df[ ,2:length(df)])
```

```
##  global_monthly_searches  est_avg_cpc       est_ad_pos   
##  Min.   :5.800e+01       Min.   : 0.000   Min.   :0.000  
##  1st Qu.:4.400e+03       1st Qu.: 0.000   1st Qu.:0.000  
##  Median :4.950e+04       Median : 0.000   Median :0.000  
##  Mean   :1.052e+07       Mean   : 1.258   Mean   :0.438  
##  3rd Qu.:1.000e+06       3rd Qu.: 1.210   3rd Qu.:1.050  
##  Max.   :3.760e+09       Max.   :27.190   Max.   :1.060  
##  est_daily_clicks   est_daily_cost      local_monthly_searches
##  Min.   :    0.00   Min.   :     0.00   Min.   :        0     
##  1st Qu.:    0.00   1st Qu.:     0.00   1st Qu.:     1900     
##  Median :    0.00   Median :     0.00   Median :    22200     
##  Mean   :  338.37   Mean   :   911.58   Mean   :  1591891     
##  3rd Qu.:   22.14   3rd Qu.:    38.49   3rd Qu.:   368000     
##  Max.   :52064.14   Max.   :137734.50   Max.   :338000000
```

--- .class #id 

## Distributions Illustrated

![plot of chunk unnamed-chunk-4](assets/fig/unnamed-chunk-4-1.png) 

--- .class #id 

## Conclusion

Because the search frequency does not follow the same distribution of the cost 
there may be undervalued search keywords. This application will help identify 
those keywords.

https://fastzhong.shinyapps.io/developing-data-products/
