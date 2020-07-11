---
title: "About"
permalink: /about/
header:
  image: "assets/images/IMG.jpg"
---

Skilled data analyst with more than 2 years of freelance and about 1 year of industry experience in collecting, organizing and interpreting various types of data. Energetic presenter and confident communicator with the ability to communicate insights clearly and efficiently for decision making purpose. Creative in finding solutions to problems and determining modifications for optimal use of organizational data. Skilled at providing realistic projections and establishing scenarios to determine viable process strategies to utilize in executing insights. Organized and timely in providing clients with reports on specific data findings and their impact on organizational growth and success.


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
