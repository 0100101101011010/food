---
layout: default
title: Showing posts in "bookclub"
permalink: /bookclub/
---

<h1>Showing posts in "bookclub"</h1>

<ul>
  {% for post in site.categories.bookclub %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
