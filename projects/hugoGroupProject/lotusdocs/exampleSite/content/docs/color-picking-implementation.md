---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Color Picker Page implementation"
icon: "rocket_launch"
toc: true
description: "A guide to implement the color picking page"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Beginners"]
---


## Introduction
   In this page it is possible to follow a step by step guide that aims to educate the reader on how to make a the olor picker page in this website.

## Set up
   1. Install Hugo and Go
       
       If you haven’t installed Hugo and Go, you can go see the installation guidelines provided in [Hugo Installation](https://gohugo.io/installation/). If you do already have them installed you can skip this step and go directly to the next one. 
       
       Do not forget the prerequisites. You should need the following command or similar: `choco install hugo-extended` (windows) or `brew install hugo` (mac), for instance. 

       Check the version using: `hugo version`. 

       Check how to install Go ([Go Installation](https://go.dev/dl/)) and proceed with the installation, check that everything is fine at the end: `go version`.

   2. Download Lotus Docs theme
       
       Use the Lotus Docs example project as a template. Start by cloning the repository from [Lotus Docs GitHub Repository](https://github.com/colinwilson/lotusdocs) and changing to the exampleSite folder. There, execute the following command: `hugo server`. You should now see something like Figure 1.

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
  Your website should be avalable at available at http://localhost:1313/

## MD Code
Now you are able to copy and paste the following code in the desired file, in the end, press save and go to the website to check the results.


```shell
---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Color Picking"
icon: "rocket_launch"
toc: true
description: "A guide to create color picking functionality in Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Beginners"]
---

# Customizing the Top Header with Color Pickers

We've introduced an interactive feature to the top header of our site, allowing users to personalize their experience by changing the background and font colors. 

This guide will walk you through the changes made to top-header.html to add this functionality.

## Introduction

The top header of our website now includes two color pickers: one for the background color and another for the font color. 

This addition enhances user engagement by providing a more customizable interface.

## Implementation Details


#### Adding the Color Pickers

We added two HTML input elements of type color to the top header. These inputs allow users to select colors, which are then applied to the page's background and font.



2. Styling the Color Pickers


Inline CSS was used to style the color pickers, ensuring they blend seamlessly with the site's design. The styles include setting the height, removing the border, and adding a border-radius to make the pickers appear rounded.



#### Scripting Color Changes

A JavaScript snippet was added to listen for color changes through the color pickers and apply these changes to the website's background and font colors dynamically.

## How It Works

When the document is fully loaded, the script listens for a "change" event on each color picker.

Changing the background color picker's value updates the entire page's background color to match the selected color.

Similarly, changing the font color picker's value updates the text color across the website.

## Conclusion

With these enhancements, our site now offers a more interactive and personalized user experience. Visitors can customize the look of the site to their preference, making their browsing experience more enjoyable.

[How was this page implemented](/docs/color-picking-implementation/)

```