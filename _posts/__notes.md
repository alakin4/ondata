**CATS**
news
data
tech
language
howto
life


**TAGS**
deployment
workflow
writing
learning

r
python

blog
cms
jekyll

ssl
cdn
github
netlify

world
life
nature
future
walkaway

variable
structure
algorithm
measurement

**Gefilterte Tags**
<ul class="tag__list">
  {% assign sorted_tags = site.tags | sort_tags_by_name %}
  {% for tag in sorted_tags %}
    <li><a href="{{ site.url }}/tag/{{ tag[0] | replace:' ','-' | downcase }}/" class="tag__item"><span class="tag__name">{{ tag[0] }}</span></a> <span class="tag__count">()</span></li>
  {% endfor %}
</ul>


**REPLACE RNB**
<div class="sourceCode"><pre class="sourceCode r"><code class="sourceCode r">
<div class="highlight"><pre class="sourceCode r"><code class="sourceCode r language-r">

**WannCry**
https://apnews.com/amp/dc60584d4b214f0fa6eb9ef88fdf46a7
http://abcnews.go.com/Technology/wireStory/computer-expert-foiled-cyberattack-hero-47427837


**Random facts about numbers**
https://www.theguardian.com/childrens-books-site/2014/sep/21/top-10-numbers-for-random-facts-adam-frost

http://www.catalog.update.microsoft.com/search.aspx?q=3212646

**Suche**
https://github.com/mmistakes/minimal-mistakes/issues/588

**Everything**

### Notizen 2

Da kommt ich ja mit dem Meinung haben gar nicht mehr hinterher: http://www.zeit.de/politik/ausland/2017-06/katar-russland-hacker-saudi-arabien-iran-trump-israel-fbi-cnn 

https://markmanson.net/everything-is-fucked
https://markmanson.net/outrage


Muster-Erkennung wird zur Analyse unserer Daten verwendet. Warum verwenden wir es nicht zur Erkennung von Datenmanipulation?   




### VIDEOS

---
permalink: /video-test/
title: "Video Test"
excerpt: ""
date: 2018-02-23 00:48:11 +0100 
last_modified_at: 2018-03-11 21:54:34 +0100 
comments: false
header:
    video:
        id: 202734109
        provider: vimeo
---

## Das ist ein Video-Test

{% vimeo 202734109 %}

Wird alles richtig schön groß angezeigt? Ja!
