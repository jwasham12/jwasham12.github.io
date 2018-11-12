---
layout: archive
permalink: /blogs/
title: "Blogs"
author_profile: true
header:
  image: "/images/data-photo.jpg"
---

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
