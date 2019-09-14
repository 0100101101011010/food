---
layout: page
title: My weekly food diaries
permalink: /diary/
---

See what I make and eat each week.

Older food diary entries (earlier than September 2019) are under the tag ["foodventures"](/food/foodventures). Newer posts can be found below.

<ul>
  {% for post in site.categories.diary %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
