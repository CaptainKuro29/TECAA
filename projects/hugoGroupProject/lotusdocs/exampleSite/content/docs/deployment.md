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

This guide will help you deploy your Hugo website using Netlify, a platform for hosting static websites.

## Before You Start

Make sure you have:

- A Hugo website project ready.
- Signed up for a Netlify account.
- Installed Hugo on your computer.

## Steps

### 1. Sign Up for Netlify

If you haven't already, create an account on Netlify. It's quick and free.

### 2. Add Your Site to Netlify

Go to the Netlify sites page and click "New site from Git."

### 3. Connect Your Repository

Choose your Git provider (like GitHub). Netlify will guide you through connecting your repository.

### 4. Set Build Settings

Netlify will automatically detect your Hugo website. Check the build settings, and adjust if needed.

### 5. Deploy Your Site

Option 1 : Click "Deploy site." Netlify will start building your Hugo website.
Option 2 : Access the folder where your hugo website is stored. Install netlify using 
```shell
npm install -g netlify-cli
```
. After the  is finished, type 
```shell 
netlify deploy prod
```
and follow the steps. 

### 6. Access Your Site

After the build is complete, Netlify will give you a URL to view your deployed site.

## Conclusion

You've successfully deployed your Hugo website with Netlify! Explore Netlify's additional features to enhance your site further.
