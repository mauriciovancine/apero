---
title: "Conectividade: métrica de Hanski"
subtitle: "Cálculo da distância de pontos a linhas no R e no QGIS"
summary: "Cálculo da distância de pontos a linhas no R e no QGIS"
author: Maurício Vancine
date: "2023-07-10"
publishDate: r`Sys.time()`
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: eco-pai-hanski
links:
categories:
  - Blog
tags:
  - Geoprocessamento
  - Geoespacial
  - R
  - Distância
featured: yes
format: hugo
draft: true
---



## Contextualização

https://bookdown.org/hhwagner1/LandGenCourse_book/bonus_7a.html

https://stackoverflow.com/questions/71379775/r-function-for-hanski-connectivity-index

https://rdrr.io/github/mstrimas/metacapa/man/patch_config.html


```r
patch_config(x, units = c("m", "km"))

HanskiIC<-function(area, dist, alp, bet){ alphmat<-matrix(-alp,1,1)
                                      alphdist<-dist*c(alphmat)
                                      IC<-(exp(alphdist)%*%(area^bet))-area^bet
                                        return(IC)}
```

