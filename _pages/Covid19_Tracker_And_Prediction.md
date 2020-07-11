---
layout: "archive"
permalink: /covid19-lm/
title: "Covid19 Tracker and Linear Model Prediction"
author_profile: true
header:
  image: "images/image.jpg"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tags in group-names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>  
  {% for post in posts %}
  {% unless post.hidden %}
    {% include archive-single.html %}
  {% endunless %}
{% endfor %}
