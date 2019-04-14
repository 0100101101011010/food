---
layout: default
title: Posts in "foodventures"
permalink: /foodventures/
---

<h1>Posts in "foodventures"</h1>

<ul>
  {% for post in site.categories.foodventures %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
<hr>
