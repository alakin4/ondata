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

Nein, eigentlich ging ich auf die Suche nach einem schönen einfachen und minimalistischen Foto-Theme für Wordpress und kam dabei an [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/){:target="_blank"} vorbei, diesem schlichten Jekyll Theme, und es sah gut aus. Einfach, gut zu gestalten. Hätte ich gern für Wordpress, aber habe ich nicht gefunden. Also erstmal nix Foto-Theme. Daß wollte ich selber ausprobieren. Aber es lief auf Jekyll, unbekannterweise. Hörte sich jedoch nach einem von den 'Neuen' aus dem t3n-Artikel an und da kam Spannung auf.

Ein paar Dokus und Howtos später läuft der erste Build von Minimal Mistakes auf Jekyll als Ruby Gem erfolgreich lokal auf meiner Linux Box. Schön. Einen vHost dazu und das sah doch schon sehr gut aus. 
Ein bißchen Styling, CSS und das ganze mit Lieblingsschriften abgrundet, Bilder zurechtgeschnitten und ab als statische Seite auf den Server.

Guter Gedanke, der von statischen Seiten, ohne Datenbank und großes Backend und einem schlanken Workflow. Also als nächstes ausprobieren, ob alles so einfach geht, wie vorgestellt.

## Workflow #1

Der erste Ablauf also wie oben beschrieben: Lokaler Build, mit lokalem vHost zur Kontrolle und dann Upload der Dateien per FTP zu meinem Hoster.
Die Vorteile: komplette Kontrolle über den Build Prozess und die Build Tools. Und die Nachteile? Wenn ich ich einen neuen Post online stellen möchte, benötige ich meine lokale Maschine und mehrere Schritte, bis der neue Post endlich online ist. Außerdem muß ich die Build Tools selber aktuell und funktionsfähig halten. So keine Möglichkeit zu haben, unterwegs etwas online zu stelen, störte mich dabei am meisten.

Der erste Workflow ging so:
+ lokale Änderungen, Dateien hinzufügen oder löschen
+ `bundle exec jekyll b`, um die statischen Seite zu bauen
+ Kontrolle über lokalen vHost
+ wenn alles gut ist, in der _config.yml die Variable `url` umstellen
+ nochmal `bundle exec jekyll b`, um die statischen Dateien mit der richtigen URL für Online zu erzeugen
+ `url` in der _config.yml wieder zurückstellen auf lokal (besser gleich, sondern vergißt man es)
+ Statische Seiten aus dem Ordner /_site per FTP in den Webroot auf den Server laden

## Git

Die Seite muß natürlich ins Git, weil Minimal Mistakes liegt ja auch da und überhaupt. Da in meinem ersten Setup das Theme als Ruby Gem installiert ist, wird es auch über `bundle update` aktualisiert. Für meine eigenen Themeanpassungen das Paket als Zip runterladen und entpacken oder `git clone` und dann den .git-Ordner löschen, dann alles überflüssige (ist in der Installationsanleitung beschrieben, was das ist) wegschmeißen und dann schön anstreichen. Bei Github ein Repos erstellt und `push`.

## Github Pages

Gut, da ich schon bei Github bin, liegt da auch das Repos. Und dann stolpert man ja unweigerlich über Github Pages. Man kann bei Github entweder einen Branchen des gesamten Repos oder eines Projekts per Github Pages ausliefern lassen, also als Webseite zur Verfügung stellen. Das ganze geht standardmäßig über eine Subdomain von github.io. Und über HTTPS. Großartig. Man kann sogar seine eigene Domain hinterlegen. Allerdings mit dem Nachteil, daß man dann kein Zertifikat dafür hinterlegen kann. Aber eins nach dem anderen.
Ein weiterer Vorteil - und weshalb Github Pages überhaupt hier interessant sind - Github Pages unterstützen auch Jekyll.

Jekyll auf Github Pages unterstützt nur eine Reihe von Themen. Das hier - Minimal Mistakes - wird erstmal nicht unterstützt. Aber Minimal Mistakes kann so konfiguriert werden, daß es auch mit den Github Pages läuft. Das ist alles schon vorbereitet und im Quickstart Guide beschrieben. Dazu muß dann doch das ganze Theme gecloned werden. Die Anpassungen von vorher - Theme als Ruby Gem, das die Default Theme Dateien mit den lokalen überschreibt - sind nicht umsonst. Einfach die angepaßt Dateien in die entsprechenden Theme Ordner kopieren. Dann alles committen und pushen. Im Github-Repo in die Settings gehen und die Github Pages aktivieren und dabei angeben, welcher Branche ausgeliefert werden soll. Und voilà, fertig ist die Webseite, über Github Pages deployed und per HTTPS ausgeliefert. Wen man sich nicht an der github.io Subdomain stört ist man schon fertig. Wie folgt wäre damit der

## Workflow #2

