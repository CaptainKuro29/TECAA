---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Sélection des couleurs"
icon: "rocket_launch"
toc: true
description: "Un guide pour créer une fonctionnalité de sélection de couleur dans Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Débutants"]
---

<div style="border: 2px solid black; padding: 20px; background-color: black; color: white; border-radius: 10px;">

# Personnalisation de l'en-tête supérieur avec des sélecteurs de couleur

Nous avons introduit une fonctionnalité interactive dans l'en-tête supérieur de notre site, permettant aux utilisateurs de personnaliser leur expérience en modifiant les couleurs de fond et de police.

Ce guide vous guidera à travers les modifications apportées à top-header.html pour ajouter cette fonctionnalité. À la fin, vous devriez être en mesure de recréer cette fonctionnalité.

</div>


## Introduction

L'en-tête supérieur de notre site Web comprend désormais deux sélecteurs de couleur : un pour la couleur de fond et un autre pour la couleur de la police.

Cette addition améliore l'engagement des utilisateurs en fournissant une interface plus personnalisable.

## Détails de l'implémentation

#### Ajout des sélecteurs de couleur

Nous avons ajouté deux éléments HTML de type couleur à l'en-tête supérieur. Ces entrées permettent aux utilisateurs de sélectionner des couleurs, qui sont ensuite appliquées à l'arrière-plan de la page et à la police.



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

2. Stylisation des Sélecteurs de Couleur


Nous avons utilisé du CSS en ligne pour styliser les sélecteurs de couleur, garantissant qu'ils s'intègrent parfaitement au design du site. Les styles comprennent le réglage de la hauteur, la suppression de la bordure et l'ajout d'un border-radius pour que les sélecteurs apparaissent arrondis.



#### Script pour les Changements de Couleur

Un extrait de code JavaScript a été ajouté pour écouter les changements de couleur via les sélecteurs de couleur et appliquer ces changements aux couleurs de fond et de police du site de manière dynamique.


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


## Fonctionnement

Lorsque le document est entièrement chargé, le script écoute un événement "change" sur chaque sélecteur de couleur.

Le changement de la valeur du sélecteur de couleur de fond met à jour la couleur de fond de toute la page pour correspondre à la couleur sélectionnée.

De même, le changement de la valeur du sélecteur de couleur de police met à jour la couleur du texte sur l'ensemble du site.

## Conclusion

Grâce à ces améliorations, notre site offre désormais une expérience utilisateur plus interactive et personnalisée. Les visiteurs peuvent personnaliser l'apparence du site selon leurs préférences, rendant leur expérience de navigation plus agréable.