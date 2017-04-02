---
permalink: /deployment-jekyll-with-github-and-netlify/
title:  "Auf der Suche nach einem guten Deployment Workflow"
date: 2017-04-03 01:14:35 +02:00  
comments: true
comments_locked: false
excerpt: "Neben den großen und kleinen CMS gibt es da auch noch die 'flat file cms'. Generatoren für statische HTML-Seiten. Bei der Suche nach einem Wordpress Theme bin ich darauf gestoßen und bei Jekyll hängengeblieben. Nach Installation und Anpassungen eines Themes versuche ich, den Veröffentlichungsworkflow für mich zu optimieren und zu vereinfachen. Er soll wenige Schritte lang und vor allem auch mobil begehbar sein."
categories: jekyll github
tags: deployment cdn ssl
---

{% include toc title="TOC" %}

## Am Anfang

Darauf gebracht hat mich dieser Artikel [So geht Publishing heute: 13 kompakte CMS im Vergleich](http://t3n.de/news/13-kompakte-cms-im-vergleich-461933/){:target="_blank"}. Dazu die in den vergangenen Jahren gesammelten Erfahrungen mit Wordpress und die Suche nach einer einfachen Möglichkeit, eine Webseite zu veröffentlichen. In dem Artikel ist [Jekyll](https://jekyllrb.com/docs/home){:target="_blank"} nicht mal genannt, aber beim Lesen über und der Recherche nach [Kirby](https://getkirby.com/){:target="_blank"}, [Pico](http://picocms.org/){:target="_blank"}, [Grav](https://getgrav.org/){:target="_blank"} und Co. kommt man unweigerlich auch an Jekyll vorbei. 

Nein, eigentlich ging ich auf die Suche nach einem schönen einfachen und minimalistischen Foto-Theme für Wordpress und kam dabei an [Minimal Mistakes](https://mmistakes._github.io_/minimal-mistakes/){:target="_blank"} vorbei, diesem schlichten Jekyll Theme, und es sah gut aus. Einfach, gut zu gestalten. Hätte ich gern für Wordpress, aber habe ich nicht gefunden. Also erstmal nix Foto-Theme. Daß wollte ich selber ausprobieren. Aber es lief auf Jekyll, unbekannterweise. Hörte sich jedoch nach einem von den 'Neuen' aus dem t3n-Artikel an. Ich war gespannt.

Ein paar Dokus und Howtos später läuft der erste Build von Minimal Mistakes auf Jekyll als Ruby Gem erfolgreich lokal auf meiner Linux Box. Schön. Einen vHost dazu und das sah doch schon sehr gut aus. 
Ein bißchen Styling, CSS und das ganze mit Lieblingsschriften abgerundet, Bilder zurechtgeschnitten und ab als statische Seite auf den Server.

Guter Gedanke, der von statischen Seiten, ohne Datenbank und großes Backend und einem schlanken Workflow. Also als nächstes ausprobieren, ob alles so einfach geht, wie vorgestellt.

## Workflow #1

Der erste Ablauf also wie oben beschrieben: Lokaler Build, mit lokalem vHost zur Kontrolle und dann Upload der Dateien per FTP zu meinem Hoster.
Die Vorteile: komplette Kontrolle über den Build Prozess und die Build Tools. Und die Nachteile? Wenn ich ich einen neuen Post online stellen möchte, benötige ich meine lokale Maschine und mehrere Schritte, bis der neue Post endlich online ist. Außerdem muß ich die Build Tools selber aktuell und funktionsfähig halten. So keine Möglichkeit zu haben, unterwegs etwas online zu stellen, stört mich dabei am meisten.

Der erste Workflow ging so:
+ lokale Änderungen, Dateien hinzufügen oder löschen
+ `bundle exec jekyll b`, um die statischen Seiten zu bauen
+ Kontrolle über lokalen vHost
+ wenn alles gut ist, in der __config.yml_ die Variable `url` umstellen
+ nochmal `bundle exec jekyll b`, um die statischen Dateien mit der richtigen URL für Online zu erzeugen
+ `url` in der __config.yml_ wieder zurückstellen auf lokal (besser gleich, sondern vergißt man es)
+ Statische Seiten aus dem Ordner /_site per FTP in den Webroot auf den Server laden

## Git

Die Seite muß natürlich ins Git, weil: Minimal Mistakes liegt ja auch da und überhaupt. Da in meinem ersten Setup das Theme als Ruby Gem installiert ist, wird es auch über `bundle update` aktualisiert. Für die eigenen Themeanpassungen einfach das Datei-Paket bei Github als ZIP runterladen und entpacken oder `git clone` und dann den .git-Ordner löschen und alles 'überflüssige' (ist in der Installationsanleitung beschrieben, was das ist) dazu und dann per CSS schön anstreichen. Dann bei Github ein Repository erstellt und `push`.

## Github Pages

Gut, da ich schon bei Github bin, liegt da auch das Repository. Und dann stolpert man unweigerlich über die Github Pages. Man kann bei Github entweder einen Branchen des gesamten Repositorys oder eines Projekts per Github Pages ausliefern lassen, also als statische Webseite zur Verfügung stellen. Das ganze geht standardmäßig über eine Subdomain von _github.io_. Sogar über HTTPS (wenn über die Github-Subdomain ausgeliefert wird, darüber werde ich weiter unten stolpern). Großartig. Man kann sogar seine eigene Domain hinterlegen. Allerdings mit dem Nachteil, daß man dann kein HTTPS dafür aktivieren kann. Aber eins nach dem anderen.
Ein weiterer Vorteil - und weshalb Github Pages überhaupt hier interessant sind - Github Pages unterstützen auch die Auslieferung von Jekyll Projekten.

Jekyll auf Github Pages unterstützt eine Reihe von Themen, nicht alle. Das hier - Minimal Mistakes - wird erstmal nicht unterstützt. Aber Minimal Mistakes kann so konfiguriert werden, daß es auch unter Github Pages läuft. Das ist alles schon vorbereitet und im Quickstart Guide beschrieben. Dazu muß dann doch das ganze Theme gecloned werden. Die Anpassungen von vorher - Theme als Ruby Gem, das die Default Theme Dateien mit den lokalen überschreibt - sind nicht umsonst. Einfach die angepaßten Dateien in die entsprechenden Theme Ordner kopieren. Dann alles committen und pushen. Im Github-Repository in die Settings gehen und die Github Pages aktivieren und dabei angeben, welcher Branche ausgeliefert werden soll. Und voilà, fertig ist die Webseite, über Github Pages deployed und gebaut und per HTTPS ausgeliefert. Wen man sich nicht an der _github.io_-Subdomain stört ist man schon fertig. Wie folgt wäre damit der

## Workflow #2

+ lokale Änderungen, Dateien hinzufügen oder löschen
+ `bundle exec jekyll b`, um die statischen Seiten zu bauen, um sie über den lokalen vHost kontrollieren zu können
+ wenn alles gut ist, in der __config.yml_ die Variable `url` umstellen
+ `git commit` und `git push`
+ `url` in der __config.yml_ wieder zurückstellen auf lokal (besser gleich, sondern vergißt man es)
+ kurz warten und dann sind die Änderungen unter der _github.io_-Adresse online

Das ganze kann man natürlich auch noch in Branches organisieren und nach der lokalen Kontrolle den Branch in den Branch mergen, den man den Github Pages zugewiesen hat.

## Eigene Domain, und SSL

Jetzt möchte ich natürlich die Github Pages unter meiner eigenen Domain ausliefern lassen. Dazu muß man, je nachdem was für eine Domain das ist, verschiedene DNS Einträge beim Hosting Provider der Domain anpassen (können).
Ich möchte die Subdomain nutzen und muß dafür für die Subdomain einen CNAME Eintrag anlegen, der auf die entsprechende _github.io_-Subdomain zeigt. Und im ROOT des Repository eine Datei namens CNAME anlegen, die ebenfalls den Domain-Namen enthält. Die Einträge sind schnell angelegt und dann stelle ich fest, das unter Github Pages für die Auslieferung über eine eigene Domain das HTTPS Protokoll nicht unterstützt wird. Github bietet leider keinen Service an, z.B. ein kostenloses Let's-encrypt-Zertifikat für die eigene Domain zu zertifizieren oder auch nicht die Möglichkeit, eigene Zertifikate einzubinden.

Ich finde das verständlich für einen kostenlosen Service. Da ich die Auslieferung über HTTPS für sehr wichtig halte, sehe ich mich nach weiteren Möglichkeiten um. 

Bei der Suche nach anderen Wegen, die HTTPS unterstützen, wird hier immer wieder die Auslieferung über ein CDN genannt und dabei auf Cloudflare verwiesen. Cloudflare bietet auch ein kostenloses Paket an. 

## Einsatz eines CDN: Cloudflare

Der Account bei Cloudflare ist schnell angelegt. Dann muß man die Top Level Domain, die umgeleitet werden soll angeben und beim Hoster der TLD die Nameserver von Cloudflare eintragen. Die Nameserver-Einträge werden dann bei Cloudflare geprüft und bei Erfolg wird der Account bestätigt. 

Damit sind auch schon die Hauptprobleme dieser Lösung genannt. Wenn man bei seinem Hoster die Nameserver-Einträge einer Domain nicht ändern darf, funktioniert diese Lösung nicht. Das war bei mir der Fall. Auf der Hauptdomain läuft mein [YOURLS](https://yourls.org/){:target="_blank"} und ich möchte nur eine Subdomain über das CDN ausliefern. 

Die Möglichkeiten, die man mit Cloudflare hat, sehen sehr gut aus bis hin zu einem SSL Zertifikat bei Cloudflare für die Domain, aber mit den Vorraussetzungen ist das keine Möglichkeit für mich.

Also weiter auf der Suche nach einer Möglichkeit, eine Subdomain über ein CDN incl. HTTPS auszuliefern. Erstaunlicherweise habe ich die Lösung dann erst nach langem Suchen und quasi per Zufall gefunden. Sie wurde in einem Beitrag eher nebenher erwähnt.

## Die Lösung: netlify

Netlify vereint die Vorteile eines continuous deployment mit der Auslieferung über ein CDN und der Einbindung eines [Let's-encrypt](https://letsencrypt.org/){:target="_blank"}-Zertifikats für die eigene Domain.
Der kostenfreie Account beinhaltet alles, was ich brauche und ist schnell angelegt und mit Github verbunden. Dabei wird auch hier der Branch ausgewählt, der über die Domain ausgeliefert werden soll. Und damit auch der erst Build angestoßen. Die Github-Pages-Konfiguration des Minimal-Mistakes-Themes funktioniert anscheinend auch hier bei netlify ohne Probleme. Jekyll und alle Gems werden installiert und dann meine Seite gebaut.
Meine Subdomain zeigt per CNAME-Eintrag auf das netlify-CDN. Dann noch per Klick das Let's-encrypt-Zertifikat aktivieren und nach etwas warten kann ich mir meine Seite anschauen.

### Vorschau

Lokal kann ich mir natürlich meine Seite immernoch bauen, aber da ich ja auch von unterwegs deployen will, brauche ich eine Möglichkeit der Vorschau eines Builds. Dazu kommt noch, daß ich den Master als _protected branch_ gesetzt habe.
Weil: um eine kleine Sicherheit gegen einen Push in den Master einzubauen, habe ich den Master bei Githb geschützt, so daß er nur noch mit Pull Requests incl. vorherigem Review aktualisiert werden kann. Ich schreibe und pushe in anderen Branches und wenn eine neuer Release ansteht, erstelle ich auf Github einen Pull Request und merge dann. Wenn man Git Admin ist, darf man den Review auch überschreiben ;-) 
Und die Vorschau? Dafür gibt es ganz einfach die Deploy Preview bei netlify. Für jeden Pull Request in den Master bei Github erstellt netlify automatisch eine Deploy Preview unter einer _netlify.com_-Subdomain. Somit kann man alle Änderungen, bevor sie in den Master gemerged werden, noch einmal kontrollieren. Sehr gutes Feature.
Nur ein kleines Problem dabei: in der __config.yml_ ist ja die `url` der Seite hinterlegt, mit der natürlich alle Links der Seite gebaut werden. Das heißt für die Vorschau, daß die erste Seite zwar funktioniert, aber die Links von der Seite wegführen und die Assets können auf den Unterseiten nicht eingebunden werden (die Same-Origin-Policy verhindert die Einbindung von Ressourcen, die von einer anderen Domain kommen). Nicht so schön für eine Vorschau. Nach kurzem Suchen finde ich schnell die Abhilfe dafür, nämlich

### [Deploy Kontexte](https://www.netlify.com/docs/continuous-deployment/){:target="_blank"}

Es gibt 3 Deploy Kontexte: _production_, _deploy-preview_ und _branch-preview_. Jeden kann man einzeln konfigurieren. Dazu wir die Datei _netlify.toml_ ins Repository-Root gelegt. Um underschiedliche URLs für die Kontexte zu verwenden, sind meine Jekyll-Konfigurationen aufgeteilt. Eine für _production_, eine für die _previews_ und eine für _local_. Da man bei den _previews_ die URL vorher nicht kennt, habe ich die `url` hier ein einfach leergelassen. Dadurch werden die Links relativ gesetzt.

Sieht so aus als hätte ich jetzt alles zusammen für den

## Workflow #3

+ lokale Änderungen, Dateien hinzufügen oder löschen
    * `bundle exec jekyll b`, falls man die Änderungen nochmal lokal überprüfen möchte
+ `git add`, `git commit` und `git push`, um die lokalen Änderungen in den Entwicklungsbranch zu pushen
+ falls netlify-Branch-Previews zur Verfügung stehen, kann man nach kurzem warten die Seite unter der netlify-Branch-URL anschauen
+ sonst bei Github einen Pull Request in den Branch erstellen, der bei netlify unter der Live-URL deployed wird
+ kurz warten, dann kann man die Seite unter der netlify-Preview-URL bei  anschauen
+ wenn alles gut ist, den Pull Request mergen und nach kurzem warten ist die Seite live

## Und mobiles Deployment?

Dafür benutze ich diese Apps auf einem Android Smartphone: 
+ [MGit](https://play.google.com/store/apps/details?id=com.manichord.mgit){:target="_blank"} als Git Client
+ [FastHub](https://play.google.com/store/apps/details?id=com.fastaccess.github){:target="_blank"} für Github -- hier können auch Pull Requests freigegeben werden
+ einen guten Text Editor, z.B. [Jota+](https://play.google.com/store/apps/details?id=jp.sblo.pandora.jota.plus){:target="_blank"} oder [DroidEdit](https://play.google.com/store/apps/details?id=com.aor.droidedit){:target="_blank"}.

## Ergebnis

Ich hab mir einen statisches Seiten Deployment mit Github und CDN für eine Jekyll-Seite zusammenkonfiguriert. Der Workflow erlaubt ein mobiles Deployment inklusive Seitenvorschau. Alles was man braucht, um konfortabel eine kleine Blog-Seite zu pflegen. Die Einrichtung von zusätzlichen Funktionalitäten wie eine Kommentarfunktion über [Staticman](https://staticman.net/){:target="_blank"}, reCaptcha für die Kommentare, die einfachen Themeanpassungen haben mich schon soweit überzeugt. Ich bin gespannt, wie alles im benutzen funktionieren wird. 

