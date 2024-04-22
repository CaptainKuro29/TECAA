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

2. Styling the Color Pickers


Inline CSS was used to style the color pickers, ensuring they blend seamlessly with the site's design. The styles include setting the height, removing the border, and adding a border-radius to make the pickers appear rounded.



#### Scripting Color Changes

A JavaScript snippet was added to listen for color changes through the color pickers and apply these changes to the website's background and font colors dynamically.


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


## How It Works

When the document is fully loaded, the script listens for a "change" event on each color picker.

Changing the background color picker's value updates the entire page's background color to match the selected color.

Similarly, changing the font color picker's value updates the text color across the website.

## Conclusion

With these enhancements, our site now offers a more interactive and personalized user experience. Visitors can customize the look of the site to their preference, making their browsing experience more enjoyable.

[How was this page implemented](/docs/color-picking-implementation/)