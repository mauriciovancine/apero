---
title: "Reinstalar pacotes depois de atualizar o R"
subtitle: "Depois de atualizar o R, vem a parte chata de reinstalar todos os pacotes, mas o R mesmo pode te ajudar"
summary: "Depois de atualizar o R, vem a parte chata de reinstalar todos os pacotes, mas o R mesmo pode te ajudar"
author: Maurício Vancine 
date: "2024-06-04"
publishDate: r`Sys.time()`
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: r-reinstall-packages
links:
categories:
  - Blog
tags:
  - r
  - atualizacao
  - pacotes
featured: yes
format: hugo
draft: false
---



## Contextualização

Depois de atualizar uma versão do R, vem a parte chata de reinstalar todos os pacotes. Aqui eu escrevi um código para automatizar essa tarefa.

Isso funciona para os pacotes disponíveis no CRAN. Os pacotes instalados do GitHub, por exemplo, ainda precisarão ser instalados usando os pacotes `devtools` ou  `remotes`.

## Listando os pacotes da versão antiga

Primeiramente, vamos listar os pacotes da versão antiga. Aqui eu estou rodando um exemplo para a versão 4.4 no GNU/Linux. Em outros sistemas operacionais esse diretório tem outro endereço.


``` r
# listar os pacotes instalados na versao 4.4
pkgs <- list.files(path = "~/R/x86_64-pc-linux-gnu-library/4.4")

# vendo os pacotes
head(pkgs)
```

```
## [1] "_cache"    "abc"       "abc.data"  "abind"     "ade4"      "ade4TkGUI"
```

``` r
# contando os pacotes
length(pkgs)
```

```
## [1] 1272
```

## Instalando os pacotes

Agora basta instalar os pacotes, verificando se eles já não estão instalados.


``` r
# verifica e instala os pacotes nao instalados
lapply(pkgs, function(pkg){if(!pkg %in% installed.packages()){install.packages(pkg)}})
```

## Paralelizando

Como esse é um processo demorado um boa opção é fazer a instalação de modo paralelizado.


``` r
# paralelizado
library(furrr)
plan(multisession, workers = 10)

future_map(pkgs, function(pkg){if(!pkg %in% installed.packages()){install.packages(pkg)}})
```

Fonte da imagem: [cottonbro studio/Pexels](https://www.pexels.com/pt-br/@cottonbro/).
