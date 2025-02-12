---
title: "Big Data no R: como ler um conjunto de dados maior que a RAM"
subtitle: "Importar e manejar grandes volumes de dados no R"
summary: "Importar e manejar grandes volumes de dados no R"
author: Maurício Vancine
date: "2024-08-24"
publishDate: r`Sys.time()`
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: r-big-data
links:
categories: 
  - Blog
tags:
  - R
  - Big Data
  - arrow
  - vroom
featured: yes
format: hugo
draft: false
---



## Contextualização

A Ciência de Dados (*Data Science*) é uma área de conhecimento que vem ganhando notoriedade, principalmente na era digital e pelo grande volume de dados gerados, com o uso de diversos algoritmos matemáticos para análise de dados. Podemos dizer que Ciência de Dados é composta por três componentes principais: *Big Data*, *Machine Learning* e *Internet of Things*.

Neste post, vou falar sobre *Big Data*, que geralmente se refere a volumes massivos de dados que não são facilmente manipulados pelas ferramentas e práticas de dados usuais, como uma planilha eletrônica, por exemplo.

Na Ecologia, diversos estudos (confira o final do post) têm abordado esse tema, mas aqui gostaria de falar especificamente de como trabalhar com esses dados no R.

Quando importamos um conjunto de dados de uma planilha eletrônica para o R, ele aloca esses dados na memória RAM (espaço temporário de armazenamento). 

Dessa forma, se eu tenho um computador com 16 Gb de RAM, em teoria eu poderia importar e manejar um conjunto de dados de 16 Gb. Entretanto, na prática, a quantidade de memória disponível para o R é menor do que a quantidade total de RAM, pois parte dela é usada pelo sistema operacional e outros processos. Uma parte da memória RAM está sempre sendo usada pelo sistema operacional, e além disso, cada nova atribuição de dados no R vai necessitar alocar o objeto em uma nova parte da RAM.

Verifique a quantidade de memória RAM do seu computador no R:


``` r
# install.packages(memuse)
memuse::Sys.meminfo()
```

```
## Totalram:  15.461 GiB 
## Freeram:    6.066 GiB
```

Há diversas opções para contornar essa limitação e trabalhar com dados gigantes no R, mas aqui vou explorar um pacote específico e um conjunto de dados que tive que trabalhar recentemente.

## eBird

