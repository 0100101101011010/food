---
layout: default
title: Showing posts in "discussion"
permalink: /discussion/
---

<h1>Showing posts in "discussion"</h1>

<ul>
  {% for post in site.categories.discussion %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
