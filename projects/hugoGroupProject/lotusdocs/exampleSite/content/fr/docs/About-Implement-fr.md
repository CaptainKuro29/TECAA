---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Pedro Martins"
title: "Mise en Place de la Page À Propos"
icon: "rocket_launch"
toc: true
description: "Un guide pour implémenter la page À Propos"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Débutants"]
---

## Introduction
   Sur cette page, il est possible de suivre un guide étape par étape qui vise à éduquer le lecteur sur la manière de créer la page de sélection de couleur sur ce site web.

## Configuration
   1. Installer Hugo et Go
       
       Si vous n'avez pas encore installé Hugo et Go, vous pouvez consulter les instructions d'installation fournies dans [Installation de Hugo](https://gohugo.io/installation/). Si vous les avez déjà installés, vous pouvez passer cette étape et aller directement à la suivante.
       
       N'oubliez pas les prérequis. Vous devriez avoir besoin de la commande suivante ou similaire : `choco install hugo-extended` (windows) ou `brew install hugo` (mac).

       Vérifiez la version en utilisant : `hugo version`.

       Vérifiez comment installer Go ([Installation de Go](https://go.dev/dl/)) et procédez à l'installation, vérifiez que tout est correct à la fin : `go version`.

   2. Télécharger le thème Lotus Docs
       
       Utilisez le projet d'exemple Lotus Docs comme modèle. Commencez par cloner le dépôt depuis [Répertoire GitHub de Lotus Docs](https://github.com/colinwilson/lotusdocs) et changez pour le dossier exampleSite. Là, exécutez la commande suivante : `hugo server`. Vous devriez maintenant voir quelque chose comme la Figure 1.

  ```shell
                   | EN  | FR  | DE
-------------------+-----+-----+------
  Pages            |  19 |  14 |  14
  Paginator pages  |   0 |   0 |   0
  Non-page files   |   1 |   1 |   1
  Static files     | 367 | 367 | 367
  Processed images |  18 |   0 |   0
  Aliases          |   1 |   0 |   0
  Nettoyé          |   0 |   0 |   0

```

Votre site web devrait être disponible à http://localhost:1313/

## Implémentation de la Page À Propos/Code MD

```shell
---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Pedro Martins"
title: "À propos"
icon: "rocket_launch"
toc: true
description: "Découvrez comment nous créons un guide centré sur l'utilisateur pour construire des sites Web de documentation technique."
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Débutants"]
---

# Bienvenue dans notre projet de documentation technique

Ce projet fait partie de notre cours de génie informatique. Il vous offre une aide pratique pour construire et gérer des sites Web de documentation technique. Nous utilisons des technologies Web modernes et suivons les meilleures pratiques de l'industrie pour vous aider à bien apprendre la documentation technique.

## Ce que nous visons à faire

Nous sommes ici pour aider les développeurs, nouveaux et expérimentés, à comprendre comment créer des sites Web de documentation. Notre projet comprend tout, de la gestion de contenu et du design au respect des normes d'accessibilité et à la gestion des technologies backend.

## Rencontrez l'équipe

- **Pedro Martins** de Felgueiras dirige le récit de cette page avec une communication claire.
- **Ricardo Mascarenhas** s'occupe de la "Page de sélection des couleurs" et vient de Porto sur son scooter électrique, s'assurant que notre site est superbe.
- **João Martins** gère notre "Page de déploiement", utilisant ses compétences en HTML pour que notre site fonctionne bien sur différentes plateformes.
- **Pedro Simões**, fan d'anime et expert en technologies backend de Porto, prend en charge la "Page de configuration" avec ses solides compétences en Java.

## Comment nous construisons

Utilisant le cadre Hugo pour sa rapidité et son efficacité, notre site Web est conçu pour être rapide, facile à utiliser et réactif. Cela assure une expérience utilisateur fluide.

## Notre engagement envers l'accessibilité

Nous suivons les directives d'accessibilité du contenu Web (WCAG) pour garantir que notre site est accessible à tous, quelles que soient leurs capacités. Vous pouvez voir notre engagement dans chaque choix que nous faisons, de la sélection des couleurs aux éléments interactifs.

## Déclaration d'accessibilité

### Introduction
Notre engagement va au-delà de la simple conformité. Nous voulons créer un lieu accueillant en ligne pour tous, en particulier pour les personnes handicapées. Nous continuons à travailler pour améliorer l'accès et l'utilisation pour tous en utilisant les normes et technologies les plus récentes.

### Notre engagement envers l'accessibilité
**Objectif :**  
Notre objectif principal est de suivre les directives d'accessibilité du contenu Web (WCAG) 2.1 Niveau AA. Cela assure que notre site Web est utilisable par des personnes de toutes capacités et handicaps.

**Fonctionnalités d'accessibilité :**  
Nous avons ajouté des fonctionnalités pour garantir que tout le monde puisse utiliser le site facilement :
- **Navigation au clavier** : Vous pouvez utiliser notre site Web avec un clavier seul, ce qui vous permet d'interagir sans souris.
- **Compatibilité avec les lecteurs d'écran** : Nous nous assurons que notre contenu fonctionne avec les lecteurs d'écran, qui aident à lire le texte à haute voix.
- **Taille de texte et contraste ajustables** : Vous pouvez modifier les tailles de texte et les contrastes pour faciliter la lecture.

### Conseils d'utilisation
**Recommandations pour une expérience optimale :**  
Pour la meilleure expérience, nous suggérons d'utiliser les derniers outils d'accessibilité et les navigateurs qui soutiennent ces technologies. Si vous avez des difficultés à utiliser notre site, veuillez contacter directement notre équipe de support.

### Retours et Contact
**Nous apprécions vos retours :**  
Vos commentaires sont très importants pour nous aider à rendre notre site Web meilleur pour tous. Veuillez nous informer de tout problème que vous rencontrez ou suggérer des améliorations :
- **Email** : [1230204@isep.ipp.pt](mailto:1230204@isep.ipp.pt)
- **Téléphone** : [+351912206445]

### Engagement pour l'amélioration continue
Nous voyons l'accessibilité comme un objectif continu et cherchons toujours de nouvelles façons de rendre le site meilleur. Vos retours nous aident à continuer à améliorer et à garantir que notre site répond à divers besoins.

### Conformité légale et réglementaire
**Respect des lois :**  
Notre site Web respecte toutes les lois et règles d'accessibilité pour dépasser ce qui est requis.

### Mises à jour et modifications
**Mises à jour régulières :**  
Nous mettons souvent à jour nos fonctionnalités et méthodes d'accessibilité pour suivre les lois, les changements technologiques et les retours des utilisateurs.

## Contrôle de la performance

Nous ne nous contentons pas de construire ; nous nous assurons que notre site fonctionne bien. Nous continuons à vérifier et à améliorer pour atteindre les normes de performance les plus élevées, en garantissant qu'il fonctionne rapidement et sans problème pour chaque utilisateur.
```