---
title: Principais repositórios de dados para publicação
subtitle: "Lista dos principais repositórios de dados para publicação"
summary: "Lista das principais repositórios de dados para publicação"
author: Maurício Vancine
date: "2025-01-03"
publishDate: r`Sys.time()` 
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: pub-data-repo
links:
categories:
  - Blog
tags:
  - Repositório
  - Conjunto de dados
  - Ciência aberta
featured: yes
format: hugo
draft: false
---

## Contextualização

Disponibilizar dados dos artigos publicados é uma ótima forma de aumentar a reprodutibilidade e acesso aos dados. Entretanto, essa é não é uma tarefa muito fácil, principalmente se a intenção a disponibilida de grandes conjuntos de dados.

Para um tabela simples com poucas linhas e colunas a tarefa pode ser realizada no [GitHub](), por exemplo, mas no meu caso, onde eu tinha mais de 250 GB de camadas rasters, a coisa ficou um pouco mais complicada.

Eu optei por disponibilizar os dados no [Zenodo](https://zenodo.org), mas antes de chegar a ele, fiz uma busca de vários repositórios de dados, os quais eu listo aqui.

## Principais repositórios de dados 

Fiz uma tabela com informações sobre os principais repositórios, incluindo detalhes sobre o tamanho do repositório, limites de tamanho de arquivos e quantidade de arquivos.


|Repositório                  |Descrição                                                               |Limite de tamanho por arquivo                                                                     |Limite de tamanho por repositório                                                                                    |Características principais                                                                                 |
|:----------------------------|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
|[Zenodo](https://zenodoorg)  |Mantido pelo CERN; suporta dados de todas as áreas de pesquisa          |Até 50 GB por arquivo                                                                             |Limite total de armazenamento de 50 GB por repositório; máximo de 100 arquivos; mas sujeito a políticas de uso justo |Integração com GitHub; atribuição de DOI; compartilhamento gratuito                                        |
|[Figshare](https://figsharecom)|Compartilhamento de dados de pesquisa; documentos; apresentações e mais |Até 5 GB por arquivo para usuários gratuitos; até 20 GB para usuários institucionais              |Limite total de armazenamento de 20 GB para usuários gratuitos; ilimitado para usuários institucionais               |Fácil visualização de arquivos; suporte para muitos formatos; atribuição de DOI                            |
|[Dryad](https://datadryadorg)|Voltado para dados associados a artigos científicos                     |Até 10 GB por arquivo; arquivos maiores podem ser considerados mediante solicitação               |Sem limite explícito; mas taxas adicionais podem ser aplicadas para grandes volumes de dados                         |Focado em dados biológicos e ambientais; metadados detalhados; requer taxa para publicação em alguns casos |
|[Open Science Framework (OSF)](https://osfio)|Repositório e plataforma colaborativa para projetos científicos         |Até 5 GB por arquivo                                                                              |Limite total de armazenamento de 50 GB para usuários gratuitos; planos pagos disponíveis para mais armazenamento     |Integração com ferramentas como GitHub; Google Drive e Dropbox; suporte para projetos interdisciplinares   |
|[Harvard Dataverse](https://dataverseharvardedu)|Parte do Dataverse Project; suporta múltiplas disciplinas               |Até 2 GB por arquivo; arquivos maiores podem ser carregados via API ou ferramentas especializadas |Sem limite explícito para o conjunto de dados                                                                        |Metadados detalhados; foco em dados de pesquisa; gratuito para compartilhar                                |
|[Mendeley Data](https://datamendeleycom)|Plataforma para compartilhar conjuntos de dados em diversos formatos    |Até 10 GB por conjunto de dados para contas pessoais; até 100 GB para contas institucionais       |Até 10 GB por conjunto de dados para contas pessoais; até 100 GB para contas institucionais                          |Oferecido pela Elsevier; integração com artigos científicos publicados na plataforma                       |
|[PANGAEA](https://wwwpangaeade)|Repositório para dados de ciências da Terra e meio ambiente             |Não especificado publicamente; recomenda-se contato para dados muito grandes                      |Sem limite explícito; mas grandes volumes devem ser discutidos com os administradores                                |Focado em dados ambientais; integração com artigos científicos e periódicos específicos                    |
|[ScienceBase](https://wwwsciencebasegov)|Repositório para dados ambientais e geológicos; mantido pelo USGS       |Não especificado publicamente                                                                     |Não especificado publicamente                                                                                        |Focado em dados geoespaciais; suporte para diversas áreas ambientais                                       |
|[Kaggle Datasets](https://wwwkagglecom/datasets)|Plataforma para compartilhamento de conjuntos de dados                  |Até 20 GB por arquivo                                                                             |Limite total de 100 GB por conjunto de dados                                                                         |Popular entre cientistas de dados; fácil acesso a dados para aprendizado de máquina e análise              |
|[DataCite Search](https://searchdataciteorg)|Agregador de repositórios que utilizam DOIs para dados científicos      |Não aplicável                                                                                     |Não aplicável                                                                                                        |Permite localizar conjuntos de dados em múltiplos repositórios                                             |

Fonte da imagem: [freepik](https://www.freepik.com/free-vector/server-concept-illustration_5357389.htm?log-in=google#fromView=search&page=1&position=10&uuid=5e151ded-9f1e-4a2d-9671-66c1b46cd933&new_detail=true).
