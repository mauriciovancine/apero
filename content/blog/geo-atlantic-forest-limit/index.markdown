---
title: Limites da Mata Atlântica
subtitle: "Uma comparação dos diversos limites da Mata Atlântica para diferentes finalidades"
summary: "Uma comparação dos diversos limites da Mata Atlântica para diferentes finalidades"
author: Maurício Vancine
date: "2022-08-10"
publishDate: r`Sys.time()`
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: eco-pai-limites-mata-atlantica
links:
categories:
  - Blog
tags:
  - Biogeografia
  - Bioma
  - Mata Atlântica
  - Limites geográficos
featured: yes
format: hugo
draft: true
---



## Contextualização

Desde minha iniciação científica, eu compilo dados. Inicialmente, comecei compilando dados de amostragem de comunidades de anfíbios para a Mata Atlântica. Desde aquela época sempre foi houve uma dúvida sobre o que iríamos considerar como Mata Atlântica. Ainda lembro de sair da sala, à época meu coorientador o Prof. Célio Haddad, com umas 20 dissertações e teses carregando no braço até o laboratório do meu orientador, Prof. Milton Cezar Ribeiro (Miltinho), uns 200 metros de distância. Talvez meu único trabalho de campo... Enfim, passado a euforia do aceite de realização da iniciação científica (IC), começaram os trabalhos de compilação de dados das comunidades de anfíbios. Logo iria perceber que a tarefa seria mais complexa do que inicialmente havia imaginado. Sempre que eu compilava uma comunidade em uma área que para o Miltinho era Mata Atlântica e caía em área aberta, o Célio falava: "essa comunidade que você inclui não faz parte da Mata Atlântica". Logo notei que definir o que era Mata Atlântica seria fundamental, pois evitaria incorrer nesse tipo de erro, que poderia afetar as análises, principalmente por que iria usar Modelagem de Distribuição de Espécies usando o MaxEnt, que é altamente influenciado pelo limite da área escolhida para criar o modelo. Dessa forma, ara minha IC (2013-2015), decidimos usar um limite mais geral, me contentando com o limite que o Miltinho usou na tese dele.

Anos depois, por volta de 2016 ou 2017, enquanto estava no meu mestrado, nós começamos a compilar dados de uso e cobertura da terra para a Mata Atlântica para atualizar as métricas de paisagem usando os dados mais recentes da Fundação Brasileira para o Desenvolvimento Sustentável (FBDS). Nesse interim de vai e vem de discussões, lembro de um dia comentar: legal gente, mas que limite iremos utilizar para calcular as métricas, uma vez que o Célio, agora meu orientador, sempre me atentava para esse fato: cuidado com o que você vai considerar como Mata Atlântica. Dessas discussões, surgiu a nota que publicamos em 2018. 

Agora no meu doutorado, estamos focados em terminar essas métricas usando dados mais recentes e com mais métricas de paisagem e finalmente finalizar o que iniciamos em 2017. Iremos utilizar um limite concensual, com ajustes refinados para o litoral. 

No entanto, esse assunto dos limites da Mata Atlântica nunca deixou de ser algo que gostaria de explorar com mais profundidade, dado que é um Bioma complexo, com diversas formações únicas, variando desde o litoral com mangues, restigas e costões rochosos, até uma exuberante floresta densa nas partes mais úmidas, florestas mais secas na sua interface com o Cerrado e Caatinga, e ainda uma "intrusão" de florestas mistas de araucárias numa porções mais alta entre o Paraná e Santa Catarina.

Mais recentemente, numa conversa com o Prof. Diogo Provete, ele me perguntou que limite da Mata Atlântica deveria utilizar para algumas análises de Biogeografia. Aí eu perguntei: rapaz, isso vai depender de muitos fatores, como escala espacial, escala temporal, método de análise, objetivo... Vou te mostrar o que eu compilei aqui e você analisa o que faz mais sentido. 

Esse post é um resumo dessa história toda, com a atualização dessa última conversa que tive com o Diogo, que me pediu para registrar isso em algum lugar, porque poderia ser interessante para estudos futuros.

Eu vou fazer mapas de todos os limites que descrever, assim como deixar esses arquivos disponíveis num repositório do GitHub em ESRI Shapefile (.shp) e todos dentro de um Geopackage (.gpkg).

