---
permalink: /tags/
title: "Tag Index"
excerpt: "Post-Tags alphabetisch sortiert."
ads: false
share: false
sitemap: false
author: false
author_profile: false 
header:
    image: /assets/images/header/head_datanature_06.jpg
    caption: "&copy; [Kral • Photography](https://kral-photography.com)"
image:
    twitter: /assets/images/header/head_datanature_06_b.jpg
---

<ul class="tag__list">
  {% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}
    <li><a href="{{ site.url }}/tag/{{t | downcase | replace:" ","-" }}/" class="tag__item"><span class="tag__name">{{t | replace:" ","-" }}</span></a> <span class="tag__count">({{ posts | size }})</span></li>
  {% endfor %}
</ul>

