---
permalink: /jekyll-static-comments-with-staticman-and-mailgun/
title: "Statische Kommentare in Jekyll mit eigener Instanz von Staticman"
date: 2019-11-22 01:03:38 +0100 
last_modified_at: 2019-11-22 01:10:45 +0100  
excerpt: "Eine Kommentar-Funktion mit Hilfe einer eigenen Instanz der Staticman-App auf Heroku gehostet in einer Webseite realisieren, die mit einem statischen Webseiten-Generator wie Jekyll gebaut ist."
comments: true
comments_locked: false
header:
        image: /assets/images/header/head_deepweb_03.jpg
        caption: "&copy; [Kral • Photography](https://kral-photography.com)"
        title: "DEEP WEB, kinetic audiovisual installation and performance by Christopher Bauder (Lichtgrenze/SKALAR) &amp; Robert Henke (Monolake) in cooperation with Kraftwerk Berlin, Berlin, 2019"
        twitter: /assets/images/header/head_deepweb_03_b.jpg
categories: news howto
tags: cms jekyll workflow github staticman
related: true
related_count: 2
---

{% include toc_open title="TOC" %}

<br />

## Einführung

Mit [Staticman](https://github.com/eduardoboucas/staticman){:target="_blank"} lassen sich in Webseiten, die von statischen Generatoren wie [Jekyll](https://jekyllrb.com/){:target="_blank"} gebaut werden, eine Kommentarfunktion umsetzen umsetzen. Staticman ist eine NodeJS Applikation, die benutzergenerierten Inhalt von der Webseite durch z.B. ein Formular erhält und sie als Datendateien zu Github (oder Gitlab) hochlädt.    
Eduardo Bouças, der Entwickler von Staticman, stellte dazu sein App öffentlich zur Verfügung. Wegen der zunehmenden Beliebtheit von statischen Webseiten-Generatoren und weil man nicht auf Kommentare verzichten wollte, stößt die App jetzt leider regelmäßig an ihre Quota-Grenzen und ist nicht mehr gut nutzbar.    
Da die App Open Source ist, ist der einfachste Weg, die App selbst zu hosten. Zum Hosten besorgt man sich einen kostenlosen Account auf [Heroku](https://www.heroku.com/){:target="_blank"}, erstellt sich einen Fork von Staticman und veröffentlicht diesen auf Heroku. Doch dazu jetzt im einzelnen.

## Staticman Fork auf Github

Als erstes erstelle ich mir einen neuen Github-Account, sozusagen einen Bot-Account, der die Daten in meinen Webseiten-Repos pusht. Außerdem habe ich einen Fork des Staticman-Repos hier abgelegt. Das beides hängt sonst nicht zusammen. Man kann auch das Staticman-Repos nach local klonen und von dort dann zum App-Hoster pushen. Wenn man jedoch den Heroku-Account mit dem Bot-Account verbindet, kann man auch automatisch bei Push nach Heroku deployen.    
Warum der Bot-Account? Damit die vom Kommentarformular geposteten Daten und von der Staticman-App daraus gebauten Datendateien in unserer Webseiten-Repository gepusht werden können, muß das neue Bot-Github-Repos Schreibrechte auf das Webseiten-Repos erhalten. Sollte der neue Bot-Account einmal kompromitiert werden, ist nur der Bot-Account verloren und nicht der Account, in dem all meine Repositories wohnen.    
In den Account-Settings des Bot-Accounts in die Developer Settings gehen und einen *Personal Access Token* erstellen. Ich habe diesen mit allen Rechten bei *repo* und bei *admin:repo_hook* erstellt. Zweiteres ist für das automatische Deployment zu Heroku. Den Key sofort kopieren und sicher wegspeichern, da er nur dieses eine mal angezeigt wird.    
Dann einen Fork des Staticman-Repos in diesen Bot-Account erstellen und zum Bearbeiten das Repos lokal klonen.

## Konfiguration der Staticman-App

Wie man den Artikeln hier[^1] und hier[^3] entnehmen kann (die restlichen Quellen[^2],[^4],[^5]), funktioniert der aktulle Master-Branch von Staticman nicht wie erwartet. Der in diesen Artikeln erwähnte [Commit 55d1430](https://github.com/eduardoboucas/staticman/commit/55d14306d851059a2a27d24b5eb4cb17c5009477){:target="_blank"} funktioniert jedoch. Daher erstellen wir daraus einen Branch und arbeiten damit:

```bash
$ git checkout -b production 55d1430
```

Zur Konfiguration der App müssen wir der App einige Daten mitgeben, wie z.B. das Personal Access Token unseres Bot-Accounts. Damit dieser aber nicht im Klartext in unserem Repos liegt, erstellen wir die Konfigurationsdatei mit Platzhaltern. Die echten Werte kann man dann per `heroku cli` übertragen oder im Admin von Heroku in den Einstellungen der App hinterlegen.
Als erstes die Datei `config.production.json` als Kopie der Datei `config.sample.json` erstellen.

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

In den Settings des Webseiten-Repos bei Github dann noch den Bot-Account als Collaborator eintragen und den Einladungslink kopieren. Dann aus diesem Account ausloggen und in den Bot-Account einloggen und den Einladungslink im Browser aurufen. Nach der Bestätigung kann der Bot-Account bei Github auch in das Webseiten-Repos schreiben. Und pushen, was dafür nötig ist, daß die Posts in der Webseite erscheinen.

## Heroku

In Heroku erstellt man sich einen kostenlosen Account und legt eine App an. In der App kann man unter dem Menlüpunkt *Deploy* als Deploymethode *Github* auswählen. Ist man in Github in seinem Bot-Account eingeloggt, wählt man das Repos mit dem Staticman-Fork aus und als Branch den vorher angelegten *production*-Branch. Aktiviert man dann noch die automatischen Deploys wird bei jedem Push in das Staticman-Repos ein Deployment nach Heroku durchgeführt, die App neu gebaut und gestartet.
Unter [https://HEROKU_APP_NAME.herokuapp.com]() sollte dann ein *Hello from Staticman version 3.0.0!* erscheinen, womit man weiß, daß die App läuft.   

### Heroku App Settings

In der App unter Settings den Button `Reveal Config Vars` klicken. Hier müssen 3 Parameter gesetzt werden.

1. `GITHUB_TOKEN`: Als Wert den oben im Github-Bot-Account angelegten (und hoffentlich abgespeicherten) Personal Access Token eingeben.
2. `NODE_ENV`: Hier `production` als Wert eintragen.
3. `RSA_PRIVATE_KEY`: Hier müssen wir einen Verschlüsselungsschlüssel erstellen, mit dessen Hilfe die App bestimmte sensible Daten ver- und entschlüsselt.

Diesen Key erstellt man einfach an der lokalen Konsole mit dem Befehl

```
openssl genrsa -out staticman-key.pem
```

Diesen Key mit einem Text-Editor öffnen und alle Zeilenümbrüche entfernen, so daß der gesamte Inhalt in einer Zeile steht. Diesen String dann als Wert eintragen.

### Heroku Endpoints

Zur Arbeit mit der App benötigen wir zwei Endpoints, also URLs, unter der wir Funktionen der App aufrufen können.    
Das ist einmal die Verschlüsselungsfunktion unter [https://HEROKU_APP_NAME.herokuapp.com/v3/encrypt/STRING_TO_ENCRYPT](). Damit werden folgende Werte in der _staticman.yml_ verschlüsselt:

- notifications.apiKey und notifications.domain
- reCaptcha.secret

Nicht vergessen, den Wert für reCaptcha.secret auch in der _config.yml_ zu hinterlegen.    
Der zweite Endpoint ist der eigentliche Endpoint, den wir im Formular als Action hinterlegen. Er lautet

[https://HEROKU_APP_NAME.herokuapp.com/v3/entry/github/GITHUB_USERNAME/GITHUB_REPOS/GITHUB_BRANCH/comments]()

### Anpassung der Staticman-App

Bei der Verwendung der App fielen mir zwei Dinge auf. Einmal gibt es beim Bauen der App Warnings in den Heroku-Logs, das bestimmte Informationen nicht im Schema der App enthalten sind. Es fehlen: _allowedOrigins_, _endpoint_ und die _notifications.fromAddress_.
Im Webseiten-Repos in der _staticman.yml_ steht, das die hier angegebe _notifications.fromAddress_ die in der App hinterlegte fromAddress überschreibt. Meine Tests haben ergeben, daß sie nicht überschrieben wird. Im Code der App -- auch nicht im aktuellen master-Branch -- habe ich das jedoch nicht gefunden. Daher habe ich das in meinem Fork implementiert.
Beide Änderungen sind [hier](https://github.com/dev4223-bot/staticman/compare/b8d07dafad582af48eb0cf69fd296819358733db...dev4223-bot:e6be62b29f223e2138f57c81a5603d279131cf22) zu finden.

## Mailgun

Damit man über die Kommentare und Antworten auf Kommentare benachrichtigt wird, kann man sich einen freien [Mailgun-Account](https://www.mailgun.com/){:target="_blank"} besorgen. Der Api-Key und die Mail-Domain wird dann verschlüsselt wie oben beschrieben in die _staticman.yml_ eingetragen. 

## Schlußbemerkung

Mit Hilfe dieser Services hat man eine Kommentarfunktion mit Email-Benachrichtigung in die statischen Webseite eingebaut. Viel Spaß beim Kommentieren!

## Quellen

Diese Artikel haben mir bei der Umsetzung sehr geholfen. Danke!

[^1]: <p><a href="https://muffinman.io/running-staticman-on-heroku/" target="_blank">Running Staticman on Heroku - Stanko Tadić</a></p>
[^2]: <p><a href="https://vincenttam.gitlab.io/post/2018-09-16-staticman-powered-gitlab-pages/2/" target="_blank">Staticman API Hosting 2018 - Vincent Tam</a></p>
[^3]: <p><a href="https://networkhobo.com/staticman-the-journey-continues" target="_blank">Staticman Staticman...The Journey Continues - Dan C Williams</a></p>
[^4]: <p><a href="https://www.datascienceblog.net/post/other/staticman_comments/" target="_blank">Staticman: An Alternative to Disqus for Comments on Static Sites - Matthias Döring</a></p>
[^5]: <p><a href="https://yasoob.me/posts/running_staticman_on_static_hugo_blog_with_nested_comments/" target="_blank">Running Staticman on Hugo Blog With Nested Comments - Yasoob Khalid</a></p>





