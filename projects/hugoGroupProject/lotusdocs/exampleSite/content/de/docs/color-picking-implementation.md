---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Implementierung der Farbauswahlseite"
icon: "rocket_launch"
toc: true
description: "Ein Leitfaden zur Implementierung der Farbauswahlseite"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Anfänger"]
---

## Einführung
In dieser Seite ist es möglich, einem schrittweisen Leitfaden zu folgen, der den Leser darüber informiert, wie die Farbauswahlseite auf dieser Website erstellt wird.

## Einrichtung
1. Hugo und Go installieren
       
    Wenn Sie Hugo und Go noch nicht installiert haben, können Sie die Installationsanleitungen unter [Hugo Installation](https://gohugo.io/installation/) einsehen. Wenn Sie sie bereits installiert haben, können Sie diesen Schritt überspringen und direkt zum nächsten übergehen.
       
    Vergessen Sie nicht die Voraussetzungen. Sie sollten den folgenden Befehl oder ähnliches benötigen: `choco install hugo-extended` (Windows) oder `brew install hugo` (Mac) zum Beispiel.

    Überprüfen Sie die Version mit: `hugo version`.

    Überprüfen Sie, wie Go installiert wird ([Go Installation](https://go.dev/dl/)) und fahren Sie mit der Installation fort, überprüfen Sie am Ende, ob alles in Ordnung ist: `go version`.

2. Lotus Docs Theme herunterladen
       
    Verwenden Sie das Lotus Docs-Beispielprojekt als Vorlage. Beginnen Sie damit, das Repository von [Lotus Docs GitHub Repository](https://github.com/colinwilson/lotusdocs) zu klonen und wechseln Sie zum exampleSite-Ordner. Führen Sie dort den folgenden Befehl aus: `hugo server`. Sie sollten jetzt etwas Ähnliches wie in Abbildung 1 sehen.

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

Ihre Website sollte unter http://localhost:1313/ verfügbar sein.

## MD-Code
Jetzt können Sie den folgenden Code kopieren und im gewünschten Datei einfügen, speichern und zur Website gehen, um die Ergebnisse zu überprüfen.

```shell
---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Ricardo Mascarenhas"
title: "Farbauswahl"
icon: "rocket_launch"
toc: true
description: "Ein Leitfaden zur Erstellung der Farbauswahlfunktionalität in Lotus Docs"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Anfänger"]
---

# Anpassen des oberen Headers mit Farbauswahl

Wir haben eine interaktive Funktion im oberen Header unserer Seite eingeführt, die es Benutzern ermöglicht, ihr Erlebnis durch Ändern der Hintergrund- und Schriftfarben individuell anzupassen.

Dieser Leitfaden führt Sie durch die Änderungen, die an top-header.html vorgenommen wurden, um diese Funktionalität hinzuzufügen.

## Einführung

Der obere Header unserer Website enthält jetzt zwei Farbauswähler: einen für die Hintergrundfarbe und einen anderen für die Schriftfarbe.

Diese Ergänzung verbessert die Benutzerinteraktion, indem sie eine individuellere Schnittstelle bietet.

## Implementierungsdetails

#### Hinzufügen der Farbauswähler

Wir haben zwei HTML-Eingabeelemente vom Typ Farbe zum oberen Header hinzugefügt. Diese Eingaben ermöglichen es den Benutzern, Farben auszuwählen, die dann auf die Hintergrund- und Schriftfarben der Seite angewendet werden.

#### Stylen der Farbauswähler

Inline-CSS wurde verwendet, um die Farbauswähler zu gestalten und sicherzustellen, dass sie nahtlos in das Design der Website passen. Die Stile umfassen das Festlegen der Höhe, das Entfernen des Rahmens und das Hinzufügen eines Border-Radius, um die Auswähler abgerundet erscheinen zu lassen.

#### Skripten von Farbänderungen

Ein JavaScript-Schnipsel wurde hinzugefügt, um auf Farbänderungen über die Farbauswähler zu hören und diese Änderungen dynamisch auf die Hintergrund- und Schriftfarben der Website anzuwenden.

## Wie es funktioniert

Wenn das Dokument vollständig geladen ist, hört das Skript auf ein "Änderungs"-Ereignis für jeden Farbauswähler.

Durch Ändern des Werts des Hintergrundfarbauswählers wird die Hintergrundfarbe der gesamten Seite an die ausgewählte Farbe angepasst.

Ebenso wird durch Ändern des Werts des Schriftfarbauswählers die Textfarbe auf der gesamten Website aktualisiert.

## Fazit

Mit diesen Verbesserungen bietet unsere Website nun eine interaktivere und personalisiertere Benutzererfahrung. Besucher können das Aussehen der Website nach ihren Wünschen anpassen, was ihr Surferlebnis angenehmer macht.

[Wie wurde diese Seite implementiert?](/docs/color-picking-implementation/)
