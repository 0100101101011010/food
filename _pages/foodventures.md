---
layout: default
title: pages in FOODVENTURES
permalink: /foodventures/
---

<ul>
  {% for page in site.tags.foodventures %}
    <li><a href="{{ page.url }}">{{ page.title }}</a> ({{ page.date | date_to_string }})<br>
      {{ page.description }}
    </li>
  {% endfor %}
</ul>
<hr>
