---
title: Fontes de dados de biodiversidade 
subtitle: "Lista das principais fontes e pacotes do R de dados de biodiversidade"
summary: "Lista das principais fontes e pacotes do R de dados de biodiversidade"
author: Maurício Vancine
date: "2024-10-06"
publishDate: r`Sys.time()` 
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: eco-dados-biodiversidade
links:
categories:
  - Blog
tags:
  - Compilação
  - Biodiversidade
  - Ocorrências
  - Atributos funcionais
  - Vocalização
  - Biogegrafia
  - Filogenia
  - Genética
featured: yes
format: hugo
draft: false
---



## Contextualização

Desde minha graduação, sempre trabalhei com dados secundários. Dados secundários são dados que alguém coletou em campo e que você organizou. 

Dados primários são dados que você mesmo coletou em campo. E como "dados são o novo ouro" como dizem por aí, nada melhor que ter isso junto num único lugar.

Pensando nisso, escrevi esse post para reunir as bases de dados e artigos que conheço, com muita ajuda do [Thiago Gonçalvez Souza](https://lsa.umich.edu/eeb/people/postdoctoral-fellows/thiago-goncalves-souza.html). Também listei os pacotes no R que fazem essa busca. 

## Dados de ocorrências


|Bases de dados                                                    |Descrição |
|:-----------------------------------------------------------------|:---------|
|[speciesLink](https://specieslink.net/)                           |          |
|[Plataforma SALVE](https://salve.icmbio.gov.br)                   |          |
|[Portal da Biodiversidade](https://portaldabiodiversidade.icmbio.gov.br/portal/)|          |
|[Plataforma de Biodiversidade do Brasil (SiBBr)](https://www.sibbr.gov.br/)|          |
|[Global Biodiversity Information Facility (GBIF)](https://www.gbif.org/)|          |
|[eBird](https://ebird.org/home)                                   |          |
|[AntWeb](https://www.antweb.org/)                                 |          |
|[iNaturalist](https://www.inaturalist.org)                        |          |
|[VertNet](https://vertnet.org)                                    |          |
|[Integrated Digitized Biocollections (iDigBio)](https://www.idigbio.org)|          |
|[Berkeley Ecoinformatics Engine (EcoEngine)](https://ecoengine.berkeley.edu)|          |
|[BIEN](https://bien.nceas.ucsb.edu/bien/)                         |          |
|[New York Botanical Garden](http://www.nybg.org)                  |          |
|[Missouri Botanical Garden](http://www.missouribotanicalgarden.org)|          |
|[SALVIAS (Enquist & Boyle 2012)](http://www.salvias.net)          |          |
|[Tropical Ecology Assessment and Monitoring Network (Fegraus 2012)](http://www.teamnetwork.org)|          |
|[University of Arizona](https://ag.arizona.edu/herbarium)         |          |
|[VegBank](http://vegbank.org)                                     |          |
|[University of Texas at Austin](http://prc-symbiota.tacc.utexas.edu)|          |
|[Botanical Research Institute of Texas](http://www.brit.org)      |          |
|[Forest Inventory and Analysis National Program (USA)(2013)](http://www.fia.fs.fed.us)|          |
|[Naturalis](http://www.naturalis.nl)                              |          |
|[University of British Columbia](http://www.biodiversity.ubc.ca/museum/herbarium)|          |
|[Acadia University](http://herbarium.acadiau.ca)                  |          |
|[University of Manitoba](http://winherbarium.weebly.com)          |          |
|[Carolina Vegetation Survey (Peetet al. 2012a)](http://cvs.bio.unc.edu)|          |
|[University of North Carolina](http://www.herbarium.unc.edu)      |          |
|[Université Laval](http://www.herbier.ulaval.ca)                  |          |
|[OBIS](https://obis.org/)                                         |          |

## Dados de ciência cidadã


|Bases de dados |Descrição |
|:--------------|:---------|
|[Táxeus](https://www.taxeus.com.br)|          |
|[eBird](https://ebird.org/home)|          |
|[iNaturalist](https://www.inaturalist.org)|          |
|[Wikiaves](https://www.wikiaves.com.br)|          |
|[Xeno-canto](https://xeno-canto.org)|          |

## Dados de comunidades ecológicas


|Bases de dados                                                          |Descrição |
|:-----------------------------------------------------------------------|:---------|
|[ATLANTIC AMPHIBIANS](https://doi.org/10.1002/ecy.2392)                 |          |
|[ATLANTIC ANTS](https://doi.org/10.1002/ecy.3580)                       |          |
|[ATLANTIC BATS](https://doi/10.1002/ecy.2007)                           |          |
|[ATLANTIC BIRDS](https://doi/10.1002/ecy.2119)                          |          |
|[ATLANTIC BIRD TRAITS](https://doi/10.1002/ecy.2647)                    |          |
|[ATLANTIC BUTTERFLIES](https://doi/10.1002/ecy.2507)                    |          |
|[ATLANTIC CAMTRAPS](https://doi/10.1002/ecy.1998)                       |          |
|[Camera trap surveys of Atlantic Forest mammals](https://doi.org/10.1002/ecy.4298)|          |
|[ATLANTIC EPIPHYTES](https://doi/10.1002/ecy.2541)                      |          |
|[Atlantic flower--invertebrate interactions](https://doi/10.1002/ecy.2541)|          |
|[ATLANTIC FRUGIVORY](https://doi/10.1002/ecy.1818)                      |          |
|[ATLANTIC MAMMALS](https://esajournals.doi/abs/10.1002/ecy.2785)        |          |
|[ATLANTIC MAMMAL TRAITS](https://doi/10.1002/ecy.2106)                  |          |
|[Non-volant mammals from the Upper Paraná River Basin](https://doi/10.1002/ecy.2107)|          |
|[ATLANTIC POLLINATION](https://doi/abs/10.1002/ecy.3595)                |          |
|[ATLANTIC PRIMATES](https://doi/10.1002/ecy.2525)                       |          |
|[ATLANTIC SMALL-MAMMAL](https://doi/10.1002/ecy.1893)                   |          |
|[Abundance of small mammals in the Atlantic Forest (ASMAF)](https://doi/10.1002/ecy.2005)|          |
|[AMAZONIA CAMTRAP](https://doi/abs/10.1002/ecy.3738)                    |          |
|[Amazonian amphibians](https://bdj.pensoft.net/article/109785/)         |          |
|[Plant-galling insect interactions](https://doi.org/10.1002/ecy.3149)   |          |
|[BRAZIL ROAD‐KILL](https://doi/10.1002/ecy.2464)                        |          |
|[VTMaxHerp](https://doi.org/10.1002/ecy.3602)                           |          |
|[SIA-BRA](https://doi.org/10.1111/geb.13449)                            |          |
|[Jaguar movement database](https://doi/10.1002/ecy.2379)                |          |
|[NEOTROPICAL CARNIVORES](https://esajournals.doi/abs/10.1002/ecy.3128)  |          |
|[NEOTROPICAL ALIEN MAMMALS](https://esajournals.doi/abs/10.1002/ecy.3115)|          |
|[NEOTROPICAL XENARTHRANS](https://esajournals.doi/abs/10.1002/ecy.2663) |          |
|[NEOTROPICAL FRESHWATER FISHES](https://doi.org/10.1002/ecy.3713)       |          |
|[Species composition and abundance of mammalian communities](https://doi.org/10.1890/11-0262.1)|          |
|[PanTHERIA](https://doi.org/10.1890/08-1494.1)                          |          |
|[Matrix population models from 20 studies of perennial plant populations]( https://doi.org/10.1890/11-1052.1)|          |
|[Global rheophytes data set]( https://doi.org/10.1002/ecy.3056)         |          |

## Dados de taxonomia


|Bases de dados                 |Descrição |
|:------------------------------|:---------|
|[Amphibian Species of the World](https://amphibiansoftheworld.amnh.org/)|          |
|[AmphibiaWeb](https://amphibiaweb.org/)|          |
|[ReptileDB](http://www.reptile-database.org/)|          |
|[AntWeb](https://www.antweb.org/)|          |
|[Programa REFLORA](https://floradobrasil.jbrj.gov.br/reflora/PrincipalUC/PrincipalUC.do)|          |
|[World Flora Online](https://www.worldfloraonline.org/)|          |
|[The Plant List](https://wfoplantlist.org/)|          |

## Dados de biogeografia


|Bases de dados                                    |Descrição |
|:-------------------------------------------------|:---------|
|[Biogeografia da Flora e Fungos do Brasil](https://biogeo.inct.florabrasil.net/)|          |
|[biodiversitymapping.org](https://biodiversitymapping.org/)|          |
|[Map of Life (MOL)](https://mol.org/)             |          |
|[Global Assessment of Reptile Distributions (GARD)](http://www.gardinitiative.org/)|          |

## Dados de movimento


|Bases de dados |Descrição |
|:--------------|:---------|
|[Movebank](https://www.movebank.org/cms/movebank-main)|          |

## Dados de vocalização


|Bases de dados |Descrição |
|:--------------|:---------|
|[Wikiaves](https://www.wikiaves.com.br)|          |
|[Xeno-canto](https://xeno-canto.org)|          |

## Dados de traços funcionais


|Bases de dados                                                                          |Descrição                                         |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------|
|[AmphiBIO]( https://doi.org/10.1038/sdata.2017.123)                                     |Banco de dados de traits de plantas para os Andes |
|[SpiderTraits](https://doi.org/10.1093/database/baab064)                                |                                                  |
|[GlobalAnts](https://doi.org/10.1111/icad.12211)                                        |                                                  |
|[TRY](https://doi.org/10.1111/gcb.14904)                                                |                                                  |
|[LizardTraits](https://doi.org/10.1111/geb.12773)                                       |                                                  |
|[EltonTraits](https://doi.org/10.1890/13-1917.1)                                        |                                                  |
|[TetrapodTraits](https://doi.org/10.1371/journal.pbio.3002658)                          |                                                  |
|[Body sizes and diversification rates of lizards, snakes, amphisbaenians and the tuatara]( https://doi.org/10.1111/geb.12398)|                                                  |
|[]()                                                                                    |                                                  |
|[]()                                                                                    |                                                  |
|[]()                                                                                    |                                                  |
|[]()                                                                                    |                                                  |
|[]()                                                                                    |                                                  |
|[FunAndes – A functional trait database of Andean plants](https://www.nature.com/articles/s41597-022-01626-6)|                                                  |
|[AVONET](https://opentraits.org/datasets/avonet.html)                                   |                                                  |

## Dados filogenéticos


|Bases de dados |Descrição |
|:--------------|:---------|
|[phylomeDB](https://phylomedb.org)|          |

## Dados genéticos


|Bases de dados                                                        |Descrição |
|:---------------------------------------------------------------------|:---------|
|[genbank](https://www.ncbi.nlm.nih.gov/genbank/)                      |          |
|[Sistema de Informação de Coleções de Interesse Biotecnológico (SICol)](https://sicol.cria.org.br/)|          |

## Pacotes no R


|Bases de dados |Descrição |
|:--------------|:---------|
|[spocc](https://cloud.r-project.org/web/packages/spocc/index.html)|          |
|[rgbif](https://cran.r-project.org/web/packages/rgbif/index.html)|          |
|[rebird](https://cran.r-project.org/web/packages/rebird/index.html)|          |
|[rvertnet](https://cran.r-project.org/web/packages/rvertnet/index.html)|          |
|[ridigbio](https://cran.r-project.org/web/packages/ridigbio/index.html)|          |
|[ecoengine](https://cran.r-project.org/web/packages/ecoengine/index.html)|          |
|[robis](https://cloud.r-project.org/web/packages/robis/index.html)|          |
|[BIEN](https://cran.r-project.org/web/packages/BIEN/index.html)|          |
|[taxize](https://cloud.r-project.org/web/packages/taxize/index.html)|          |
|[AmphiNom](https://github.com/hcliedtke/AmphiNom)|          |
|[flora](https://cran.r-project.org/web/packages/flora/index.html)|          |
|[WorldFlora](https://cran.r-project.org/web/packages/WorldFlora/index.html)|          |

## Artigos

Bello, C., Galetti, M., Montan, D., Pizo, M. A., Mariguela, T. C., Culot, L., Bufalo, F., Labecca, F., Pedrosa, F., Constantini, R., Emer, C., Silva, W. R., da Silva, F. R., Ovaskainen, O., & Jordano, P. (2017). Atlantic frugivory: A plant-frugivore interaction data set for the Atlantic Forest. Ecology, 98(6), 1729–1729. https://doi.org/10.1002/ecy.1818

Boscolo, D., Nobrega Rodrigues, B., Ferreira, P. A., Lopes, L. E., Tonetti, V. R., Reis dos Santos, I. C., Hiruma-Lima, J. A., Nery, L., Baptista de Lima, K., Perozi, J., Freitas, A. V. L., Viana, B. F., Antunes-Carvalho, C., Amorim, D. de S., Freitas de Oliveira, F., Groppo, M., Absy, M. L., de Almeida-Scabbia, R. J., Alves-Araújo, A., … Ribeiro, M. C. (2023). Atlantic flower–invertebrate interactions: A data set of occurrence and frequency of floral visits. Ecology, 104(3), e3900. https://doi.org/10.1002/ecy.3900

Bovendorp, R. S., Villar, N., de Abreu-Junior, E. F., Bello, C., Regolin, A. L., Percequillo, A. R., & Galetti, M. (2017). Atlantic small-mammal: A dataset of communities of rodents and marsupials of the Atlantic forests of South America. Ecology, 98(8), 2226–2226. https://doi.org/10.1002/ecy.1893

Culot, L., Pereira, L. A., Agostini, I., Almeida, M. A. B., Alves, R. S. C., Aximoff, I., Bager, A., Baldovino, M. C., Bella, T. R., Bicca‐Marques, J. C., Braga, C., Brocardo, C. R., Campelo, A. K. N., Canale, G. R., Cardoso, J. da C., Carrano, E., Casanova, D. C., Cassano, C. R., Castro, E., … Galetti, M. (2019). ATLANTIC PRIMATES: a dataset of communities and occurrences of primates in the Atlantic Forests of South America. Ecology, 100(1). https://doi.org/10.1002/ecy.2525

Figueiredo, M. S. L., Barros, C. S., Delciellos, A. C., Guerra, E. B., Cordeiro-Estrela, P., Kajin, M., Alvarez, M. R., Asfora, P. H., Astúa, D., Bergallo, H. G., Cerqueira, R., Geise, L., Gentile, R., Grelle, C. E. V., Iack-Ximenes, G. E., Oliveira, L. C., Weksler, M., & Vieira, M. V. (2017). Abundance of small mammals in the Atlantic Forest (ASMAF): A data set for analyzing tropical community patterns. Ecology, 98(11), 2981–2981. https://doi.org/10.1002/ecy.2005

Franceschi, I. C., Dornas, R. A. da P., Lermen, I. S., Coelho, A. V. P., Vilas Boas, A. H., Chiarello, A. G., Paglia, A. P., de Souza, A. C., Borsekowsky, A. R., Rocha, A., Bager, A., de Souza, A. Z., Lopes, A. M. C., de Moura, A. S., Ferreira, A. S., García-Olaechea, A., Delciellos, A. C., Bacellar, A. E. de F., Campelo, A. K. N., … Coelho, I. P. (2024). Camera trap surveys of Atlantic Forest mammals: A data set for analyses considering imperfect detection (2004–2020). Ecology, n/a(n/a), e4298. https://doi.org/10.1002/ecy.4298

Gonçalves, F., Bovendorp, R. S., Beca, G., Bello, C., Costa-Pereira, R., Muylaert, R. L., Rodarte, R. R., Villar, N., Souza, R., Graipel, M. E., Cherem, J. J., Faria, D., Baumgarten, J., Alvarez, M. R., Vieira, E. M., Cáceres, N., Pardini, R., Leite, Y. L. R., Costa, L. P., … Galetti, M. (2018). ATLANTIC MAMMAL TRAITS: A data set of morphological traits of mammals in the Atlantic Forest of South America. Ecology, 99(2), 498–498. https://doi.org/10.1002/ecy.2106
Gonçalves, F., Hannibal, W., Godoi, M. N., Martins, F. I., Oliveira, R. F., Figueiredo, V. V., Casella, J., & de Sá, É. F. G. G. (2018). Non-volant mammals from the Upper Paraná River Basin: A data set from a critical region for conservation in Brazil. Ecology, 99(2), 499–499. https://doi.org/10.1002/ecy.2107

Hasui, É., Metzger, J. P., Pimentel, R. G., Silveira, L. F., Bovo, A. A. d. A., Martensen, A. C., Uezu, A., Regolin, A. L., Bispo de Oliveira, A. Â., Gatto, C. A. F. R., Duca, C., Andretti, C. B., Banks-Leite, C., Luz, D., Mariz, D., Alexandrino, E. R., de Barros, F. M., Martello, F., Pereira, I. M. d. S., … Ribeiro, M. C. (2018). ATLANTIC BIRDS: A data set of bird species from the Brazilian Atlantic Forest. Ecology, 99(2), 497–497. https://doi.org/10.1002/ecy.2119
Iamara-Nogueira, J., Targhetta, N., Allain, G., Gambarini, A., Pinto, A. R., Rui, A. M., Araújo, A. C., Lopes, A., Pereira-Silva, B., de Camargo, B. B., Machado, C. G., Missagia, C., Scultori, C., Boscolo, D., Fischer, E., Araújo-Oliveira, E. S., Gava, H., Paulino-Neto, H. F., Machado, I. C., … Buzato, S. (2022). ATLANTIC POLLINATION: A data set of flowers and interaction with nectar-feeding vertebrates from the Atlantic Forest. Ecology, 103(2), e03595. https://doi.org/10.1002/ecy.3595

Lima, F., Beca, G., Muylaert, R. L., Jenkins, C. N., Perilli, M. L. L., Paschoal, A. M. O., Massara, R. L., Paglia, A. P., Chiarello, A. G., Graipel, M. E., Cherem, J. J., Regolin, A. L., Oliveira Santos, L. G. R., Brocardo, C. R., Paviolo, A., Di Bitetti, M. S., Scoss, L. M., Rocha, F. L., Fusco-Costa, R., … Galetti, M. (2017). ATLANTIC-CAMTRAPS: A dataset of medium and large terrestrial mammal communities in the Atlantic Forest of South America. Ecology, 98(11), 2979–2979. https://doi.org/10.1002/ecy.1998

Muylaert, R. d. L., Stevens, R. D., Esbérard, C. E. L., Mello, M. A. R., Garbino, G. S. T., Varzinczak, L. H., Faria, D., Weber, M. d. M., Kerches Rogeri, P., Regolin, A. L., Oliveira, H. F. M. d., Costa, L. d. M., Barros, M. A. S., Sabino-Santos, G., Crepaldi de Morais, M. A., Kavagutti, V. S., Passos, F. C., Marjakangas, E.-L., Maia, F. G. M., … Galetti, M. (2017). ATLANTIC BATS: A data set of bat communities from the Atlantic Forests of South America. Ecology, 98(12), 3227–3227. https://doi.org/10.1002/ecy.2007

Ramos, F. N., Mortara, S. R., Monalisa‐Francisco, N., Elias, J. P. C., Neto, L. M., Freitas, L., Kersten, R., Amorim, A. M., Matos, F. B., Nunes‐Freitas, A. F., Alcantara, S., Alexandre, M. H. N., Almeida‐Scabbia, R. J., Almeida, O. J. G., Alves, F. E., Oliveira Alves, R. M., Alvim, F. S., Andrade, A. C. S., Andrade, S., … Ribeiro, M. C. (2019). ATLANTIC EPIPHYTES: a data set of vascular and non‐vascular epiphyte plants and lichens from the Atlantic Forest. Ecology, 100(2), e02541. https://doi.org/10.1002/ecy.2541

Rodrigues, R. C., Hasui, É., Assis, J. C., Pena, J. C. C., Muylaert, R. L., Tonetti, V. R., Martello, F., Regolin, A. L., Costa, T. V. V. da, Pichorim, M., Carrano, E., Lopes, L. E., Vasconcelos, M. F. de, Fontana, C. S., Roos, A. L., Gonçalves, F., Banks‐Leite, C., Cavarzere, V., Efe, M. A., … Ribeiro, M. C. (2019). ATLANTIC BIRD TRAITS: a data set of bird morphological traits from the Atlantic forests of South America. Ecology, e02647. https://doi.org/10.1002/ecy.2647

Santos, J. P. dos, Freitas, A. V. L., Brown, K. S., Carreira, J. Y. O., Gueratto, P. E., Rosa, A. H. B., Lourenço, G. M., Accacio, G. M., Uehara‐Prado, M., Iserhard, C. A., Richter, A., Gawlinski, K., Romanowski, H. P., Mega, N. O., Teixeira, M. O., Moser, A., Ribeiro, D. B., Araujo, P. F., Filgueiras, B. K. C., … Ribeiro, M. C. (2018). Atlantic butterflies: A data set of fruit‐feeding butterfly communities from the Atlantic forests. Ecology, 99(12), 2875–2875. https://doi.org/10.1002/ecy.2507

Silva, R. R., Martello, F., Feitosa, R. M., Silva, O. G. M., do Prado, L. P., Brandão, C. R. F., de Albuquerque, E. Z., Morini, M. S. C., Delabie, J. H. C., dos Santos Monteiro, E. C., Emanuel Oliveira Alves, A., Wild, A. L., Christianini, A. V., Arnhold, A., Casadei Ferreira, A., Oliveira, A. M., Santos, A. D., Galbán, A., de Oliveira, A. A., … Ribeiro, M. C. (2022). ATLANTIC ANTS: A data set of ants in Atlantic Forests of South America. Ecology, 103(2), e03580. https://doi.org/10.1002/ecy.3580

Souza, Y., Gonçalves, F., Lautenschlager, L., Akkawi, P., Mendes, C., Carvalho, M. M., Bovendorp, R. S., Fernandes-Ferreira, H., Rosa, C., Graipel, M. E., Peroni, N., Cherem, J. J., Bogoni, J. A., Brocardo, C. R., Miranda, J., Silva, L. Z. da, Melo, G., Cáceres, N., Sponchiado, J., … Galetti, M. (2019). ATLANTIC MAMMALS: A data set of assemblages of medium- and large-sized mammals of the Atlantic Forest of South America. Ecology, 100(10), e02785. https://doi.org/10.1002/ecy.2785

Tobias, J. A., Sheard, C., Pigot, A. L., Devenish, A. J. M., Yang, J., Sayol, F., Neate‐Clegg, M. H. C., Alioravainen, N., Weeks, T. L., Barber, R. A., Walkden, P. A., MacGregor, H. E. A., Jones, S. E. I., Vincent, C., Phillips, A. G., Marples, N. M., Montaño‐Centellas, F. A., Leandro‐Silva, V., Claramunt, S., … Schleuning, M. (2022). AVONET: Morphological, ecological and geographical data for all birds. Ecology Letters, 25(3), 581–597. https://doi.org/10.1111/ele.13898

Vancine, M. H., Duarte, K. da S., de Souza, Y. S., Giovanelli, J. G. R., Martins-Sobrinho, P. M., López, A., Bovo, R. P., Maffei, F., Lion, M. B., Ribeiro Júnior, J. W., Brassaloti, R., da Costa, C. O. R., Sawakuchi, H. O., Forti, L. R., Cacciali, P., Bertoluci, J., Haddad, C. F. B., & Ribeiro, M. C. (2018). ATLANTIC AMPHIBIANS: A data set of amphibian communities from the Atlantic Forests of South America. Ecology, 99(7), 1692–1692. https://doi.org/10.1002/ecy.2392

Fonte da imagem: [Diana/Pexels](https://www.pexels.com/pt-br/foto/colecao-beetle-2694485).
