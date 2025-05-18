---
title: "News"
layout: textlay
sitemap: false
permalink: /allnews.html
---

## News

<div class="jumbotron">

{% for item in site.data.news %}
  <h3>{{ item.title }}</h3>
  <p><strong>{{ item.date }}</strong></p>
  <p>{{ item.content }}</p>
  {% if item.link %}
      <a href="{{ item.link }}" class="btn btn-primary" target="_blank" rel="noopener">View Certificate</a>
  {% endif %}
{% endfor %}



</div>
