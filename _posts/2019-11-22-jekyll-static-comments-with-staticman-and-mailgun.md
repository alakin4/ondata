---
permalink: /jekyll-static-comments-with-staticman-and-mailgun/
title: "Statische Kommentare in Jekyll mit eigener Instanz von Staticman"
date: 2019-11-22 01:03:38 +0100 
last_modified_at: 2019-11-22 01:10:45 +0100  
excerpt: "Was verbindet uns mit anderen, mit der Welt? Welches Medium liegt zwischen uns? Oder ist es eine Struktur? Müssen wir sie er-lernen oder gar selbst errichten?"
comments: true
comments_locked: false
header:
        image: /assets/images/header/head_deepweb_03.jpg
        caption: "&copy; [Kral • Photography](https://kral-photography.com)"
        title: "DEEP WEB, kinetic audiovisual installation and performance by Christopher Bauder (Lichtgrenze/SKALAR) &amp; Robert Henke (Monolake) in cooperation with Kraftwerk Berlin, Berlin, 2019"
        twitter: /assets/images/header/head_deepweb_03_b.jpg
categories: news howto
tags: cms jekyll workflow deployment cdn github netlify
related: true
related_count: 2
---

{% include toc_open title="TOC" %}

<br />

# Einführung

Mit [Staticman](https://github.com/eduardoboucas/staticman) lassen sich in Webseiten, die von statischen Generatoren wie [Jekyll](https://jekyllrb.com/) gebaut werden, eine Kommentarfunktion umsetzen umsetzen. Staticman ist eine NodeJS Applikation, die benutzergenerierten Inhalt von der Webseite durch z.B. ein Formular erhält und sie als Datendateien zu Github (oder Gitlab) hochlädt.    
Eduardo Bouças, der Entwickler von Staticman, stellte dazu sein App öffentlich zur Verfügung. Wegen der zunehmenden Beliebtheit von statischen Webseiten-Generatoren und weil man nicht auf Kommentare verzichten wollte, stößt die App jetzt leider regelmäßig an ihre Quota-Grenzen und ist nicht mehr gut nutzbar.    
Da die App Open Source ist, ist der einfachste Weg, die App selbst zu hosten. Zum Hosten besorgt man sich einen kostenlosen Account auf [Heroku](https://www.heroku.com/), erstellt sich einen Fork von Staticman und veröffentlicht diesen auf Heroku. Doch dazu jetzt im einzelnen.

# Staticman Fork auf Github

Als erstes erstelle ich mir einen neuen Github-Account, sozusagen einen Bot-Account, der die Daten in meinen Webseiten-Repos pusht. Außerdem habe ich einen Fork des Staticman-Repos hier abgelegt. Das beides hängt sonst nicht zusammen. Man kann auch das Staticman-Repos nach local klonen und von dort dann zum App-Hoster pushen. Wenn man jedoch den Heroku-Account mit dem Bot-Account verbindet, kann man auch automatisch bei Push nach Heroku deployen.    
Warum der Bot-Account? Damit die vom Kommentarformular geposteten Daten und von der Staticman-App daraus gebauten Datendateien in unserer Webseiten-Repository gepusht werden können, muß das neue Bot-Github-Repos Schreibrechte auf das Webseiten-Repos erhalten. Sollte der neue Bot-Account einmal kompromitiert werden, ist nur der Bot-Account verloren und nicht der Account, in dem all meine Repositories wohnen.    
In den Account-Settings des Bot-Accounts in die Developer Settings gehen und einen **Personal Access Token** erstellen. Ich habe diesen mit allen Rechten bei **repo** und bei **admin:repo_hook** erstellt. Zweiteres ist für das automatische Deployment zu Heroku. Den Key sofort kopieren und sicher wegspeichern, da er nur dieses eine mal angezeigt wird.    
Dann einen Fork des Staticman-Repos in diesen Bot-Account erstellen und zum Bearbeiten das Repos lokal klonen.

# Konfiguration der Staticman-App

Wie man den Artikeln [hier](https://muffinman.io/running-staticman-on-heroku/) und [hier](https://networkhobo.com/staticman-the-journey-continues) entnehmen kann, funktioniert der aktulle Master-Branch von Staticman nicht wie erwartet. Der in diesen Artikeln erwähnte [Commit 55d1430](https://github.com/eduardoboucas/staticman/commit/55d14306d851059a2a27d24b5eb4cb17c5009477) funktioniert jedoch. Daher erstellen wir daraus einen Branch und arbeiten damit:

```bash
$ git checkout -b production 55d1430
```

Zur Konfiguration der App müssen wir der App einige Daten mitgeben, wie z.B. das Personal Access Token unseres Bot-Accounts. Damit dieser aber nicht im Klartext in unserem Repos liegt, erstellen wir die Konfigurationsdatei mit Platzhaltern. Die echten Werte kann man dann per `heroku cli` übertragen oder im Admin von Heroku in den Einstellungen der App hinterlegen.
Als erstes als die Datei `config.production.json` als Kopie der `config.sample.json` erstellen

```bash
$ cp config.sample.json config.production.json
```

Dann den Inhalt der `config.production.json` so abändern

```
{
  "githubToken": process.env.GITHUB_TOKEN,
  "rsaPrivateKey": JSON.stringify(process.env.RSA_PRIVATE_KEY)
}
```

Diese Konfigurationsdatei dann zur gitignore so hinzufügen, das sie auf jeden Fall von Git beachtet wird. Konfigurationsdateien werden von der gitignore eigentlich nicht beachtet. Dazu

```bash
$ echo "!config.production.json" >> .gitignore
```

ausführen.    
Zum Schluß wir noch eine Datei namens `Procfile` erstellt, die dazu dient, daß die App nach einem Deploy automatisch gestart.    

```
web: npm start
```

Alle Änderungen werden dann dem Repos hinzuzufügt.

```bash
$ git add config.production.json Procfile .gitignore
$ git commit -m "Set up Staticman v3 for deployment to Heroku"
```
