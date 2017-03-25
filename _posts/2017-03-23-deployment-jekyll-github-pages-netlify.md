---
permalink: /deployment-jekyll-with-github-pages-and-netlify/
title:  "Auf der Suche nach einem guten Deployment Workflow"
date:   2017-03-23 21:33:19 +0100
excerpt: "Der Workflow soll wenige Schritte enthalten und vor allem auch mobil möglich sein."
categories: jekyll
tags: blog github deployment ssl
---

## Am Anfang

Darauf gebracht hat mich dieser Artikel [So geht Publishing heute: 13 kompakte CMS im Vergleich](http://t3n.de/news/13-kompakte-cms-im-vergleich-461933/){:target="_blank"}. Dazu die in den vergangenen Jahren gesammelten Erfahrungen mit Wordpress und die Suche nach einer einfachen Möglichkeit, eine Webseite zu veröffentlichen. In dem Artikel ist [Jekyll](https://jekyllrb.com/docs/home){:target="_blank"} nicht mal genannt, aber beim Lesen über und der Recherche nach [Kirby](https://getkirby.com/){:target="_blank"}, [Pico](http://picocms.org/){:target="_blank"}, [Grav](https://getgrav.org/){:target="_blank"} und Co. kommt man unweigerlich auch an Jekyll vorbei. 

Nein, eigentlich war ich auf der Suche nach einem schönen einfachen und minimalistischen Foto-Theme für Wordpress und kam dabei an [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/){:target="_blank"} vorbei und es sah gut aus. Einfach, gut zu gestalten. Also nix Foto-Theme, daß wollte ich selber ausprobieren. Aber es lief auf Jekyll. Kannte ich nicht, hörte sich jedoch nach einem von den 'Neuen' aus dem t3n-Artikel an.

Ein paar Docus und Howtos später lief der erste Build von Minimal Mistakes auf Jekyll als Ruby Gem erfolgreich lokal auf meiner Linux Box. Schön. Einen vHost dazu und das sah doch schon sehr gut aus. 
Ein bißchen Styling mit Lieblingsschriften angrundet, Bilder zurechtgeschnitten und ab als statische Seite auf den Server.

Ein guter Gedanke, der von statischen Seiten, ohne Datenbank und großes Backend dahinter und einem schlanken Workflow. Also als nächstes ausprobieren, ob alles so einfach geht, wie ich mir das vorstelle.

## Workflow #1

Lokaler Build, mit lokalem vHost zur Kontrolle und dann Upload der statischen Dateien per FTP zu meinem Hoster.
Die Vorteile sind hier schnell klar. Komplette Kontrolle über den Build Prozess und die Build Tools. Und die Nachteile? Wenn ich ich einen neuen post online stellen möchte, benötige ich meine lokale Maschine und mehrere Schritte, bis der neue Post endlich online ist. Außerdem muß ich die Build Tools selber aktuell und funktionsfähig halten. So keine Möglichkeit zu haben, unterwegs etwas online zu stelen, störte mich dabei am meisten.

## Git

## Github Pages




