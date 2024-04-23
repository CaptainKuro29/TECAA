---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Seleçao de cores"
icon: "rocket_launch"
toc: true
description: "Um guia para criar uma funcionalidade de seleção de cores no Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Iniciantes"]
---

<div style="border: 2px solid black; padding: 20px; background-color: black; color: white; border-radius: 10px;">

# Personalização do Cabeçalho Superior com Seletor de Cores

Introduzimos uma funcionalidade interativa no cabeçalho superior do nosso site, permitindo que os usuários personalizem sua experiência alterando as cores de fundo e da fonte.

Este guia irá guiá-lo pelas alterações feitas no top-header.html para adicionar essa funcionalidade. No final, você deverá ser capaz de recriar essa funcionalidade.

</div>


## Introdução

O cabeçalho superior do nosso site agora inclui dois seletores de cores: um para a cor de fundo e outro para a cor da fonte.

Essa adição melhora o envolvimento do usuário, proporcionando uma interface mais personalizável.

## Detalhes de Implementação

#### Adicionando os Seletores de Cores

Adicionamos dois elementos HTML do tipo “color” ao cabeçalho superior. Esses campos permitem que os usuários escolham cores, que são então aplicadas ao fundo e à fonte da página.



```shell
    <!-- Frontend for Color Picker Background and Font -->
        <div class="d-flex align-items-center ms-3">
            <label class="me-2">Background: </label>
            <input class="me-2" type="color" id="backgroundColorPicker" value="#ffffff" title="Choose background color"
            style="height: 40px; border: none; border-radius: 8px;" aria-label="change-background-color">
            <label class="me-2">Text: </label>
            <input class="me-2" type="color" id="fontColorPicker" value="#000000" title="Choose font color"
            style="height: 40px; border: none; border-radius: 8px;" aria-label="change-text-color">
        </div>
    <!-- Color Picker End -->
```

2. Estilização dos Seletores de Cor

Utilizamos CSS inline para estilizar os seletores de cor, garantindo que eles se integrem perfeitamente ao design do site. Os estilos incluem definição de altura, remoção da borda e adição de um border-radius para que os seletores apareçam arredondados.



#### Script para Alterações de Cor

Foi adicionado um trecho de código JavaScript para ouvir as mudanças de cor através dos seletores de cor e aplicar essas mudanças às cores de fundo e de fonte do site de forma dinâmica.

```shell
<!-- Script for Color Picker -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
          var backgroundColorPicker = document.getElementById('backgroundColorPicker');
          backgroundColorPicker.addEventListener('change', function() {
            document.body.style.backgroundColor = this.value;
            document.documentElement.style.backgroundColor = this.value;
          });
      
          var fontColorPicker = document.getElementById('fontColorPicker');
          fontColorPicker.addEventListener('change', function() {
            document.querySelectorAll('p').forEach(element => {
                element.style.color = this.value;
            });
          });
        });
    </script>
```


## Funcionamento

Quando o documento está totalmente carregado, o script escuta um evento "change" em cada seletor de cor.

A alteração do valor do seletor de cor de fundo atualiza a cor de fundo de toda a página para corresponder à cor selecionada.

Da mesma forma, a alteração do valor do seletor de cor da fonte atualiza a cor do texto em todo o site.

## Conclusão

Com estas melhorias, o site agora oferece uma experiência do usuário mais interativa e personalizada. Os visitantes podem personalizar a aparência do site de acordo com as suas preferências, tornando sua experiência de navegação mais agradável.

[Como foi implementado](/docs/color-picking-implementation/)