O [eBird](https://ebird.org/home) é um empreendimento coletivo que adota uma abordagem inovadora para a ciência cidadã para a observação de aves. O eBird é gerenciado pelo Cornell Lab of Ornithology. Seu objetivo é aumentar a quantidade de dados por meio do recrutamento e engajamento de participantes globalmente, além de quantificar e controlar problemas de qualidade de dados. 

Os dados do eBird estão disponíveis de forma aberta e são utilizados por um amplo espectro de estudantes, professores, cientistas, ONGs, agências governamentais, gestores de terras e formuladores de políticas. Como resultado, o eBird se tornou uma importante fonte de dados de biodiversidade, aumentando nosso conhecimento sobre as dinâmicas de distribuição de espécies e tendo um impacto direto na conservação de aves e seus habitats.

## eBird e GBIF

O [GBIF](https://www.gbif.org) (Sistema Global de Informação sobre Biodiversidade) é uma rede internacional e infraestrutura de dados financiada por governos de todo o mundo, com o objetivo de dar a qualquer pessoa, em qualquer lugar, acesso aberto a dados sobre toda a vida na Terra. 

Mas ele também disponibiliza os dados do eBird do mundo todo, através do [EOD – eBird Observation Dataset](https://www.gbif.org/pt/dataset/4fa7b334-ce0d-4e88-aaae-2e0c138d049e#description).

Esse conjunto de dados possui atualmente 1.512.208.412 ocorrências, com dados desde 1 de janeiro de 1800 a 31 de dezembro de 2023.

Para citar esse conjunto de dados:

> Auer T, Barker S, Barry J, Charnoky M, Curtis J, Davies I, Davis C, Downie I, Fink D, Fredericks T, Ganger J, Gerbracht J, Hanks C, Hochachka W, Iliff M, Imani J, Jordan A, Levatich T, Ligocki S, Long M T, Morris W, Morrow S, Oldham L, Padilla Obregon F, Robinson O, Rodewald A, Ruiz-Gutierrez V, Schloss M, Smith A, Smith J, Stillman A, Strimas-Mackey M, Sullivan B, Weber D, Wolf H, Wood C (2024). EOD – eBird Observation Dataset. Cornell Lab of Ornithology. Occurrence dataset https://doi.org/10.15468/aomfnb accessed via GBIF.org on 2024-08-23.

Esses dados estão disponíveis em um único arquivo no formato CSV (Comma-Separated Values) ou valores separados por vírgula (.csv), que possui 824 Gb, que é muito mais do que geralmente os computadores têm de memória RAM.

Sendo assim, precisamos de um pacote específico para importar e manejar esses dados.

## Importar e manejar esses dados

Aqui, vamos utilizar o pacote [arrow](https://arrow.apache.org/docs/r). Esse pacote fornece acesso a recursos da biblioteca Apache Arrow C++. O objetivo do arrow é fornecer um backend Arrow C++ para o dplyr e acesso à biblioteca Apache Arrow C++ através de funções familiares do base R e do tidyverse, ou classes R6. O projeto Arrow oferece funcionalidades para uma ampla gama de tarefas de análise de dados, permitindo armazenar, processar e mover dados rapidamente.

Para mais detalhes do funcionamento do pacote arrow, consultar o capítulo [22  Arrow](https://cienciadedatos.github.io/pt-r4ds/arrow.html) do [R para Ciência de Dados 2ªed](https://cienciadedatos.github.io/pt-r4ds/).

Vamos ler os dados:


``` r
# packages
library(tidyverse)
library(arrow)

# ebird
ebird_data <- arrow::open_delim_dataset("0043987-240626123714530.csv", 
                                        parse_options = csv_parse_options(
                                            delimiter = "\t", 
                                            newlines_in_values = TRUE),
                                        read_options = list(
                                            block_size = 1000000000L, 
                                            use_threads = TRUE))
ebird_data
```

Esse banco de dados é cheio de problemas, então tive que fazer alguns testes com vários parâmetros para fazer com que a leitura funcionasse.

O código acima apenas lê os dados sem carregá-los completamente na memória do R. Dessa forma, com os códigos abaixo é possível fazer um filtro dos dados que precisamos, por exemplo, para o joão-de-barro (*Furnarius rufus*) [adoro esse bicho], depois de 1985 e para algumas colunas de interesse.


``` r
# filter
ebird_data_filter <- ebird_data %>% 
    dplyr::filter(species == "Furnarius rufus",
                  year >= 1985) %>% 
    dplyr::select(species, decimalLongitude, decimalLatitude, year) %>%  
    dplyr::collect()
ebird_data_filter
```

Entretanto, mesmo num notebook parrudo (Intel i7 e 64 Gb de RAM) demorou 2:45 h para fazer o filtro.

Acabei atribuindo os dados a um objeto, mas talvez fosse mais interessante exportar o arquivo diretamente para evitar o uso excessivo de memória.


``` r
# filter
ebird_data %>% 
    dplyr::filter(species == "Furnarius rufus",
                  year >= 1985) %>% 
    dplyr::select(species, decimalLongitude, decimalLatitude, year) %>% 
    readr::write("ebird_furnarius_rufus.csv")
```

Há ainda muitos pontos para eu estudar do pacote arrow, como o formato [parquet](https://parquet.apache.org/), que parece ser muito mais interessante do que o CSV. Sendo assim, vale ler mais o capítulo [22  Arrow](https://cienciadedatos.github.io/pt-r4ds/arrow.html) do [R para Ciência de Dados 2ªed](https://cienciadedatos.github.io/pt-r4ds/).

## Saiba mais 

Farley, S.S., Dawson, A., Goring, S.J. & Williams, J.W. (2018). Situating Ecology as a Big-Data Science: Current Advances, Challenges, and Solutions. BioScience, 68, 563–576.

Hampton, S.E., Strasser, C.A., Tewksbury, J.J., Gram, W.K., Budden, A.E., Batcheller, A.L., et al. (2013). Big data and the future of ecology. Frontiers in Ecology and the Environment, 11, 156–162.

Nimmagadda, S.L., Reiners, T. & Rudra, A. (2017). Development of a Total Environment Data Science Approach in a Big Data Scale. Procedia Computer Science, Knowledge-Based and Intelligent Information & Engineering Systems: Proceedings of the 21st International Conference, KES-20176-8 September 2017, Marseille, France, 112, 1891–1900.

Fonte da imagem: [Sergei Starostin/Pexels](https://www.pexels.com/pt-br/foto/computador-salgadinhos-memoria-lembranca-6636474).
