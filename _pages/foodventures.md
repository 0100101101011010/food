---
layout: page
title: Showing posts in "foodventures"
permalink: /foodventures/
---

<ul>
  {% for post in site.categories.foodventures %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
