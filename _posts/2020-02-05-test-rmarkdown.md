---
title: "An example post with RMarkdown - knitted to md and html"
author: "Frie"
output:
  md_document:
    toc: true
    toc_depth: 2
    preserve_yaml: true
layout: post
description: a minimal example of using fastpages with rmarkdown
categories: [howto]
---

-   [R Markdown](#r-markdown)
-   [Including Plots](#including-plots)

R Markdown
----------

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

    summary(cars)

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

Including Plots
---------------

You can also embed plots, for example:

    pp <- get_plot_paths(2)

    ggplot(cars, aes(x = speed))+
        geom_bar()

![](/Users/frie/dev/correlaid/websites/open-data-ideas/images/2020-02-05-test-rmarkdown///pressure-1.png)

    ggplot(cars, aes(x = dist))+
        geom_bar()

![](/Users/frie/dev/correlaid/websites/open-data-ideas/images/2020-02-05-test-rmarkdown///pressure-2.png)

![image](/open-data-ideas/images/2020-02-05-test-rmarkdown/pressure-1.png)
![image](/open-data-ideas/images/2020-02-05-test-rmarkdown/pressure-2.png)

    pp <- get_plot_paths(1)
    reactable(palmerpenguins::penguins)

![](/Users/frie/dev/correlaid/websites/open-data-ideas/images/2020-02-05-test-rmarkdown///unnamed-chunk-2-1.png)

![image](/open-data-ideas/images/2020-02-05-test-rmarkdown/unnamed-chunk-2-1.png)

    pp <- get_plot_paths(1)
    m <- leaflet() %>%
      addTiles() %>%  # Add default OpenStreetMap map tiles
      addMarkers(lng=174.768, lat=-36.852, popup="The birthplace of R")
    m

![](/Users/frie/dev/correlaid/websites/open-data-ideas/images/2020-02-05-test-rmarkdown///leaflet-1.png)

![image](/open-data-ideas/images/2020-02-05-test-rmarkdown/leaflet-1.png)
