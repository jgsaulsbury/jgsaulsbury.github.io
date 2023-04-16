---
layout: default
title: "Papers"
permalink: /papers
---
This is where my publications and preprints will go.

<l>
  {% for item in site.data.navigation %}
    <a href="{{ item.link }}" {% if page.url == item.link %}style="color: red;"{% endif %}>
      {{ item.name }}
    </a>
    <br>
  {% endfor %}
</l>


<l>
  {% for paper in site.data.papers %}
    {{paper.year}}
    <br>
  {% endfor %}
</l>
