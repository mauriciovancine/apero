---
title: "Métrica de paisagem: quantidade de habitat usando vetores"
subtitle: "Cálculo da quantidade de hatbiat no R usando vetores"
summary: "Cálculo da quantidade de hatbiat no R usando vetores"
author: Maurício Vancine
date: "2024-02-18"
publishDate: r`Sys.time()`
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: landscape-habitat-amount-vetor
links:
categories:
  - Blog
tags:
  - Ecologia da paisagem
  - Métricas
  - Quantidade de habitat
  - R
featured: yes
format: hugo
draft: true
---



## Contextualização


## Download dos dados


```r
# data
download.file("https://geo.fbds.org.br/SP/RIO_CLARO/USO/SP_3543907_USO.dbf", "/home/mude/Downloads/SP_3543907_USO.dbf", mode = "wb")
download.file("https://geo.fbds.org.br/SP/RIO_CLARO/USO/SP_3543907_USO.prj", "/home/mude/Downloads/SP_3543907_USO.prj", mode = "wb")
download.file("https://geo.fbds.org.br/SP/RIO_CLARO/USO/SP_3543907_USO.shp", "/home/mude/Downloads/SP_3543907_USO.shp", mode = "wb")
download.file("https://geo.fbds.org.br/SP/RIO_CLARO/USO/SP_3543907_USO.shx", "/home/mude/Downloads/SP_3543907_USO.shx", mode = "wb")
```

## Importar dados


```r
rc <- sf::st_read("/home/mude/Downloads/SP_3543907_USO.shp") %>%
    dplyr::filter(CLASSE_USO == "formação florestal")

tm_shape(rc) +
    tm_fill(fill = "forestgreen")
```

## Amostragem dos pontos e buffers


```r
# buffers
set.seed(42)
po <- sf::st_sample(x = rc, size = 10) %>%
    sf::st_buffer(1e3) %>%
    sf::st_as_sf() %>%
    dplyr::mutate(area_ha = sf::st_area(.)/1e4,
                  porcentagem = NA)
po

tm_shape(rc) +
    tm_fill(fill = "forestgreen") +
    tm_shape(po) +
    tm_borders(col = "red")
```

## Quantidade de habitat


```r
# habitat amount
rc_po <- NULL
for(i in 1:nrow(po)){
    
    po_i <- po[i,]
    rc_po_i <- sf::st_as_sf(sf::st_union(sf::st_intersection(rc, po_i)))
    rc_po <- rbind(rc_po, rc_po_i)
    rc_po_area <- sf::st_area(rc_po_i)/1e4
    po[i,]$porcentagem <- round(rc_po_area/po[i, ]$area_ha*100, 2)
    
}
po

map_habitat_amount <- tm_shape(rc) +
    tm_fill(fill = "gray") +
    tm_shape(rc_po) +
    tm_fill(fill = "forestgreen") +
    tm_shape(po) +
    tm_borders(col = "red") +
    tm_text(text = "porcentagem")
map_habitat_amount
```
