---
layout: default
title: Projects
---

{% assign items = site.projects | sort: "date" | reverse %}

<h2>{{ page.title }}</h2>
<ul class="card-list">
  {% for item in items %}
    <li class="card">
      <a href="{{ item.url | relative_url }}">
        {% if item.thumbnail %}
          <img src="{{ item.thumbnail | relative_url }}" alt="">
        {% endif %}
        <h3>{{ item.title }}</h3>
        <p>{{ item.summary | default: item.excerpt }}</p>
      </a>
    </li>
  {% endfor %}
</ul>
