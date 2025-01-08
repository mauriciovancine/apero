---
title: "QGIS: plugins"
subtitle: "Uma lista dos principais plugins do QGIS"
summary: "Uma lista dos principais plugins do QGIS"
author: Maurício Vancine
date: "2025-01-03"
publishDate: r`Sys.time()`
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: r-big-data
links:
categories: 
  - Blog
tags:
  - QGIS
  - Plugins
featured: yes
format: hugo
draft: true
---



## Contextualização

Os **plugins do QGIS** são extensões que expandem as funcionalidades nativas da plataforma, tornando-a ainda mais poderosa e flexível para análises espaciais, visualização de dados e aplicações específicas. 

Como o QGIS é um software de código aberto, sua arquitetura modular permite que a comunidade de usuários e desenvolvedores contribua constantemente com novos plugins para atender às demandas em diversas áreas, como mapeamento interativo, geoprocessamento, sensoriamento remoto, análise temporal, gerenciamento de dados espaciais e integração com outras ferramentas.

Os plugins podem ser instalados diretamente no gerenciador de complementos do QGIS, e são classificados em três categorias principais:  

1. **Ferramentas de análise e processamento**  
Plugins como o *Processing Toolbox*, *Zonal Statistics* e *SCP* oferecem algoritmos avançados de geoprocessamento, estatísticas zonais e classificação de imagens de satélite, facilitando análises detalhadas de paisagens, vegetação e uso do solo.

2. **Visualização e apresentação de dados**  
Extensões como o *QGIS2Web*, *TimeManager* e *OpenLayers Plugin* permitem criar mapas interativos, visualizar séries temporais e adicionar camadas de fundo, como Google Maps ou OpenStreetMap, para enriquecer os projetos cartográficos.

3. **Coleta e gestão de dados**  
Ferramentas como o *QField for QGIS*, *DB Manager* e *Points2One* são voltadas para coleta de dados em campo, integração com bancos de dados espaciais e manipulação de pontos para criar linhas e polígonos.

Os plugins também incluem integrações com linguagens e plataformas externas, como o *R Plugin* para análises estatísticas avançadas.

A vasta biblioteca de plugins permite que o QGIS seja usado em uma ampla variedade de aplicações, desde projetos de conservação ambiental até o planejamento urbano, engenharia e gestão de recursos naturais. Essa flexibilidade é um dos principais fatores que contribuem para o crescente uso do QGIS em todo o mundo.

A lista total de plugins pode ser acessa no repositório de plugins: [QGIS Python Plugins Repository](https://plugins.qgis.org/plugins/).

## Principais plugins do QGIS

Aqui, listo os principais plugins.


|Plugin             |Descrição                                                                                                                                 |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
|[GeoReferencer](https://pluginsqgisorg/plugins/Georeferencer/)|Permite georreferenciar imagens raster para coordenadas espaciais                                                                         |
|[QGIS2Web](https://pluginsqgisorg/plugins/qgis2web/)|Gera mapas interativos em HTML, JavaScript e Leaflet para publicação na web                                                               |
|[OpenLayers](https://pluginsqgisorg/plugins/OpenLayers/)|Adiciona camadas de fundo a partir de serviços como OpenStreetMap, Google Maps, Bing, etc.                                                |
|[Processing Toolbox](https://pluginsqgisorg/plugins/processing/)|Oferece algoritmos de geoprocessamento, com integração de bibliotecas e ferramentas externas                                              |
|[SCP](https://pluginsqgisorg/plugins/SemiAutomaticClassificationPlugin/)|Facilita a classificação semiautomática de imagens de satélite (Landsat, Sentinel, etc)                                                   |
|[DB Manager](https://pluginsqgisorg/plugins/db_manager/)|Gestão de bancos de dados espaciais (PostGIS, SpatiaLite, etc) diretamente no QGIS                                                        |
|[MapText](https://pluginsqgisorg/plugins/MapText/)|Adiciona textos dinâmicos e personalizados nos mapas com controle avançado                                                                |
|[R-Plugin](https://pluginsqgisorg/plugins/R/)|Integra o QGIS com a linguagem R para análises avançadas dentro do QGIS                                                                   |
|[Zonal Statistics](https://pluginsqgisorg/plugins/zonal_statistics/)|Calcula estatísticas de zonas dentro de áreas de interesse (polígonos), útil para dados raster                                            |
|[Points2One](https://pluginsqgisorg/plugins/points2one/)|Converte um conjunto de pontos em uma linha ou polígono, útil em trajetórias ou redes                                                     |
|[TimeManager](https://pluginsqgisorg/plugins/TimeManager/)|Visualiza dados espaciais e temporais, criando animações de séries temporais                                                              |
|[Field Calculator](https://pluginsqgisorg/plugins/field_calculator/)|Permite cálculos e manipulação de atributos dentro das tabelas de atributos                                                               |
|[LRS Plugin](https://pluginsqgisorg/plugins/lrs/)|Trabalha com dados de redes lineares, aplicando referências lineares para análise espacial                                                |
|[MOLUSCE](https://plugins.qgis.org/plugins/molusce/)|Fornece um conjunto de algoritmos para simulações de mudança de uso do solo, como ANN, LR, WoE, MCE e validação usando estatísticas kappa |

## Para saber mais

### Sites

https://www.geoaplicada.com/plugins-essenciais-para-o-qgis/
https://clickgeo.com.br/plugins-python-qgis/
https://www.qgistutorials.com/en/docs/using_plugins.html
https://gis.escoladedados.org/plugins-qgis.html
https://docs.qgis.org/3.34/en/docs/training_manual/qgis_plugins/index.html

### Vídeos


Fonte da imagem: [QGIS](https://www.qgis.org/styleguide).
