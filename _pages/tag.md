---
permalink: /tags/
title: "Tag Index"
last_modified_at: 2017-05-04 19:39:46 +02:00 
excerpt: "Post-Tags alphabetisch sortiert."
ads: false
share: false
sitemap: false
author: false
author_profile: false 
header:
    image: /assets/images/header/head_datanature_06.jpg
    caption: "&copy; [Kral • Photography](https://kral-photography.com)"
    twitter: /assets/images/header/head_datanature_06_b.jpg
---

<ul class="tag__list">
  {% assign sorted_tags = site.tags | sort_tags_by_name %}
  {% for tag in sorted_tags %}
    <li><a href="{{ site.url }}/tag/{{ tag[0] | replace:' ','-' | downcase }}/" class="tag__item"><span class="tag__name">{{ tag[0] }}</span></a> <span class="tag__count">({{ tag[1] }})</span></li>
  {% endfor %}
</ul>
