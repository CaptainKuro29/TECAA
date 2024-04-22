---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Farbauswahl"
icon: "rocket_launch"
toc: true
description: "Ein Leitfaden zur Erstellung einer Farbauswahlfunktion in Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Anfänger"]
---

# Anpassung des oberen Headers mit Farbauswahl

Wir haben eine interaktive Funktion im oberen Header unserer Website eingeführt, mit der Benutzer ihr Erlebnis personalisieren können, indem sie die Hintergrund- und Schriftfarben ändern.

Dieser Leitfaden führt Sie durch die Änderungen, die an top-header.html vorgenommen wurden, um diese Funktion hinzuzufügen.

## Einführung

Der obere Header unserer Website enthält jetzt zwei Farbauswähler: einen für die Hintergrundfarbe und einen anderen für die Schriftfarbe.

Diese Ergänzung verbessert das Benutzerengagement, indem sie eine anpassbarere Benutzeroberfläche bietet.

## Implementierungsdetails

#### Hinzufügen der Farbauswähler

Wir haben zwei HTML-Eingabeelemente vom Typ Farbe zum oberen Header hinzugefügt. Diese Eingaben ermöglichen es Benutzern, Farben auszuwählen, die dann auf den Hintergrund und die Schriftfarbe der Seite angewendet werden.



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

2. Stilisierung der Farbauswähler


Wir haben Inline-CSS verwendet, um die Farbauswähler zu gestalten und sicherzustellen, dass sie nahtlos in das Design der Website passen. Die Stile umfassen das Festlegen der Höhe, das Entfernen des Rahmens und das Hinzufügen eines border-radius, um die Auswahlfelder abgerundet erscheinen zu lassen.



#### Skript für Farbänderungen

Ein JavaScript-Ausschnitt wurde hinzugefügt, um Änderungen der Farben über die Farbauswähler zu verfolgen und diese Änderungen dynamisch auf die Hintergrund- und Schriftfarben der Website anzuwenden.


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


## Funktionsweise

Wenn das Dokument vollständig geladen ist, lauscht das Skript auf ein "change"-Ereignis für jeden Farbauswähler.

Die Änderung des Wertes des Hintergrundfarbauswählers aktualisiert die Hintergrundfarbe der gesamten Seite entsprechend der ausgewählten Farbe.

Ebenso aktualisiert die Änderung des Wertes des Schriftfarbauswählers die Textfarbe auf der gesamten Website.

## Fazit

Mit diesen Verbesserungen bietet unsere Website jetzt eine interaktivere und personalisiertere Benutzererfahrung. Besucher können das Aussehen der Website nach ihren Wünschen anpassen und ihre Browser-Erfahrung damit angenehmer gestalten.