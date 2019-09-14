---
layout: page
title: My weekly "foodventures" (what I eat each week)
permalink: /foodventures/
---

(Starting September 2019, I have stopped using the "foodventures" tag and new posts will be posted in my ["diary"](/food/diary/) tag. This tag is still up as an archive of all pre-September 2019 entries.)

<ul>
  {% for post in site.categories.foodventures %}
    <li><a href="/food{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})<br>
      <i>{{ post.excerpt }}</i>
    </li>
  {% endfor %}
</ul>
<hr>
