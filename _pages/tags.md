---
layout: default
permalink: /tags/
title: Browse Posts by Calorie Count
---

<h1>Browse Recipes by Calorie Count</h1>

<div id="archives">
{% for tag in site.tags %}
  <div class="archive-group">
    {% capture tag_name %}{{ tag | first }}{% endcapture %}
    <div id="#{{ tag_name | slugize }}"></div>
    <p></p>

    <h3 class="tag-head">{{ tag_name }}</h3>
    <a name="{{ tag_name | slugize }}"></a>
    <ul>
      {% for post in site.tags[tag_name] %}
        <article class="archive-item">
          <li>
            <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a> ({{ post.date | date_to_string }})<br>
            <i>{{ post.excerpt }}</i>
          </li>
        </article>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
</div>
