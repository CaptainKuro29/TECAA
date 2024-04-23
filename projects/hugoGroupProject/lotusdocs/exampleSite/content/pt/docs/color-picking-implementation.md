---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Implémentation de la page de sélection de couleur"
icon: "rocket_launch"
toc: true
description: "Un guide pour mettre en œuvre la page de sélection de couleur"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Débutants"]
---

## Introduction
Sur cette page, il est possible de suivre un guide étape par étape qui vise à éduquer le lecteur sur la façon de créer la page de sélection de couleur sur ce site Web.

## Configuration
1. Installer Hugo et Go
       
    Si vous n'avez pas encore installé Hugo et Go, vous pouvez consulter les directives d'installation fournies dans [Installation de Hugo](https://gohugo.io/installation/). Si vous les avez déjà installés, vous pouvez passer cette étape et passer directement à la suivante.
       
    N'oubliez pas les prérequis. Vous devriez avoir besoin de la commande suivante ou similaire : `choco install hugo-extended` (Windows) ou `brew install hugo` (Mac), par exemple.

    Vérifiez la version avec : `hugo version`.

    Vérifiez comment installer Go ([Installation de Go](https://go.dev/dl/)) et procédez à l'installation, vérifiez que tout est bon à la fin : `go version`.

2. Télécharger le thème Lotus Docs
       
    Utilisez le projet d'exemple Lotus Docs comme modèle. Commencez par cloner le dépôt depuis [Répertoire GitHub de Lotus Docs](https://github.com/colinwilson/lotusdocs) et passez au dossier exampleSite. Là, exécutez la commande suivante : `hugo server`. Vous devriez maintenant voir quelque chose comme la Figure 1.

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
 Votre site Web devrait être disponible à l'adresse http://localhost:1313/

## Code MD
Maintenant, vous pouvez copier et coller le code suivant dans le fichier désiré, puis enregistrer et aller sur le site Web pour vérifier les résultats.

  ```shell
---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Choix de la couleur"
icon: "rocket_launch"
toc: true
description: "Un guide pour créer la fonctionnalité de sélection de couleur dans Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Débutants"]
---

# Personnalisation de l'en-tête supérieur avec des sélecteurs de couleur

Nous avons introduit une fonctionnalité interactive dans l'en-tête supérieur de notre site, permettant aux utilisateurs de personnaliser leur expérience en modifiant les couleurs d'arrière-plan et de police.

Ce guide vous guidera à travers les modifications apportées à top-header.html pour ajouter cette fonctionnalité.

## Introduction

L'en-tête supérieur de notre site Web comprend désormais deux sélecteurs de couleur : un pour la couleur d'arrière-plan et un autre pour la couleur de police.

Cette addition améliore l'engagement des utilisateurs en offrant une interface plus personnalisable.

## Détails de l'implémentation

#### Ajout des sélecteurs de couleur

Nous avons ajouté deux éléments d'entrée HTML de type couleur à l'en-tête supérieur. Ces entrées permettent aux utilisateurs de sélectionner des couleurs, qui sont ensuite appliquées à l'arrière-plan et aux couleurs de police de la page.

#### Stylisation des sélecteurs de couleur

Du CSS en ligne a été utilisé pour styliser les sélecteurs de couleur, en veillant à ce qu'ils se fondent harmonieusement dans le design du site. Les styles incluent le réglage de la hauteur, la suppression de la bordure et l'ajout d'un rayon de bordure pour que les sélecteurs semblent arrondis.

#### Scripting des changements de couleur

Un extrait de code JavaScript a été ajouté pour écouter les changements de couleur via les sélecteurs de couleur et appliquer ces changements aux couleurs d'arrière-plan et de police du site Web de manière dynamique.

## Comment ça marche

Lorsque le document est entièrement chargé, le script écoute un événement "changement" sur chaque sélecteur de couleur.

Le changement de la valeur du sélecteur de couleur d'arrière-plan met à jour la couleur d'arrière-plan de la page entière pour correspondre à la couleur sélectionnée.

De même, le changement de la valeur du sélecteur de couleur de police met à jour la couleur du texte sur l'ensemble du site.

## Conclusion

Grâce à ces améliorations, notre site offre désormais une expérience utilisateur plus interactive et personnalisée. Les visiteurs peuvent personnaliser l'apparence du site selon leurs préférences, rendant leur expérience de navigation plus agréable.

[Comment cette page a-t-elle été implémentée ?](/docs/color-picking-implementation/)
```