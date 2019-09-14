---
layout: page
title: My weekly food diaries
permalink: /diary/
---

<ul>
  {% for post in site.categories.diary %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
