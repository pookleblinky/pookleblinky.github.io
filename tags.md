---
layout: page
title: Tags
permalink: /Tags/
---
{% for tag in site.tags %}
{% assign t = tag | first %}
{% assign posts = tag | last %}

{{ t | downcase }}
<ul>
    {% for post in posts %}
    {% if post.tags contains t %}
    <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%Y/%m/%e"  }}</span>
    </li>
    {% endif %}
    {% endfor %}
</ul>
{% endfor %}
