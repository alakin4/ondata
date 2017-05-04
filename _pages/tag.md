---
permalink: /tag/
title: "Tag Index"
last_modified_at: 2017-05-04 19:39:46 +02:00 
excerpt: "Post-Archiv sortiert nach Tag-Häufigkeit."
share: false
---
<ul class="tag__list">
  {% assign sorted_tags = site.tags | sort_tags_by_name %}
  {% for tag in sorted_tags %}
    <li><a href="{{ site.url }}/tag/{{ tag[0] | replace:' ','-' | downcase }}/" class="tag__item"><span class="tag__name">{{ tag[0] }}</span></a> <span class="tag__count">({{ tag[1] }})</span></li>
  {% endfor %}
</ul>