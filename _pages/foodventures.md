---
layout: default
title: posts in FOODVENTURES
permalink: /foodventures/
---

<ul>
  {% for post in site.categories.foodventures %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      {{ post.description }}
    </li>
  {% endfor %}
</ul>
<hr>
