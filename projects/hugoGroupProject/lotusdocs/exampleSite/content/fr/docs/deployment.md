---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Joao Martins"
title: "Deployment"
icon: "rocket_launch"
toc: true
description: "Un guide pour déployer un site web Hugo"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Beginners"]
---

# Déploiement d'un site Hugo avec Netlify

Ce guide vous aidera à publier votre site Hugo en utilisant Netlify, une plateforme pour héberger des sites statiques.

## Avant de commencer

Assurez-vous d'avoir :

- Un projet de site Hugo prêt.
- Un compte enregistré sur Netlify.
- Hugo installé sur votre ordinateur.

## Étapes

### 1. S'inscrire sur Netlify

Si ce n'est pas déjà fait, créez un compte sur Netlify. C'est rapide et gratuit.

### 2. Ajouter votre site à Netlify

Allez sur la page "Sites" de Netlify et cliquez sur "Nouveau site depuis Git".

Vous pouvez consulter la documentation de [Netlify Docs](https://docs.netlify.com/get-started/).

### 3. Connecter votre dépôt

Choisissez votre fournisseur Git (comme GitHub). Netlify vous guidera pour connecter votre dépôt.

### 4. Configurer les paramètres de construction

Netlify détecte automatiquement votre site Hugo. Vérifiez les paramètres de construction et ajustez-les si nécessaire.

### 5. Publier votre site

Option 1 : Cliquez sur "Publier le site". Netlify commencera à créer votre site Hugo.
Option 2 : Accédez au dossier contenant votre site Hugo. Installez Netlify avec :
```shell
npm install -g netlify-cli
```
Après l'installation, tapez :
```shell 
netlify deploy prod
```
et suivez les instructions.

### 6. Access Your Site

After the build is complete, Netlify will give you a URL to view your deployed site.

## Conclusion

You've successfully deployed your Hugo website with Netlify! Explore Netlify's additional features to enhance your site further.
