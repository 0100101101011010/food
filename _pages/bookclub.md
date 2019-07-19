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

## Books on my To-Read List

* Cuisine of the sun : classic recipes from Nice and Provence / Mireille Johnston.
* Simca's cuisine / Beck, Simone
* The 100-mile diet : a year of local eating / Smith, Alisa
* Encarnación's kitchen Mexican recipes from nineteenth-century California : selections from Encarnación Pinedo's El cocinero español / Pinedo, Encarnació
* Food culture in the Caribbean / Houston, Lynn Marie
* Traveling Jamaica with knife, fork & spoon : a righteous guide to Jamaican cookery / Walsh, Robb. McCarthy, Jay.
* The flavor of Cuba : traditional recipes from the Cuban kitchen / Milera, Laura
* Down to earth Jamaican cooking / DeGale, Laurice
* Food culture in Central America / McDonald, Michael R.
* Pig tails 'n breadfruit : rituals of slave food : a Barbadian memoir / Clarke, Austin
* Heritage cookbook : recipes from the Barkman clan. / Reimer, Esther
* The Hispanic-American cookbook / Rexach, Nilda Luz
* Latin American cooking / Leonard, Jonathan Norton
* Latino food culture Janer, Zilkia
* The Farmer's Food Manual, A Recipe Book for the West Indies. / Jamaica Agricultural Society
* The Food and Drink of Mexico / Booth, George C
* The Real Jerk : new Caribbean cuisine / Pottinger, Lily
* Food culture in South America / Lovera, José Rafael
* Taco USA : how Mexican food conquered America / Arellano, Gustavo
* The Art of Mexican Cooking / Aaron, Jan Salom
* Voices in the kitchen views of food and the world from working-class Mexican and Mexican American women / Abarca, Meredith E.
* Michael Field's culinary classics and improvisations / Field, Michael
* Stuffed : adventures of a restaurant family / Volk, Patricia
* Educated Tastes: Food, Drink, and Connoisseur Culture / Jeremy Strong
