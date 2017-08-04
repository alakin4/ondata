---
permalink: /categories/
title: "Kategorie Index"
last_modified_at: 2017-05-04 19:39:46 +02:00 
excerpt: "Post-Kategorien alphabetisch sortiert."
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
{% assign sorted_categories = site.categories | sort %}
  {% if sorted_categories.first[0] == null %}
    {% for cat in sorted_categories %}
      <li><a href="{{ site.url }}/category/{{ cat | replace:' ','-' | downcase }}/" class="tag__item"><span class="tag__name">{{ cat }}</span></a> <span class="tag__count">({{ tag[0] }})</span></li>
    {% endfor %}
  {% else %}
    {% for cat in sorted_categories %}
      <li><a href="{{ site.url }}/category/{{ cat[0] | replace:' ','-' | downcase }}/" class="tag__item"><span class="tag__name">{{ cat[0] }}</span></a> <span class="tag__count">({{ cat[1].size }})</span></li>
    {% endfor %}
  {% endif %}
</ul>
