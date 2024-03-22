---
layout: default
title: "Papers"
permalink: /papers
---
## Journal articles
<l>
  {% for paper in site.data.papers %}
    {% if paper.journal != "bioRxiv" %}
    {% for author in paper.authors %}
      {% if author == "James G. Saulsbury" %}<b>{{author}}</b>{% else %}{{author}}{% endif %}{% if forloop.last == true %}. {% elsif forloop.rindex0 == 1 %}{% if forloop.length > 2 %},{% endif %} and{% else %},{% endif %}{% endfor %}{% if paper.doi %}<a href="https://doi.org/{{paper.doi}}">{{paper.title}}</a>{% else %}{{paper.title}}{% endif %}. {{paper.year}}, <i>{{paper.journal}}</i>.{% if paper.press %}<a href="{{paper.press}}">{{ Covered here.}}</a>{% endif %}
    <br><br>
    {% endif %}
  {% endfor %}
</l>
## Preprints
<l>
  {% for paper in site.data.papers %}
    {% if paper.journal == "bioRxiv" %}  
    {% for author in paper.authors %}
      {% if author == "James G. Saulsbury" %}<b>{{author}}</b>{% else %}{{author}}{% endif %}{% if forloop.last == true %}. {% elsif forloop.rindex0 == 1 %}{% if forloop.length > 2 %},{% endif %} and{% else %},{% endif %}{% endfor %}<a href="https://doi.org/{{paper.doi}}">{{paper.title}}</a>. <i>bioRxiv.</i>
    <br><br>
    {% endif %}
  {% endfor %}
</l>
