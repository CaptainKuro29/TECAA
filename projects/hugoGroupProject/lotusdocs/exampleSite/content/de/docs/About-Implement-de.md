---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Pedro Martins"
title: "Implementierung der Über uns-Seite"
icon: "rocket_launch"
toc: true
description: "Ein Leitfaden zur Implementierung der Über uns-Seite"
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Anfänger"]
---

## Einleitung
   Auf dieser Seite können Sie einer schrittweisen Anleitung folgen, die darauf abzielt, den Leser darüber zu informieren, wie die Farbwähler-Seite auf dieser Website erstellt wird.

## Einrichtung
   1. Installieren Sie Hugo und Go
       
       Wenn Sie Hugo und Go noch nicht installiert haben, können Sie die Installationsanleitungen unter [Hugo Installation](https://gohugo.io/installation/) einsehen. Wenn Sie sie bereits installiert haben, können Sie diesen Schritt überspringen und direkt zum nächsten übergehen.
       
       Vergessen Sie nicht die Voraussetzungen. Sie benötigen den folgenden oder einen ähnlichen Befehl: `choco install hugo-extended` (Windows) oder `brew install hugo` (Mac).

       Überprüfen Sie die Version mit: `hugo version`.

       Sehen Sie nach, wie Sie Go installieren ([Go Installation](https://go.dev/dl/)) und fahren Sie mit der Installation fort, überprüfen Sie am Ende, dass alles in Ordnung ist: `go version`.

   2. Laden Sie das Lotus Docs-Theme herunter
       
       Verwenden Sie das Lotus Docs-Beispielprojekt als Vorlage. Beginnen Sie damit, das Repository von [Lotus Docs GitHub Repository](https://github.com/colinwilson/lotusdocs) zu klonen und wechseln Sie in den Ordner exampleSite. Dort führen Sie den folgenden Befehl aus: `hugo server`. Jetzt sollten Sie etwas Ähnliches wie Abbildung 1 sehen.



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



Ihre Website sollte jetzt unter http://localhost:1313/ verfügbar sein

## Implementierung der Über uns-Seite/ Ihr MD-Code

  ```shell
  ---
weight: 100
date: "2023-05-03T22:37:22+01:00"
draft: false
author: "Pedro Martins"
title: "Über"
icon: "rocket_launch"
toc: true
description: "Entdecken Sie, wie wir einen benutzerorientierten Leitfaden zum Erstellen von technischen Dokumentationswebsites erstellen."
publishdate: "2023-05-03T22:37:22+01:00"
tags: ["Anfänger"]
---

# Willkommen bei unserem Projekt zur technischen Dokumentation

Dieses Projekt ist Teil unseres Kurses für Informatiktechnik. Es bietet Ihnen praktische Hilfe beim Aufbau und der Verwaltung von Websites für technische Dokumentationen. Wir verwenden moderne Webtechnologien und folgen den besten Praktiken der Branche, um Ihnen zu helfen, technische Dokumentation gut zu erlernen.

## Was wir erreichen wollen

Wir sind hier, um sowohl neuen als auch erfahrenen Entwicklern zu helfen, den Aufbau von Dokumentationswebsites zu verstehen. Unser Projekt umfasst alles von der Inhaltsverwaltung und dem Design bis hin zu Zugänglichkeitsstandards und Backend-Technologien.

## Lernen Sie das Team kennen

- **Pedro Martins** aus Felgueiras führt die Erzählung auf dieser Seite mit klarer Kommunikation an.
- **Ricardo Mascarenhas** kümmert sich um die "Farbauswahl-Seite" und pendelt mit seinem Elektroroller aus Porto, um sicherzustellen, dass unsere Seite großartig aussieht.
- **João Martins** leitet unsere "Bereitstellungsseite" und verwendet seine HTML-Fähigkeiten, damit unsere Website gut auf verschiedenen Plattformen funktioniert.
- **Pedro Simões**, ein Anime-Fan und Backend-Experte aus Porto, betreut die "Einrichtungsseite" mit seinen starken Java-Kenntnissen.

## Wie wir bauen

Mit dem Hugo-Framework wegen seiner Schnelligkeit und Effizienz ist unsere Website darauf ausgelegt, schnell, benutzerfreundlich und reaktionsschnell zu sein. Dies stellt sicher, dass Sie eine reibungslose Erfahrung haben.

## Unser Engagement für Barrierefreiheit

Wir halten uns an die Web Content Accessibility Guidelines (WCAG), um sicherzustellen, dass unsere Seite für jeden zugänglich ist, unabhängig von seinen Fähigkeiten. Unser Engagement zeigt sich in jeder Entscheidung, von der Farbauswahl bis zu interaktiven Elementen.

## Barrierefreiheitserklärung

### Einführung
Unser Engagement geht über die bloße Einhaltung von Vorschriften hinaus. Wir möchten einen einladenden Online-Ort für alle schaffen, insbesondere für Menschen mit Behinderungen. Wir arbeiten kontinuierlich daran, den Zugang und die Benutzbarkeit für alle zu verbessern, indem wir die neuesten Standards und Technologien nutzen.

### Unser Engagement für Barrierefreiheit
**Ziel:**  
Unser Hauptziel ist es, die Web Content Accessibility Guidelines (WCAG) 2.1 Level AA zu befolgen. Dies stellt sicher, dass unsere Website von Menschen mit allen Arten von Fähigkeiten und Behinderungen genutzt werden kann.

**Barrierefreiheitsfunktionen:**  
Wir haben Funktionen hinzugefügt, um sicherzustellen, dass jeder die Seite leicht nutzen kann:
- **Tastaturnavigation**: Sie können unsere Website allein mit einer Tastatur bedienen, was die Interaktion ohne Maus ermöglicht.
- **Kompatibilität mit Screenreadern**: Wir stellen sicher, dass unser Inhalt mit Screenreadern funktioniert, die beim Vorlesen von Text helfen.
- **Anpassbare Textgröße und Kontrast**: Sie können die Textgröße und den Kontrast ändern, um die Lesbarkeit zu verbessern.

### Nutzungshinweise
**Empfehlungen für ein optimales Erlebnis:**  
Für das beste Erlebnis empfehlen wir die Verwendung der neuesten Barrierefreiheitstools und Browser, die diese Technologien unterstützen. Wenn Sie Probleme bei der Nutzung unserer Seite haben, kontaktieren Sie bitte direkt unser Support-Team.

### Feedback und Kontakt
**Wir schätzen Ihre Rückmeldung:**  
Ihr Feedback ist sehr wichtig, um unsere Website für alle besser zu machen. Bitte teilen Sie uns alle Probleme mit, die Sie haben, oder schlagen Sie Verbesserungen vor:
- **E-Mail**: [1230204@isep.ipp.pt](mailto:1230204@isep.ipp.pt)
- **Telefon**: [+351912206445]

### Engagement für kontinuierliche Verbesserung
Wir sehen Barrierefreiheit als ein fortlaufendes Ziel und suchen ständig nach neuen Wegen, die Seite zu verbessern. Ihr Feedback hilft uns, kontinuierlich zu verbessern und sicherzustellen, dass unsere Seite verschiedenen Bedürfnissen entspricht.

### Rechtliche und regulatorische Konformität
**Rechtliche Einhaltung:**  
Unsere Website entspricht allen anwendbaren Barrierefreiheitsgesetzen und -vorschriften, um sicherzustellen, dass wir die erforderlichen Anforderungen erfüllen und übertreffen.

### Updates und Modifikationen
**Regelmäßige Updates:**  
Wir aktualisieren regelmäßig unsere Barrierefreiheitsfunktionen und -methoden, um mit Gesetzen, technologischen Änderungen und Nutzerfeedback Schritt zu halten.

## Leistung im Blick behalten

Wir bauen nicht nur; wir stellen sicher, dass unsere Seite gut funktioniert. Wir überprüfen und verbessern sie kontinuierlich, um die höchsten Leistungsstandards zu erreichen, und stellen sicher, dass sie schnell und reibungslos für jeden Nutzer funktioniert.

```