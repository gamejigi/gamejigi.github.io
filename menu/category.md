---
layout: 
title: Category
---

{% for category in site.categories %}
  <li><a name="{{ category | first }}">{{ category | first }}</a>
   <ul>
   {% for posts in category %}
        {% for post in posts %}
            {% if post.title != null %}
            <li><a href="{{ post.url }}">{{ post.title }}</a></li>
            {% endif %}
        {% endfor %}
   {% endfor %}
   </ul>
  </li>
{% endfor %}
