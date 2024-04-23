---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Joao Martins"
title: "Deployment"
icon: "rocket_launch"
toc: true
description: "A guide to deploy a Hugo Website"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Beginners"]
---

# Deploying a Hugo Website with Netlify

This guide will help you deploy your Hugo website using Netlify. It is a platform for hosting static websites.

## Before You Start

Make sure you have:

- A Hugo website project ready.
- Signed up for a Netlify account.
- Installed Hugo on your computer.

## Steps

### Sign Up for Netlify

Create an account on Netlify, or login to an existent account.

### Add Your Site to Netlify

Go to the Netlify sites page and click “New site from Git.”

You can check Netlify documentation here: [Hugo CLI](https://docs.netlify.com/get-started/).

### Connect Your Repository

Choose your Git provider (like GitHub). Netlify will guide you through connecting your repository.

### Set Build Settings

Netlify will detect your Hugo website. Check the build settings, and adjust if necessary.

### Deploy Your Site

Option 1 : Click "Deploy site." Netlify will start building your Hugo website.
Option 2 : Access the folder where your hugo website is stored. Install netlify using: 
```shell
npm install -g netlify-cli
```
After the installation, type the command and follow the steps:
```shell 
netlify deploy prod
```

### Access Your Site

Netlify will give you a URL to view your deployed site.

## Conclusion

You’ve deployed your Hugo website with Netlify! Explore Netlify’s additional features to enhance your site further.
