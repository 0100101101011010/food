---
layout: page
title: Showing posts in "recipe"
permalink: /recipe/
---

<ul>
  {% for post in site.categories.recipe %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
