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
{% endfor %}


</div>
