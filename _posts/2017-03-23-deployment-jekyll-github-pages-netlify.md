---
permalink: /deployment-jekyll-with-github-pages-and-netlify/
title:  "Auf der Suche nach einem guten Deployment Workflow"
date:   2017-03-23 21:33:19 +0100
excerpt: "Der Workflow soll nöglichst einfach und vor allem auch mobil möglich sein."
categories: jekyll
tags: blog github deployment ssl
---

## Am Anfang

Nach der Entscheidung für Jekyll habe ich erstmal alles lokal unter Liux (OpenSuSE Leap 42.2)  installiert. Lokaler Build, mit lokalem vHost zur Kontrolle und dann Upload der statischen Dateien per FTP zu meinem Hoster.
Die Vorteile sind hier schnell genannt. Komplette Kontrolle über den Build Prozess und die Build Tools. Und die Nachteile? Wenn ich ich einen neuen post online stellen möchte, benötige ich meine lokale Maschine und mehrere Schritte, bis der neue Post endlich online ist. Außerdem muß ich die Build Tools selber aktuell und funktionsfähig halten. So keine Möglichkeit zu haben, unterwegs etwas online zu stelen, störte mich dabei am meisten.


