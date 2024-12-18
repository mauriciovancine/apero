---
title: "Gerando QR code no R"
subtitle: "Pacote para gerar QR code no R"
summary: "Pacote para gerar QR code no R"
author: Maurício Vancine
date: "2024-11-08"
publishDate: r`Sys.time()` 
lastUpdated: r`Sys.time()`
layout: single-sidebar
slug: r-qrcode
links:
categories: 
  - Blog
tags:
  - R
  - QR code
featured: yes
format: hugo
draft: false
---



## Contextualização

Faz um tempo que eu tenho compartilhado meus slides através de QR codes no início da apresentação. Isso facilita muito para as pessoas terem acesso aos slides, dado que é quase impossível achar uma pessoa que não tenha um celular.

Há várias ferramentas on-line gratuitas para gerar QR codes, mas porque não gerar um QR code no R, já que eu faço quase tudo nele?

## QR code

Um [QR Code](https://en.wikipedia.org/wiki/QR_code) (*Quick Response Code*) é um tipo de código de barras bidimensional que armazena informações de forma rápida e legível por dispositivos eletrônicos, como câmeras de smartphones. Ele pode conter dados variados, como URLs, textos ou informações de contato, sendo amplamente utilizado para facilitar o acesso a informações digitais ao ser escaneado. [obrigado chatGPT].

## Pacote qrcode

O pacote [qrcode](https://thierryo.github.io/qrcode/index.html) cria códigos QR estáticos em R. O conteúdo do código QR é exatamente o que o usuário define. Não há uma URL de redirecionamento, o que impossibilita rastrear o uso do código QR. Isso permite gerar códigos QR rápidos, gratuitos e amigáveis à privacidade.

Podemos gerar um QR code de forma simples usando a função `qr_code`. Essa função requer dois parâmetros: o URL que iremos direcionar e o nível de correção, que relaciona a quantidade de pixels na QR code gerado.


``` r
library(qrcode)
code <- qrcode::qr_code("QR CODE", ecl = "M")
print(code)
```

```
##               
##  ▗▄▄▄ ▗▖▗▄▄▄  
##  ▐▗▄▐▗▜▙▐▗▄▐  
##  ▐▐█▐▐▚▚▐▐█▐  
##  ▐▄▄▟▐▗▚▐▄▄▟  
##  ▗▗▄▄▝▞▖▗▄▄   
##  ▐▞▄▄▌▜▜▜▖▚▙  
##  ▝▞▟▗▌▄▜▀▖▚▐  
##  ▗▄▄▄▝▗▞▖▚▟▄  
##  ▐▗▄▐▐▚▖▖▜▟▀  
##  ▐▐█▐▐▙▜▜▌▟   
##  ▐▄▄▟▗▟▜▀▜▜▝  
##               
##               
## 
## use plot() for a better quality image
```

Usando `plot()` o QR code fica com uma qualidade maior.


``` r
plot(code)
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" width="672" />

Podemos adicionar uma URL ao QR code.


``` r
url <- "https://mauriciovancine.github.io/blog/2024-11-r-qrcode/"
code <- qrcode::qr_code(url, ecl = "M")
plot(code)
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" width="672" />

Podemos ainda adicionar um logo ao QR code através da função `add_logo`. 


``` r
code_logo <- add_logo(code = code, 
                      logo = "Rlogo.svg", 
                      ecl = "L", hjust = "c", vjust = "c")
plot(code_logo)
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-4-1.png" width="672" />

Por fim, podemos exportar a figura gerada usando a função ``.


``` r
qrcode::generate_svg(code_logo, filename = "qrcode.svg", size = 600)
```

Há ainda uma série de funções no pacote para gerar QR codes específicos, como `qr_event`, `qr_location`, `qr_sepa` e `qr_wifi`. 

Fonte da imagem: [freepik](https://www.freepik.com/free-photo/person-scanning-qr-code_23715172.htm#fromView=image_search_similar&page=1&position=0&uuid=11109289-580c-486b-b3cc-2ccbcdbcf2df).
