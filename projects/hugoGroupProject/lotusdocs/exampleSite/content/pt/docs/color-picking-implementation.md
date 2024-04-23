---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Implementaçao Seleção de Cores"
icon: "rocket_launch"
toc: true
description: "Um guia para criar funcionalidade de seleção de cores no Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Iniciantes"]
---

## Introdução
Nesta página, é possível seguir um guia passo a passo que tem como objetivo educar o leitor sobre como criar uma página de seleção de cores neste site.

## Configuração
1. Instale o Hugo e o Go

Se ainda não instalou o Hugo e o Go, pode consultar as diretrizes de instalação fornecidas em Instalação do Hugo. Se já os tiver instalado, pode ignorar este passo e avançar diretamente para o próximo.

Não se esqueça dos pré-requisitos. Pode precisar do seguinte comando ou similar: choco install hugo-extended (Windows) ou brew install hugo (Mac), por exemplo.

Verifique a versão usando: hugo version.

Verifique como instalar o Go (Instalação do Go) e prossiga com a instalação, verificando se está tudo bem no final: go version.

2. Faça o download do tema Lotus DocsUtilize o projeto de exemplo Lotus Docs como modelo. 
Comece clonando o repositório em Repositório GitHub do Lotus Docs e alterando para a pasta exampleSite. Lá, execute o seguinte comando: hugo server. Agora deverá ver algo semelhante à Figura 1.

  ```shell
                   | EN  | FR  | DE
-------------------+-----+-----+------
  Pages            |  19 |  14 |  14
  Paginator pages  |   0 |   0 |   0
  Non-page files   |   1 |   1 |   1
  Static files     | 367 | 367 | 367
  Processed images |  18 |   0 |   0
  Aliases          |   1 |   0 |   0
  Cleaned          |   0 |   0 |   0

```
O seu site deverá estar disponível em http://localhost:1313/.

## Code MD
Agora você pode copiar e colar o seguinte código no arquivo desejado. Em seguida, guarde e verifique os resultados..


  ```shell
---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Seleção de Cores"
icon: "rocket_launch"
toc: true
description: "Um guia para criar funcionalidade de seleção de cores no Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Iniciantes"]
---

# Personalização do Cabeçalho Superior com Selecionadores de Cores
Introduzimos uma funcionalidade interativa no cabeçalho superior do nosso site, permitindo aos utilizadores personalizarem a sua experiência ao alterar as cores de fundo e da fonte.

Este guia irá orientá-lo pelas alterações feitas no arquivo top-header.html para adicionar esta funcionalidade.

## Introdução
O cabeçalho superior do nosso site agora inclui dois selecionadores de cores: um para a cor de fundo e outro para a cor da fonte.

Esta adição melhora o envolvimento do utilizador, proporcionando uma interface mais personalizável.

#### Detalhes da Implementação
Adicionar os Selecionadores de Cores
Adicionamos dois elementos de entrada HTML do tipo cor ao cabeçalho superior. Estes inputs permitem aos utilizadores selecionar cores, que são então aplicadas ao fundo da página e à cor da fonte.

####Estilizar os Selecionadores de Cores
CSS em linha foi utilizado para estilizar os selecionadores de cores, garantindo que se misturam perfeitamente com o design do site. Os estilos incluem definir a altura, remover a borda e adicionar um raio de borda para que os selecionadores pareçam arredondados.

####Script para Alterações de Cor
Um trecho de JavaScript foi adicionado para ouvir as alterações de cor através dos selecionadores de cores e aplicar essas alterações às cores de fundo e da fonte do site de forma dinâmica.

####Como Funciona
Quando o documento está totalmente carregado, o script fica à escuta de um evento "change" em cada selecionador de cores.

Alterar o valor do selecionador de cor de fundo atualiza a cor de fundo de toda a página para corresponder à cor selecionada.

Da mesma forma, alterar o valor do selecionador de cor da fonte atualiza a cor do texto em todo o site.

##Conclusão
Com estas melhorias, o nosso site oferece agora uma experiência de utilizador mais interativa e personalizada. Os visitantes podem personalizar o visual do site de acordo com as suas preferências, tornando a sua experiência de navegação mais agradável.
```